# Interrupt Vector Table

An interrupt vector table is used in low level programming to handle external events such as keyboard and mouse clicks. [Polling](Polling.md) is another method used to handle events, but it uses a constant loop which checks for updates and wastes CPU time if there's no updates to handle.

In low level programming, the concept of *wait for this event and then* isn't the same as it is in higher level programming. The concept of an event is completely different in the low levels than it is in the higher levels. 

The solution to this (allong with polling) is Interrupts. When you click a key on your keyboard, the CPU is interrupted, which means it pauses it's current job to handle the key click.

Interrupt Vector Tables are basically a table of external events mapped to the address of a function. The table content can be defined by software (usually the OS), which maps all the desired interrupts to a function within the program (operating system).

Interrupts are the main way events are handled in low level programming along with [polling](Polling.md).