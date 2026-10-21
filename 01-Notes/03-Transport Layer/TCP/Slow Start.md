#flashcards/tcp/congestion
#review2

- It is one of the TCP congestion control algorithms.
- It is the mode TCP starts in after the establishment of [[The TCP connection]]
- When starting in this mode, the [[TCP congestion window]] (cwnd) is {{1 [[MSS - Maximum Segment Size|MSS]]}}.
- When an ACK is received, *cwnd* is increased by {{the same number of bytes acknowledged:
	- If an ACK acknowledging 1 MSS is received, cwnd is increased by 1 MSS. In general, if *n* MSSs are acknowledged, cwnd is increased by *n* MSSs.}}
- *Slow start* mode ends when any of these three events occurs:
	- cwnd reaches the [[TCP threshold]] (ssthresh)
		- Switch to [[Congestion Avoidance]] mode
	- The [[TCP timers|timer]] expires.
		- Severe congestion in the network is assumed.
		- Update ssthresh = 0.5 (cwnd value when the timer expires)
		- Update cwnd = 1
		- *Slow start* begins again
	- Three duplicate ACKs are received.
		- Mild congestion in the network is assumed.
		- Update ssthresh = 0.5 (cwnd value when the third duplicate ACK is received)
		- Update cwnd = ssthresh + 3
		- Switch to [[Fast Recovery]] mode
