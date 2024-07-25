# O de Collective Ownership

La propiedad colectiva del código se refiere a que el código de un proyecto es de todo el equipo. Pertenece a toda persona que haya participado. Y, a la vez, no pertenece a nadie en particular.

Es una idea muy sencilla. El código representa el conocimiento colectivo del equipo sobre el problema que esa aplicación o sistema trata de resolver. El hecho de escribir el código en sí es, en varios sentidos, secundario. En realidad, lo que importa es el conocimiento que se expresa con ese código.

Que la propiedad del código sea colectiva es muy importante. Para empezar, es lo que permite que podamos actuar sobre ese código cuando sea necesario. El desarrollo debe producirse de tal manera que cualquier persona pueda intervenir cuando sea necesario, tanto para añadir una nueva prestación, como para arreglar un error, o para mejorar la estructura y diseño.

Nadie puede actuar como guardiana, o decidir quién tiene derecho a tocar qué. El _gatekeeping_ va contra la productividad.

Esto implica una serie de derechos y deberes.

* **El derecho a conocer el código y su funcionalidad**: todas las personas que forman parte del equipo tienen derecho a conocer el código y lo que hace, para lo cual es necesario que esté bien organizado y diseñado. Es más prioritario que una documentación extensa, que corre el riesgo de quedar obsoleta muy pronto si no se mantiene sincronizada.
* **El derecho a modificarlo**: todas las personas que forman parte del equipo tienen derecho a modificarlo a fin de que el código mantenga una buena representación del conocimiento del equipo sobre su parte del negocio. Debería ser obvio que para poder ejercer este derecho es necesario conocerlo.
* **El deber de mantener el código en buen estado**: si nos limitamos a añadir prestaciones al código o modificarlo para corregir defectos, con el tiempo el código se deteriora. Para evitarlo, hay que mantenerlo activamente en buen estado, revisando su diseño y asegurándonos de que disponemos de puntos de cambio adecuados para hacerlo evolucionar.
* **El deber de aceptar los cambios que hagan otras personas del equipo**: la propiedad colectiva implica, como hemos señalado, que nadie tiene una autoridad especial para autorizar o no cambios en el código.

## Control de cambios

Se podría argumentar que puede resultar peligroso: ¿qué pasa si alguien introduce por su cuenta y riesgo un cambio que destruye datos, introduce errores o modifica el comportamiento de tal forma que no se corresponde con el objetivo de la aplicación?

Aparte de una cuestión de responsabilidad individual, también disponemos de métodos para minimizar el riesgo de que en el código ocurran este tipo de problemas, ya sea por falta de conocimiento ya sea por malicia.

**Separar el momento de publicación del software de la mezcla de cambios**, introduciendo un paso extra en el que se puede verificar que todo funciona según lo previsto. Diremos que este es el método menos ágil de todos, pero tiene sus casos de uso.

**Propuesta de cambios con autorización obligatoria**: o sea, nuestras _Pull Request_ (o _Merge Request_) y _Code Review_ de toda la vida. La idea es que no sea posible mezclar un código sin que otra persona del equipo lo supervise, preferentemente tras haber revisado los cambios y haberse hecho una idea de su impacto. Es otro método muy discutido si queremos hablar de un proceso de desarrollo realmente ágil.

**QA**: Una buena suite de tests contribuye a hacer más difícil la introducción de cambios no deseados o que alteren el comportamiento del sistema. Cuanto más automatizada mejor, para que no se convierta en un cuello de botella.

**Pair programming o mob-programming**. La ventaja de estas metodologías es que introducen la revisión de código en el propio proceso de creación. De este modo, la revisión y autorización dejan de paralizar la entrega. Pero además, estas técnicas contribuyen a que se comparta el conocimiento sobre el código, así como la responsabilidad de las decisiones, lo que favorece la disminución de problemas como el bus factor, previniendo la formación de silos.

## 10x Engineer

De tanto en cuanto se pone de moda el concepto del _10x Engineer_. Se trata de un concepto un tanto difuso que se aplicaría a aquellas personas con un rendimiento excepcionalmente alto, gracias a su motivación, conocimiento técnico y dedicación. Es un perfil que levanta polémicas: hay quien lo considera deseable y un ejemplo a seguir, y hay quien encuentra que es un peligro para los equipos, y empresas, que lo permiten.

En el contexto de este capítulo sobre _Ownership_ en un libro que habla de Agilismo, un _10x Engineer_ (lo habitual es que sea varón, para qué nos vamos a engañar) es una figura que puede ser muy peligrosa.

Es frecuente que tome sus propias decisiones al respecto de la organización del código o de las tecnologías de las que depende. Así que, de un día para otro, las otras personas del equipo se pueden encontrar con cambios significativos del código a los que deben adaptarse.

Suele ocuparse de más de una tarea al mismo tiempo, lo que incrementa el trabajo en curso del equipo y puede generar bloqueos o retrasos en las entregas.

Tiende a trabajar solo y, con frecuencia, en horario no laboral, con lo que no contribuye a la distribución del conocimiento dentro del equipo. No da oportunidades a las técnicas de programación grupal (_pair_ o _mob_) entre otras cosas porque considera que ralentizan su ritmo de trabajo.

Por otro lado, suele acumular mucho conocimiento del sistema, pero al no distribuirlo genera un silo, lo que a su vez provoca un _bus factor_ muy acusado. Con el tiempo, el equipo se vuelve totalmente dependiente. Esta persona ejerce un liderazgo técnico, que puede ser implícito o reconocido con un rol de _Tech Lead_ o similar, pero que está sustentado en la dependencia.

Uno de los problemas que derivan de tener un _10x Engineer_ en un equipo es la frustración que genera en otras personas, a las que reduce sus oportunidades: no ayuda a crecer a las que son _junior_, no deja espacio para que otros _seniors_ puedan participar en temas relevantes y liderar en sus áreas de experiencia. En poco tiempo, estas personas están buscando oportunidades en otro equipo, si es posible, o en otra compañía en el peor de los casos.

Este tipo de perfiles resultan ser relativamente valiosos para la empresa en el corto plazo, porque en términos de producción hacen que las cosas salgan. Pero en el largo plazo, encierran una trampa que puede ser mortal. El _10x Engineer_ es valioso... mientras siga en la empresa. Si se marcha, puede dar lugar a una crisis importante. Pero quedándose, puede ser bloqueante para incorporar talento.

Una de las razones por las que el concepto de _Collective Ownership_ es tan importante, es precisamente para prevenir este tipo de situaciones. Un equipo debe ser mejor que la suma de sus miembros, para lo cual todas las integrantes tienen que poder contribuir desde sus capacidades y desarrollarse. En un equipo en el que existe la figura del _10x Engineer_, no existe _Collective Ownership_, pues todo el _ownership_ posible pasa por esa persona concreta. No hace falta que tenga un rol específico, sino que la dinámica de trabajo lo refuerce.

En un equipo sano se busca una eficiencia en la entrega de valor que sea sostenible en el tiempo, no dependiendo de circunstancias particulares, o de que personas concretas estén presentes o ausentes. 
