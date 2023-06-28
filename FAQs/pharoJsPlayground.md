# PharoJS Playground

The PharoJS Playground lets you explore the JavaScript side of an app.
Access the PharoJS Playground from the world menu which will allow you to launch a playground for any app that you have in the image.
Alternatively, you can launch the PharoJS playground, by sending the `playground` message to the app class, as in:

```JS
PjMinimalWebApplication playground.
```

You can launch the app on Pharo, which means that all of your Pharo Smalltalk code will run in the Pharo image, but you can access the DOM, Javascript libraries, and other Javascript values via proxies visible as globals in the playground.

You can also launch the app on the Javascript engine (Web browser or Node). In this case, the code is all translated to Javascript and installed in the JSE.  In addition to the proxies mentioned above, the application and other installed classes running on the JSE are accessible via proxies.
