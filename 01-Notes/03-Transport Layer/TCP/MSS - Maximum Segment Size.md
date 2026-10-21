#flashcards/tcp
#review2 

# MSS
## What is it?
- {{Maximum amount of **data** that a TCP segment can carry}}
## What does it depend on?
- {{It depends on the MTU[^1] and on the size of the network-layer and transport-layer headers: MSS = MTU - network_header - transport_header}}
## When is the MSS of the TCP connection agreed?
- {{During the connection establishment phase: the client sends its MSS, then the server replies with its own MSS, and finally both entities compute the connection MSS as the minimum of the values announced by both ends. Each entity sends its MSS in an **optional** field of the TCP header, only in the first two segments (SYN and SYN+ACK)}}

[^1]: [[MTU]]
