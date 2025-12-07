## Intent

Distribute processing of a request over a structure by delegating polymorphically. Object Recursion transparently enables a request to be repeatedly broken into smaller parts that are easier to handle.

## Motivation

+ Two objects are equivalent. Simple objects easy. But when it comes to complex objects?

Use a comparer: that breaks the process into pieces until all of the peices are simple to compare

+ Underisable consequences
	+ What kind of objects is it?
	+ How to decompose it?
	+ A developer needs to add something to the comparer

Another approach:
+ Tell the comparrer to compare themselves
	+ *What* to do and no *how*
+ The objects consider what needs to be breaking and then delegates those pieces to the next one

![[objectRecursionImage.png]]

## Keys

+ 2 Polymorphic classes:
	+ One which handles a request recursively and another whuch simply handles the request without recursing
+ A separate message, usually in a third class that is not polymorphic with the first two, to initiate the request.
## Applicability

+ passing a message though a linked structure where the ultimate destination is unknown
+ Broadcasting a message to all nodes
+ Distributing behaviors responsability thoughout a linked structure

## Structure

![[objectRecursionStructure.png]]

## Consequences
Advantages 
+ Distributed processing: distributed across a structure of handlers that can be as numerous and arranged as complexly as necessary to best complete the task.
+ Responsability flexibility:
	+ Initiator doesn't know about all the handles, arrengament or processing
	+ Handler arrangment can change at runtime to reconfigure the handling responsabilities
+ Role flexibility:
	+ + Handler accs as a recurses may be a terminator for another request
+ Increased encapsulation:
	+ Encapsuletes the how to handle a request

Disadventages
+ Programming complexity: it may be difficult and it may be overused and there could me many sent messages that are difficult to understand.

## Implementation

+ Separate initiator type:
	+ As long as a method has senders, it shouldn’t be deleted. This is not true when the only senders of a method are other implementors of the same message, as is the case with object recursion. Unless there is another, non- polymorphic method to start off the recursion, none of the implementors will ever be run and they can all be deleted.
+ Defining the successor
	+ The terminator doesnt need an end.

## Related patterns

### Vs Composite and decorator
Decorator delegates to its component or a Composite this might be considered an example of Object Recursion. However, Composite and Decorator are structural (data structure) patterns, whereas Object Recursion is a behavioral (algorithm) pattern

### Adapter
+ Can sem to use a non-polymorphic form of object recursion
+ lack of polymorphism goes against the spirit of Object Recursion
### Object Recursion and Delegation

implements a message by delegating the same message to a collaborator of the same type: Proxy is a good example

+ one-level-deep example of Object Recursion, which is not a very interesting example