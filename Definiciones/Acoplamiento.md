**Acoplamiento** es el **grado de dependencia** que existe entre dos módulos, clases u objetos dentro de un sistema.  

Mientras más acoplados están, **más conocen o dependen uno del otro**, lo que hace que un cambio en uno requiera cambios en el otro.

+ **Method Object** reduce el acoplamiento
	+ Razón:
		+ Se simplifican las dependencias internas, al solamente usar variables globales que son más fáciles de modificar y con menos dependencias (menos atributos)
		+ Se conocen las dependencias (son las variables de instancia) y eliminar dependencias del entorno