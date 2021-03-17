# What is class-side `appClasses` useful for?

You might encounter such methods in the class-side of app classes.
```smalltalk
appClasses  
	<pharoJsSkip>  
	^super appClasses, {PjUser}
```

PharoJS transpiler crawls the code starting from the app class, and converts all classes it reaches to JS. At very special cases, some classes might be left out. So, adding them in this class method ensures they'll be exported. (edited) 


Note the `<pharoJsSkip>` pragma.  PharoJS transpiler skips methods with this pragma. They won't be available in generated JS code.