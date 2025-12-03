## Caso:

> You have a method that does not simplify well with Composed Method (p. 21).

The behavior at the center of a complex system is often complicated.
It has many instance variables, temporary variables and many parameters.

If applied Composed method, messages with many parameters.

## Solution: 

Create an object to represent an invocation of the method and use the shared namespace of instance variables in the object to enable further simplification using Composed Method. However, these objects have a very different flavor than most objects. Most objects are nouns, these are verbs. Most objects are easily explainable to clients, these are not because they have no analog in the real world.

## Technique

Create a class named after the method. Give it an instance variable for the receiver of the original method, each argument, and each temporary variable. Give it a Constructor Method that takes the original receiver and the method arguments. Give it one instance method, #compute, implemented by copying the body of the original method. Replace the method with one that creates an instance of the new class and sends it #compute.

Anécdota del tipo: le consiguió un trabajo este patrón porque el lider vio este patrón y dijo. Este tipo sabe.