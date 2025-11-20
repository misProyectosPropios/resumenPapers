## Intent

Define a family of algorithms, encapsulate each one, and make them interchange-
able. Strategy lets the algorithm vary independently from clients that use it.

## Example

+ Métodos de pago. Cada uno hace lo mismo (una extracción y un deposito por ejemplo), pero queremos que lo haga según una estrategia diferente en cada caso
+ Al hacer logs queremos que puedan hacer diferentes acciones: como imprimir en otro sitio (en consola por ejemplo). Si se quiere agregar más accionar usando diferentes acciones podemos usar un composite.

## Que evita
+ Romper el encapsulamiento
+ Una sola responsabilidad por método
+ Múltiples `ifs` anidados debido a cada estrategia implementada

## Structure

![[strategyPattern.png]]


## Permite

+ Elegir cada una de las estrategias entre sí sin ningún tipo de problema
+ Intercambiar la estrategia en runtime

## How to use it

+ Encontrar un caso donde dependiendo de una condición de la estructura, se haga diferentes operación
+ Separarlos a una clase polimórfica diferente
+ Tener un objeto que sirva de contexto
+ Las clases `ConcreteStategy` sirven   

## Diferencias con state

State podría considerarse una extensión
+ Permiten ambos modificar en runtime el comportamiento del algoritmo

Diferencias
+ States pueden depender una de otra, mientras que en el strategy no. Tienen que ser totalmente independientes.
+ Los estados pueden saltar de una a otro
+ La idea del strategy es tener diferentes algoritmos que hagan lo mismo, solo que usando diferentes implementaciones, mientras que en el state es hacer diferentes acciones según el estado interno de las variables