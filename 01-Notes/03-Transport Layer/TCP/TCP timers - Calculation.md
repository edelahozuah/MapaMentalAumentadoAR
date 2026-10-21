#flashcards/tcp/reliability/timers 
#review2 

- The value to which a [[TCP timers|TCP timer]] is initialized, or *timeout*, is calculated to adapt to network conditions (see [[RTT]])
- $Timeout=RTT_{estimated} + 4\times RTT_{dev}$, where
	- $RTT_{estimated}$ is the mean value of the measured $RTT$s [^1].
	- $RTT_{dev}$ is the *standard deviation* of the measured $RTT$s.
- When an active timer expires, the timeout is recalculated as twice the previous timeout.

[^1]: when a segment is sent, the sending TCP entity starts a stopwatch, which is stopped when an acknowledgment for that segment is received. This makes it possible to obtain samples of the $RTT$ values for different segments.
