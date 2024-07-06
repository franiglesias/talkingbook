# R de Retrospectiva

Hemos dedicado un capítulo de este libro a los ciclos de feedback y cómo son un elemento fundamental en cualquier práctica ágil que se precie. En general, esos ciclos de feedback se refieren a si estamos construyendo el producto que queremos o debemos construir. Los ciclos se basan en el propósito de lograr una entrega de valor contínua y sostenible, que nos lleva a plantear un estilo de desarrollo iterativo e incremental.

Además de eso, el Manifiesto Agile recomienda lo siguiente:

> A intervalos regulares el equipo reflexiona sobre cómo ser más efectivo para a continuación ajustar y perfeccionar su comportamiento en consecuencia.

Esta reflexión es lo que algunos frameworks establecen como _Retrospectiva_, que es un término de _Scrum_ para denominar una ceremonia que tiene justamente ese objetivo.

La Retrospectiva, por tanto, sería la actividad en la que el equipo analiza la forma en la que ha trabajado a fin de detectar áreas de mejora y lograr mayor eficiencia en el futuro. Esto se hace de forma periódica. En _Scrum_ se hace al final del _sprint_.

¿Y qué se puede hacer en una retrospectiva? Como acabamos de decir, lo que querríamos obtener de una retrospectiva es un conjunto de propuestas accionables que nos puedan permitir mejorar nuestra capacidad de entrega sostenible de valor.

Como es fácil adivinar, esto tiene mucho que ver con identificar los limitadores que estén impidiendo alcanzar el ritmo de entrega deseable, algo de lo que hablamos en el capítulo dedicado al WIP o trabajo en progreso.

## Métricas DORA y retrospectivas

Una forma bastante objetiva de abordar esto es mediante las métricas DORA:

**Frecuencia de implementación (Deployment Frequency)**. Se trataría de la cantidad de veces que desplegamos a producción por unidad de tiempo. Los equipos de mayor rendimiento pueden llegar a desplegar varias veces al día, y la frecuencia baja hasta aquellos que lo hacen una vez cada varios meses.

Esto tiene dos implicaciones importantes. Para incrementar la frecuencia de implementación es necesario reducir el tamaño de las entregas, lo que contribuye a reducir el riesgo de introducir errores y facilita el resolverlos cuanto antes. También es más fácil que tales entregas estén bien testeadas. Por otro lado, esta capacidad habilita al equipo para desplegar a demanda, en cualquier momento en que tenga sentido hacerlo.

Un ejercicio interesante en una retrospectiva sería entender por qué se hacen entregas poco frecuentes y muy grandes y cómo podríamos mejorarlo.

**Plazo de ejecución para cambios (Lead Time For Changes)**. Es el tiempo que tarda un commit con cambios en llegar a producción. Si tienes un proceso de _pull/merge request_ con revisión de código, este tiempo puede llegar a ser de horas o días, a lo que habrá que sumar el tiempo de despliegue.

Por tanto, los esfuerzos para mejorar esta métrica pueden conducir a varias acciones:

* Automatizar la revisión de calidad de código en todo lo que se pueda: linters, análisis estáticos, buena suite de tests, etc.
* Reducir el tiempo de espera entre que se hace el commit y es revisado, algo que se puede facilitar si las entregas de código son pequeñas y acotadas, de manera que revisarlas sea trivial.
* Reemplazar la revisión asíncrona de código por metodologías de _pair_ o _mob programming_, que nos permitan eliminar _de facto_ el tiempo de espera por la aprobación de los cambios, sin comprometer la calidad del código. 
* Aparte de eso, trabajar para optimizar el _pipeline_ de despliegue es otra mejora que puede ayudar. 

**Tasa de fallos de cambio (Change Failure Rate)**. Esta métrica nos habla de las entregas que necesitan ser corregidas tras el despliegue, bien porque se han introducido errores, bien porque han fallado cosas inesperadamente, etc. Lo ideal sería poder desplegar algo y olvidarnos de ello, pero el mundo no funciona así, por lo que una tasa inferior al 15% se considera muy buena.

Obviamente, es una tasa que nos interesa tener lo más baja posible, pero es importante entender qué cosas hacen que se eleve.

* Si es nuestro código el que introduce errores, es posible que no tengamos una buena suite de tests, o que no estemos entendiendo el problema que se nos ha pedido resolver.
* Si es la infraestructura la que falla, ¿la tenemos bien dimensionada? ¿Nuestro código está bien optimizado o estamos introduciendo problemas técnicos inadvertidamente?

**Tiempo medio de restauración (o MTTR Mean Time To Restore)**. Este es el tiempo que se tarda entre detectar un fallo y poner el sistema otra vez en funcionamiento, que en los mejores equipos sería de menos de una hora.

En general, consideramos esta métrica mirando el tiempo que tardamos en ejecutar un _rollback_, o sea, la restauración del sistema a una versión anterior que sí funcionase. Para esto se pueden utilizar varios sistemas. Uno de los más simples es desplegar esa versión anterior. Un poco más sofisticados, pero realmente rápidos, son aquellos que nos permiten hacer que el sistema apunte a la versión deseada que sigue disponible.

Para poder optimizar el tiempo de restauración, es necesario tomar algunas medidas facilitadoras. Para empezar, implementar sistemas en los _pipelines_ de despliegue que aborten en el caso de que fallen los tests. Si desplegamos cambios en bases de datos, es importante hacerlo de forma que no se rompa inesperadamente. Por ejemplo, si introduces una columna nueva para reemplazar el uso de otra, no elimines esta última en el mismo despliegue hasta tener la seguridad de que funciona.

Utilizar herramientas de _feature flags_ nos permite desplegar código y activarlo o desactivarlo rápidamente si detectamos que funciona mal. En ese caso, podemos mantener el código antiguo hasta tener la seguridad de que ya no se está usando. En general, trabajar como si estuviésemos haciendo _Trunk Based Development_ nos puede ayudar a reducir riesgos en los despliegues.



