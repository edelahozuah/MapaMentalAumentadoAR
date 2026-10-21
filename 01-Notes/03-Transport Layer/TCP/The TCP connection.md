#flashcards/tcp
#review2 

- TCP is full-duplex
	- This means that {{both entities can send data to their peer entity[^1]}}
- TCP provides a byte stream, not a message stream.
	- What TCP receives from the application layer is a stream of bytes, and therefore at the receiver the TCP layer has no notion of messages.
- TCP is a point-to-point protocol (there are only two connected entities)
	- It does not allow [[Multicast]] (one device sends to a group of devices) or [[Broadcast]] (one device sends to all other devices on the network)
- A TCP connection must be established before sending segments with data, in order to negotiate the connection parameters (see [[TCP connection establishment]])
- Once the TCP connection establishment phase ends:
	- The client process passes data to the TCP layer using the created {{[[TCP socket]]}}.
	- TCP performs [[Segmentation]] if necessary, adds a TCP [[Header]] to those segments and generates PDUs
- Once the data exchange is over, the TCP connection must be closed (see [[TCP connection termination]])

![[Socket_TCP.png]]

[^1]: [[Peer entities]]
