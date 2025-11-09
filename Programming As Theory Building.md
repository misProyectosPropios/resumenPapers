## Articulo

Link: [[Programming as Theory Building.pdf]]
## Introducción

Habla sobre que va a tratar el paper. Por qué es necesario entenderlo, la forma de entenderlo de Naur y experiencias.

## Programming and the Programmers’ Knowledge

Programación: toda la actividad de diseño e implementación de soluciones programadas
Esta connotación sirve para el desarrollo a lo largo del tiempo y las modificaciones añadidas al código. Además es la construcción de una cierta clase de conocimiento del programador, siendo este la posesión inmediata del programador y de forma secundaria la documentación.
+ Da el ejemplo del compilador: los que lo desarrollaron se lo dieron al grupo b que no lo conocía. Le querían agregar ciertas features al programa y no eran las mejores y no aprovechaban el compilador porque les faltaba el conocimento
+ Da ejemplo de un programa largo (200.000 lineas). Estas el grupo que lo diseño los puede resolver facilmente sin problemas, mientras que los que tenían que agregar cosas y no lo habían tocado antes el programa se les dificultaba.
**Conclusión**: Con programas largos, la adopción larga, modificación y correción de errores son dependientes de un cierto conocimiento que los tenían previamente los programadores

## Ryle’s Notion of Theory

Como caracterizamos ese conocimiento más detalladamente?
Usamos **Ryle's Theory**. Quien posee una teoría es capaz de hacer ciertas cosas, explicaciones y respuestas a consultas. Es una actividad intelectual, que va más allá de la no. La performance inteligente se mide en la medida que se hagan bien las cosas. Pero no hay una manera clara de medir que se hagan bien las cosas, al no haber una serie de reglas con las que constatar

Se basa en el _“knowing how”_, es decir un conocimiento práctico

## The Theory To Be Built by the Programmer

Los programadores tienen que crear una teoría sobre como ciertos aspectos de la vida real serán tratados o manejados por un programa. 
**El código es solo la _expresión_ temporal de una teoría**, y que sin la teoría el código pierde significado.

**Por qué?** Hay 3 áreas esenciales:
1) El programador con la teoría puede explicar la relación de la solución con la vida real que soluciona. En varias direcciones: como afecta a la realidad y la "mapeada" en el texto del programa y la documentación hecha. La decisión que una parte del mundo no es relevante es hecha según quien entiende que es relevante o no (el programador)
2) El programador puede explicar porque cada parte del código fue hecho de una cierta manera. Es decir, explica porque cada parte del programa es como es.
3) Es capaz de responder cada pedido de modificaciones del programa si es factible o no. Como es posible de agregarlo y la mejor manera de hacerlo.
## Problems and Costs of Program Modifications

Porque el paper?

Querer tener un comprensión de la modificación del programa para evitar fiascos.

La esencia de los programas es que serán modificados. Porque se va a expandir el dominio a resolver y el uso del programa va a generar ideas de como mejorarlo y features por agregar

A partir  de las ideas de features, queremos modificar el programa y no empezar de 0.
+ Si la programación fuera manipular texto, sería barato de modificar. Para la idea del paper, esto es falso.
+ La idea de flexibilidad si es barata de implementar no afecta, pero si para hacerlo flexible es mucho lío, es preferible no hacerlo, porque nos basamos en futuros eventos inciertos.
+ La **flexibilidad** no es algo que se pueda garantizar con reglas, solo con una buena teoría del dominio.
+ Los programas para ser buenos cada modificación debe estar basada en la teoría generadaç

## Program Life, Death, and Revival

Un programa está vivo cuando el equipo que lo diseño mantiene el control del programa y sus modificaciones.
Un programa está muerto cuando el equipo que diseño el software se disolvió. Un programa muerto puede seguir usandose hasta que falle o requiera modificaciones en donde se verá la muerte del programa. 

`Un  programa no muere cuando deja de ejecutarse, sino cuando **nadie conserva la teoría interna que lo explica**`.

El renacimiento de un programa es la reconstrucción de la teoría por un equipo nuevo de desarrolladores.

Para que un desarrollador adquiera la teoría debe ponerse manos a las obras y tratar de hacer alguna modificación o cambio al programa, pero varias veces no tendrá la misma teoría lo que generará discrepancias en el modelo

## Method and Theory Building

Un *programming method* **no** es una serie de reglas a seguir a rajatabla. Al construir una teoría no hay una serie de guías para seguir. No tiene orden.
Un método de programación **no puede ser una receta**, porque la teoría se desarrolla a medida que se entiende el problema.

Para notaciones o formalizaciones no es tan importante. Ya que se basa en sintaxis y no la generación de la teoría *per se*. 
Pero y el método científico?
+ No se siguen una serie de reglas a rajatabla. Es un error conceptual.
+ Siguen una serie sugerencias para lograr la mayor actividad mental
Las reglas no sirven para lograr éxito?
+ Un paper indica que las reglas para seguir que generan buenas soluciones son una ilusión

## Programmers’ Status and the Theory Building View

La idea del paper contrasta más con la parte de como ver al programador.

Está mal verlos como: 
+ Maquinas que siguen una serie de reglas
+ Como trabajadores de baja responsabilidad y poca educación

Hay que verlos como indispensables ya que poseen la teoría en su mente.
A su vez, tendrá que replantearse la educación de los programadores.

## Conclusions

+ Las modificaciones es parte esencial de la programación
+ Los programadores construyen una teoría sobre lo que importa y no del dominio del problema y se basan en la ejecución del programa para verificarlo
+ Los programadores deben estar constantemente aprendiendo y ampliando su conocimiento y teoría de los programas.
