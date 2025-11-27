## Intent

Define an interface for creating an object, but let subclasses decide which class to
instantiate. Factory Method lets a class defer instantiation to subclasses.

+ **Delegar la responsabilidad de la instanciación de un objeto a las subclases**.
## Example

+ A framework. Only knows when to create an instance, but not what subclass to create

## Structure

![[factoryMethodPattern.png]]

## When to use it

+ When the system needs to be open for extension but closed for modification (OCP)

## How to use it

+ Tener una jerarquía polimórfica (sea *a*)
+ Agregar una nueva jerarquía polimórfica (sea *b*) que sepa crear las instancias de *a*
+ La jerarquía *b* tiene que tener una clase por cada una de las clases de *a*