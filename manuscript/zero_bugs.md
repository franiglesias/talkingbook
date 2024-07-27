# Z de Zero Bugs

Todas conocemos la historia del primer bug: una polilla atrapada en un relé, hallazgo que se atribuye a Grace Hooper, aunque sería más correcto atribuirlo en conjunto al equipo que estaba trabajando en ese ordenador.

## Qué es un bug

Solemos definir un _bug_ como un mal funcionamiento de un sistema de software. Curiosamente, ese primer bug, tenía más que ver con el hardware. La cuestión es que hay múltiples cosas que pueden fallar, desde elementos de infraestructura hasta la lógica expresada en el código. Si nos ceñimos al código, un _bug_ es algo un tanto más complicado de definir porque habría que distinguir entre lo que podríamos considerar un comportamiento incorrecto, cuando el software no hace lo que se espera, y un fallo manifestado en forma de un error que impide que el sistema funcione.

Como era de esperar, los _bugs_ tienen un coste económico: si no se puede usar el software, se detienen los ingresos que genera, o se incrementan los costes que evitaba. O, en otros casos, aumenta la posibilidad de que un cliente deje de trabajar con nosotras. En resumidas cuentas: un _bug_ es dinero que se pierde.

La política de _Zero bugs_ consiste en dejar de registrar, clasificar y seguir _bugs_ y dedicarse a resolverlos de forma inmediata, en cuanto nos informan de ellos.

## _Zero bugs_ la forma ágil de gestionarlos

Esto hay que verlo en un contexto ágil. En él, asumimos que las entregas de valor son pequeñas y bien definidas. Si aparece un _bug_ una vez desplegada una entrega, es muy probable que haya sido introducido o habilitado por dicho cambio. Por tanto, la localización y subsanación debería ser rápida. También asumimos una cobertura razonable de tests, al menos en las partes críticas del sistema, y buenos sistemas de integración de cambios y despliegue. Todo esto contribuye a garantizar que podemos desplegar software sin defectos evidentes, pero también a localizarlos de forma relativamente fácil cuando ocurren.

Una vez que un _bug_ ha sido reportado, lo primero sería centrarnos en él y establecer una o más hipótesis y expresarlas en forma de test. Un _bug_ normalmente es el resultado de un ejemplo que no ha sido testeado. Esto puede pasar porque carecíamos de información en el momento de desarrollo, bien porque no identificábamos ese ejemplo como un caso particular. También puede ocurrir que un cierto cambio habilite un _bug_ que antes no se había manifestado.

En cualquier caso, una vez que tenemos un test, modificamos el código para hacerlo pasar, junto con todos los demás tests existentes. De este modo, subsanamos el _bug_ y podemos desplegar este nuevo cambio para arreglarlo en producción. Entonces volvemos al desarrollo habitual.

Esta forma de abordar los _bugs_ suele despertar recelos. Por ejemplo, es cierto que no se puede aplicar en organizaciones que arrastran errores desde hace largo tiempo. Pero también existe una especie de creencia de que los _bugs_ son algo así como consustanciales al desarrollo de software. Sin embargo, _Zero bugs_ no va tanto de impedir que aparezcan errores, como de evitar que se queden.

## Defectos de software

Para empezar, en lugar de _bugs_ voy a empezar a hablar de defectos. Un defecto del software es un concepto que podríamos considerar más amplio que el de _bug_. Un defecto ocurre cuando el software no se comporta como las usuarias esperan.

### Defectos de comportamiento

Un defecto del software puede ser algo así como un aspecto no especificado al definir una prestación. ¿Cómo puede ser un _bug_ algo que no sabías que era necesario?

Otro ejemplo de defecto puede ser el haber hecho asunciones incorrectas sobre una característica. Como que un cierto parámetro admita o no números negativos. De nuevo, estaríamos ante un caso de definición incompleta, de un escenario no contemplado.

Estos defectos suelen detectarlos las usuarias del software, de ahí que muchas veces se habilitan sistemas para que puedan informar de los problemas. Básicamente, se trata de _bug-trackers_ y presentan el riesgo de convertirse en _backlogs de bugs_, que tienen que esperar a ser priorizados para ser atendidos. Exceptuando, tal vez, el caso de que el problema sea tan grande que se prioriza inmediatamente.

Por este motivo, entre otros, frameworks como _extreme programming_ proponen poner al cliente en el propio equipo. Si algo no funciona bien, la pregunta _¿qué deberíamos estar haciendo?_ Se contesta sola.

### Defectos técnicos

Otra categoría de defectos nos lleva a lo que podríamos considerar errores técnicos. Por ejemplo, que se pueda dar una división por cero, desbordar la memoria, o no manejar la situación en que accedemos a un servicio externo y no funciona. Es decir, errores que no tienen que ver haber interpretado mal la lógica de nuestro negocio, sino con detalles de implementación. Obviamente, lo peor que puede pasar es que el sistema no pueda utilizarse de ninguna manera.

La mayor parte de defectos técnicos debería ser detectada con herramientas de monitorización, que nos permitan saber cuando se producen este tipo de problemas y que nos alerten cuanto antes.

## Triaje

En muchas organizaciones se hace triaje de _bugs_. El triaje sirve para decidir qué equipo debe encargarse de atender un bug. Esto implica, tanto entender si se trata de un defecto de comportamiento o es un defecto técnico. Y, en todo caso, averiguar quién tiene los conocimientos o acceso necesario para darle solución.

A la vez que escribo esto, debo reconocer que se me encienden varias alarmas. En todo caso, es cierto que a poco que una organización sea grande, es difícil saber a quién dirigir el reporte de un defecto, por lo que un proceso de triaje tiene sentido. Sin embargo, corre el riesgo de convertirse en un freno. En muchos casos, la solución del _bug_ puede ser evidente para el equipo y todo el proceso de seguimiento y triaje puede hacer que tarde mucho en hacerse la corrección.

Así, es necesario garantizar que no pasa más tiempo del necesario entre que se informa de un defecto y se le pone remedio, para lo cual debe llegar cuanto antes al equipo de desarrollo. El mejor escenario, en estos casos, es que el equipo tenga _ownership_ de su producto o, en su caso, de su micro-servicio. Si existen muchas dependencias entre equipos y proyectos, puede ser muy difícil determinar el punto de fallo, o decidir quién tiene la responsabilidad de remediar la causa.

Si tienes _bugs_ de larga duración, que llevan meses, o incluso años en tu _backlog_ o en tu sistema de seguimiento, la mejor estrategia, de largo, es eliminarlos de ese registro y empezar de cero. Si alguno de esos _bugs_ era importante, puedes tener por seguro que volverá enseguida.

## Buenas prácticas técnicas y _zero-bugs_

Aplicar buenas prácticas técnicas en el desarrollo es la mejor forma de prevenir la aparición de defectos, pero, ante todo, es la mejor forma para conseguir que sea fácil identificar sus causas e introducir una solución.

El refactor continuado no evita por sí mismo los defectos, sin embargo, es más fácil prevenirlos en un software bien estructurado que refleja de forma clara el conocimiento de negocio. Cuando seguimos principios de diseño y construimos software basado en pequeñas unidades, con responsabilidades bien acotadas, bloques de código reducidos, etc., determinar la causa que ha originado un error suele ser un proceso bastante sencillo y preciso.

El testing nos ayuda a reducir las oportunidades de introducir bugs. En general, podríamos decir que los _bugs_ aparecen en aquellas partes del código en las que no hemos podido definir el comportamiento esperado mediante al menos un test. Son zonas oscuras del comportamiento del software.
