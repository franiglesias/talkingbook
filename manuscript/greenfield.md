# G de Greenfield

La mayor parte de tu vida de trabajo consistirá en incorporarte a proyectos que ya están en marcha. En ese sentido es bastante raro empezar a trabajar en algo completamente nuevo que el equipo tenga que construir desde cero.

Muchos equipos fuerzan ese _empezar de cero_ cuando deciden rendirse con una implementación antigua y prefieren tomar el camino de volver a escribir un software sobre nuevas bases. A veces con una nueva arquitectura, en un lenguaje que consideran más apropiado y, posiblemente, usando algunas tecnologías nuevas y de moda.

Una esperanza general con respecto a este tipo de reescrituras y proyectos _greenfield_, es la de que "esta vez vamos a hacer las cosas bien". Un bonito deseo que raramente se cumple.

¿Qué es lo que lleva a un proyecto nuevo a torcerse? Seguramente hay muchas causas interviniendo a la vez, en diferentes grados.

Sospecho que la más importante es que en realidad empezar un proyecto de cero no resuelve los problemas preexistentes que llevaron por mal camino al anterior. 

Por ejemplo, si en tu empresa ha migrado de un monolito a micro-servicios y la cosa no ha ido muy bien, lo más seguro es que el problema venga de antes. Al fin y al cabo, si ya no estabáis gestionando bien la modularización del monolito, hay que pensar que los micro-servicios son muchísimo más difíciles.

Otro caso típico es cuando vuestro proyecto antiguo carecía de tests, lo que os impedía intervenir en él con seguridad. ¿Qué garantías tienes de que ahora los váis a tener? No es el primer proyecto nuevo en el que los tests se posponen, con la consecuencia de que al intentar introducirlos por fin, resulta difícil porque el diseño no está orientado a la testabilidad. Es decir, ¿a la hora de plantear un nuevo proyecto estamos teniendo en cuenta las capacidades técnicas necesarias para empezar con buen pie?

Una razón por la que los proyectos nuevos acaban igual de liados que aquellos a los que sustituyen es que olvidamos que todo código puesto en producción acumula un desfase con respecto al conocimiento de negocio. Esto es: el conocimiento de negocio que hemos representado en el código deja de estar al día con el conocimiento de negocio que maneja el equipo, y si no velamos por sincronizarlo, llegará un momento en que el desfase será tan grande que nos generará problemas. Esto tiene un nombre: deuda técnica.

A veces, el nuevo proyecto no es más que una traducción desde otro lenguaje de programación. No solamente se acumularán los problemas existentes, sino que se añadirán los derivados de intentar replicarlo con los paradigmas de otro lenguaje.

Una vieja conocida en estos casos es la Ley de Conway, que dice que una organización que produce software tiende a reproducir en él sus estructuras de comunicación. En consecuencia, reestructurar el software suele estar condenado al fracaso si no hay cambios en la propia organización. En ocasiones, se intenta aplicar la llamada Maniobra Inversa de Conway: transformar la estructura de la organización, a fin de impulsar cambios en la estructura del software.

Una de las preguntas que creo que no se hacen en los equipos que abordan nuevos proyectos, o transformaciones de proyectos existentes, es si poseen el conocimiento y la capacidad necesaria para llevar el proceso a buen puerto. ¿Cuántos proyectos se escriben otra vez de cero simplemente porque el equipo no sabe refactorizar de forma segura? ¿O porque el equipo no domina las técnicas de testing?
