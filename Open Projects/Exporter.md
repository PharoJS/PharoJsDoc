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

