# Polling

Polling is one way to manage low level external events. As apposed to [interrupts](Interrupts.md) which maps events to a function, polling is the process of a function checking the status of an external device. The difference between interrupts and polling is that interrupts call a function within the software when an event occurs, while polling is the process of checking the status of external devices (or events), which may require a loop to constantly check statuses which can lead to unnessesary resource usage. 

according to my knowledge so far:

Interrupts are the best approach for handling events in most cases, but polling is needed for some applications, and (I believe), some hardware doesn't support interrupts, in which case polling is the only option.