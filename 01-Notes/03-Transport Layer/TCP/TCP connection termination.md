#flashcards/tcp 
#review2 

- Once the data exchange has finished, either of the two entities (say, A) initiates the closing of the TCP connection by sending a segment with the FIN and ACK flags set to 1. The other entity must send an acknowledgment segment with ACK set to 1. Afterwards, entity B must send another segment with the FIN and ACK flags set to 1, to which A responds with a segment with the ACK flag set to 1.
- Once the connection is closed, both entities release all the resources allocated to the connection ([[TCP sender buffer]], [[TCP receiver buffer]], etc.)

![[Ejemplo_cierre_conexion_TCP.png]]
