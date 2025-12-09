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

+ represents a particular second in a day
	+ start at midnight.

General Protocol

+ ``millisecondCIockValue``: number of milliseconds since themillisecond clock was last reset or rolled over to 0.
+ ``millisecondsToRun: timedBIock``: the number of milliseconds timedBIock takes to return its value.
+ ``timeWords``: seconds (in Greenwich Mean Time) since Jan. 1, 1901
+ ``totalSeconds``: total seconds from Jan. 1, 1901,
+ ``dateAndTimeNow``: Array whose first element is the current date (an instance of class Date that represents today's date) and whose second element is the current time

#### Instace creation
+ `now`: instance of Time representing thesecond the message is sent.
+ `fromSeconds: secondCount`: instance of Time that is secondCount number of seconds since midnight.

#### arithmetic

+  ``addTime: timeAmount``: instance of Time that is the argument, timeAmount, after the receiver.
+ ``subtractTime: timeAmount``: instance of Time that is the argument, timeAmount, before the receiver.

#### Converting

+ ``asSeconds``: 
	+ Time: number of seconds since midnight that the receiver represents. 
	+ Date: number of seconds between a time on January 1, 1901, and the same time in the receiver's day.


### Class Character
#### instance creation
+ ``value: anlnteger``: the asci value. Character value: 65 is a capital "A".
+ ``digitValue: anlnteger``: the value starting from 0. For parsing, very useful


#### Accesing


+ ``asciiValue``:
+ ``digitValue``:

#### testing
+ ``isAIphaNumeric``
+ ``isDigit``
+ ``isLetter``
+ ``isLowercase``
+ ``isUppercase``
+ ``isSeparator``
+ `isVowel`


## Chapter 8

### Number Classes
One of objetive of Smalltalk:  
	A single metaphor for information processing as uniformly as possible.

> Metaphor: objects that communicate by sending messages

+ number classes have been implemented so that all numbers behave as if they were of the most general type.
+ a number is its value, which should never change. The object 3, for example, should never change its state to 4, or disastrous effects could occur.


#### arithmetic

+ `+ a.Num.ber`
-  `- aNumber`
-  `. aNumber`
-  `/ aNumber`
-  `// aNumber`: integer quotinet toward minus infinitive
-  `\\\\ aNumber`: integer remainder toward minus infinitive
- `abs`
- `negated`
- `quo: aNumber`: integer quotient defined by division with truncation toward zero.
- `rem: aNumber`: integer remainder defined by divisionwith truncation toward zero.
- `reciprocal`


#### mathematical functions

+ `exp`
+ `In`
+ `log: al),lumber`
+ `floorLog: radix`
+ `raisedTo: aNumber`
+ `raisedTolnteger: anlnteger`: must be a kind of Integer.
+ `sqrt`
+ `squared`


#### testing

+ `even`
+ `odd`
+ `negative`: less than 0.
+ `positive`: greater than or equal to 0.
+ `strictlyPositive`: receiver is greater than 0.
+ `sign`: Answer 1 if the receiver is greater than 0, answer-1 if less than 0, else answer 0.


#### truncation and round off

+ `ceiling`: integer nearest the receiver toward positive infinity
+ `floor` integer nearest the receiver toward negative infinity.
+ `truncated`: integer nearest the receiver toward zero.
+ `truncateTo: aNumber`: next multiple of the argument, aNumber, that is nearest the receiver toward zero.
+ `rounded`: integer nearest the receiver.
+ `roundTo: aNumber`: multiple of the argument, aNumber, that is nearest the receiver.

#### intervals
+ `to: stop`
+ `to: stop by: step`
+ `to: stop do: aBIock`
+ `to: stop by: step do: aBIock`



### Random:

+ `rand next`: can then be evaluated whenever a new random number is needed. The response is a number (Float) between 0.0 and 1.0.