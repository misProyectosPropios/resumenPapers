
Este patron sirve para sacar ifs generando menos código repetido y más abstracciones al código

**Idea**: tener una clase abstracta sobre la que hacer el method dispatch.

En esta clase, tener mensajes para cada una de las subclases (la jerarquía).

+ Estos mensajes reciben al que envía el mensaje para delegar la responsabilidad a ese. 
+ Los mensajes a los que mandan son de la forma operación + \<clase abstracta>
+ Al querer hacer un dispatch sobre esta clase, agregamos una subclase a la clase abstracta y que implementa la funcionalidad que desee.

