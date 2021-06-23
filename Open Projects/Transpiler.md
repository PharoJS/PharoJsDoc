### Better dependent transpiler
- Load only the required methods, but pull more methods on demand
- Transpiles just required methods
- Automatic detection of all required methods 
- support `async` and `await`
- use announcements - trigger compilation
  
### Transpile the full Pharo image 
- Analyzer (no code generation) to quickly list methods that cannot be transpiled : primitives, methods relying on `thisContext`, other?
- change optimization to translate primitives rather than selectors
