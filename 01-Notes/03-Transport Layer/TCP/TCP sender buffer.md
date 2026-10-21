#flashcards/tcp/reliability 
#review2 

- A TCP entity must store the sent segments in temporary memory, or sender buffer. 
- As soon as acknowledgment of the correct receipt of the segment is received, the TCP entity can remove the segment from its sender buffer.
- If [[TCP retransmission|retransmission]] of a segment is needed, it is taken from the sender buffer.
