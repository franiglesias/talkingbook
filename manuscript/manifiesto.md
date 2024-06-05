# M de Manifiesto Agile

El Manifiesto por el Desarrollo Ágil de Software fue creado en 2001 por un grupo de 17 señores programadores reunidos en un resort de ski en Utah. Representaban diversas metodologías alternativas para el desarrollo de software y su objetivo era tratar de acordar una serie de elementos comunes, a pesar de las diferentes aproximaciones que traían de partida. 



## Introducción

El manifiesto comienza con la siguiente introducción:

> Estamos descubriendo formas mejores de desarrollar software tanto por nuestra propia experiencia como ayudando a terceros. A través de este trabajo hemos aprendido a valorar:

##  Valores

A continuación se enumeran los cuatro valores del agilismo:

* Individuos e interacciones sobre procesos y herramientas
* Software funcionando sobre documentación extensiva
* Colaboración con el cliente sobre negociación contractual
* Respuesta ante el cambio sobre seguir un plan

Y se hace una aclaración importante:

> Esto es, aunque valoramos los elementos de la derecha, valoramos más los de la izquierda.

En otras palabras: el hecho de valorar más unos elementos sobre otros, no implica su negación. Es decir: procesos y herramientas son importantes, pero subordinados a los individuos. Es necesaria la documentación, pero valoramos más la entrega de software funcional. Tiene que haber una negociación de contratos con el cliente, pero en último término es esencial desarrollar una colaboración productiva con él. Y, por último, se necesita un plan y saber qué se quiere conseguir, pero es más importante ser capaz de responder al cambio.

## Principios

Los valores ágiles generan un conjunto de principios:

> Nuestra mayor prioridad es satisfacer al cliente mediante la entrega temprana y continua de software con valor.

Cuando hablamos de entrega de valor, estamos hablando siempre de valor de negocio. Lo que importa no el código, sino la funcionalidad que habilita para el cliente.

> Aceptamos que los requisitos cambien, incluso en etapas tardías del desarrollo. Los procesos Ágiles aprovechan el cambio para proporcionar ventaja competitiva al cliente.

Bajo este principio subyace la idea de que el cambio es necesario para adaptarse al mercado del negocio del cliente. Si el producto no funciona, el producto tiene que cambiar. Si el mercado se mueve en una dirección, el producto debe seguirla.

> Entregamos software funcional frecuentemente, entre dos semanas y dos meses, con preferencia al periodo de tiempo más corto posible.

La entrega frecuente es fundamental para que el cliente pueda pivotar de forma eficaz. Cuanto más tiempo tarda el software en estar funcionando, más difícil es entender si va en la dirección correcta o debe cambiar.

> Los responsables de negocio y los desarrolladores trabajamos juntos de forma cotidiana durante todo el proyecto.



> Los proyectos se desarrollan en torno a individuos motivados. Hay que darles el entorno y el apoyo que necesitan, y confiarles la ejecución del trabajo.



> El método más eficiente y efectivo de comunicar información al equipo de desarrollo y entre sus miembros es la conversación cara a cara.



> El software funcionando es la medida principal de progreso.



> Los procesos Ágiles promueven el desarrollo sostenible. Los promotores, desarrolladores y usuarios debemos ser capaces de mantener un ritmo constante de forma indefinida.

La idea de mantener un ritmo constante de forma indefinida puede sonar un poco ominosa. Pero es uno de los principios que se suele interpretar mal. Cuando decimos ritmo constante, no hablamos de velocidad, sino de la capacidad de entregar valor de una manera regular y, hasta cierto punto, predecible. 

El equipo de desarrollo no debería luchar contra un sistema difícil de descifrar. El código tiene que expresar claramente las intenciones, los lugares donde extenderlo, etc. Debería ser sencillo identificar qué cambios introducir para añadir valor.

> La atención continua a la excelencia técnica y al buen diseño mejora la Agilidad.

Para ser ágiles tenemos que escribir software bien diseñado. Y para escribir software bien diseñado necesitamos dominar toda una serie de técnicas y conocimientos. La verdad es que esto es algo que no siempre es bien entendido. Todas hemos escuchado alguna vez la idea de que no importa empezar con una solución chapucera que se pueda sacar rápidamente y ya tendremos tiempo de arreglarla. Esto no es lo que dice Agile. En su lugar, Agile dice empezar con una solución simple, pero bien hecha.

Los atajos cortos suelen traer retrasos largos. Muchos equipos acaban reescribiendo un mismo producto una o más veces desde cero. Tanto porque la solución anterior estaba mal escrita, como por carecer de habilidades de refactor, testing y diseño de software. Lo que a veces denominados las prácticas técnicas ágiles.

Reescribir productos desde cero es una táctica arriesgada y cara. Hay que reproducir toda la funcionalidad del sistema original y realizar las migraciones necesarias, lo que puede dar lugar a pérdida de datos, _downtime_ o tiempo sin funcionalidad. En muchísimos casos tener personas capaces de aplicar técnicas de refactoring progresivo hubiese permitido minimizar el riesgo del cambio, sin generar tiempos muertos.

> La simplicidad, o el arte de maximizar la cantidad de trabajo no realizado, es esencial.

Maximizar es un principio extraño, uno que no se capta a la primera tras leer su formulación. Intenta capturar una idea muy potente en una frase ingeniosa y breve. Nosotras podemos entenderla en dos formas principales:

* _Optar por las soluciones más simples que puedan funcionar_, que suena como una propuesta deseable.
* _Evitar tener que realizar la mayor cantidad posible de trabajo_, que suena contra la intuición.

Buscar las soluciones más simples posibles que puedan funcionar promueve escribir el software justo y necesario para resolver la demanda que tenemos ahora. Entre otras cosas, supone evitar en lo posible el sobre-diseño. Es decir, nos pide evitar añadir complejidad para abordar cuestiones que podrían llegar en el futuro. El caso es que como no podemos predecir el futuro, es mejor no adelantarse. Si nuestro software necesita añadir complejidad en algún momento, lo haremos cuando sea necesario.

Para ello, además de simple, el software tiene que ser fácil de cambiar. Si bien, no podemos predecir los acontecimientos del futuro, podemos hacer algunas suposiciones razonables sobre el mismo. Por ejemplo, podemos suponer que una tienda on-line querrá ofrecer diversas formas de pago, por lo que es bueno dotar al sistema de cierta flexibilidad para incorporarlos en el futuro con facilidad y seguridad. Sin embargo, los medios de pago requieren negociaciones, análisis de su demanda, etc., para poder usarlos, por lo que es preferible evitar implementaciones concretas de los mismos hasta no tener claro que los necesitamos.

Por otro lado, no hay mejor trabajo que aquel que no hay que realizar. Esto nos puede llevar a pensar en la necesidad de automatizar cuantos más procesos rutinarios, mejor.

> Las mejores arquitecturas, requisitos y diseños emergen de equipos auto-organizados.

Un punto muy importante del manifiesto Agile es que no existe una metodología Agile. Disponemos de diversos frameworks que comparten esta filosofía y establecen unas pautas metodológicas concretas. Pero la forma más genuina de ser Agile es que cada equipo decida cuál es la forma en la que trabaja mejor, que más encaja en su producto y sus personas.

Esto quiere decir que incluso en una misma empresa lo lógico sería que cada equipo de trabajo se auto-organice, sin necesidad de seguir un determinado framework común.

> A intervalos regulares el equipo reflexiona sobre cómo ser más efectivo para a continuación ajustar y perfeccionar su comportamiento en consecuencia.

Yo diría que esta es la única prescripción concreta que propone el Manifiesto. Esta reflexión es la que solemos denominar retrospectiva y su único objetivo es evaluar y reconducir el proceso que el equipo sigue para ser más eficiente y trabajar mejor.

## Las críticas a Agile

Se han publicado muchas críticas al movimiento Agile, algunas de ellas son incluso buenas críticas. Por desgracia, muchas de las que se pueden leer se equivocan en aspectos muy fundamentales. Por ejemplo, son frecuentes las críticas que en realidad se dirigen a frameworks concretos, particularmente a Scrum. Y lo curioso es que, en ocasiones esas mismas críticas son compatibles con el Manifiesto Agile. También es cierto que muchas críticas obvian que el Manifiesto habla del desarrollo de software específicamente, no del desarrollo de producto o de negocio.

De hecho, gran parte de la crítica más sólida a Agile viene de las propias _agilistas_. Por ejemplo, esta cita del _Blog de un apostol de Scrum y Kanban_:

> Otra versión del Manifiesto Ágil revisada que me gusta es la de Alexey Krivitky: "Después de 20 años tratando de entender y explicar el Manifiesto Ágil he llegado a esta versión simplificada que parece entregar el mensaje con menos palabras".
> 
> * Personas sobre procesos
> * Producto sobre especulaciones
> * Cocreación sobre política
> * Realidad sobre planes
> 
> https://scrum.menzinsky.com/2019/07/el-manifiesto-agil-deberia-de.html

Es muy interesante porque, siendo totalmente fiel a la intención del Manifiesto, resulta mucho más precisa y accionable que el original.

También podemos ver como una crítica en la línea Agile el _Manifiesto por la Artesanía de software_, que reza así:

> Como aspirantes a Artesanos del Software estamos elevando el listón de desarrollo de software profesional practicando y ayudando a otros a aprender el oficio. A través de este trabajo hemos llegado a valorar:
>
> * No solo software que funciona, sino también software bien diseñado
> * No solo responder al cambio, sino también agregar valor constantemente
> * No solo individuos e interacciones, sino también una comunidad de profesionales
> * No solo colaboración de clientes, sino también asociaciones productivas
> 
> Es decir, en la búsqueda de los elementos de la izquierda, hemos encontrado indispensables los elementos de la derecha.

También podemos ver que completa y extiende la definición de cada uno de los cuatro valores.

El mismísimo Kent Beck propuso en 2011 una revisión del Manifiesto:

> * Visión y disciplina de equipo, por encima de individuos y su interacción
> * Aprendizaje validado, por encima de software que funciona
> * Descubrimiento con el cliente, por encima de la colaboración con el cliente
> * Iniciar el cambio, por encima la respuesta al cambio
> 
> https://www.forbes.com/sites/stevedenning/2011/05/04/innovation-applying-inspect-adapt-to-the-agile-manifesto/

Se puede apreciar en todas estas nuevas formulaciones una tendencia: no se trata de negar el Manifiesto, sino de seguir profundizando en la visión ágil del desarrollo de software. Al fin y al cabo, una de las principales ideas de Agile es justamente la revisión contínua, así que tiene mucho sentido que no consideremos el Manifiesto Agile como las tablas de la Ley, sino como una filosofía en progreso y definición constante.
