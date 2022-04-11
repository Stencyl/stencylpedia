## Contents

* Visiting a URL
* HTTP Requests
* Example: Loading levels from a server
* Accessing Flash variables
* Launching Apps on Mobile using URLs
* Frequently Asked Questions


## Visiting a URL

Using the open URL block (under Game > Web), you can visit any URL from within a game. The link will open up inside a new tab, using the user's default browser. *On Flash/Desktop, a pop-up blocker can prevent this from happening.*

![Open URL block](https://static.stencyl.com/pedia2/ch5/web/image01.png)

> **Tip:** If you want an in-app browser, check out the [Web Views extension](https://community.stencyl.com/index.php/topic,38900.0.html).

#### What could you use this for?

* Visiting Social Media (Facebook, Twitter)
* Asking for a Paypal donation
* Linking to your mobile game's entry

> Note: We have [pre-built behaviors](https://www.stencyl.com/help/view/pre-shipped-behaviors) for the first 2 scenarios. Check them out under the "Utilities" category the next time you import a behavior for a scene.
 

## HTTP Requests (GET / POST)

What if you want your game to communicate with a web-based API? Stencyl also supports making HTTP requests, so that your game can communicate with REST-based APIs and can submit data to scripts that you've built yourself.

#### How to make an HTTP Request

Make an HTTP request using either the visit URL block or POST data block (both under Game > Web). The first block corresponds to a GET request, while the second corresponds to a POST request.

![HTTP request blocks](https://static.stencyl.com/help/images/web-request-blocks.png)

Either way, calls are **asynchronous** (non-blocking). We callback by executing the body of the blocks when you receive a response, which can be fetched using the red **site's response** block.

If the HTTP request fails, no callback will be issued. We recommend using a timeout (via a do-after block, for example) to handle the case of failure.

#### Multiple Field POST Requests

If you're trying to submit data, a POST request is the preferred method for doing that. What if you want to submit multiple pieces of data?

You can pass in multiple fields at once by separating them with ampersands (&), like this:

```
name=John&id=123456
```


## Example: Loading Levels from a Server

In an early Stencyl game that featured a level editor, the developer used HTTP requests to implement a level sharing system. We'll now step through a simplified example of this.

Suppose that we're building a simple game that stores its levels online. We want to create a level loader for this game that takes the data and creates actors based on the type and location.

Here's some sample data: [level1.txt](https://raw.githubusercontent.com/Stencyl/stencylpedia/master/chapter-5/files/level1.txt)

This file contains just 3 entries, one line each. The 3 "columns" correspond to: Name of the actor, x-location, y-location.

```
robot,0,0
robot,128,128
hero,256,256
```

Here's how we could parse this. We tokenize ech line one by one, knowing that each entry is separated by commas.

![Example](https://static.stencyl.com/pedia2/ch5/web/image00.png)

If you're building your own web services to communicate with Stencyl, keep your data formats simple, and you can achieve pretty cool things with web requests.


## Launching Apps on Mobile using URLs

#### Facebook

Opens the Facebook app to the page you define. Useful for directing users to your Facebook page, so they can "Like" it without having to use the official API.

```
fb://profile/[your ID]
```

#### Twitter

Opens Twitter app to the page you define. For example, you could open it up to the page for your game/studio to encourage a "Follow" without having to use the official API.

```
twitter://user?id=YOUR_ID
```

> See this [forum topic](https://community.stencyl.com/index.php/topic,30964.0.html) for more examples.


## Frequently Asked Questions

#### Does Stencyl provide XML / JSON parsing out of the box?

Many APIs provide responses in standard formats such as XML or JSON. Parsing XML and JSON-based responses is not handled by Stencyl out of the box (we don't have any blocks for it), but it is supported in code via Haxe.
 
#### Can Stencyl communicate directly with a database?

No. For security reasons, it is not best practice to allow a game to directly query a database. Instead, write a script on your server that Stencyl can communicate with using HTTP requests.

#### If I'm making a mobile game, can I show the page inside the app, instead of launching Safari / Chrome?

If you want an in-app browser, check out the [Web Views extension](https://community.stencyl.com/index.php/topic,26708.0.html).
 

## Summary

* Visit URLs to point players to your social media pages, Paypal page or iOS game entry.
* HTTP requests let you do just about anything. The "Populate" game for Flash and iOS uses HTTP requests to implement a level share system.
* Flash variables can be used to communicate with a Flash game's containing webpage.
