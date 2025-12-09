Link: https://archive.org/details/byte-magazine-1981-08/page/n299/mode/1up

# Resumen

Smalltalk: creado para proveer soporte en computadora para el espíritu creativo de todos. 

Se enfocaron en:
+ El **lenguaje de programación**: interfaz entre modelo mental y hardware
+ **Interfaz (user interface)**: que permite la comunicación del humano con la computadora

Tuvo un desarrollo de 2-4 años ciclos, desde el 72' hasta el 80' siguiendo el método científico:
+ Build an application program with the current system
+ Aprender de la experiencia y rediseñar el lenguaje. Formulate theory
+ Crear un nuevo sistema.

Los principios por los que se basaron:
+ **Personal mastery**: cada uno debería de ser capaz de entender todo el sistema para que se desarrolle el espíritu creativo. Las barreras que existan serían barreras a la creatividad.
+ **Good design**: tener un conjunto de partes no cambiables que sean lo más generales posibles
+ **Language**: se basaron en el lenguaje cotidiano, pues se perfecciono durante millones de años
+ **Objetivo del lenguaje**: proveer un framework para la comunicación humano-computadora
	+ "body" de computadora: el display de información
	+ "mind": memory y los elementos de procesamiento
+ **Scope**: querían hacer una forma de interactuar humano-computadora
  ![[relation mind-computer.png]]
+ **Communicating Objects**:
	+ If one wishes to participate, draw distinctions
	+ Identifies an object and the rest is not-that-object
	+ Identies an object and associate a unique identifier with an object
	+ **Objects**: should support the concept of object and provide **uniform** means for **referring to the objects** in its universe
	+ Objects are created when **expressions are evaluate**d and they are passed by reference. When there's no reference in  the system, its storage is reclaimed.
	+ Object metaphor: all its an object and the computation occur by message sending
	+ **Storage management**: must provie automatic storage managment. No debería encargarse el programador de eso, pues nos salimos del modelado
	+ **Messages**:  Computing should be viewed as an intrinsic capability of objects that can be uniformly invoked by sending messages.
	+  **understanding that the receiver knows best how to carry out the desired operation**. En esto se basa el envío de mensajes
	+ **Send of messages it's a process outside of objects since messages travel between objects**
+ **Uniform metaphor**: A language should be designed around a **powerful metapho**r that can be **uniformly applied in all areas.**
	+ LISP, which is built on the model of linked structures
	+  Smalltalk, which is built on the model of communicating objects.
	+  large applications are viewed in the same way as the fundamental units from which the system is built
	+ Every object in Smalltalk, even a lowly integer, has a set of messages, a protocol, that defines the explicit communication to which that object can respond.
+ **Organization**
	+ A unifrom metaphor provides a framwork in whihc complex systems can be built
+ **Modularity**: 
	+ No component in a complex system should depend on the internal details of any other component.
	+ It makes it the coupling imposible to manage as its cuadratic
	+ The complexity of a system can often be reduced by grouping similar components.
+ **Classification**: A language must provide a means for classifying similar objects, and for adding new classes of objects on equal footing with the kernel classes of the system.
	+  objectification of nessness
	+ At each stage of design, a human will naturally choose the most effective representation if the system provides for it. 
+ **Polymorphism**: A program should specify only the behavior of objects, not their representation.
	+  a program should never declare that a given object is a Smalllnteger or a Largelnteger, but only that it responds to integer protocol. Such generic description is crucial to models of the real world.
	+ The message interface establishes an ideal framework for such extension. Provided that street sweepers support the same protocol as all other vehicles, no changes are needed to include them in the simulation:
+ **Factoring**:  Each independent component in a system should appear in only one place.
	+  it saves time, effort, and space if additions to the system need only be made in one place.
	+ Smalltalk encourages well-factored designs through inheritance. Every class inherits behavior from its superclass. This inheritance extends through increasingly general classes, ultimately ending with class Object which describes the default behavior
+ **Leverage**: When a system is well factored, great leverage is available to users and implementers alike.
+ **Virtual Machine**: A virtual machine specification establishes a framework for the application of technology.
	+ establishes an object-oriented model for storage, a message-oriented model for processing, and a bitmap model for visual display of information
+ **user interface**: 
	+ language in which most of the communication is visual
+ **Reactive Principle**: Every component accessible to the user should be able to present itself in a meaningful way for observation and manipulation.
+ **Operating System**: An operating system is a collection of things that don't fit into a language. There shouldn't be one.
	+ Things that have been incorporated into Smalltalk langauge:
		+  Storage management — Entirely automatic. Objects are created by a message to their class and reclaimed when no further references to them exist. 
		+ File system 
		+  Display handling — The display is simply an instance of class Form, which is continually visible
		+ Keyboard input:  as objects with appropriate messages for determining their state or reading their history as a sequence of events
		+ Debugger: accessible as an instance of class Process
### Future Work

The continued application of the principles in this paper
+ message protocols have not been formalized.
+  clearly other aspects to human thought that have not been addressed in this paper. 

> **Se confundió muchisimo**

**Natural Selection**: Languages and systems that are of sound design will persist, to be supplanted only by better ones.