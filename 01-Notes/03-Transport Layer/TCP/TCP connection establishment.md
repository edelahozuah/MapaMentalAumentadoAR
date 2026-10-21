#flashcards/tcp 
#review2 

- TCP connection establishment is carried out by means of a three-way handshake
	- Exchange of **three special segments**.
		- The first two segments ({{SYN and SYN+ACK}}) do not carry [[Application layer]] data. These two segments include optional headers that are used to negotiate the [[MSS - Maximum Segment Size|MSS]].
		- The third segment ({{ACK}}) _can_ carry [[Application layer]] data
	- TCP connection establishment ends with the setting up of {{the state variables[^2] and buffer capacities[^1]}} that will be used in the data transfer phase.
![[Ejemplo_conexion_TCP.png]]

[^1]: [[TCP receiver buffer]] and [[TCP sender buffer]]
[^2]: [[TCP state variables]]
