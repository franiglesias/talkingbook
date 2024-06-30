# F de Software Funcionando

El _Manifiesto Agile_ afirma que prefiere Software funcionando en producción que documentación extensiva. 

Hace no tantos años, cuando comprabas un software solía venir acompañado de uno o dos voluminosos manuales de instrucciones y o referencia, explicando todas y cada una de las funciones. Hoy en día ya casi no se distribuye software en un soporte físico, mucho menos con un manual en papel. En todo caso, puedes acceder a documentación digital para manejarlo. O, mejor aún, el diseño de experiencia de usuario muchas veces logra que puedas usar un software complejo sin tener que leer instrucciones. Al menos, lo que entendemos como uso básico y cotidiano.

Por ejemplo, la usuaria podría decirnos que hay ciertos casos infrecuentes que el software no procesa correctamente. O que cuando ocurre un error, no se entiende lo que ha pasado. O, tal vez, que el recuadro para introducir ciertos datos es demasiado grande o demasiado pequeño. O que la etiqueta de un botón resulta confusa. O que un proceso resulta farragoso. Asi que en vez de documentar los pasos con los que completar el alambicado proceso que hemos diseñado, nuestro trabajo consiste en reducir su _farragosidad_.

Pero volvamos al _Manifiesto_, porque no se refiere precisamente a un manual de instrucciones. Cuando este dice que preferimos software funcionando sobre documentación extensiva, está implícita la entrega de valor incremental. Si publicas pequeños paquetes de funcionalidad es más fácil que la usuaria aprenda como usarla y que pueda validar también el comportamiento del software, y también su usabilidad. Ese feedback es el que permite al equipo de desarrollo decidir qué tiene que hacer a continuación y le permite saber si el camino que sigue es el correcto.

Por otra parte, las entregas pequeñas permiten que el conocimiento expresado en el código sea comunicado más fácilmente y sea más fácil de aprender. Y, por supuesto, también más fácil de documentar.

## Preferir software funcionando no es negar la documentación

El problema de la documentación extensiva del software es que es un proceso que consume mucho tiempo y esfuerzo, sin que proporcione un beneficio real. Además, incluye un riesgo: generar documentación es mucho más lento que desarrollar software, con lo cual es muy difícil mantener software y documentación en sincronía. En último término, cuando la documentación no está al día, se vuelve inútil. ¿O es que vamos a detener el desarrollo para poder actualizar la documentación?

Por esa razón, es importante decidir qué documentar, cuando y cómo.

En el capítulo sobre Equipo, mencionábamos diversos lugares y formas en las que poner documentación. Así, por ejemplo, la primera línea de documentación sobre el código, debería ser el propio código. Complementada por los comentarios, que añadirían contexto sobre la toma de decisiones. Y se completaba la lista con una serie de documentos que se ubicarían cada vez más lejos del código, a medida que sea menos necesaria para el día a día y que abarque aspectos más generales.

En ese capítulo no llegamos a mencionar un par de aspectos, así que lo hacemos ahora. El primero, son los tests como documentación. El segundo es lo que ocurre cuando otros equipos necesitan interactuar con nuestro software.

Los tests son una forma viva de documentación, que nos habla no solo de como funciona el código, sino también cómo se usa.

En los sistemas distribuidos con comunicación basada en eventos y APIs, es necesario proporcionar documentación.

En cualquier caso, lo que nos dice este valor del Manifiesto es que nuestro objetivo es poner el software en las manos de las usuarias. Y esto es lo que debería constituir la famosa _Definition of Done_. 


