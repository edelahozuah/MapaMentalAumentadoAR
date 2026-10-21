#flashcards/tcp/reliability 
#review2 

- Goal: {{to prevent a sender from overflowing [^1] a receiver}}.
- Memory at the receiver.
	- An entity reserves a certain amount of memory to temporarily store information sent to it by the other entity in a [[TCP receiver buffer]]
	- The segments stored in the [[TCP receiver buffer]] are processed in order.
	- The available memory in the [[TCP receiver buffer]] is advertised in every TCP segment sent by the entity.
		- In the [[TCP receive window]] field of the mandatory TCP header.

[^1]: in this context, *overflowing* means receiving more data than can be processed within a given time.
