
## Nuestra definición
+ **Modelo** **Computable** de un **Dominio de Problema** de la **Realidad**
	+ *Realidad*: *Todo* aquello que podemos *percibir, tocar, hablar sobre*, etc
	+ *Dominio de Problema*: *recorte de la realidad* que nos *interesa* para el negocio que estamos modelando
	+ *Modelo*: *Representación* de aquello que se está *modelando*
	+ *Computable*: Que puede ejecutar en una máquina de Turing (a-contextual)
		+ implementa el cómo, no solo el qué

### Buen Modelo:
+ *Eje Funcional*: Qué tan buena es la *representación* del *dominio*
	+ puede *representar* correctamente toda *observación* de aquello que *modela*
	+ algo nuevo en el dominio, debe aparecer algo nuevo en el modelo (no modificarlo)
	+ Modifica dominio -> modificar representación en el modelo
	+ Relación 1-1 (isomorfismo)
	+ **Observacional** del desarrollo
+ *Eje Descriptivo*: Qué tan bien está *descripto el modelo*, qué tan “*entendible* es”
	+ se lo puede “*entender*” y por lo tanto “*cambiar*”
	+ buenos nombres
	+ mismo lenguaje que el del dominio de problema
	+ lindo
	+ **Artistico** del desarrollo
+ *Eje Implementativo*: *Cómo* “ejecuta” en el ambiente técnico
	+ ejecuta en el tiempo esperado usando recursos definidos
		+ **Detallista** del software
		+ Performance
		+ Espacio 
		+ Escalabilidad
		+ Requerimientos no funcionales


### Que es el desarrollo de software?

Similar a un proceso de aprendizaje. Implica
+ Es **iterativo**
+ Es **incremental**
+ El conocimiento se genera a partir de **hechos concretos**
+ El conocimiento generado debe ser **organizado**


Características
+ El dominio de problema está generalmente *especificado* en *lenguajes ambiguos y contextuales* (ej. Lenguaje natural)
+ El proceso de desarrollo implica *desambiguar* y *descontextualizar* el conocimiento del dominio de problema
+ desarrollo implica hacer explícito y externo el conocimiento implícito e internalizado de los expertos de dominio
+ **Cambio esencial**:
	+ Cambia el dominio de problema
	+ Cambia nuestro entendimiento del dominio de problema 
	+ Cambia la manera de modelar lo que entendemos del dominio de problema