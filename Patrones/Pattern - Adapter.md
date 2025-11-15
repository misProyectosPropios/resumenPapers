Se basa en la metáfora del adaptador eléctrico

## Intent

Convert the interface of a class into another interface clients expect. Adapter lets
classes work together that couldn't otherwise because of incompatible interfaces

## Motivation

+ Sometimes a toolkit class that's designed for reuse isn't reusable only because its interface doesn't match the domain-specific interface an application requires
+ 

## Example

+ `TextView`: tenga otra intrefaz y nosotros no podemos modificarlo, entonces podemos crear un adapter nosotros para no tener que tocar el source-code (que no podemos) y de esa forma podemos usarlo de forma intercambiable con el resto

## Structure

![[adapterPattern.png]]

## How to use it

+ A la clase que queremos adaptar, crear una clase en medio con la interfaz que queremos nosotros
+ Hacer que los mensajes hagan lo que queremos que hagamos
+ Llamar al adapter en vez de la clase

## Diferencias con proxy

+ Su semántica
	+ Adapter: simplemente es una adaptación de los mensajes para usarlos con otro nombre
	+ Proxy: agrega una lógica interna para no modificar la clase con información irrelevante a la clase. 