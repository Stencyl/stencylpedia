# Game > Web

***

> View our article on [Web Requests](https://www.stencyl.com/help/view/web-requests/) for an explanation of these blocks.

***

## Web Browser

### <a name="show-browser"></a> Open URL in Browser

![open url text in browser](https://static.stencyl.com/pedia2/block-images/game/web/show-browser.png)

Opens the given URL in the system's default web browser. On mobile devices, this will open up the browser app. To view pages in-game, use the [Web Views](https://community.stencyl.com/index.php/topic,26708.0.html) extension.

> For a Flash game you may need to give [permissions](https://www.stencyl.com/help/view/web-flash-security/) to access the web.

```
openURLInBrowser([TEXT]);
```

***

## HTTP Requests

### <a name="visit-site"></a> GET Request

![visit url text and then do...](https://static.stencyl.com/pedia2/block-images/game/web/visit-site.png)

Issues an HTTP GET request at the given URL, then executes the enclosed blocks if the request succeeded. The server's response is enclosed in the `site's response` block.

> For a Flash game you may need to give [permissions](https://www.stencyl.com/help/view/web-flash-security/) to access the web.

```
visitURL([TEXT], function(event:Event):Void {
  [ACTIONS]
});
```

***

### <a name="visit-site-post"></a> POST Request

![post data text to url text and then do...](https://static.stencyl.com/pedia2/block-images/game/web/visit-site-post.png)

Issues an HTTP POST request at the given URL with the given parameters, then executes the enclosed blocks if the request succeeded. The server's response is enclosed in the `site's response` block.

Parameters are pased in as key=value pairs, separated by ampersands (&), like this `name=John&id=123456`.

> For a Flash game you may need to give [permissions](https://www.stencyl.com/help/view/web-flash-security/) to access the web.

```
postToURL([TEXT], [TEXT], function(event:Event):Void {
  [ACTIONS]
});
```

***
