# What is class-side `appClasses` useful for?

You might see such methods on the class-side of app classes.
```smalltalk
appClasses  
	<pharoJsSkip>  
	^super appClasses, {PjUser}
```

The PharoJS transpiler crawls the code starting from the app class, and converts all classes it reaches to JS. In some very special cases, some classes might be left out. So, adding them in this class method ensures they'll be exported.

Note the `<pharoJsSkip>` pragma.  The PharoJS transpiler skips methods with this pragma. They won't be available in generated JS code. This is normally used with methods like this, that are directions/information for the PharoJS transpiler or exporter.