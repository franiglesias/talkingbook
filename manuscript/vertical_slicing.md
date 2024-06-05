# V de Vertical (Rebanado de historias)

En la ingeniería física es frecuente que un sistema se divida en subsistemas o componentes y que cada uno de ellos sea construído de forma separada. Cuando todos los elementos están disponibles, se ensambla el sistema completo. Por esa razón, es muy importante establecer unas especificaciones muy precisas y esforzarse en cumplirlas. En caso contrario, se producirán problemas, que pueden ser muy graves y difíciles de solucionar.

El objetivo, por supuesto, es optimizar y aprovechar las ventajas de la especialización y de la estandarización. La especialización permite que los fabricantes de un componente aprovechen su conocimiento y experiencia, ahorrando tiempo de aprendizaje y diseño. La estandarización, por otro lado, facilita que se puedan recurrir a distintos proveedores del mismo tipo de componente y que puedan inter-operar.

Este modelo se aplica con cierta asiduidad en ingeniería de software y plantea compromisos y desafíos.

Así, por ejemplo, en un proyecto de software podemos identificar especialidades como Frontend, Mobile, Desktop, Backend, Bases de Datos, Data, y Sistemas o Infraestructura. A cada una de ellas le asignamos responsabilidades y personal diferente.

Por esa razón, en las metodologías ágiles se suele insistir en la idea de que un equipo debe configurarse de modo que posea todas las capacidades necesarias para desarrollar su producto o proyecto. De ahí que un equipo ágil normalmente incluya una representación de todas estas especialidades... O al menos de algunas, ya que es cierto que algunos perfiles se comparten entre equipos, como puede ser Sistemas o Data, por poner un ejemplo.

Posiblemente, esto último ocurre porque se trata de aspectos del proyecto que cambian con poca frecuencia. Son importantes a la hora de ponerlo en marcha, pero no necesitamos cambiar cosas constantemente como ocurre con el código.

Pero ciñámonos al código. Es relativamente frecuente que los proyectos de software se diseñen también organizados por componentes. Esto es habitual cuando se utiliza una metodología waterfall en la que existe una fase de diseño previa, tras la recogida de requisitos, en las que se planifican todos y cada uno de los componentes del sistema. En ese contexto, parece natural distribuir el trabajo entre varios equipos, cada uno encargado de un componente.

Este enfoque es generalmente rechazado en los _frameworks_ ágiles por varias razones. La primera es que suele llevar a una entrega tardía de valor. Se desarrollan los componentes y hay que resolver todos los posibles problemas de integración antes de ser capaces de poner el software en producción y a disposición del público.

En consecuencia pueden producirse algunos efectos indeseados:

* No sabemos si el producto funcionará. Es una pregunta a la que solo podremos dar respuesta cuando todos los componentes estén terminados e integrados.
* No tenemos _feedback_ temprano, puesto que el software no está en producción. Si la hipótesis de negocio no es correcta, no lo vamos a saber. Si la oportunidad de negocio ha pasado y una empresa competidora ha salido antes, es posible que hayamos perdido el mercado.

Esta aproximación es lo que se conoce como rebanado o slicing horizontal: una prestación o proyecto se divide en componentes o fases que se desarrollan en paralelo y el producto se entrega después de una fase de integración.

Los frameworks ágiles suelen preferir un tipo de rebanado o slicing vertical. En lugar de dividir una prestación o proyecto en componentes, proponen una aproximación distinta basada entregas de valor iterativas e incrementales. En lugar de preguntarse: ¿qué piezas necesito para construir esta funcionalidad?, la cuestión es más bien: ¿qué necesito hacer para entregar al menos una mínima parte de la funcionalidad que aporte valor? Intentaré explicarlo con un ejemplo.

Supongamos que tenemos una tienda de material para modelismo: maquetas, pinturas, herramientas, libros, etc. y queremos vender online. 

Lo primero que necesitamos es una web que se pueda visitar, lo que implica disponer de una infraestructura adecuada, y una aplicación básica que pueda exponer una _landing page_, tal vez con acceso a un catálogo de productos. Como queremos vender, podríamos incluir un simple formulario de pedido en el que el cliente anote los productos deseados y una forma de contacto. Es cierto: toda la gestión de la venta tendríamos que hacerla a mano, pero al mismo tiempo estamos obteniendo información:

* ¿Existe interés en nuestra tienda?
* ¿Qué tipo de productos se piden más?
* ¿Qué tipo de clientes tenemos?
* ¿Desde dónde nos contactan?

Esta información nos puede ayudar a tomar decisiones para priorizar los siguientes pasos. Entonces se repite la pregunta: ¿qué necesito hacer para entregar al menos una mínima parte de la funcionalidad que aporte valor?

Así, por ejemplo, me interesará probablemente introducir un carrito de compra y un catálogo de productos. Pero a lo mejor, gracias a la información recibida, puedo ver que hay interés en herramientas, pero no en libros, así que puedo dedicar mis esfuerzos a esas gamas de productos.

En una siguiente iteración podríamos empezar a plantear introducir un medio de pago. La decisión de cuál en concreto puede venir determinada por lo que hayamos aprendido de interactuar con nuestros clientes. De este modo, nos aseguramos de introducir una integración con aquella pasarela de pago que sí va a ser usada.

Estas capas de funcionalidad implican diversos componentes, porque atraviesan todos los estratos de la arquitectura de la solución, por eso se le llama rebanado vertical. Así, en lugar de desarrollar componentes muy detallados, lo que vamos añadiendo es funcionalidad de extremo a extremo a medida que la necesitamos. Para hacer esto bien, es necesario escribir código simple sobre el que sea fácil intervenir, lo cual requiere un refactor constante de modo que el código se abra a introducir cambios cuando sea preciso.
