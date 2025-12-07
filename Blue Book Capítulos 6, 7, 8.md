## Chapter 6: Protocol for All Objects

+ All is an object.
+ Protocol common to all object is in class `Object`
	+ Default behavior
	+ To modify: override this messages or to add behavior create new messages

### Testing the Functionality of an Object

+ isKindOf: *is a superclass or class of the receiver.*
+ isMemberOf:  *direct instance of the argument, aClass*
+ respondsTo: *receiver's class or one of its superclasses contains the argument, aSymbol, as a message selector.*

### Comparing Objects
+ `==` (Equivalence) test of whether 2 objects are the same object.
+ `=` (Equality): whether two objects represent the same component
	+ What means being equal two objects? Depends on the receiver.
	+ Must reimplement = to specify which of its instance variables should enter into the test.
+ `~=` anObject: do not represent the same component
+ `~~` anObject: are not the same object.
+ ``hash``: Integer computed with respect to the representation of the receiver.

+ ``isNil``: whether the receiver is nil.
+ ``notNil``: whether the receiver is nil.

### Copying Objects

+ ``copy``: another instance just like the receiver
+ ``shallowCopy``: copy of the receiver which shares the receiver's instance variables
+ ``deepCopy``: a copy of the receiver with its own copy of each instance variable
![[copyImage.png]]

### Accessing the Parts of an Object

> Its used mostly in Collections

+ ``at: index`` : value of the indexed isntance variable of the receiver. Report an error if doesnt have indexed variables or it has not
+ ``at: index put: anObject``: put an object in the index value.
+ `` basiAt: index``: same as index it cannot be modified by subclass
+ ``basicAt: index put: anObject``: cannot be modifed in any subclass
+ ``size``: receiver's number of indexed variables
+ `basiSize`: same as size. Cannot be overrided

### Printing and Storing Objects

+ printring
	+ ``printString``: whose characters are a description of the receiver.
	+ ``printOn: aStream``: Append to the argument, aStrearn, a String whose characters are a description of the receiver
+ storing: to store the state of an object
	+ ``storeString``: Answer a String representation of the receiver from which the receiver can be reconstructed
	+ `` storeOn: aStream``: Append to the argument, aStrearn, a String representation of the receiver from which the receiver can be reconstructed

### Error Handling

If a method doens't know how to respond to a message: ``doesNotUnderstand: aMessage.``

+ ``error: aString``: an error occurred in the context of responding to a message to the receive
+ ``primitiveFailed``: Report to the user that a method implemented as a system primitive has failed.
+ ``shouldNotlmplement``:  Report to the user that, although the superclass of the receiver specifies that a message should be implemented by subclasses, the class of the receiver cannot provide an appropriate implementation.
+ ``subclassResponsibility``: Report to the user that a method specified in the superclass of the receiver should have been implemented in the receiver's class.

## Chapter 7: Linear Measures

### Class Magnitude

+ ``< aMagnitude``
+ ``<= aMagnitude``
+ ``> aMagnitude``
+ ``>= aMagnitude``
+ `between: min and: max`: greater than or equal to the argument, rain, and less than or equal to the argument, max.


+ ``min: aMagnitude``: Answer the receiver or the argument, whichever has the lesser magnitude.
+ ``max: aMagnitude``: Answer the receiver or the argument, whichever has the greater magnitude.

### Class Date

An instance of Date represents a specific day since the start of the Julian calendar. A day exists in a particular month and year.

Protocol
+ ``dayOfWeek: dayName``
+ ``nameOfDay: daylndex``
+ ``indexOfMonth: monthName``
+ ``nameOfMonth: monthlndex``
+ ``dayslnMonth: monthName forYear: yearlnteger``
+ ``dayslnYear: yearlntege``
+ ``leapYear: yearlntege``
+ ``dateAndTimeNow``: Array whose first element is the current date (an instance of class Date representing today's date) and whose second element is the current time (an instance of class Time representing the time right now).

#### Create an instance of class Date
+ ``today``
+ ``fromDays: dayCount``: instance of Date that is dayCount number of days before or after January 1, 1901 (depending on the sign of the argument)
+ ``newDay: day month: monthName year: yearlnteger``
+ ``newDay: dayCount year: yearlnteger``

#### Arithmetic
+ ``addDays: dayCount``
+ ``subtractDays: dayCount``
+ ``subtractDate: aDate``

### Class Time

## Chapter 8

