# F de Feedback

Todo en _Agile_ gira en torno a bucles de _feedback_. O más bien espirales. Los bucles ágiles no consisten en girar sobre un mismo punto una y otra vez, sino un movimiento constante de autoevaluación, revisión del conocimiento y evolución. El desarrollo de software agile pretende ser espiral, o sea: incremental e iterativo.

Por desarrollo incremental entendemos un proceso en el que un producto se construye a base de añadir pequeños aumentos de funcionalidad de forma sostenida y relativamente predecible, en lugar de apostar todo a única entrega final del producto completo.

De este modo, se logran varios beneficios:

* Al desarrollar pequeñas cantidades de funcionalidad es relativamente fácil definir qué criterios de aceptación debe cumplir, podemos escribir código sencillo para implementarla, lo que reduce el tiempo de entrega y el riesgo asociado a la introducción de grandes cambios.
* Las entregas pequeñas nos facilitan identificar los defectos nada más poner una pieza de funcionalidad en producción. Si aparece un defecto, sabes que el origen tiene que estar en esa última entrega. Puedes volverla atrás fácilmente, o simplemente ver si puedes resolver el problema desplegando un arreglo.
* Una vez que ponemos una funcionalidad, aunque sea limitada, en producción, en manos de sus usuarias, podemos empezar a recibir feedback: ¿responde efectivamente a una demanda? ¿Está siendo usada? ¿Tiene limitaciones que las usuarias perciben? Con esta información podemos decidir nuestros pasos inmediatos: seguir con nuestro plan, hacer mejoras en la funcionalidad entregada, dejar ese camino, etc.

Desarrollo iterativo se refiere a que el proceso vuelve constantemente sobre el producto para refinar y ampliar su comportamiento. Al principio puede ser una idea sencilla y genérica, definida con trazos bastos, que nos permite poner a prueba una hipótesis de negocio sin arriesgar demasiada inversión y esfuerzo.

Cada nueva iteración se alimenta del feedback obtenido por la anterior, proporcionándonos información con la que tomar decisiones sobre nuestro siguiente paso: ¿qué es lo que ha funcionado? ¿Qué es lo que no? Y, por tanto, ¿qué deberíamos hacer para maximizar lo primero y minimizar lo segundo?

## Feedback loops

En general, los frameworks ágiles abrazan la idea de _feedback loop_ de una manera u otra. Scrum, por ejemplo, usa el sprint como la unidad de tiempo en la que se realiza una entrega o incremento y se obtiene feedback.

Pero si hay un framework que haya profundizado en la idea del bucle es Extreme Programming. Los bucles de feedback están definidos por el contexto en que se producen y están insertos en la propia forma de trabajar propuesta. En XP los ciclos de feedback comienzan en el mismo momento de escribir código:

* Puesto que XP promueve el uso de Test Driven Development, el primer ciclo de feedback nos lo proporciona el ciclo de TDD, que nos dice si estamos escribiendo el código necesario para hacer pasar el test que, a su vez, define el pequeño incremento de funcionalidad que estamos buscando. Este feedback es inmediato.
* Otra práctica técnica de XP es _Pair-programming_, en el que se produce creación y revisión colaborativa de código. Cada persona de la pareja propone ideas y las discuten inmediatamente, obteniendo feedback en segundos: ¿es una buena solución para este problema? ¿Es un patrón que nos brindará flexibilidad para cambios en el futuro? ¿O, en cambio, esconde un problema potencial?
* La ejecución de la suite completa de tests unitarios nos puede proporcionar feedback en minutos acerca del impacto de nuestros cambios en el conjunto del software.
* La negociación en las parejas de _Pair-programming_ es una fase de algo más alto nivel de abstracción que la fase de código. Aquí se discuten aspectos más generales de diseño, que pueden discutirse en el equipo completo y que posiblemente consuman un tiempo que se puede medir en horas.
* La _stand-up meeting_ (o _daily_ en términos de scrum) nos proporciona un ciclo de feedback que dura un día, y que nos sirve para verificar que estamos usando los recursos de forma equilibrada y que estamos moviéndonos en la dirección adecuada.
* Los tests de aceptación, que definen la _feature_ en desarrollo, nos proporcionan feedback acerca de si estamos construyendo el producto deseado. Este ciclo tiene se cumple en días.
* El plan de iteración, en el que se decide en qué vamos a estar trabajando, puede definir un ciclo de unas pocas semanas.
* El plan de release, en el que se decide qué se va a poner en manos de los usuarios, puede definir un ciclo de meses.

La duración de alguno de los ciclos puede variar dependiendo del tipo de producto. Por ejemplo, si estamos hablando de una aplicación web, prácticamente cada feature se puede habilitar en el momento, lo que hace que el ciclo de iteración y release coincidan.

Pero si se trata de una aplicación móvil, los ciclos son diferentes. Incluso publicando versiones con cierta frecuencia, acumulamos distintas _features_ y mejoras para desplegarlas juntas.

En cualquier caso, estos bucles tienen sentido en el marco de prácticas concretas diseñadas justamente para que el feedback sea utilizado.

