## Link:

# Paper

## Capitulo 1
Empieza el capítulo explicando que

> Software development is a process of discovery and exploration;
> Software engineers need to become experts at learning

Usando el método científico para evitar errores
+ **Characterize**: observar el estado actual
+ **Hypothesize**: hacer una descripción / teoría que explique la observación
+ **Predict**: hacer una predicción según la teoría formulada
+ **Experiment**: test the results


### What is software  Engineering?

> Software engineering is the application of an empirical, scientific approach to finding efficient, economic solutions to practical problems in software.

+ Become **experts** at **learning** and experts at **managing complexity**

#### Experts at learning
+ Iteration
+ Feedback
+ Incrementalism
+ Experimentation
+ Empiricism

#### Experts at managing complexity

+ Modularity
+ Cohesion
+ Separation of Concerns
+ Abstraction
+ Loose Coupling
### Reclaiming Software Engineering

Engineering simply means the “stuff that works.” It is the process and practice you apply to increase your chances of doing a good job.

### How to Make Progress

We don't want to have some kind of directives to rule us, because what happen if they are wrong or incomplete? 
We want intellectual freedom to challenge and refute dogma and innovate with great ideas. That way, we can replace bad ideas with better ones.


### The Birth of Software Engineering

+ It was created in the end of 1960s
+ First used by: Margaret Hamilton
+ First conference: NATO in Garmisch-Partenkirchen, Germany
+ At first, the computer were created by **manually flipping switches or hard-coded**. That doesn't work at great scale. 
+ **Stored programs** are born. Separating hardware from software for the first time
+ It starts the software crisis: hardware is being developed much better than hardware.

>There is no single development, in either technology or management technique, which by itself promises even one order of magnitude improvement within a decade in productivity, in reliability, in simplicity. 

> computer hardware progress is so fast

[[No Silver Bullet – Essence and Accident in Software Engineering]]]

### Shifting the Paradigm

Explica que es un cambio de paradigma y menciona que lo que trata de hacer con el libro es un cambio de paradigma sobre como se enfoca el `Software Engineering`

## Capitulo 2

### What Is Engineering?

Empieza comentando que siempre que se habla de la ingeniería ded software, siempre se la compara con construir puentes para decir que no son lo mismo - cuando eso es una obviedad, aun para el autor-.

### Production Is Not Our Problem

A diferencia del resto, la producción no es el problema del software.
Pero durante bastante tiempo se tuvo el *paradigma* de *production-style*. El conocido **[[Waterfall]]**

Es mucho más barato de crear, por lo que no nos preocupamos casi en ese aspecto.

> “Production” is not our problem. This makes our discipline unusual

### Design Engineering, Not Production Engineering

En la producción hay 2 etapas:
+ Cuando algo ya fue creado
+ Cuando se creó por primera vez

Además, están los problemas de producción: materiales y tiempo de producción. 
Por lo que se basan en modelos y maquetas.

Pero al software no le pasa eso. El modelo es la realidad. Por eso es más fácil de iterar. Los problemas usuales son por un entendimiento erróneo de la disciplina, junto con una mirada incorrecta de la alta dificultad de implementar un modelado con base científica. 

Igual en la producción se puede aplicar una forma de testing mientras se desarrolla (TDD). 
Da el ejemplo de *SpaceX* y sus prototipos

>Our problem is one of exploration, and so we, even more than the spaceship designers, should be applying the techniques of exploration rather than the techniques of production engineering. 

## Capitulo 3
### Fundamentals of an Engineering Approach

Todas las otras ingenierías van a tener sus particularidades, pero todas se basan en
+ scientific rationalism;
+ pragmatic, empirical approach to making progress.

Vamos a ver que cosas caracterizan a la ingeniería del software
### An Industry of Change?

A pesar de desarrollarse muchas tecnologías constantemente, en el fondo no cambia tanto para el autor.

Usan la analogía de la creación de una torta

> Do you make your cake with a cake mix or choose fresh ingredients and make it from scratch?

Muchos cambios no generan valor añadido. Ej: hibernate que usarlo lo hacía mas inentendible y era más largo de hacer

> My impression is that our industry struggles to learn and struggles to make progress.

Se enfoca en que muchos **lenguajes no aportan nada nuevo a la mesa**. Muchas veces **se generan perdidas** debido al mal uso de las tecnologías.

Además, nos cuesta **abandonar ideas obsoletas**

### The Importance of Measurement

No dejamos atrás ideas obsoletas al no saber medir las cosas. Muchas métricas desarrolladas hasta ahora son obsoletas (velocidad) o sin ningún efecto (líneas e código, test-coverage).

Se menciona las medidas de:
+ **Stability**
	+ **Change Failure Rate**: The rate at which a change introduces a defect at a particular point in the process
	+ **Recovery Failure Time**: How long to recover from a failure at a particular point in the process
+ **Throughput**
	+ **Lead Time**: A measure of the efficiency of the development process. How long for a single-line change to go from “idea” to “working software”?
	+ **Frequency**: A measure of speed. How often are changes deployed into production?

Hay una correlación entre teams `high-performing` y  `low-performing`
+ `high-performing`: 
	+ usa **continuous-delivery**
	+ Agrupado en equipos más pequeños


### Applying Stability and Throughput
Aprendamos de lo visto hasta ahora más algunos datos
+ Agentes externos que aprueben cambios no sirven
	+ Conviene hacer decisiones basadas en la evidencia y no en la intuición


> We finally have a useful measuring stick

Analizar. + Analizar. + Analizar. Hasta el infinito .

### The Foundations of a Software Engineering Discipline

+ **Experts at learning**
	+ Creative design discipline and has no meaningful relationship to production-engineering
+ **Expert at managing complexity**

#### Experts at Learning
Características:
+ Practical, light weight, and pervasive in our approach to solving problems in software

Consejos:
+ Working iteratively
+ Employing fast, high-quality feedback
+ Working incrementally
+ Being experimental
+ Being empirical

#### Experts at Managing Complexity
