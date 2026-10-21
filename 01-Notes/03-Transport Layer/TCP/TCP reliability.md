#flashcards/tcp/reliability 
#review2 

- Reliability in TCP consists of detecting {{both **packet losses** (using the [[TCP sequence number]]) and **errors** [[TCP error detection]] (using the [[TCP checksum]] of each segment), as well as correcting these problems by **retransmitting the affected segments** ([[TCP retransmission]]).}}
- To be able to detect packet losses, senders must identify each segment with a [[TCP sequence number]] when [[Sending segments in TCP|sending segments with data]]. 
- In turn, receivers use the [[TCP acknowledgment number]] to acknowledge receipt of segments, according to the [[TCP ACK generation policy]]. These acknowledgments are cumulative [[Cumulative acknowledgments]].
- When receiving segments with acknowledgments, the receiver must [[ACK processing|process the ACKs]].
	- A TCP entity must store the segments it sends in a [[TCP sender buffer]]
- When segments are lost, a sender may not receive the receiver's acknowledgments. [[TCP timers]] are used for this purpose. When a timer expires, [[TCP retransmission]] begins.

- #todo link examples

