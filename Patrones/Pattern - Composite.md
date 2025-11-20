## Intent

Compose objects into tree structures to represent part-whole hierarchies. Composite lets clients treat individual objects and compositions of objects uniformly.

## Example

+ Lógica booleana
+ Portfolio: había que aplicar el composite para tenerlo de una forma más adaptable al futuro, porque como aprendimos si ocurrió 2 veces, puede ocurrir muchas más

## Structure

![[compositePattern.png]]

## Razones de uso

+ Evitar código repetido entre varias clases
+ Obtener un mejor modelado al entender mejor el problema
+ you want clients to be able to ignore the difference between compositions of objects and individual objects. Clients will treat all objects in the composite structure uniformly

## How to use it
+ Si vemos que ocurre 
+ Agregar una clase que identifique a todos (padres y hojas) y hacer que el resto se convierta en hijos de esta superclase