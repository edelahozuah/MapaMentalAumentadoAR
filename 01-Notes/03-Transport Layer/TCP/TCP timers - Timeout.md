#flashcards/tcp/reliability/timers 
#review2 

- When a timer expires, TCP retransmits {{the segment associated with that timer}} which, following the recommendation of RFC 2988, will be the {{oldest segment awaiting acknowledgment}}.
- The timer duration is redefined as {{twice the previous timer value}}.
- A new timer associated with the resent segment is started.
