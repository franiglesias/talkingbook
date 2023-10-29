# Técnica (Deuda)

La idea de la deuda técnica es una metáfora usada por Ward Cunningham para explicar la refactorización de un producto financiero llamado WyCash. Seguramente, el hecho de estar trabajando en un dominio de este tipo facilitó el uso de esta analogía del mundo de las finanzas. 

http://wiki.c2.com/?WardExplainsDebtMetaphor

La intención de Cunningham con la reescritura era reflejar el conocimiento que iban ganando sobre el producto a medida que se desarrollaba y se usaba. Es decir, se percibía una diferencia entre el conocimiento de negocio que se reflejaba en el código en producción y el conocimiento de negocio que el equipo tenía. El objetivo, por tanto, era alinear el código con ese conocimiento, para lo cual deberían refactorizarlo regularmente. En esencia, se trata de aprovechar la maleabilidad del software.

La razón para hacerlo era evitar que en el futuro la discrepancia se hiciese tan grande que llegase a ralentizar el desarrollo del producto. Esa ralentización, siguiendo la metáfora, equivaldría al pago de intereses de un préstamo.

Pero, ¿cuál es el préstamo? La deuda se origina cuando se pone en producción un código de forma temprana para poder aprender sobre él. Dicho en otras palabras: es cuando lanzamos una funcionalidad de un producto, pero nuestro conocimiento sobre ese aspecto del negocio es todavía tosco e impreciso. El feedback y la experiencia nos ayudan a refinar ese modelo mental del negocio que tenemos como equipo. Lanzar el producto de forma temprana nos permite adquirir conocimiento que tardaríamos mucho en lograr por otros medios y así entender por dónde deberíamos seguir avanzando.

Pero todo préstamo tiene que devolverse. La forma de pagar la deuda técnica es refactorizar el código para reflejar el conocimiento adquirido. Debería resultar bastante claro que seguramente prefiramos pagar en pequeñas cuotas aunque sean frecuentes, que encontramos en un momento dado teniendo que pagar capital e intereses de golpe. Esto es: aplicar el refactor de forma activa y constante en cada oportunidad que tengamos.

## La deuda técnica como justificación de malas decisiones

La metáfora original interpreta la deuda como falta de conocimiento o falta de articulación del conocimiento. Se incurre en deuda porque carecemos del conocimiento suficiente, así que pedimos prestado ese conocimiento publicando un software. Es una acción deliberada y el pago se formalizará en forma de refactoring para recoger ese conocimiento que hemos pedido prestado.

**Deuda técnica como decisión entre opciones**. En muchos artículos sobre deuda técnica se plantea la idea de que los equipos de desarrollo incurren en la deuda tomando una decisión entre salir pronto a producción (arreglando después) o salir bien construído. Este enfoque me parece erróneo y refleja otro tipo de problemas.

¿Qué queremos decir con que tenemos dos opciones? ¿Quiere decir que tenemos dos versiones de ese conocimiento, una incompleta y otra completa? ¿Qué sentido tiene no poner nuestra mejor versión del conocimiento que tenemos en el código?

En la práctica eso se suele traducir en algo por el estilo de: lancemos una versión del producto armado con un framework de desarrollo rápido, representando nuestro conocimiento de manera defectuosa por las limitaciones del propio framework, para empezar a obtener feedback y refactoricemos a una arquitectura razonable en un futuro indefinido.

**Escribir mal código pero rápido**. Uno de los errores más graves que se cometen con la cuestión de la deuda técnica es pensar que es correcto poner cualquier porquería de código en producción con la idea de arreglarlo en el futuro. Pues nada de eso. El propio Cunningham alerta sobre ello:

> No estoy nunca a favor de escribir código pobremente, pero estoy a favor de escribir código para reflejar tu entendimiento actual de un problema, incluso si esa comprensión es parcial. 

Y abunda:

> En otras palabras, la metáfora de la deuda en sí, digamos, la capacidad de devolver la deuda, y hacer que la metáfora trabaje a tu favor depende de que escribas código que sea lo bastante limpio para poder refactorizarlo a medida que vas entendiendo tu problema.

Es decir, lo que la metáfora de la deuda promueve es: está bien tener una idea de negocio modelada en el código y ponerla en producción, aunque sea incompleta, pero ese código debe reflejar correctamente el conocimiento que tienes en ese momento. A medida que adquieres nuevo conocimiento, refléjalo activamente en el código.

Escribir mal código es como suscribir un préstamo y gastar más dinero del que has pedido.

**No reflejar el aprendizaje en el código**. Los equipos que no refactorizan su código para reflejar el conocimiento que adquieren están pidiendo un préstamo que piensan que nunca van a tener que pagar.

El propósito del refactor como pago de la deuda técnica es asegurar que el conocimiento reflejado en el código es una representación lo más exacta posible del conocimiento que tiene el equipo sobre el negocio. De este modo, cuando se produzcan cambios, el código estará mejor preparado para incorporarlos de forma rápida y efectiva.

Si el conocimiento en el código tiene un gran desfase con el conocimiento del equipo, cada nueva prestación o cada cambio será más difícil de incorporar y el desarrollo se hará más lento. Es entonces cuando los intereses se convierten en una carga.



