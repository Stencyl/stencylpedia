> **Extending Stencyl**

> Engine ([Basics](http://www.stencyl.com/help/view/how-to-create-engine-extension/) - [iOS & Android](http://www.stencyl.com/help/view/how-to-create-native-engine-extension/) - [Native Events](http://www.stencyl.com/help/view/native-events/) - [Flash](http://www.stencyl.com/help/view/flash-extensions/) - [Blocks](http://www.stencyl.com/help/view/adding-blocks/) - [API](http://static.stencyl.com/api/33/))

> Toolset ([Extensions](http://www.stencyl.com/help/view/creating-extensions/) - [API](http://api.stencyl.com/extensions/))


## Introduction

A big part of Stencyl's ease of use comes in the form of [Events](Events). As a developer, it's more convenient to be **automatically notified** that something has happened, versus having to constantly check if that something has happened.

To implement Events for your native (iOS/Android) extensions, you would need to know how to get the Objective-C (or Java) code to send notifications back to Haxe. For example, if the player completed an in-app purchase, you'd want to inform the player if the purchase succeeded and do something in-game in response to that.

How do we accomplish this?

> **Note:** Refer to the purchases extension for a real example of how to send data back from Objective-C/Java to Haxe.


## iOS (Objective-C --> Haxe)

Recall that in Haxe, we set up function pointers to the C++ layer and can specify how many parameters are passed in. What we can do is **pass in a pointer to a callback function**. In other words, we can pass in a Haxe function that will get called back when the time is right.

Here is the Haxe code that does this.

```
private function init()
{
  set_event_handle(notifyListeners);
}

private static function notifyListeners(inEvent:Dynamic)
{
  [...]
}

[...]

private static var set_event_handle = Lib.load("purchases", "purchases_set_event_handle", 1);
```

In this code, `set_event_handle()` is a C++ function that we use to pass a pointer to `notifyListeners()` to the C++ layer, so that the C++ code can call `notifyListeners()` at the right time in the future. `notifyListeners()` takes one parameter - a data field that contains all the callback data we need to determine what kind of event is coming back and any additional data that comes with that event.

Now, let's look at what the C++ (ExternalInterface.cpp) looks like for this example. *(Again, this is simplified a bit to make the important bits clear. See the Purchases extension for the full source.)*

```
AutoGCRoot* purchaseEventHandle = 0;

static void purchases_set_event_handle(value onEvent)
{
  purchaseEventHandle = new AutoGCRoot(onEvent);
}
DEFINE_PRIM(purchases_set_event_handle, 1);

extern "C" void sendPurchaseEvent(const char* type, const char* data)
{
    value o = alloc_empty_object();
    alloc_field(o,val_id("type"),alloc_string(type));
    alloc_field(o,val_id("data"),alloc_string(data));
    val_call1(purchaseEventHandle->get(), o);
}
```

A bit more is going on here.

* `purchaseEventHandle` is a variable that holds the pointer to the Haxe function that we want to callback. In other words, it's holding a pointer to `notifyListeners()`

* `purchases_set_event_handle()` is the function that sets the pointer. We called this function in Haxe (see above) and passed in `notifyListeners()`.

* `sendPurchaseEvent()` is a function that's called from Objective-C. It takes two String (char*) parameters. The first one tells us what kind of event we're calling. The second passes in any additional data that's relevant to the event.

Finally, a simplified example of Objective-C code from Purchases.mm that demonstrates how the code would call `sendPurchaseEvent()`

```
-(void)finishTransaction:(SKTransaction*)t succeeded:(BOOL)succeeded {
  if(succeeded) {
		  sendPurchaseEvent("success", t.ID);
	 }

	 else {
		  sendPurchaseEvent("failed", t.ID);
	 }

	 [[SKPaymentQueue defaultQueue] finishTransaction:t];
}
```

Everything we've talked about is summarized in the following diagram.

![ios-callbacks](http://static.stencyl.com/pedia2/chapter-d/IOSCallback.png)

To reiterate, this is an advanced use case where it’s best to view existing examples to understand what's going on. It sounds a lot more confusing than it really is, and there’s no better explanation than viewing the source for yourself.


## Android (Java -> Haxe)

Calling back Haxe from Java code follows a similar line of thinking, except that instead of passing in a function pointer that gets called back, you pass in the entire Haxe class instead and call any function you want form Java.

* **Pass in the entire Haxe class** to Java by calling a Java function (via JNI).
* In Java, said function accepts a parameter of **org.haxe.nme.HaxeObject**.
* Calling back Haxe from Java involves doing **HaxeObject.call(functionName, args)**.

This is summarized in the following diagram.

![android-callbacks](http://static.stencyl.com/pedia2/chapter-d/AndroidCallback.png)

Let's walk through what's going on. First, let's peek at Purchases.hx once more.

```
class Purchases {	
  public function new() {
    var fn = nme.JNI.createStaticMethod("Billing", "initialize", "(Lorg/haxe/nme/HaxeObject;)V", true);
    fn([this]);
  }

  public function onPurchase(productID:String) {
    trace(productID);
  }
}
```

As you can see, the JNI call takes in a pointer to the entire class. `onSuccessfulPurchase()` will be called from Java, as we'll see next.

```
import org.haxe.nme.HaxeObject;

public class Billing {
  public static void initialize(final HaxeObject callback) {
    //Make a test purchase
    GameActivity.getInstance().runOnUiThread(new Runnable() { 
      public void run() {
        callback.call("onPurchase", new Object[] {"FHDKJHSDF1231231"});
      }
    });
  }
}
```

As you can see, `initialize()` takes in the Haxe class as a Java HaxeObject. It calls a function `onPurchase` through reflection and passes back the purchaseID of this mock purchase.

`runOnUiThread()` is required here because these operations have to be run in sync with the UI, even though they don't have anything to do with the UI. Failure to do this may result in a crash.
