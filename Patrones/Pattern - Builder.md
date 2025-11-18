## Intent

Separate the construction of a complex object from its representation so that the same construction process can create different representations.

## Example

+ Creación de autos
+ 

## Structure



## Applicability

+ The algorithm for creating a complex object should be independent of the parts that make up the object and how they're assembled.
+ the construction process must allow different representations for the object that's constructed

Si queremos restringir las creaciones a ciertos tipos, es más fácil tenerlo de esta forma

## How to use it
Tenemos que tener un builder que sepa responder mensajes que devuelvan los tipos y setters para ponerle los valores que queremos

+ Ya está
+ Podemos agregar lógica para que los builder generen más valores que deben ser por defecto, pero no queremos que se encargue la clase per se, como los **ids** al no ser del dominio del problema