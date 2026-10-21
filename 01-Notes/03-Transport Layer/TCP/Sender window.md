#flashcards/tcp 
#review2 

- The sender window (SW) is the number of bytes that an entity can transmit without waiting for ACKs, taking into account both [[TCP flow control]] and [[TCP congestion control]]:
	- SW = min(Congestion window, Receive window[^1])=min(cwnd,rwnd)
- SW indicates the maximum number of bytes that can be transmitted, but it is useful to use an auxiliary variable to count the number of bytes in the [[TCP sender buffer]] that are awaiting acknowledgment, which we will call BS (bytes sent). Thus:
	- BS = LastByteSent - LastByteAcked ≤ SW = min(cwnd, rwnd)
	- BS ≤ SW

[^1]: it is important to remember that both entities have their own congestion and receive windows. In this case, the SW of a TCP entity is computed as the minimum of the local cwnd and the rwnd reported by the other entity using the [[TCP receive window]] field
