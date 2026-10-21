#review2

- Examples using figure 1, shown below.
	- When the segment with SN=1 is transmitted, a timer associated with that segment is started. When the segment with AN=11 is received, which acknowledges receipt of the previously transmitted segment, the timer of the segment with SN=1 is stopped.
	- When the segment with SN=11 is transmitted, a timer associated with that segment is started, since there is no active timer. When the segment with SN=21 is transmitted, no timer is started for that segment [^1]. When the acknowledgment for the two previously sent segments is received, the active timer, associated with SN=11, is stopped.

Figure 1:
![[Ejemplo_Temporizadores_1.png]]

- Examples using figure 2, shown below.
	- When the segment with SN=31 is transmitted, a timer associated with that segment is started. The segments with SN 41, 51 and 61 do not start new timers, since at the time they are transmitted there is already an active timer.
	- When AN=51 is received at host A, it detects that the segment associated with the active timer has been acknowledged. Therefore, the active timer is stopped. In addition, since segments SN=51 and SN=61 are still awaiting acknowledgment, a new timer is started associated with the oldest of them, that is, for SN=51.
	- When AN=71 is received, the active timer is stopped, since the segment associated with that timer has been acknowledged. As there are no segments awaiting acknowledgment, no timer is started.
	- When the segment with SN=71 is sent, a timer is started for that segment. Since that segment is lost, host B, upon receiving SN=81 (out of order), sends a duplicate ACK with AN=71.
	- Since a single duplicate ACK does not trigger any event, the timer associated with segment SN=71 expires, so segment SN=71 is sent again. Host B sends an ACK with AN=91, which, when it reaches host A, stops the active timer.

Figure 2:
![[Ejemplo_Temporizadores_2.png]]

[^1]: it is assumed that there can be only one active timer, as recommended in RFC 2988 [[TCP timers]]
