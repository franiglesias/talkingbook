# E de Equipo

Digámoslo con claridad: juntar a un cierto número de personas y ponerlas a trabajar en el mismo lugar no es crear un equipo. Para que exista un equipo tiene que haber un objetivo común, unos valores e intereses compartidos. Un equipo tiene que ser algo más grande que la suma de sus componentes.

Se podría decir que un equipo tiene que actuar como una unidad. Incluso diría que como un organismo. Cada uno de sus componentes aporta sus propias capacidades al fin común. Como todo, esto implica que es necesario aprender a trabajar de una cierta manera.

Por lo general, todas las aproximaciones _agile_ consideran que un equipo de desarrollo de software debe dotarse de todas las capacidades necesarias para cumplir sus objetivos de forma autónoma. Así, normalmente, queremos que haya personas con conocimientos en _frontend_, _backend_, sistemas, _user experience_ y negocio.

Esto no siempre quiere decir que tenga que formar parte del equipo una persona de cada una de esas especialidades. Las que tienen que estar presentes son las capacidades y los conocimientos. Sin embargo, la complejidad de cada uno de los ámbitos hace que sea muy frecuente tener especialistas. En cualquier caso, también depende de la organización, su propia complejidad y, por qué no decirlo, de su capacidad económica.

En muchos casos, lo suyo sería que los equipos se formasen de esta manera, con los múltiples perfiles necesarios. Con el tiempo, el conocimiento debería transmitirse horizontalmente. Por ejemplo, las desarrolladoras aprenderían lo suficiente como para llegar a valorar la prioridad de una prestación en términos de negocio. La persona de producto, por su parte, podría entender el coste técnico de ciertas soluciones. Las desarrolladoras podrían ser capaces de trabajar tanto en backend como en frontend, y controlar aspectos de la infraestructura necesarios.

Este desarrollo es lo que se conoce como perfil en "T": fuertes conocimientos de tu propia especialidad, y suficientes de las otras, tanto como para poder contribuir en ellas, aunque sea de una forma limitada.

Este tipo de perfiles "T" contribuye a reducir el _bus factor_ en los equipos. El _bus factor_ es un índice que nos dice cuantas personas del equipo tendrían que desaparecer súbitamente para que el proyecto se paralice porque poseen información o conocimiento crítico de forma exclusiva. Si no están, se pierde ese conocimiento. Este índice nos está indicando si el conocimiento fluye entre las personas del equipo.

Este _bus factor_ se puede reducir de varias formas. En lo que toca al equipo de personas, se deben aplicar medidas que faciliten la diseminación del conocimiento, lo que acaba llevando a desarrollar estos perfiles "T" de los que hablábamos hace un momento. Algunos ejemplos:

**Evitar la multitarea de equipo**. El equipo debería trabajar conjuntamente en los mismos proyectos o historias de usuario, o al menos hasta el punto de que no se molesten entre sí.

Cuando las distintas personas del equipo trabajan en proyectos no relacionados, o mínimamente relacionados, tienden a generarse silos de conocimiento. Con el tiempo, las mismas personas tenderán a dedicarse a los mismos temas. Esto es por una cuestión de familiaridad y eficiencia. Si cada semana tienes que elegir entre trabajar en algo de lo que tienes experiencia previa y algo que te resulta totalmente nuevo, lo más seguro es que acabes escogiendo lo conocido. Además, el trabajo saldrá adelante más rápido.

Si escoges la tarea completamente nueva, aparte de trabajar más lentamente porque tienes que aprender lo necesario para poder ejecutarla, lo más seguro es que acabes pidiendo ayuda a alguien que tendrá que aparcar su propia tarea para dedicarte un tiempo. Esto acaba generando una sensación negativa de ineficiencia y bajo rendimiento.

Si el equipo practica revisiones de código asíncronas para poder mezclar los cambios se manifestarán otros problemas. Es difícil revisar un código del que no tienes contexto.

**Trabajar regularmente en formatos de _pair-programming_ o _mob-programming_**. Estos son los más adecuados para favorecer la diseminación de conocimiento entre desarrolladores, pero también entre otros miembros del equipo.

_Pair-programming_ es la práctica de trabajar en pareja para desarrollar una prestación en código. La idea básica es que una de las personas, o _driver_, se encargue de escribir el código y la otra _navigator_ se ocupe de dirigirlo con un enfoque más estratégico. Estos roles se deben alternar, incluso dentro de la misma sesión. Hay diversas configuraciones para llevar a cabo sesiones de _pair-programming_, dependiendo del grado de experiencia de cada persona y de los objetivos de la sesión.

_Mob-programming_ es una práctica similar, pero en este caso, es todo el equipo el que participa aportando ideas, haciendo preguntas, proponiendo soluciones, buscando información, etc. Una forma de conceptualizarlo es entender estas sesiones como conversaciones del equipo en las que se toman notas en forma de código. De hecho, se puede entrar y salir de la sesión, invitar a otras personas de otros equipos que puedan tener algo que ver con lo que estamos desarrollando, etc. Es una técnica ideal para los primeros pasos de diseño de una prestación, en los que se pueden ir estableciendo los componentes necesarios, los contratos entre distintas partes, etc. 

Esto no quiere decir que tengamos que trabajar en uno de estos formatos todo el tiempo. Lo ideal es que el equipo entero trabaje conjuntamente en el análisis de la historia de usuario, definiendo sus criterios de aceptación, y los primeros pasos de diseño de la solución, hasta el punto en que el trabajo por especialidad tenga más sentido. Y así, sucesivamente, hasta que tengamos tareas muy acotadas que sea fácil realizar individualmente. 

**Diseñar soluciones sencillas, fáciles de entender y cambiar.** En lo que respecta al código, lo ideal es que sea lo más expresivo y fácil de entender posible. El código, como expresión de un conocimiento del negocio, debería reflejar los conceptos y el lenguaje que manejamos en el equipo. Si el código no se puede entender, no es fácil ni económico intervenir en él. Por eso, las soluciones ingeniosas, pero incomprensibles, no son una buena idea.

**Documentar procesos, decisiones, soluciones y diseños**, y mantener al día esa documentación. La documentación debería estar siempre lo más cerca posible de donde se va a necesitar. En muchos, casos, la documentación se va a necesitar junto al código, lo cual nos permite establecer una espacie de reglas de preferencia a la hora de documentar:

* **El código** debería ser lo bastante expresivo como para que sea fácil entender qué hace y cómo, para lo cual son necesarios buenos nombres y el uso de patrones comunes.
* **Los comentarios** en el código tendrían la función de explicar decisiones concretas que se hayan aplicado. Si bien el código mismo describe qué hace y cómo lo hace, el porqué de escoger una cierta manera de hacer las cosas es difícil o imposible de expresar en código. Para eso, añadiremos comentarios.
* **Architecture Decision Records (ADR)**: algunas decisiones se refieren no tanto a partes específicas del código, como a cuestiones de amplio alcance: estructura de la aplicación, organización del código, elección de una cierta tecnología, etc. Estas decisiones o recomendaciones se pueden registrar en documentos que viven en el propio repositorio del código.
* **Readme**: el archivo readme del proyecto debería contener una descripción del proyecto y sus objetivos, así como las instrucciones necesarias para trabajar y contribuir.
* **Tooling**: lo ideal es que automaticemos cuantos más pasos necesarios para configurar y empezar a trabajar con el proyecto, asegurando un entorno de desarrollo común, independiente de la persona que trabaje con él. Para eso podemos usar herramientas como Make, Docker, etc.
* **How-to o recetas**: en algunos casos, introducir documentos que expliquen como realizar ciertos procesos ayudará a que cualquier persona del equipo pueda ser autónoma y no dependa de alguien en exclusiva para realizarlo. Mejor aún si esto se encuentra automatizado. Típico ejemplo: herramientas para corregir datos, probar ciertas prestaciones sin riesgo para producción, etc.
* **Otra documentación**: La documentación que no está relacionada directamente con el código, puede alojarse en otros sistemas, para los cuales existe numerosa oferta. Lo ideal siempre es que sean herramientas fáciles de usar y que, idealmente, permitan integrar distintas fuentes de información.
