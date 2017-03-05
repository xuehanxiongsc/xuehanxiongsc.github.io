---
layout: post
title:  "The power of writing"
date:   2017-03-03 20:02:00 -0800
categories: jekyll update
---
During my [thesis](http://www.ri.cmu.edu/publication_view.html?pub_id=8016) writing, 
many new ideas came up by simply writing down what I’ve already done in an organized fashion. 
There must be something magical about this process of writing. 
Professor [Manuel Blum](https://www.cs.cmu.edu/~mblum/) explained it the best:
```
You are all computer scientists.
You know what FINITE AUTOMATA can do. 
You know what TURING MACHINES can do. 
For example, Finite Automata can add but not multiply.
Turing Machines can compute any computable function.
Turing machines are incredibly more powerful than Finite Automata.
Yet the only difference between a FA and a TM is that 
the TM, unlike the FA, has paper and pencil.
Think about it. 
It tells you something about the power of writing.
Without writing, you are reduced to a finite automaton.
With writing you have the extraordinary power of a Turing machine.

                                                               -- Manuel Blum
```
To be a Turing machine, you need a unlimited memory tape. Even for our brain memory is limited. 
Writing is similar of passing knowledge through a forget gate[^1], 
and leaving a pointer in the brain for later retrieval purposes. 
Also, you are writing a condensed, filtered, distilled version of the raw observation 
(e.g., a 4096-dimensional vector in fc7 from the [VGG](http://www.robots.ox.ac.uk/~vgg/research/very_deep/) network). 
Later, reviewing those writings loads the "knowledge vectors" into the brain, 
together with new observation resulting in new thoughts. 

Does the above process remind you some type of networks? Yes, Recurrent Neural Networks (RNNs).
Those "knowledge vectors" are known as hidden states in RNNs. The same writing power makes RNNs Turing-Complete while feed forward networks are not. 
The computer memory is limited and you almost need an infinite dimensional hidden vector to 
capture life-long dependencies of knowledge. 
This makes life-long learning impossible under the current structure of RNNs, 
which lacks of a “reviewing process”.  The reviewing process could be implemented as follows: 
we periodically write the knowledge vectors to the disk since we can almost have infinite 
amount of disk space. And, periodically load them in a mini-batch fashion into the memory 
and combine with recent observation to generate new thoughts. However, such structure cannot be 
trained end-to-end since disk operations are not differentiable. Life-long learning modeled as 
RNNs could be an interesting research topic for decades to come. 

Let me end this post in a fun note. The great wizard [Albus Dumbledore]( https://en.wikipedia.org/wiki/Albus_Dumbledore) is a master of memory extraction spell.
Over the years, he repeated extracting important memories into a flask, 
and reviewing them in a [Pensieve](http://harrypotter.wikia.com/wiki/Pensieve) when new information present themselves. 
Finally, when the last piece of evidence (Professor Horace Slughorn’s memory) was found, 
all dots were connected and he discovered Lord Vodemont’s darkest secret -- Horcruxes. 
One man’s memory is another man’s observation. Well, Albus may just inspire a new research topic on cross operations on multiple RNNs. 

<p style="text-align:center"><img src="https://xuehanxiongsc.github.io/images/Dumbledore-memory.jpg" alt="Dumbledore" style="width: 50%"/></p>

Disk (or paper if you prefer the old fashion way) is the extension of your memory that makes you a true Turing machine. 
Be patient and your “Horace Slughorn’s piece” will eventually arrive to assist you on whatever difficult problems you are working on 
or even saving the world from the uprise of evil robots. Meanwhile, keep on writing. See you next time.

[^1]: forget gate is implemented as a sigmoid layer in LSTM to decide what information to throw away from the cell state. 
