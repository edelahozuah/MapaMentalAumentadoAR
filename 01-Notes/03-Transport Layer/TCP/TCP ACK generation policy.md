#flashcards/tcp 

- Recommendation according to RFCs 1122 and 2581.
- Segments received out of order are NOT discarded. Acknowledgments are cumulative.
- On arrival of a segment from the other entity:
 
| **Identifier** | **Event** | **TCP Receiver Action** |
| --- | --- | --- |
| CR1 | TCP connection establishment or termination | ACK is sent immediately |
| CR2 | There is data to send to the other entity | ACK is sent immediately |
| CR3 | Segment received with the expected sequence number. Previous sequence numbers already acknowledged. No other in-order segment waiting for an ACK to be sent. | Delayed ACK*. Wait 500 ms for the arrival of another in-order segment. If none arrives, send ACK. |
| CR4 | Segment received with the expected sequence number. Another in-order segment is waiting for an ACK to be sent. | Single cumulative ACK. Both in-order segments are acknowledged immediately. |
| CR5 | Out-of-order segment received, with a number higher than expected. A “gap” is detected. | Duplicate ACK. An ACK is sent immediately with the sequence number of the next expected byte (lower end of the “gap”). |
| CR6 | Segment received that partially or completely fills a “gap” in the received data. | Immediate ACK. An ACK is sent immediately if the segment starts at the lower end of the “gap”. Otherwise, immediate duplicate ACK. |
