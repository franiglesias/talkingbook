# Zero Bugs

Todas conocemos la historia del primer bug: una polilla atrapada en un relé, hallazgo que se atribuye a Grace Hooper, aunque parece ser más correcto atribuirlo en conjunto al equipo que estaba trabajando en ese ordenador.

Solemos definir un bug como un mal funcionamiento de un sistema de software. Curiosamente, ese primer bug, tenía más que ver con el hardware. La cuestión es que hay múltiples cosas que pueden fallar, desde elementos de infraestructura hasta la lógica expresada en el código. Si nos ceñimos al código, un bug es algo un tanto más complicado de definir porque habría que distinguir entre lo que podríamos considerar un comportamiento incorrecto (el software no hace lo que se espera) y un fallo manifestado en forma de un error que impide que el sistema funcione.

Como era de esperar, los bugs tienen un coste económico: si no se puede usar el software, se detienen los ingresos que genera, o incrementa los costes que evitaba. O, en otros casos, aumenta la posibilidad de que un cliente deje de trabajar con nosotras.

La política de Zero bugs consiste en dejar de registrar, clasificar y seguir bugs y dedicarse a resolverlos de forma inmediata, en cuanto son informados.

Esto hay que verlo en un contexto ágil. En este contexto asumimos que las entregas de valor son pequeñas y bien definidas. Si aparece un bug una vez desplegada la feature, es muy probable que haya sido introducido o habilitado por ese cambio. Por tanto, la localización y subsanación debería ser rápida. También asumimos una cobertura razonable de tests, al menos en las partes críticas del sistema, y buenos sistemas de integración de cambios y despliegue. Todo esto contribuye a garantizar que podemos desplegar software sin defectos evidentes.

Eso no evita su aparición, pero permite que si aparecen sean relativamente fáciles de controlar.

Una vez que un bug ha sido reportado, lo primero sería centrarnos en él, y establecer una o más hipótesis y expresarlas en forma de test. Un bug normalmente es el resultado de un ejemplo que no ha sido testeado. Esto puede pasar porque carecíamos de información en el momento de desarrollo, bien porque no identificábamos ese ejemplo como un caso particular. También puede ocurrir que un cierto cambio habilite un bug que antes no se había manifestado.

En cualquier caso, una vez que tenemos un test, modificamos el código para hacerlo pasar, junto con todos los demás teste existentes. De este modo, subsanamos el bug y podemos desplegar este nuevo cambio para arreglarlo en producción. Entonces volvemos al desarrollo habitual.

Esta forma de abordar los bugs suele despertar recelos. En buena parte, es cierto que no se puede aplicar en organizaciones que arrastran errores desde hace largo tiempo. En otra parte, existe una especie de creencia de que los bugs son algo así como consustanciales al desarrollo de software.

Para empezar, en lugar de bugs voy a empezar a hablar de defectos. Un defecto del software es un concepto que podríamos considerar más amplio que el de bug. Un defecto ocurre cuando el software no se comporta como las usuarias esperan.


### Defectos de comportamiento

Un defecto del software puede ser algo así como un aspecto no especificado al definir una prestación. ¿Cómo puede ser un bug algo que no sabías que era necesario?

Otro ejemplo de defecto puede ser el haber hecho asunciones incorrectas sobre una característica. Por ejemplo, que un cierto parámetro permita o no números negativos. De nuevo, estaríamos ante un caso de definición incompleta, de un escenario no contemplado.

### Defectos técnicos

Otra categoría de defectos nos lleva




