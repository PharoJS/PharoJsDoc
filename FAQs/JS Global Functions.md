# How to call JS Global Functions?

JS global functions are functions attached to global `window`. An example is `alert()`. 

In JS, such functions can be called as in a procedural language.  So, the following expression opens a dialog with string `'Hello PharoJS'`.

```js
alert('Hello PharoJS')
```

Pharo being pure OO language, we need to switch to message sends. Meaning, that the receiver must be provided for every call. So, the above function call should be written in PharoJS as:

```Smalltalk
window alert: 'Hello PharoJS'
```