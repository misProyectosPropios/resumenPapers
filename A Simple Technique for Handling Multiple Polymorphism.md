## Link:

# Paper

## Abstract

Some situations arise that lead to multiply polymorphic expressions.
Expression whcih several terms may each be of variable type

>This occurs when an operation or expression involves _several_ terms, and the specific behavior depends on the _combination_ of types of those multiple terms.

## Polymorphism and messages

OO introduced to have polymorphism in extensible languages.
But, if a problem depends of 2 types, then the naive solution violates modularity or/and encapsulation. 

Then, it came message paradigm:  absorbs the need for type testing.

> Different but appropriate results will be produced depending on the type of each receiver. It has same purpose, but differents outcomes because they are not the same.

### Problem
More than one variable in an expression is independently polymorphic.

Leads to: explicit type testing. 
+ Problems with modularity.

+ Example:
	+ Graphical objects with display ports



```asd
displayOn: aPort 
	aPort isMemberOf: DisplayPort 
		ifTrue: ["code for displaying on DisplayPort"]. 
	aPort isMemberOf: PrinterPort 
		ifTrue: ["code for displaying on PrinterPort"]. 
	aPort isMemberOf: RemotePort 
		ifTrue: ["code for displaying on RemotePort"|.
```

> Thus the programmer has been let down by conventional message dispatch, which only supports polymorphism of message receivers, not of arguments as well

Problemas
+  a new kind of object will result in failure of existing code, possibly leading to complete loss of environmental support
+ The furst message dispatch only does half the job
+ It doesn't do what OO was supposed to cure


So, it needs some abstractions. 
> **Send more messages!!!**

Solution

```
	aPort displayRectangle: sel
```

```
<DisplayPort> displayRectangle: aRect 
	"code to display a rectangle on a displayPort" 

<DisplayPort> displayOval: aRect 
	"code to display an oval on a displayPort" 
	<DisplayPort> displayBitmap: aRect "code to display a bitmap on a displayPort" ... and similarly for the other graphical objects, <PrlnterPort> displayRectangle: aRect "code to display a rectangle on a printerPort" <PrinterPort> displayOval: aRect "code to display an oval on a printerPort" < PrinterPort> displayBitmap: aRect "code to display a bimmp on a printerPort" ... and similarly for the other graphical objects,
```

And the port should know how to deal with it

**What it achieves**

+ This solution preserves the modularity of object-oriented programming style.
+ Adding a new port class is even simpler, as it amounts only to implementing the full family of displayX: messages.
+ It mantains modularity
+ We don't want to modify existing code to add new kinds of objects
+ Each message dispatch reduces a further degree of polymorphism

## Experience

It describes how it benefits some existing projects. Smalltalk arithmetic for example