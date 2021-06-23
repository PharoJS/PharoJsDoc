# Open Projects

## Continuous integration server

## Documentation
- Plan based on documentation quadrants
- Move old doc from web site and merge it with new contents

## Bridge
### More functional bridge
- Support JS asynchronous messaging

### Usable in production
- allows creating more interactive applications that could interact over the bridge
- work well with Seaside
### Notes
- make a listener process for each bridge that listens for responses
- a read request will lock, check if the numbered response is there yet
	- if not, add to pending dictionary: key=response number, value=a mutex I wait on
- if a callback comes in, check if there is a callback process available. if not, fork one
- callback processes run the callback, then put self in queue to wait for more work
- when a bridge is closed, listener and callback processes destroyed
- 

## Transpiler

### Better dependent transpiler
- Load only the required methods, but pull more methods on demand
- Transpiles just required methods
- Automatic detection of all required methods 
- support `async` and `await`
- use announcements - trigger compilation
  
### Transpile the full Pharo image 
- Analyzer (no code generation) to quickly list methods that cannot be transpiled : primitives, methods relying on `thisContext`, other?

## Exporter
### export libraries
### export workers
### more than one file
- e.g. core  wouldn't change over time - note that unchanged transpilation shouldn't touch the file so browser caches don't have to re-load
- levels of transpiled code
- separate files for separate sub-packages/components?
### support seaside
- multiple download parts so don't regenerate e.g. core on every page
- SPA Seaside
	- rather than new pages, generate DOM changes and updates the SPA
	- like a distributed React
- depends on better production-time bridge


## Playground
Better playground
- accessing all JS globals
- more seamless interaction
	- should not need to use `bridge evalBlock:`
- auto-loading changed code


## Debug remote JS code as Smalltalk code
- allow opening from debugger, a PharoJS playground attached the debugged context

## Related work
Might be worth thinking of porting parts of these
- [Code paradise](https://github.com/ErikOnBike/CodeParadise)
- [Silk](https://smalltalkrenaissance.wordpress.com/2015/06/29/silk-is-just-too-flexible/)
- [Seaside](https://github.com/SeasideSt/Seaside)