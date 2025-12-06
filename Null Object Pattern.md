## Intent

Provide a surrogate for another object that shares the same interface but does nothing. The Null Object encapsulates the implementation decisions of how to “do nothing” and hides those details from its collaborators

## Motivation

A class requires a collaborator that does nothing. It should be treated as the ones that does something.

For example, we know that all the View and it needs to require a controller. There, we want a read-only. The controller thus shouldn't do anything because 

+ The key to the Null Object pattern is an abstract class that defines the interface for all objects of this type. The Null Object is implemented as a subclass of this abstract class. Because it conforms to the abstract class’ interface, it can be used any place this type of object is needed.

## Applicabiliity

Use it when
+ an object requires a collaborator;
+ some collaborator instances should do nothing
+ client should be able to ignore difference between collaborator and nothingness. 

## Structure

![[nullPattern.png]]

## Example

Model View Controller (MVC). If they are read-only

## Consequences

+ Defines class hierarchies consisting of real objects and null objects. 
+ Make client code simple
	+ Treat collaboratorand null collaborators uniformly.
+ Encapsulates the do nothing into the null object
+ easy to reuses code to do nothing
+ can necessitate creating a new NullObject class for every new AbstractObject class.
+ can be difficult to implement if various clients do not agree on how the null object should do nothing.
+ always acts as a do nothing object. The Null Object does not transform into a Real Object. 

## Implementation

+ Special null instance of Real Object
+ Clients don’t agree on null behavior. If some clients expect the null object to do nothing one way and some another, multiple NullObject classes will be required. If the do nothing behavior must be customized at run time, the NullObject class will require pluggable variables so that the client can specify how the null object should do nothing
+ Null Object as special Strategy. A Null Object can be a special case of the Strategy pattern
+ Null Object is not Proxy. 
+ Null Object as special State. A Null Object can be a special case of the State pattern 
+ The Null Object class is not a mixin. Null Object is a concrete collaborator class that acts as the collaborator for a client which needs on
## Known Uses

+ NoController
+ NullInputManager
+ NullScope
+ Null Lock