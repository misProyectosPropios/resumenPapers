Link:

## Rules are for fools, patterns are for cool fools

Describe su vida laboral durante los últimos 18 años.
Cuando probó los patrones de diseño, los empezó a aplicar por el hecho de aplicarlos.

Los vio como la manera de mejorar como diseñador / modelador.
Aplicó la regla que no había que hacer: tener reglas para medir que tan bueno el código es. En este caso, uso como base la cantidad de patrones de diseño.

Los patrones que usaba:
+ State pattern: #TODO  explicar
+ Strategy pattern: #TODO explicar
+ Chain of responsibility pattern: #TODO  explicar
+ Iterator pattern: #TODO  explicar
+ Visitor pattern: #TODO  explicar
+ Observer pattern: #TODO explicar
+ Proxy pattern: #TODO explicar
+ Facade pattern: #TODO explicar
+ Bridge pattern: #TODO explicar
+ Adapter pattern: #TODO explicar
+ Abstract Factory pattern: #TODO explicar
+ Abstract builder pattern: #TODO explicar
+ Factory Method pattern: #TODO explicar
+ Prototype pattern: #TODO explicar

## Dark side (of the moon)

+ Tras un análisis en el futuro, no podía notar una mejora en la calidad tras la "patternización" del código. 
+ Los desarrolladores  no entendían el código nuevo. No tenían la teoría del modelado para esos refactors. 
+ Llegó a una espiral de aplicar más "patterns" para resolver problemas
+ No sabía cuando aplicarlos y cuando no (muy subjetivo como la materia)

## Consecuencias del pattern abuser

+ Generará una sobre generalización innecesaria.
+ Nos desconectamos del problema al agregar mensajes a los objetos (ya que los objetos son lo que saben responder)
+ Diluimos el modelado con el mundo real.
+ Generará una complejidad accidental al agregar demasiados mensajes y generar una serie de envío de mensajes muy grande.

## Razones por las que abusaban de patrones
+ Surgen a partir del diseño y de heurísticas, no al revés (aunque las heurísticas hay que saber cuando utilizarlas)
+ Encajar un patrón por la fuerza en un modelado

## Como sabemos si un patrón estuvo bien aplicado?

+ Dejamos abiertos cambios posibles, no porque pensemos que van a ocurrir, sino porque ya tenemos unos casos en donde paso (ejemplo: `account summary`).
+ Según nuestro dominio del problema
+ Depende los criterios que tomemos: performance, modelado, seguridad, declaratividad, etc.
