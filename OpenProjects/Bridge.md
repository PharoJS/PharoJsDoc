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
