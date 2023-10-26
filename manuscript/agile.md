# Qué es y que no es agile

Agile no es una metodología, ni un proceso, ni un framework. Creo que hasta es incorrecto decir que es una mentalidad o _mindset_. Quizá podríamos decir que agile es una forma de reflexionar sobre el desarrollo de software, o una filosofía, si lo prefieres.

Históricamente, podemos pensar que Agile nace con el Manifiesto Agile, pero más bien el Manifiesto es un punto de encuentro para diversos grupos y profesionales preexistentes que habían desarrollado sus propias metodologías y frameworks, como extreme programming, scrum, lean software... Muchos de ellos inspirados o derivados de las metodologías Lean o el Toyota Production System.

¿Por qué? Pues porque los equipos de desarrollo de software entendieron que las metodologías clásicas de la ingeniería no funcionaban bien aplicadas al software. 

Por lo general, la ingeniería física require un diseño meticuloso y una planificación cuidadosa antes de comenzar a implementar. No puedes empezar a construir un puente sin saber donde vas a poner los pilares, qué hay al otro lado, cómo se va a usar, qué peso va a tener que soportar, qué fuerzas pueden influir sobre él, como corrientes de agua o vientos, y un largo etcétera.

En muchos sentidos, la ingeniería física crea productos que han de acertar a la primera. Pero al requerir mucho tiempo de desarrollo y ejecución, es muy posible que cuando por fin han sido desplegados pueden haber ocurrido cambios en el entorno a los que ya no se puede adaptar. 

Pero el software no tiene los mismos condicionantes. En comparación con cualquier ingeniería física, que trabaja con materiales sujetos a las leyes de la naturaleza, el software es mucho más libre. Puedes usar el software a medida que se construye, una vez que hay suficientes elementos desplegados. Incluso aunque esté incompleto puede proporcionar un valor. Por otro lado, es relativamente fácil de cambiar, lo que permite reaccionar cuando vemos que el negocio va cambiando de maneras que no habíamos previsto.

Para ello son fundamentales los ciclos de feedback, es decir, la información que obtenemos sobre el comportamiento del software de diversas fuentes. Cuanto más cortos, mejor. Y por cortos entendemos minutos mejor que horas, horas mejor que días y así sucesivamente. Para lograrlo necesitamos incorporar, por un lado, a la cliente o usuaria en el equipo de desarrollo de forma que podamos tener conversaciones con ella cada vez que sea necesario. Por otro lado, también incorporamos prácticas que nos faciliten el feedback, como _pair-programming_, test driven development, etc. Pero también implica entregar el software en pequeños lotes de funcionalidad, de tal modo que revertir lo desplegado o introducir cambios sea lo menos costoso posible.

Esta forma de abordar los proyectos de software puede parecer idílica, pero mucho más factible de lo que podrías pensar. 

Lo primero que hay que tener en cuenta es que no es algo que se pueda conseguir de la noche a la mañana. Requiere un proceso de aprendizaje. Requiere hacerse consciente de como trabajas y reflexionar sobre cómo mejorar esa forma de trabajar. Por tanto, requiere una cierta capacidad de autocrítica, individual y grupal.

Es decir: un equipo no se vuelve agile porque le adjudiquemos la etiqueta. En vez de eso, un equipo aprende a trabajar de forma agile a medida que desarrolla un proyecto.

No existe una receta para ser agile salvo aplicar, quizá, los principios del Manifiesto. Por otro lado, disponemos de frameworks como Scrum.

Por lo general Scrum es el framework agile más usado. Sin embargo, muchos proponentes originales de agile reniegan de él, no sin buenos motivos. Esto ocurre por varias razones, pero quizá las más importantes sean:

* Scrum hace énfasis en el proceso, mientras agile pone las personas por encima de los procesos. Lo que dice agile es que cada equipo debe buscar su propio proceso.
* En realidad, pocos equipos siguen Scrum por la guía, y han ido introduciendo, modificando o eliminando elementos, según conveniencia. Así que podríamos decir que, en realidad, no están haciendo Scrum. Esto estaría bien si fuese consecuencia de una reflexión crítica sobre la metodología, pero no está claro que se cumpla en todos los casos.
* Scrum ha sido _secuestrado_ por el management como forma de control.
* Scrum a veces se identifica con una herramienta específica como Jira.

Algunas ideas incorrectas sobre agile:

**El objetivo de agile es conseguir más velocidad en el desarrollo**. Esto es falso. Como se afirma en el Manifesto se promueve un ritmo de desarrollo sostenible. En el largo plazo, los equipos agiles genuinos son muy rápidos, porque han ido creando las condiciones para ello. Pero no porque hayan priorizado la velocidad de desarrollo, sea eso lo que sea, sino porque son capaces de definir lotes de trabajo que se pueden entregar rápidamente y de forma regular.

**Estimar es parte de una metodología agile.** Es otro mito. Las estimaciones pretenden cumplir una necesidad de la empresa como es la de establecer un marco temporal para la finalización de un proyecto. Esto también deriva de la gestión de proyectos de ingeniería física. Sin embargo, en agile existe un producto en desarrollo contínuo: hay un momento en que se puede empezar a trabajar con el producto y se van incorporando nuevas prestaciones. Idealmente, de forma regular y sostenible.

Derivado de las estimaciones está el concepto de los puntos de historia. Fueron introducidos como una forma de desviar la atención sobre las medidas temporales (¿cuántas horas/días requiere este desarrollo?) y sustituirlo por otra forma de medición del esfuerzo que puede requerir un desarrollo (los famosos puntos). El objetivo era proteger a los equipos de desarrollo de los plazos de entrega. Sin embargo, siempre hacemos una traducción de los puntos a tiempo, por lo que pierden su sentido. 

**El Product Owner es el encargado de dirigir el equipo y decidir lo que hay que hacer**. Para empezar, la figura del Product Owner es exclusiva de Scrum. Un equipo agile no necesita Product Owner. En principio, el rol de Product Owner es actuar más o menos como representación del cliente en el equipo, ayudando al equipo de desarrollo a entender cuáles son las necesidades del cliente. En la práctica, lo PO oscilan entre una especie de Project Manager y un gestor de tarjetas de Jira. 

La figura tiene sentido en tanto y cuanto no es posible tener a la cliente o usuaria real en conversación con el equipo. De todos modos, una buena Product Owner puede ser un gran recurso a la hora de entender qué es lo más valioso que el equipo debería estar haciendo, algo que sí aporta a un equipo ágil.

**Scrum Master**. Es un rol muy poco comprendida, en gran parte porque no se sigue Scrum por la guía. El rol forma parte del framework Scrum, pero un equipo agile no lo necesita. 
