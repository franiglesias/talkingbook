# P de Prácticas Técnicas

Las prácticas técnicas ágiles son una de las grandes olvidadas en los equipos de tecnología. "¿Y qué eso?", preguntarán muchas personas.

Las prácticas técnicas ágiles son un conjunto de destrezas y procedimientos que se aplican en el proceso de desarrollo de software y cuyo objetivo es mejorarlo en todas sus fases. Hay que tener en cuenta que en los equipos de desarrollo ágiles, las fases de diseño, especificación, implementación, pruebas y mantenimiento, se condensan en un espacio de tiempo y en un ámbito muy delimitado del proyecto: la historia de usuario, e incluso se pueden superponer en el tiempo.

Las prácticas técnicas nos permiten realizar una aproximación intencionada y metódica al desarrollo de software. La programación se percibe a veces como el producto de una especie de inspiración y, sin embargo, es necesario cultivar una serie de técnicas mediante las cuales escribir software de una forma eficiente.

Pedro Moreira Santos, Marco Consolaro y Alessandro Di Gioia, en su libro Agile Technical Practices Distilled, señalan cuatro prácticas técnicas fundamentales: TDD, pair programming, refactoring y diseño simple.

## Pair programming

Pair programming es la práctica de trabajar dos personas (o más si se trata de mob-programming) con el objetivo de obtener software de calidad gracias al feedback inmediato. Al trabajar con otra persona esta nos puede ayudar a identificar problemas potenciales, ofrecernos aproximaciones alternativas, discutir y refinar conceptos, etc. Un beneficio extra de pair programming es que contribuye a que el conocimiento se distribuya de forma fluida entre los miembros del equipo.

En pair programming cada persona adopta un rol:

* **Driver**: es la persona que escribe el código en un momento dado.
* **Navigator**: responsable de revisar el código desde un punto de vista estratégico.

Existen varios formatos de trabajo en pair programming y técnicas para repartir los roles en una misma sesión.

* **Chess clock**: los roles se intercambian en un tiempo prefijado, o bien si hay una pausa natural en el proceso. Para eso puede ayudar la técnica Pomodoro.
* **Ping-pong** (combinada con TDD): una persona escribe un test que falle y pasa el rol de driver a la otra. Esta escribe el código para pasar el test y un nuevo test que falle, pasando de nuevo el driver.
* **Strong-style**: la persona que hace de _driver_ tiene que confiar en lo que le indica la que hace de _navigator_. Puede hacer preguntas para aclarar lo que quiere hacer, pero el debate acerca de por qué debe suceder al final.

Las sesiones de pair programming pueden ser bastante fatigosas por lo que es importante utilizar herramientas para delimitar el tiempo y tener descansos. Para ello, la técnica Pomodoro puede ser muy útil.

Mob programming es un concepto similar, pero en lugar de ser dos personas, puede participar todo el equipo. Incluso personas externas si puede resultar útil. Las personas pueden entrar y salir de la sesión de mob programming libremente y contribuir a la discusión, mientras que alguien se encarga de escribir el código.

## Test Driven Development

Test Driven Development (TDD) es una práctica técnica en la que definimos las especificaciones de un software mediante tests creados a partir de ejemplos del comportamiento deseado. El código de producción se escribe con el objetivo de hacer pasar esos tests.

Para empezar, escribimos una lista de todos los elementos de funcionalidad que queremos conseguir. Esta lista no es definitiva, pues podríamos darnos cuenta tanto de nuevas necesidades durante el desarrollo, como descubrir que algunas no las necesitamos, o al menos no como las habíamos definido.

Sin embargo, TDD no es escribir previamente la totalidad de especificaciones en forma de tests, sino que procedemos una por una. Es decir, escogemos un elemento de la lista, y escribimos un test que sea un ejemplo del mismo. A continuación, escribimos el código de producción justo y necesario para hacer pasar ese test.

Una vez conseguido, añadimos un nuevo ejemplo en forma de test que falle. Es decir, que el código de producción actual no sea capaz de hacerlo pasar. Cuando tenemos este test y vemos que falla por la razón adecuada, añadimos el código necesario para que este segundo test pase, a la vez que pasa el anterior también.

Una vez que hemos hecho pasar el último test, podemos revisar el código de producción para ver si es posible organizarlo mejor. Por ejemplo, identificando alguna regularidad del código que nos permita generalizar. Si es así, realizamos el cambio. Si no, pasamos al siguiente elemento de la lista, o introducimos un nuevo ejemplo para completar el que estemos trabajando.

Cada vez que introducimos código de producción para hacer pasar un test, debemos evitar que los tests anteriores fallen. De este modo, nos aseguramos de mantener la funcionalidad que ya hubiésemos conseguido implementar.

Cuando tenemos todos los tests pasando, podemos aplicar técnicas de refactoring a fin de mejorar la organización o diseño del código de producción.

Es importante no confundir Test Driven Development con Test de Quality Assurance. Ambas disciplinas usan las mismas herramientas, pero sus objetivos son diferentes. Sin embargo, el software escrito con TDD aporta varias cosas. Entre ellas:

* Una batería de tests de regresión, que será útil en QA, aunque no todos los test de TDD son significativos para QA.
* Un diseño de software más fácil de poner bajo tests.

## Refactoring

Refactoring es un término muy abusado, que se aplica a cualquier proceso en el que cambiamos o reescribimos software. Pero en el ámbito de las prácticas técnicas ágiles, refactoring es un conjunto de técnicas que nos permite transformar el diseño de un código sin afectar a su comportamiento. El refactoring contribuye al buen diseño, el cual, a su vez, favorece la sostenibilidad a largo plazo del software y reduce el coste del cambio futuro.

Las técnicas de refactoring nos permiten cambiar un código sin interrumpir su funcionamiento ni detener su desarrollo. Una forma de asegurar esto, es tener tests que cubran la parte de código modificado. Un refactoring correctamente aplicado no hará fallar los tests en ningún momento.

De hecho, los mejores entornos de desarrollo incluyen numerosas herramientas que automatizan algunas de las técnicas específicas. Esto garantiza que los cambios sean inocuos y no afectan al comportamiento de tal modo que ni siquiera necesitaríamos verificarlo con tests. A este tipo de refactors se les suele llamar provable refactors, porque se ha verificado que aplicados correctamente no alteran la funcionalidad del software.

Los refactors son los cambios específicos que podemos aplicar. Pueden ser tan simples como cambiar el nombre de un símbolo en el código, como una variable o una función; o tan complejos como convertir una estructura condicional en un conjunto de objetos polimórficos.

Para aplicar refactor es importante aprender a identificar señales en el código que nos indiquen un problema potencial de diseño. A estas señales las denominamos _code smells_. Los _code smells_ no son errores, pues el software no funciona mal, sino patrones de código que nos indicarían que algo podría tener un mejor diseño o que, llegado el momento, podría ser costoso entenderlo o cambiarlo.

Asi, por ejemplo, si tenemos dos variables que siempre van juntas (se pasan juntas a funciones, se asignan a la vez, se actualizan o recalculan a la vez, etc.) tenemos un smell llamado _Data Clump_ y lo que este nos dice es que probablemente esas variables representan un único concepto, que estaría mejor reflejado en forma de objeto o de otra estructura de datos adecuada al lenguaje de programación.

## Diseño simple

Las prácticas técnicas anteriores no sirven de mucho si no entendemos el diseño, en particular, lo que hace que un diseño sea simple. Kent Beck definió las siguientes reglas para ello. El código simple:

* Pasa sus tests: hace lo que dice.
* Minimiza la duplicación: define una fuente de verdad para cada pieza de funcionalidad.
* Maximiza la claridad: dice lo que hace.
* Usa la menor cantidad de elementos posibles: reduce 

### Calistenia

La calistenia es una serie de reglas que cumplir cuando diseñamos software. En líneas generales, estas reglas nos indican ciertos patrones que debemos aplicar y son totalmente independientes de la finalidad del código. 

Por ejemplo: mantener un solo nivel de indentación en cada bloque de código es una regla que podemos detectar fácilmente cuando la incumplimos. Para aplicarla, normalmente lo que haremos será extraer los fragmentos de código más internos a métodos o funciones con nombres descriptivos. Se generan varios beneficios:

* Cada uno de esos métodos o funciones será muy simple.
* Los distintos niveles de abstracción del código quedarán bien identificados y aislados.
* Será más fácil entender qué hace el código, pudiendo leerlo de forma general o descendiendo a los detalles si fuese necesario.
* Incluso podríamos identificar partes del código duplicadas o que podrían extraerse a otros objetos.

Podemos aplicar las reglas de calistenia en ejercicios de práctica deliberada a fin de educar nuestro sentido del diseño o bien intentar refactorizar nuestro código de producción con ellas como objetivo.

### Acoplamiento vs. Cohesión

### Connascence

El término Connascence intenta unificar las ideas de acoplamiento y cohesión de una forma más sistemática. Se dice que dos o más elementos de un sistema de software son _connascentes_ si el cambio de un elemento conlleva el cambio de otros. Tiene tres dimensiones:

* Grado: es la cantidad de elementos que tienen que cambiar simultáneamente, cuanto más reducido más aceptable.
* Localidad: es la cercanía entre los elementos que cambian. Así, por ejemplo, sería aceptable si los elementos cambian el ámbito de una función, pero no sí cambian entre distintas entidades
* Fuerza: se refiere a la probabilidad de necesitar cambios en los elementos _connascentes_ y el esfuerzo que supone.

### Patrones

Los patrones de diseño describen problemas comunes del desarrollo de software junto con soluciones probadas. Por supuesto, aquí hay que citar el libro fundacional de The Gang of Four.

Es muy importante tener presente que un patrón de diseño no es una receta para aplicar ciegamente. El patrón tiene dos elementos y no tiene sentido que tengamos en cuenta uno solo de ellos.

El primer elemento es el problema. Un patrón de diseño describe un problema común que puede presentarse en cualquier proyecto de software. Por ejemplo: cómo añadir un número indefinido de funcionalidades a un objeto en tiempo de ejecución.

El segundo elemento es una propuesta de solución de ese problema que ha sido probada. Así, para el ejemplo anterior, una solución es envolver el objeto en otro (u otros) que implemente la misma interfaz, interceptando y modificando (decorando) su _output_. Este par concreto de problema y solución es conocido como _Decorador_.

La implementación que se describe en el patrón no es una receta, sino una guía. Esta implementación puede depender del lenguaje en que estemos trabajando y de la complejidad del propio problema.

Se han identificado infinidad de patrones, que se pueden clasificar en:

* Creacionales: nos ayudan a resolver problemas en la creación de objetos.
* Comportamentales: nos ayudan a resolver problemas en la comunicación entre objetos.
* Estructurales: reducir la complejidad del diseño de objetos mediante la composición.

### Principios

Los principios de diseño de software son guías para tomar decisiones. No son normas escritas en piedra, pero tampoco son ocurrencias. La idea es que los tomemos en consideración para valorar si un software está bien escrito y es sostenible en el tiempo. Por lo general, si seguimos principios de diseño, el código tenderá a ser fácil de entender y de mantener.

Los principios pueden ayudarnos a decidir donde poner ciertas estructuras y comportamientos en su sistema de software. Esto es lo que nos proporcionan los llamados Principios o Patrones GRASP.

Los principios SOLID, por otro lado, están orientados a ayudarnos a diseñar software con bajo acoplamiento.

Pero existen muchos otros.

En ocasiones, podemos sentir que algunos principios se oponen o entorpecen a otros, por así decir. Como decíamos antes, los principios de diseño son criterios para tomar decisiones, no son leyes. En ocasiones, nos convendrá darle más peso a unos que otros. El diseño consiste en decidir qué compromisos estamos dispuestas a aceptar.
