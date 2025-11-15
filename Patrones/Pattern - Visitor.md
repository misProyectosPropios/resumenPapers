
## Intent

Hace que se pueda generar una operación sobre los elementos de la estructura de un objeto. Permite añadir nuevas operaciones **sin** modificar los elementos sobre los que opera.
Tiene que tener la palabra: **accept** como mensaje la clase sobre la que se aplica el visitor
## Example

Portfolio.
+ Teníamos que recorrer la estructura interna del portfolio, pero sin agregar nuevos mensajes, por lo que al hacerlo pudimos recorrer la estructura interna pudiendo agregar nuevas operaciones sin necesidad de agregar mensajes cada vez al objeto

## Structure

![[visitorPattern.png]]

## Para que sirve

+ Separar responsabilidades no intrínsecas del objeto, sino de un visitor
+ Evitar que se diluya el objeto al agregar mensajes para cada una de las nuevas operaciones sobre su estructura y lograr recorrerla desde afuera
+ Evitar romper el encapsulamiento

## How to use it

+ Utiliza el method object y el method dispatch.
+ Tenes una clase y en esa haces un método para empezar con el visitor reciviendo un valor por el que recorra.
+ Se usa usualmente en arboles y listas.
+ La clase que recorre tiene un mensaje que es accept que manda el self al visitor correspondiente y además, tenes un mensaje que itera sobre el resto de la estructura para lograr obtener todo el recorrido sobre al estructura. Si no tiene una estructura como árbol o lista, entonces va a ser un double-dispatch sin más.