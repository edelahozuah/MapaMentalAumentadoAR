#flashcards/tcp/reliability/timers
#review2 

- Timer management requires a lot of resources, so for TCP, [RFC 2988](https://datatracker.ietf.org/doc/html/rfc2988) **recommends**
	- A single retransmission timer, regardless of the number of segments awaiting acknowledgment.
- Important events at the TCP sender, related to data transmission and retransmission, are:
	- Messages received from an application ([[TCP timers - Messages]])
	- Timeout ([[TCP timers - Timeout]])
	- Reception of a new ACK ([[ACK processing]])
