#flashcards/tcp/congestion 
#review2 

- TCP congestion control mode in which the [[TCP congestion window]] is increased linearly.
- The [[TCP congestion window]] (cwnd) is increased by {{one unit when cwnd acknowledgments are received.
	- Example: if cwnd is 10 MSS [^1], 10 segments of MSS bytes can be sent. When the ACK acknowledging the tenth segment is received, cwnd becomes 11.}}
- Therefore, cwnd is increased by $MSS/cwnd$ each time the ACK for a segment is received [^1].
- Congestion Avoidance mode ends when either of these two events occurs:
	-  The [[TCP timers|timer]] expires.
		- Severe congestion in the network is assumed.
		- Update ssthresh = 0.5 (cwnd value when the timer expires)
		- Update cwnd = 1
		- Switch to [[Slow Start]] mode
	- Three duplicate ACKs are received.
		- Mild congestion in the network is assumed.
		- Update ssthresh = 0.5 (cwnd value when the third duplicate ACK is received)
		- Update cwnd = ssthresh + 3
		- Switch to [[Fast Recovery]] mode

[^1]: the RFC uses the previous cwnd, not its integer value (here we use the integer value to simplify the calculation).
