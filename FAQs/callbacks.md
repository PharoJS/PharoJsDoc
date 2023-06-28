# Dealing with NodeJS Callbacks

When using NodeJS, callbacks are a fact of life.
Many NodeJS packages provide functions that run asynchronously calling
a callback function upon error or completion.  The PharoJS way to
provide these callbacks is with Smalltalk blocks.  Normally these will
take 2 parameters: an error value and a success value.  The key point
is that you should NOT attempt to return from these callbacks.
Firstly, the return will not make any sense as the original call stack
has long since disappeared.  Secondly, Smalltalk non-local returns are
implemented in PharoJS as throwing a value, which will appear to the
NodeJS runtime as an uncaught error, and abort execution.
