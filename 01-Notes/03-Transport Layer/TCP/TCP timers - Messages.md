#flashcards/tcp/reliability/timers 
#review2 

- When it receives a message from the [[Application layer]], TCP segments it ([[Segmentation]]) if necessary, adds the corresponding TCP header, and passes it to its [[Network layer]] (in the case of the Internet model, to the [[IP protocol]]).
- If there is no active timer, {{a timer associated with that segment is started}}.
