#flashcards/tcp/reliability 

- A sender must store the segments it has sent in its [[TCP sender buffer]].
- When a [[TCP timers|timer]] expires or when entering [[Fast Recovery]] mode, the sender must resend the oldest segment awaiting acknowledgment.

