# Inspecting JS Objects

Thanks to `PjProxy`, the Pharo **Inspector** can handle JS object and communicates with the
relevant Javascript engine (browser or NodeJS) to examine programmatic values.

For example, in a PharoJS Playground, by selecting and Cmd-I the following:
```JS
	document fonts
```
you would get an inspector showing all the fields of the object
-- if document were defined in this scope, which it's not.

However this works fine in a PharoJS Playground, or in
methods of a class that specify the pool dictionary `PjDomGlobals`