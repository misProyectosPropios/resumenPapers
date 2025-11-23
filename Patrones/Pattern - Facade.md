## Intent

Provide a unified interface to a set of interfaces in a subsystem. Facade defines a
higher-level interface that makes the subsystem easier to use.

## Example

+ En **TusLibros**, cuando queríamos simular la interfaz de la parte del modelo (conexión entre controlador y modelo) usamos un facade para poder testear más fácilmente las respuestas de las funcionalidades del modelo 

## Motivation
A common design goal is to minimize the communication and dependencies between subsystems. One way to achieve this goal is to introduce a facade object that provides a single, simplified interface to the more general facilities of a subsyste
## Applicability
+ Provide a simple interface to a complex subsystem
	+ makes the subsystem more reusable and easier to customize, but it also becomes harder to use for clients that don't need to customize it. A facade can provide a simple default view of the subsystem that is good enough for most clients. Only clients needing more customizability will need to look beyond the facade
+ facade to decouple the subsystem from clients and other subsystems, thereby promoting subsystem independence and portability.
+  layer your subsystems. Use a facade to define an entry point to each subsystem level.

## Structure and colaborations:
![[facadePattern.png]]

## Participants
+ Facade
	+ Knows which classes are responsible for a request
	+ Delegates cliente requests to appropriate subsystem objects
+ Subsystem classes
	+ Implement subsystem functionality.
	+ Handle work assigned by the Facade object
	+ They have no references of facade, they just work

We could think of a facade as an adapter for the subsystem, but it's more than a adapter. It could add more information and more funcitonality
## Advantages
+ The client uses it as a black-box to a very complicated structure
+ It promotes weak coupling between the subsystem and its clients.
+ It doesn't prevent applications from using subsystem classes if they need to
	+ This is the difference between an adapter an a facade
## How to use it
Create a class facade which interacts with the subsystems classes and use it to call the model instead of actually calling all the facade