# Q de Quality Assurance

El modelo _agilista_ cuestiona la gestión de proyectos basada en etapas separadas como el modelo en cascada o _waterfall_. En este tipo de metodologías, por lo general, las fases deben transcurrir en su totalidad de forma secuencial y separada. Típicamente, estas fases son:

* Toma de requerimientos
* Diseño
* Implementación
* Pruebas
* Mantenimiento

La fase de pruebas es la que solemos asociar a Quality Assurance y al personal dedicado a testing. Pero esto es una simplificación. Sin embargo, ilustra un problema que es frecuente en el mundo de desarrollo de software: el peligro de los compartimentos estancos entre distintas especialidades en el proyecto.

El cambio que proponen los frameworks ágiles al respecto de estas fases las resitúa. El proyecto se considera un trabajo iterativo e incremental, donde cada incremento de valor se completa integrando todas las fases entre ellas, pero sobre un ámbito muy pequeño. Existe toma de requisitos, pero se prefiere expresarla mediante tests. Existe una fase de diseño, que se ejecuta antes y durante el desarrollo. Por supuesto, existe la fase de implementación. Y la de mantenimiento es permanente durante la vida del proyecto. ¿Y las pruebas? Por supuesto, también están presentes, pero no queremos que exista una fase que detenga la entrega de valor.

Por esa razón, en muchos equipos ágiles no existe o se ha redefinido la figura de Tester o QA. No siempre para bien.

Como hemos mencionado en otros momentos, un equipo ágil debe ser autónomo en el sentido de poseer todas las capacidades necesarias para realizar su trabajo. Eso incluye la _Quality Assurance_, o sea, asegurarse de que está construyendo correctamente el producto correcto. Y como otras capacidades, no implica necesariamente que existe la figura especialista que hace un trabajo separado del resto del equipo.

En cualquier caso, la calidad debería estar presente desde el inicio de todo el proceso, incluyendo el diseño. Dado que vamos a construir este producto de esta manera... ¿Cómo vamos a saber que lo estamos haciendo bien?

Si bien las desarrolladoras del equipo deben saber escribir tests, puede que necesiten ayuda para escribir buenos tests y que sean los adecuados. Dicho esto, QA no es solo poner tests en un proyecto de código. Ni mucho menos. Y esto es algo que muchos equipos nos han entendido bien.

Para empezar, la calidad se refiere globalmente al producto y no únicamente al software que lo hace posible. Hay muchas empresas que hacen software y limitan el equipo de QA solo a ese ámbito, pero no entienden la calidad de forma holística. Que el software funcione bien es importante y disponer de un plan de testing para verificarlo, también, pero no sirve de nada si el producto es una porquería.

Ciñéndonos solo a la parte de software, desde el punto de vista ágil, deben quedar claro dos puntos:

* Agilidad no es lanzar software de mala calidad para probar ideas de negocio, con la esperanza de arreglarlo en el futuro. En realidad, agilidad es construir productos de software de alta calidad que nacen simples (con pocas prestaciones, dirigidos a un público definido) y crecen en complejidad a medida que las hipótesis de negocio se confirman.
* El proceso de _Quality Assurance_ no debe interponerse en la capacidad de entregar valor, por lo que es necesario integrarlo en todo el desarrollo: desde el diseño a la implementación. Pero eso no es sinónimo de añadir tests al código para pasar un _pipeline_, sino integrar prácticas técnicas que nos ayudan a escribir software de calidad.

Todo esto nos debe llevar a una reflexión sobre si los equipos de desarrollo lo estamos haciendo realmente bien.

Por otro lado, en los últimos años se han ido imponiendo, con mayor o menor fortuna, arquitecturas basadas en micro-servicios que se comunican mediante API y eventos. Esto ha incrementado la dificultad de garantizar la calidad global de nuestros productos y servicios de software.

Así, diseñar sistema de calidad que permitan entender si nuestro sistema funciona como es debido se ha vuelto una tarea que excede las capacidades de los equipos. Incluso si los equipos están bien dimensionados para gestionar los micro-servicios que les corresponden, cosa que no ocurre siempre, pierden la visión de conjunto necesaria para saber como asegurar la calidad del sistema completa.

Y aquí también tenemos una oportunidad para la especialidad de QA.
