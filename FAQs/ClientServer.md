# How would I write a Client-Server web app with PharoJS as a client?

There are two options:
- You can use forms and a REST server to do very trivial interactions. 
- You can use the [`fetch()` function](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) provided by Javascript.

Both options are illustrated by the [Smalltalk REPL example](https://github.com/PharoJS/WebStREPL). You can also look at [the COVID tracking app](https://covid.cs.ryerson.ca/compare/) that relies on `fetch()`.
