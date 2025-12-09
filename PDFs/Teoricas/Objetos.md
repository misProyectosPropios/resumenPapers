La OPP apareció antes que la estructurada

Se divide en 2
+ Fundacional / Pura / Orientada a Cálculo Lambda
	+ Smalltalk, Self 
+ No fundacional
	+ Orientada a la máquina / a Turing
	+ C++, Java, C#


### Historia
+ Simula 67
+ Smalltalk 80


### Principios Originales:

+ Simplicidad
+ Consistencia
+ Concretitud
+ Inmediate Feedback (no es tan así, según Hernán)
+ Hacer frente a Complejidad ( [[No Silver Bullet – Essence and Accident in Software Engineering]])

### **Complejidad**: 
Esencial + accidental
+ Esencial: 
	+ Tiene que ver con el problema en si
	+ No se puede reducir más allá de la complejidad del problema
+ Accidental:
	+ Tiene que ver con las herramientas que uso, en nuestro caso Lenguaje de Programación
	+ Tengo que minimizarlo para minimizar Complejidad
	+ Consistencia/Homogeneidad
		+ Casos especiales
	+ Sintaxis
		+ Simple vs compleja
		+ Expresividad
	+ Madurez (años de uso junto con usuarios)
	+ Herramientas
		+ Representacion concreta vs. Representación textual
		+ Contextualización (Debugger) 

## Paradigma
Minimalista
+ Conjunto de axiomas básicos mínimos
+ Pensar mucho antes de agregar un nuevo axioma
Puro
+ No traer conceptos de otros paradigmas, crearlos en base al paradigma
Fundamentalista
+ No salir de nuestra actitud minimalista/purista


## Que es un programa?
+ **Programa**: *Objetos* que *Colaboran* entre si enviándose *mensajes*

+ **Objeto**: Representación de un ente del dominio de problema
	+ No es código + datos! (error de definición)
	+ Ente: Cualquier cosa que podamos observar,hablar sobre, etc.
	+ La esencia del ente es modelado por los mensajes que el objeto sabe responder

+ **Mensaje**: *Especificación* sobre *QUE* puede hacer un *objeto*
	+ Un Mensaje es un objeto!
	+ Por lo tanto representa un ente de la realidad, pero del domimio de la “comunicación”
	+ Se debería poder decir qué representa un objeto a partir de los mensajes que sabe responder

+ **Colaboración**: Hecho por el cual dos objetos se comunican por medio de un mensaje
	+ Un emisor del mensaje
	+ Un receptor del mensaje
	+ Un conjunto de objetos que forman parte del mensaje (colaboradores externos o parámetros)
	+ Una respuesta

+ *Características*
	+ Dirigida (no broadcast)
	+ sincrónicas, el emisor no continúa hasta que obtenga una respuesta del receptor.
	+ receptor desconoce al emisor à su reacción será siempre la misma no importa quién le envía el mensaje
	+ Siempre hay respueste

Si se cuestiona alguna de las características va a ser *context aware*


+ **Método**: Objeto que representa un conjunto de colaboraciones
	+ Es evaluado como el resultado de la recepción de un mensaje por parte de un objeto
	+ Para encontrarlo: *Method Lookup*
	+ mensaje principal que un programa: execute o value

+ **Relación de Conocimiento**: describe qué objetos conocen a qué otros objetos, es decir, a quién pueden enviarle mensajes.
	+ Determina 
		+ el acoplamiento
		+ Las responsabilidades
		+ Diseño

+ Colaborador/Variable (en que se basa la relación de conocimiento)
	+ Nombre contextual que se le asigna a una relación de conocimiento