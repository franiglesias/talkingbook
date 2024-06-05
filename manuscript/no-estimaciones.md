# N de No-Estimaciones

La estimación sobre el coste de desarrollo de una feature o historia de usuario es uno de los temas que genera más discusiones en nuestro sector.

A la hora de decidir desarrollar una funcionalidad en el software tenemos que sopesar dos dimensiones fundamentales:

* El valor que puede aportar a la usuaria o cliente
* El coste de desarrollo

## Estimar la aportación de valor

Siendo sincero, no he visto demasiada literatura acerca de cómo estimar o cuantificar la aportación de valor de una prestación del software. En ese sentido, creo que podríamos estar de acuerdo en algunos parámetros de la misma:

* Aporta una capacidad que antes no existía
* Reduce el tiempo necesario para ejecutar un proceso de negocio
* Potencialmente, permite generar una cierta cantidad de ingresos
* Potencialmente, permite ahorrar una cierta cantidad en gastos

Digo "potencialmente" en cuando a la generación de ingresos o al ahorro de gastos porque eso se basa en suposiciones: que las usuarias están interesadas en la prestación, que los clientes pagarán por ella, que incrementará las ventas, etc.

En conclusión, el valor de una prestación también es una estimación que debería basarse en un análisis racional. Algo más elaborado que "el cliente/usuario lo quiere". Para estas cosas los equipos tienen analistas de negocio y, si me apuras, product owners que entienden ese mercado y sus necesidades.

## Estimar el coste de desarrollo

El coste de desarrollo es la otra dimensión a tener en cuenta y también es otra dimensión compleja. En último término todas las unidades de estimación del esfuerzo de desarrollo se basan en una medida de tiempo. La necesidad de estimar surge de la gestión de proyectos tradicional, con sus plazos y fechas de entrega. Se puede argumentar que un negocio viable necesita saber cuándo estará listo un proyecto, a fin de ajustar otros procesos de negocio como marketing, ventas, finanzas, etc.

Es muy difícil valorar cuánto cuesta realizar una tarea de programación. En una cadena de montaje es posible que puedas tener estimaciones bastante precisas de cuanto tiempo requiere realizar una fase e incluso optimizarla. Pero el desarrollo de software tiene otra naturaleza.

Por hacer una analogía. En una cadena de montaje de coches, hay que colocar unas piezas definidas en un chasis que está preparado para ello. Quitando imprevistos como que se hayan agotado las piezas o algún tipo de accidente, es relativamente fácil saber cuánto tiempo se consume en montarlas. En realidad, bastaría con obtener una buena muestra de medidas y calcular un índice de tendencia central, como la media o la mediana, para tener una estimación muy aceptable.

Pero en software... el software no tiene nada que ver. Para empezar puede que ese chasis no exista, o que la pieza que hay que añadir no encaje en el existente, puede que haya que rediseñar esa parte del chasis porque las necesidades han cambiado o puede que no esté preparado para añadir o cambiar esa pieza específica. En software esto ocurre porque cada vez que tenemos que modificar código la situación es diferente.

En resumen: el coste de desarrollo de software incluye un alto grado de incertidumbre.

Reducir el nivel de incertidumbre es el camino a seguir, pero no es fácil. No se puede reducir mediante técnicas de estimación más precisas. El ideal es llegar a dividir la funcionalidad en trozos más pequeños cuya expresión en código no tenga incertidumbre o sea mínima. Aunque entreguen una fracción del valor, se pueden ejecutar en un tiempo reducido.

Si llegamos a este tipo de fraccionamiento, es relativamente fácil predecir hasta donde vamos a llegar en un período de tiempo dado.

## La relación entre valor y coste

Ron Jeffreys representa el valor como la altura de un rectángulo y el coste como su anchura. De este modo, los rectángulos _verticales_ indicarían una prestación que aporta mucho valor con poco esfuerzo. Por el contrario, los rectángulos _horizontales_ nos estarían diciendo que el coste de desarrollo es muy alto con relación al valor que nos aporta.

Pero también nos dice que la situación óptima es cuando podemos desarrollar prestaciones con bajo coste aunque su aportación de valor sea relativamente baja. ¿Y esto por qué? Porque con ello generamos una entrega de valor contínua y sostenible. Eso sí, el valor debe ser perceptible por la usuaria final.

Esto nos proporciona un criterio relativamente sencillo para tomar decisiones sobre el desarrollo:

* Priorizar la entrega de valor aunque sea en unidades pequeñas pero visibles
* En lugar de introducir tareas de alto coste, partirlas hasta descomponerlas en entregas de valor pequeñas pero de bajo coste

## Puntos de historia

Estimar es, literalmente, timar. Los puntos de historia para estimar el esfuerzo de una tarea se inventaron justamente para _timar_ a los managers y no darles estimaciones de tiempo. El objetivo era tratar de librar a los equipos de desarrollo de la presión de los plazos de entrega.




