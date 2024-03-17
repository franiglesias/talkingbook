# WIP

WIP es el acrónimo en inglés de Trabajo en Progreso o Work In Progress. El trabajo en progreso en un equipo es todo el trabajo que está en marcha, pero sin terminar.

La gestión del WIP es fundamental en un equipo ágil o de alto rendimiento, porque es uno de los factores que determina la capacidad de entrega. Y, por lo general, la gestión del WIP consiste en limitarlo y reducirlo lo máximo posible.

Esto puede sonar un poco contra intuitivo, ya que puede parecer que si podemos trabajar en varias cosas a la vez en paralelo, deberíamos poder acabarlas todas más o menos a la vez. Así que un equipo de _n_ personas, podría abordar _n_ proyectos o tareas simultáneas. Decimos que su capacidad es de _n_. Lo razonable, entonces, sería que un equipo en un momento dado limita su trabajo en progreso a _n_ ítems o tareas.

Sin embargo, muchas veces resulta que las cuentas no acaban de salir. Por ejemplo, si un equipo está formado por cinco desarrolladoras, se asume que su capacidad es de cinco tareas simultáneas y su límite de trabajo en progreso sería de cinco ítems. Todo cuadra perfectamente, ¿no? Pues, no.

Resulta que una de las desarrolladoras es la manager del equipo, por lo que entre sus funciones están participar en reuniones de coordinación con otros equipos, las reuniones de seguimiento de las personas a su cargo y otras tareas asociadas a su rol. Su posibilidad de aportar al flujo de trabajo está reducida, asi que si asume tareas del equipo lo normal es que siempre lleve retraso o no las pueda realizar. Eso sin contar, que frecuentemente tiene que resolver dudas y preguntas del resto del equipo por cuestiones técnicas o de negocio.

En consecuencia, sería mucho más realista asumir que la capacidad y el límite del WIP del equipo es cuatro. Es importante tener en cuenta la capacidad efectiva. Por ejemplo, si una persona en junior es posible que no tenga aún autonomía para completar tareas por sí mismas. En ese caso, quizá deberíamos plantearnos que esta persona trabaje siempre junto con otra de más experiencia, de tal forma que la capacidad del equipo sería tres, al igual que el límite del WIP.

Bueno, esto parece solucionar el problema. Pero... No tan deprisa.

Supongamos que el equipo ha decidido trabajar en dos historias de usuario. Estas historias se han dividido en tareas y cada desarrolladora se asigna una tarea. De este modo tendríamos cuatro tareas en marcha. Son posibles varias configuraciones, por ejemplo, que hayan iniciado dos tareas de cada historia de usuario, o cuatro de una. Incluso tres de una y una de la otra.

En ese caso, es posible que unas tareas bloqueen otras. O sea: si trabajamos paralelamente en dos tareas de la misma historia podría ocurrir que una consista en desarrollar un elemento que es requerido por la otra. Esto haría necesario detener una de las tareas para esperar por la otra. En ese caso, estamos desperdiciando tiempo.

Se podría aducir aquí que, mientras una tarea está bloqueada, podemos iniciar otra. Pero esto no reduce el WIP, sino que lo aumenta, porque la tarea bloqueada sigue siendo trabajo en progreso, aunque esté parada. En nuestro ejemplo, pasamos de un WIP de cuatro a cinco, superando el límite que habíamos definido.

El límite de WIP, por tanto, no depende únicamente del número de personas, sino también de la relación entre las tareas. De hecho, los mayores problemas con el WIP suelen ocurrir en equipos que trabajan por tareas y no por historias de usuario.

Otro problema, relacionado tiene que ver con el cambio de contexto. Cuando una desarrolladora termina una tarea y se asigna otra que está en un proyecto o historia de usuario diferente, tiene que emplear un tiempo en adaptarse al nuevo contexto. En algunos equipos, podría implicar incluso trabajar en una base de código diferente. Este tiempo de adaptación es tiempo en el que la tarea no progresa. De nuevo, desperdicio.

Una forma de limitar el WIP de manera eficiente es definirlo como historias de usuario simultáneas en lugar de tareas. En este punto quizá sea necesario hacer algunas definiciones.

Ya hablamos de historias de usuario en otro capítulo de este libro, pero podemos pensar en ellas como proyectos concretos para poner una prestación funcionando en manos de los clientes. Las tareas serían la construcción de las piezas necesarias para completar esos proyectos.

Las tareas tienen sentido en el contexto de la historia de usuario. Por ejemplo, en la historia de usuario "los clientes pueden pagar su pedido con Paypal", puede haber tareas como:

* Añadir un componente en la página web para seleccionar pago con Paypal.
* Desarrollar la integración para redirigir al cliente a su cuenta de Paypal si escoge este medio.
* Procesar la respuesta del medio de pago para marcar el pedido como confirmado y pagado e iniciar el proceso de envío.
* Añadir una página de confirmación del pedido pagado con este medio.
* Enviar una notificación.
* Mostrar una página indicando que no se ha podido realizar el pago, si es el caso.

Estas tareas son dependientes entre sí y pueden generar bloqueos. Pero podemos ver que unas corresponden a la especialidad de frontend, y otras a la de backend, lo que nos proporciona un criterio de asignación de recursos. Dos personas, una por especialidad, podrían trabajar juntas en la historia de usuario, estableciendo contratos para la comunicación entre ambas partes. Según los casos, podríamos decidir que necesitamos más personas trabajando en esta historia. Pero si no es así, contamos con otras dos personas que pueden estar trabajando con otra historia.

En este caso, el límite de WIP podría ser de dos historias de usuario simultáneas. Durante esta iteración solo deberíamos estar trabajando en esas dos historias.

Lo curioso del asunto es que la historia que acabamos de describir abarca seis tareas. ¿No es algo contradictorio? Resulta que reduciendo el WIP podríamos tener más productividad.

Esto se explica por varias razones. Por un lado, la historia de usuario proporciona un contexto único durante toda la iteración para las desarrolladoras participantes. No tienen que cambiar entre contextos, no tienen que entender como encaja cada tarea en cada momento. De hecho, puede que desarrollen una compresión de la historia de usuario que les permita hacer una partición conveniente de las tareas.

También es más fácil prevenir, evitar o gestionar, los bloqueos entre tareas. Por ejemplo, si la tarea implica frontend y backend, pueden acordarse contratos de las API que expone el backend, de tal forma que el frontend puede trabajar con stubs, o incluso tirando peticiones contra endpoints "tontos", mientras el backend se ocupa de otros elementos. Gracias a esto es posible paralelizar el desarrollo.

Lo que ocurre es que cuando distribuimos las personas del equipo para trabajar en historias de usuario, lo que estamos haciendo en crear equipos enfocados (_task force_) que tienen un objetivo claro y un límite del WIP igual a uno. Si es necesario añadir personas, el límite de WIP se mantiene igual. Pero solo podemos añadir personas hasta un punto en que no se molesten.

Es importante coordinar el límite del WIP con la definición de objetivos. Si tenemos varias historias de usuario en una iteración, una de ellas tiene que ser la prioritaria y tenemos que asignarle todos los recursos que admita para que se pueda entregar en esa iteración.

De hecho, las preguntas más importantes que un equipo debe hacerse son:

* ¿Qué es lo más importante que deberíamos estar haciendo ahora? Que básicamente, coincide con lo que es más importante para el cliente.
* ¿Qué es lo que NO tendríamos que estar haciendo ahora? Que es cualquier otra cosa.
