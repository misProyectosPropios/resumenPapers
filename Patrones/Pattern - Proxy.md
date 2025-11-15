## Intent

Provide a surrogate or placeholder for another object to control access to it.

## Motivation
+ Crear los objetos una vez se los necesite y no antes
+ Contar la cantidad de referencias de un objeto

## Example

Ejemplos: 
+ drawing editor para on-demand
+ Landlord que no quiere lidiar con inquilinos -> hay un proxy: la inmobiliaria 


## Structure

![[proxyPattern.png]]

## How to use it

+ Bastante sencillo
+ Solo llamar al proxy que va agregar una lógica o mapeará a lo necesario y continuará el código hacia el verdadero objeto que tiene la implementación de algún modelado
+ Este lo que hace es usar los mismos mensajes, pero los usa de forma que no se entere el cliente del proxy