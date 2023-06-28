# How to embed JS Code?

PharoJS allows defining methods with code written in JavaScript. This is possible thanks to the `javascript` pragma.  

Javascript code is provided as a string inside the pragma. This string is exported as is, instead of transpiling the method's body, written in Pharo. The body of the function is what will be executed if the method is invoked on Pharo.

**This should be used as a last resort.** Having your code in Smalltalk is generally more flexible, and will better leverage future PharoJS capabilities.

## Zero Arg Method

```smalltalk
zeroArgMethod
	<javascript: 'window.alert: "Welcome to PharoJS"'>
	
	UIManager default alert: 'Welcome to PharoJS'
```

## Method with Arguments

```smalltalk
add: a to: b
	<javascript: 'return a + b'>
	
	^a + b
```

## Accessing Instance Variables 

We assume the following method defined in a class with instance variable x.

```smalltalk
getIvX
	<javascript: 'return this.x'>
	
	^x
```