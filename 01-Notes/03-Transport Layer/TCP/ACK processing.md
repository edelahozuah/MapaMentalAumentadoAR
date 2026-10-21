#flashcards/tcp/reliability/timers 
#review2 

- When an ACK is received, the TCP entity that has segments awaiting acknowledgment must:
	- Compare the value of the [[TCP acknowledgment number]] (AN) with the internal variable **SendBase**, which stores {{the oldest [[TCP sequence number]] still awaiting acknowledgment}}
	- If AN > SendBase, this means that {{the ACK acknowledges one or more segments that were awaiting acknowledgment}}. Therefore:
		- The SendBase variable is updated to the oldest sequence number still waiting to be acknowledged.
		- If there are still unacknowledged segments, the timer value is updated ([[TCP timers - Calculation]]) and {{a new timer is started}} associated with the {{oldest segment still awaiting acknowledgment}}.
