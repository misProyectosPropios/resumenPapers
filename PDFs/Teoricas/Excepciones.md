## Qué son?

Una abstracción debido al código repetido. Cada vez que se enviaba un mensaje, se tendría que verificar si es un error o no (lógica clásica boe)

### Prágmaticamente
Las excepciones son el resultado de sacar código repetido de la técnica de **"código de retorno"**

**El try-catch**

### Explicación conceptual
+ Programación por Contratos - Bertrand Meyer 
+ Contratos explícitos
+ Contratos implícitos 
+ ¿Quién verifica los contratos? 
+ ¿Qué hacer cuando no se cumple un contrato?

**Definición**: Las excepciones se utilizan para indicar que no se cumple un contrato 

### Qué es un contrato?

Acuerdo de voluntades entre partes que genera derechos y obligaciones y a cuyo cumplimiento pueden ser compelidas

+ Características:
	+ Orales o Escritos 
	+ Contratos explícitos o Implícitos
	+ Legales
+ Acciones relacionadas:
	+ ¿Quién verifica los contratos?
	+ ¿Qué hacer cuando no se cumple un contrato?

### Qué es un contrato en objeto?

Condiciones que se deben cumplir entre los objetos que colaboran y que de hacerlo, aseguran un resultado definido algorítmicamente

+ Pre-Condiciones
	+ Condiciones que se deben mantener para poder ejecutar un método
+ Post-Condiciones
	+ Condiciones que se deben mantener después de ejecutar un método
+ Invariantes
	+ Condiciones que siempre se deben mantener en las instancias de una clase
## Escuelas de verificación que se cumpla contrato

### C  
 +  El **objeto que envía** el mensaje/función llamadora debe asegurar las pre-condiciones

#### Ventajas: 
+ Performance
#### Desventajas
+ Código repetido / inseguridad
### Lisp
+ El **objeto que recibe** el mensaje/función llamada debe asegurar la pre-condiciones
#### #### Ventajas: 
+ Validaciones en un lugar/Seguridad
#### Desventajas
+ Performance

## Quien informa 

En un árbol de ejecución las informa las **hojas (leafs)**

![[arbolHojas.png]]

## Quien las handlea

Las **raíces** se encargan

![[arbolRaiz.png]]

## Como handlear excepciones
+ Solo se debe handlear una excepción si se puede resolver la ruptura del contrato
+ No handlear excepciones si no se puede hacer nada con ellas
	+ Según la semántica del error
+ No ocultar las excepciones
+ Handlear todas las excepciones en la raíz del árbol de ejecución

## Implementación según disponibilidad de Implementación
+ Cerrada
	+ Java
	+ No se puede ver ni modificar 
+ Abierta
	+ Smalltalk
	+ Se puede ver la implementación
		+ Aprender
	+ Ampliar las prestaciones
## Tratamiento de Stack
+ Deshacer el Stack
	+ Fuerza logs (horrible, nadie los entiende)
	+ Pérdida de contexto
	+ Difícil debugging
+ Mantener el Stack
	+ No se pierde el contexto
	+ Más fácil de debugear
	+ Se puede dumpear el stack y revivirlo (volver a ver como ocurrió el error)