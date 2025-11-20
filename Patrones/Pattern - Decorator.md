## Intent

Attach additional responsibilities to an object dynamically. Decorators provide a
flexible alternative to subclassing for extending functionality

## Example

Ventana de una interfaz gráfica. Para agregar los bordes se puede usar un decorator. 

## Motivation

+ Queremos agregar nuevas features sin usar herencia porque al agregar muchas features llevarían un número cuadrático de subclases diluyendo el modelado.
	+ Crearíamos clases para cada combinación.
+ Delegamos la responsabilidad al **decorator**
+ Logramos conseguir de forma dinámica todas las combinaciones
+ Es el problema **composition vs inheritance**
	+ Strategy no serviría porque tendría el mismo problema que herencia
	+ Proxy tampoco porque modificarían el comportamiento dinámicamente y no debería hacer eso proxy.

## Structure

![[decoratorPattern.png]]

## How to use it


+ Teniendo una clase que queremos agregarles features sin usar herencia (porque haría muchas subclases)
+ Hacemos una clase por cada feature que queremos agregarle (los **decorator**)
+ Usar organización por capas (cual cebolla)
+ Un decorador es, a su vez, un componente porque debe poder modificar también el comportamiento. A su vez, tiene un componente dentro: para hacer la especie de **pseudo-link-list**