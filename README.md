# Pipelining
how CPUs save time

Say you ran a successful crowd-funding-campaign for a cool gadget you designed. The gadgets just arrived from the factory and now you need to package mail and mail them to thousands of people.

Packaging and mailing consitst of a number of separate steps:
- folding a box
- wrapping the gadget in bubble wrap
- putting the gadget into the box, along with a manual
- clsoing the box and secure it with sticky tape
- put on an address label (with a digital stamp)
- carry the box to the post-office

If you are alone, there is no other way then to do all those steps yourself and in sequence (one aftaer another). You can optimize the process a little bit by doing the separate steps in batches: Instead of carrying each individual box to the post office, you might, as a very last step, transport all of them at once to the post office (if you have a van). Likewise, you might work more efficient by first folding all the boxes, then wrapping all the devices etc. This however is more or lass all you can do to save time when you are alone.

If, on the other hand, there are some friends that can help you, you can save a lot of time by doing steps in parallel: While you put an address label onto a box, a friend can already wrap the gadget that goes into the next box, while yet another friend can already fold the next box etc. This is called a pipeline. Pipelining is what processors do to dave time as well. 

Depending on how many friends are willing to help you, you can reach different levels of parallelism. If there's only two of you, both of you most likely will perform a sequence of tasks, but you both work in parallel. If however there are as many people as there are tasks, you take advantage of the full potential of pipelining: every task is perfomred in parallel with every other task.

In a CPU the tasks (or stages) are:

- fetch an instruction from memory
- decode the instruction (figure out what it means)
- read values from memory
- perform the logic or arithmetic operation
- write to memory

In microprocessor design the level of parallelism is dictated by the maximum amount of transistors you can fit onto a chip (or are willing to fit onto a chip). The more transistors you use, the bigger your CPU gets, the more power it consumes, the longer you need to design it and thus the more expensive it will be. (Compare this to the number of friends in the mailing example above)

Because of Moore's law (Moore observed that, between 1980 and 2006, (TODO: fact check) the numbers of transistors you could fit onto the same size of silicon doubled every two years), pipelining became more and more popular among CPU designers. (Imagine, if the number of your friends would double every two years, what positive effect that would have on the amount of time it takes to mail your gadgets!)

