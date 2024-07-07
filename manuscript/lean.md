# L de Lean Software Development

El framework de Lean Software Development es una adaptación del método Lean Manufacturing que, a su vez, se inspira en el Toyota Production System (TPS). Este sistema fue creado en los años 50 del siglo XX, para optimizar el proceso de producción industrial. Si hubiese que resumirlo en unas pocas frases podríamos decir que el TPS consiste en producir lo necesario, consumiendo lo justo y no gastar en lo que no necesitamos. Es una gran simplificación, pero condensa la idea principal, y hay que entenderlo en el contexto de la reconstrucción de Japón tras la Segunda Guerra Mundial.

La adaptación de estas ideas al desarrollo de software vino de la mano de Mary y Tom Poppendieck, concretado en su libro fundacional _Lean Software Development: An Agile Toolkit_. Este framework se basa en los siguientes principios:

**Eliminar el desperdicio**. Todo lo que no agregue valor al cliente es desperdicio y debe eliminarse. Esto se traduce, por ejemplo, en no desarrollar nada más que lo que se necesita, evitando buscar anticiparse a un futuro que no conocemos. Por tanto, es necesario aprender a discernir lo que es necesario de lo que no.

Desperdicio, en el ámbito Lean, abarca varias cosas. No desarrollar prestaciones innecesarias, es una de ellas. El trabajo terminado parcialmente es otra, lo que nos llevaría a utilizar diversas prácticas técnicas como adoptar Trunk Based Development, evitando ramas de código que vivan más allá de unas horas; TDD _outside-in_ para añadir solo el código necesario con buena calidad y otras relacionadas.

También es desperdicio cuando un equipo tiene que hacer multitarea y se tiene un nivel de trabajo en progreso alto. Cuando se emprenden tareas de gran incertidumbre, o cuando las historias de usuario se dividen horizontalmente, generando dependencias y esperas.

**Calidad desde el inicio**. La calidad en el desarrollo del software tiene que estar presente desde el primer momento. No se puede esperar, pues eso genera deuda técnica y, por lo tanto, desperdicio en el futuro.

En ese sentido, los equipos que hacen Lean Software Development, suelen usar las prácticas técnicas ágiles que caracterizan Extreme Programming: TDD, Ensemble programming, Merciless Refactoring, etc.

**Crear conocimiento**. El desarrollo de software es un proceso de aprendizaje constante, tanto de lo que el cliente necesita como de lo que no necesita. Para ello son fundamentales los ciclos de feedback y una buena comunicación.

**Retrasar decisiones**: Los equipos tienen que retrasar decisiones en lo posible para mantener flexibilidad y adaptarse a los posibles cambios. 

La idea es no empezar el desarrollo pensando en detalles como una tecnología concreta que podríamos llegar a necesitar, sino desarrollando la funcionalidad con el recurso más barato y fácil de cambiar posible, que me comprometa menos. Si llegado el caso, vemos que necesitamos una tecnología específica, siempre podremos adoptarla con la ventaja de tomar una decisión informada.

Para ello es útil definir límites de producto, que serían valores fijos de ciertos parámetros. Se desarrolla una solución sencilla que funcione dentro de esos límites y si llegado un momento se superan o se alcanza un cierto umbral de seguridad, nos planteamos una solución más potente.

Por ejemplo, si tenemos un servicio en que las usuarias suben documentos a un almacenamiento, podríamos poner un límite de tamaño de esos documentos, o de espacio total por usuaria, que nos permitan usar una solución barata que tal vez tenemos fácilmente disponible. Si con el tiempo vemos que se supera ese límite con demasiada frecuencia, es cuando podemos empezar a pensar en una alternativa de más capacidad. En estos casos es bueno definir también un umbral a partir del cual sí tenemos que plantear como mejorar esa prestación.

**Entregar rápido**: En otros capítulos hemos hablado de la necesidad de hacer entregas de valor frecuentes que hagan posible tener feedback cuanto antes, lo que nos facilita decidir nuestros siguientes pasos.

Para facilitar la entrega rápida se usa el Vertical Slicing, una técnica para decidir las iteraciones de una historia de usuario, de forma que cada una de ellas nos permita entregar valor. Pero también, se añaden prácticas como Trunk Based Development, Ensemble programming, etc., que permite reducir el tiempo de desarrollo, revisión de código y esperas.

**Respetar a las personas**: Se busca generar un ambiente de respeto y colaboración, independientemente de roles o experiencia, que permita a cada persona del equipo contribuir al éxito y aprender sobre el producto y el propio proceso de desarrollo.

También es necesario que los equipos como tales estén _empoderados_, o sea, que tengan la capacidad de decidir qué hacen y cómo lo hacen. Para ello, tienen que contar con las capacidades y conocimientos necesarios, lo que evita las dependencias y las esperas, que son una de las formas de desperdicio. 

**Visión de conjunto**: El proceso de desarrollo se ha de considerar en su totalidad. El producto es algo más que la simple suma de las partes.

Lean Software Development, es un _framework_ muy alineado con _Extreme Programming_, con el que comparte muchas ideas. Aparte del libro original, puedes aprender más en la web de [Emilio Ferro](https://www.eferro.net/)
