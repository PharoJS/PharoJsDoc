# How to use Promises?

Regarding promises, you can use existing JS that produces promises  

```smalltalk
myPromise := ...  
myPromise then: [: result | ...]
myPromise catch: [: reason | ...]
```

You can chain them just as you would do in Javascript:
```smalltalk
myPromise := ...  
((myPromise then: [: result | ...])
  then: [: result | ...])
    catch: [: reason | ...]
```

The parentheses can get a bit tedious if you have a long nesting chain, in which case you might want to add the [Pharo-Functional](https://github.com/dvmason/Pharo-Functional) package to your image which gives you a piping operator called parrot, so the above becomes:
```smalltalk
myPromise := ...  
myPromise
    then: [: result | ...]
 :> then: [: result | ...]
 :> catch: [: reason | ...]
```

The only limitation that we didn't address yet is to create `async` functions.

But the point of PharoJS is to use Pharo constructions, and run them on JS. We can call pretty much any third party JS code.