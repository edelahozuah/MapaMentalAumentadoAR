#flashcards/tcp 
#review2 

- Mechanism used in TCP to {{detect possible errors during transmission}}.
- The sender computes the checksum, which is a function of the contents of the TCP segment to be transmitted and of the IP pseudo-header[^1], and then includes it in the corresponding field of the TCP header. The receiver checks whether the value included in the checksum field matches its own calculation of that value.

[^1]: the IP pseudo-header includes the source and destination IP addresses, the TCP segment length and the transport protocol, as well as a fixed sequence of zeros (see [[IP pseudo-header]]). This pseudo-header is only used to compute the checksum, but it is **not transmitted**.
