	Link:

## Introduction

El autor muestra un fastidio sobre los software que parecen funcionar bien hasta que de repente fallan repentinamente (casi como lo de silver bullet en donde se transforma un programa).
Menciona que existe una técnica, no para reducir la cantidad de bugs (inherente del desarrollo de código #TODO consultar)

## Immediate and visible failure

Compara entre `failing slowly` contra `fail fast`

+ **Failing slowly**: va a continuar funcionando a pesar del error, pero va a fallar de maneras raras después.
+ **Failing inmediatamente and visibly**: genera los errores una vez ocurrieron.

Ejemplo de fail-fast:
+ Un método que lea una propiedad de un archivo de configuración no debería devolver `null` ni un valor por defecto porque lo que genera es que oculta el error, sino que debería mostrar un mensaje de error descriptivo.

## Fail-fast fundamentals
#### Assertions
Son la clave de fail fast

##### Que son
Condiciones que verifican una condición y fallan en caso de que no se cumpla la condición (los asserts de generación de objetos en smalltalk). Logran hacer los errores visibles

##### Como agregarlas

+ Tener las assumptions en comentarios no sirve porque no se mantienen los comentarios.
	+ Cada vez que escribas un comentario pensar en como convertirlas en un assert
+ Evitar hacer asserts en los métodos de por sí.
+ Usar asserts para asegurar que el **sistema** funcione correctamente.

### Writing assertions

+ No poner asserts porque sí, sino para como interactúa el sistema *per se*.
+ Poner las assertions para que falle **cerca de la causa original** del problema
+ Cuando un **parámetro de método** (que puede ser `null`) se utiliza para inicializar una **variable de instancia/campo** (que podría usarse mucho después), el programa **no fallará rápido sin ayuda**.

### Eliminate the debugger

+ Poner nombres de las assertions descriptibles para evitar tener que 
+ No poner las condiciones en los assertions. 
	+ Ex: `Assert.notNull(result, “can’t find property”);`
+ Poner el error en un contexto para entender que paso.

### Robust failure

A pesar de parecer que hace al código frágil, vamos a ver que no es así.

Al debuggearlo, vimos que va a ser más fácil de debuggear, pero en *deploy stage?* 

 Alternativa: 
 + **FATAL**:  desactivar assertions. Perdemos oportunidades de verificar donde está mal el código
 + **FATAL**: dejar los fallos igual que al testear. No se debería el *workflow* al usuario por un error
 + **Solución**: mostrar que fallo algo y enviar el error a un handler específico.
	 + Evitar `try-catch` ya que queremos que llegue hasta el handler de errores.
	 + Usar `finally` si hay recursos que deberían cerrarse.

#### Porque guardar los contextos de error?

+ Porque lo más difícil de debugging es lograr reproducir los errores.

#### Ventajas

Se puede empezar a implementar desde ahora que lo sabes, no hace falta nada más que tener un handler global que reciba las excepciones y refactorizar los try-catch para que muestre los errores