# Introducing Stability

New software emerges like a new college graduate, full of optimistic vigor, suddenly facing the harsh realities of the world outside the lab.

Enterprise software must be cynical. Cynical software expects bad things to happen and is never surprised when they do. Cynical software doesn’t even trust itself, so it puts up internal barriers to protect itself from failures. It refuses to get too intimate with other systems, because it could get hurt.

Less tangible, but just as painful, is lost reputation.


## Defining stability

To talk about stability, I need to define some terms. A transaction is an abstract unit of work processed by the system.

When I use the word system, I mean the complete, interdependent set of hardware, applications, and services required to process transactions for users. A system might be as small as a single application, or it might be a sprawling, multitier network of applications and servers.

I use system when I mean a collection of hosts, applications, network segments, power supplies, and so on, that process transactions from end to end.

A resilient system keeps processing transactions, even when there are transient impulses, persistent stresses, or component failures disrupting normal processing.

The major dangers to your system’s longevity are memory leaks and data growth. Both kinds of sludge will kill your system in production. Both are rarely caught during testing.

The trouble is that applications never run long enough in the development environment to reveal their longevity bugs.


## Failure modes

No matter what, your system will have a variety of failure modes. Denying the inevitability of failures robs you of your power to control and contain them. Once you accept that failures will happen, you have the ability to design your system’s reaction to specific failures.

Chiles calls these protections crackstoppers. Like building crumple zones into cars to absorb impacts and keep passengers safe, you can decide what features of the system are indispensable and build in failure modes that keep cracks away from those features. If you do not design your failure modes, then you will get whatever unpredictable—and usually dangerous—ones happen to emerge.


## Chain of failure

A failure in one point or layer actually increases the probability of other failures. If the database gets slow, then the application servers are more likely to run out of memory. Because the layers are coupled, the events are not independent.

At each step in the chain of failure, the crack can be accelerated, slowed, or stopped. High levels of complexity provide more directions for the cracks to propagate in.

One way to prepare for every possible failure is to look at every external call every I/O, every use of resources, and every expected outcome and ask, “What are all the ways this can go wrong?” 


## Patterns and Antipatterns

I’ve dealt with hundreds of production failures. Each one was unique. (They were mostly unique, anyway, since I try not to have the same failure happen twice!) I can’t think of two incidents where the precise chain of failure happened the same way: same triggers, same fracture, same propagation. Over time, however, patterns of failure do emerge.





