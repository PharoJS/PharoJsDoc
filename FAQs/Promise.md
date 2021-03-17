# How to use Promises?

Regarding promises, you can use existing JS that produces promises  

```
myPromise := ...  
myPromise then: [: result | ...]
```

The only limitation that we didn't address yet is to create `async` functions.

But the point of PharoJS is to use Pharo constructions, and run them on JS. We can call pretty much any third party JS code.