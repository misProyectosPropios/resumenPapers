## Abstract

Self:
+ object-oriented language; 
+ Used for exploration;
+ Based on
	+ Prototypes: inheritance and instantiation. Simpler and more flexible than other languages
	+ Slots unite variable and procedures in a single construct
		+ Permits the inheritance hierarchy to take over the function of lexical scoping
+ Narrows the gaps between objects, procedures and closures.

## Introduction
Object-oriented languages: offer a useful perspective for designing programs.
There are some different perspective. Self presents a new perspective.

It has
+ runtime typing (no type declaration)
+ Automatic storage reclamation
+ Doesn't have any class neither variables
+ Prototype metaphor for object creation


Smalltalk has: sending message and variables, while in self there's only messages. To access "instance variables", send self. 
> Name came from the use of *self*

It's an even more uniformity than smalltalk. Only send messages. Greater expressive power.

### Principles of design of self

+ Messages at the bottom:
+ Occam's razor
	+ As Smalltalk
	+ Different from Smalltalk
+ Concreteness

## Prototypes: Blending classes and instances

## Comparing prototypes and classes
+ Simpler relationships
+ Creation by copying
+ Examples of pre-existing modules
+ Support for one-of-a-kind objects
+ Elimination of meta-regress
## Blending state and behavior
No direct way to access variable: send message to access data or set the data. 
makes it the inherentance more powerful. 
>Example: create a new kind of point, whose x coordinate is a random number, copy the standar point remove the x: slot and replace the content of the x slot with the code to generate a random number. (so we can modify the slots)

Active varialbes is trivial, because we can modify all the slots freely.

+ Message passing is less powerful if you have assignment different from a message
	+ Harder for specialization to replace a variable with computed result
	+ Class based languages store the names and orders of instance variables in an objects class
	+ Add accidental complexity because of scopes.
## Closures
Easy-to-use metaphor for users to exploit and define control structures.
+ Fundamental for language with user-defineed abstract data types

Blocks are similar to objects (store behavior and state)
**Self**: created with objects.

+ **Local variables**: require storage for local variables: *slots*
+ 