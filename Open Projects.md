# Open Projects

## More functional bridge
### Asynchronous
### Into production mode
- allows creating more interactive applications that could interact over the bridge
- work well with Seaside

## Better dependent transpiler
- Load only the required methods, but pull more methods on demand
 - Transpiles just required methods
 - Automatic detection of all methods 
### Transpile the full Pharo image 
### support `async` and `await`

## Exporting
### export libraries
### export workers
### more than one file
- e.g. core  wouldn't change over time - note that unchanged transpilation shouldn't touch the file so browser caches don't have to re-load
- levels of transpiled code
- separate files for separate sub-packages?
### support seaside
- multiple download parts so don't regenerate e.g. core on every page
- SPA Seaside
	- rather than new pages, generate DOM changes and updates the SPA
	- like a distributed React
- depends on better production-time bridge


## Better playground
- accessing all JS globals
- more seamless interaction
	- should not need to use `bridge evalBlock:`
- auto-loading changed code


## Debug remote JS code as Smalltalk code
### openable from debugger

## Documentation plan

## Continuous integration server