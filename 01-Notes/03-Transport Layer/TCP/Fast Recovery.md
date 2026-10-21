#flashcards/tcp/congestion 
#review2 

- It is a recommended, not mandatory, mode, although most current implementations include it.
- In this mode, the aim is to recover from the loss of a segment as quickly as possible.
- cwnd is increased {{by one MSS for each duplicate ACK received}}.
- When the ACK for the missing segment is received, then:
	- cwnd = ssthresh
	- Switch to [[Congestion Avoidance]] mode
- When the timer expires
	- ssthresh = 0.5 (cwnd value when the timer expires)
	- Set cwnd = 1 MSS.
	- Switch to [[Slow Start]] mode
