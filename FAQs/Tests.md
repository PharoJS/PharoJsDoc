# How to Write Tests?

To write a test for your `MyPharoJsApp` app class, create a test class as following:
```smalltalk
PjWebAppTestCase subclass: #MyTest  
	instanceVariableNames: ''  
	classVariableNames: ''  
	package: 'MyPackage-Tests'	
```

Add this newly created test class the following **class side** method:
```smalltalk
appClass
	^MyPharoJsApp
```

The inherited `setUp` method ensures that an instance of the `MyPharoJsApp` is created, and available via instance variable `app`. So, your test methods can use it. Since we are testing a web-based app, the PharoJS test framework ensures the default web browser opens and displays the HTML linked to your app.

By default, the app instance is created on the Pharo side, and talks remotely to JS objects (e.g. `window` and `document`).

You can however for PharoJS to run your code on JS side. Simply make your test class use trait `PjTAppRunsInJS`. So, your test class definition would become:

```Smalltalk
PjWebAppTestCase subclass: #MyTest  
	uses: PjTAppRunsInJS
	instanceVariableNames: ''  
	classVariableNames: ''  
	package: 'MyPackage-Tests'	
```
