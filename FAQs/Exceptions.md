# How to Throw & Catch Exceptions

## Signaling an Exception (`throw`)
In the following example, we first create an exception object. The argument of the `new:` is a string message attached to the exception. Alternatively we could use a plain `new` message to create an exception with no message.

Last, we use `signal` message to throw the exception. JavaScript operator `throw` is mapped to message `signal` in PharoJS. 

```Smalltalk
|myError|
myError := Error new: 'Some meaningful message'.
myError signal
```

## Catching an Exception (`try/catch`) 
We map the `on:do:` Pharo message to JS `try/catch`. Here is an example. Of course, the 

```Smalltalk
["some code possibly signaling an exception"] on: Error do: [: error |  
	console log: 'An error occured!';
		log: error message
]]
```

## Ensuring the Execution of Some Code (`finally`)
JavaScript `finally` operator allows having a code that is executed no matter what happens. It is always run if an exception occurs or not. It is mapped to Pharo's `ensure:` message as in this example.
```Smalltalk
["some code possibly signaling an exception"] ensure: [
	console log: 'This is always displayed'
]
```