# Historias de Usuario

Según Wikipedia, la idea de _Historia de Usuario_ la introdujo Kent Beck en 1997, en el contexto del ya famoso proyecto _Chrysler C3_, en el cual definió las bases de lo que sería _Extreme Programming_, e introdujo prácticas técnicas como TDD o _pair programming_. En 1998, Alistair Cockburn, que estaba de visita en el proyecto y a quien conocerás por ser proponente de la Arquitectura Hexagonal, acuñó la frase "Una historia de usuario es la promesa de una conversación".

Tengo que decir que me encanta la expresión, ya que describe algo que tendemos a olvidar. La Historia de Usuario no es una toma de requisitos, sino la expresión de un deseo o necesidad del cliente y, por tanto, la promesa o inicio de una conversación con este para entender esa necesidad y cómo se tiene que reflejar en el desarrollo del producto.

En 1999, Beck habla de las historias de usuario en la primera edición de su libro _Extreme Programming Explained_ al describir el _Planning Game_. Esta es una reunión de planificación, en la que el equipo de desarrollo acuerda con el cliente qué historias deberían abordarse en la siguiente iteración del producto. Las historias se escriben en tarjetas, describiendo la necesidad expresada por el cliente, de forma que estas se manipulan físicamente, se ordenan, se apuntan detalles, etc.

Posteriormente, en 2001 Ron Jeffries propone un formato para la creación de Historias de Usuario, llamado "las 3 C": _Card, Conversation and Confirmation_:

* _Card_ o tarjeta: es un objeto físico en el que se registran las historias.
* _Conversation_: es la que sucede entre todas las personas interesadas e implicadas.
* _Confirmation_: para asegurar que se han alcanzado los objetivos de la conversación.

También en 2001, el equipo XP de Connextra introdujo un formato de Historia de Usuario que se ha hecho tremendamente popular y que seguramente te sonará:

* Como [Rol]
* Quiero [Requerimiento]
* A fin de [Razón]

Este formato lo puedes encontrar en el libro _User Stories Applied: For Agile Software Development_ de Mike Cohn. El libro tiene ideas interesantes, aunque tengo la sensación de que el tratamiento de las historias de usuario se está complicando en demasía. ¿Por qué digo esto? 

Las historias de usuario nacieron como un concepto útil para romper con la tradicional "toma de requisitos" heredada de los procesos de ingeniería física. Beck y otros se dieron cuenta de varios aspectos que caracterizan el desarrollo de software si lo comparamos con otros proyectos de ingeniería.

* El software es maleable y flexible, podemos cambiarlo tantas veces como necesitemos.
* No necesitamos un conocimiento preciso y exhaustivo de sus requerimientos al empezar los proyectos, podemos darnos tiempo para descubrirlos o establecerlos.
* De hecho, ni siquiera los propios clientes, sean internos o externos, tienen claros todos los detalles. Saben lo que quieren, pero no necesariamente como conseguirlo. La conversación es necesaria precisamente para profundizar en esos detalles.

La consecuencia de esto es que podemos empezar a trabajar con una idea general de la necesidad expresada por el cliente: la historia de usuario. Para implementarla, el equipo de desarrollo inicia una conversación con el cliente, a fin de ayudarle a expresar esa necesidad de una forma cada vez más concreta, preferiblemente describiendo qué es lo que espera obtener. Esto último es lo que entendemos como criterios de aceptación.

Cuando consideramos que sabemos lo suficiente podemos empezar a desarrollar el software. Durante el proceso descubriremos más puntos que necesitan aclaraciones, por lo que volveremos a hablar con la cliente. Mejor, si podemos mostrar esto en forma de software funcionando. Precisamente, porque tendrá carencias, la cliente podrá identificarlas y describirlas. Esto inicia un nuevo ciclo de desarrollo, en el que el objetivo es solucionar las limitaciones señaladas.
