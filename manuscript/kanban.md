# K de Kanban

Kanban es el framework Agile que probablemente no sabes que estás usando. O bueno, al menos es casi seguro que estarás usando uno de sus artefactos característicos: el tablero Kanban. La metodología nació en Toyota, creada a finales de los años 40 del siglo XX por el ingeniero Taiichi Ōno, como parte de la gestión de stocks. Básicamente, se trataba de sincronizar la producción con la demanda real.

Este modelo se ha aplicado como metodología para la gestión de proyectos de desarrollo de software.

En tablero Kanban permite visualizar el estado de un proyecto mediante tarjetas que describen tareas individuales o _work items_ organizadas en un sistema de columnas que muestran su estado. En el modelo más básico los estados son:

* **To-do**: lo que queremos hacer en algún momento en el futuro.
* **Doing**: lo que estamos haciendo ahora mismo.
* **Done**: lo que ya está completado.

Sin embargo, es frecuente que existan más estados en el tablero. Esto depende, en parte, de la _resolución_ con que se quiera examinar el proceso. Por ejemplo, podríamos tener columnas para _Testing_, para _Deployment_, etc. Y hemos visto algunos tableros con tantas columnas que resulta difícil entender para qué sirve cada uno.

Estos estados se representan de izquierda a derecha, de modo que cada tarjeta comienza en la columna _To-do_ y se mueve hacia la derecha, a la columna _Doing_, cuando nos ponemos a trabajar en ella. Una vez terminada, la volvemos a mover hacia la derecha para situarla en la columna _Done_ y, ojalá, poder olvidarnos de ellas.

Un punto muy importante de Kanban es definir límites del trabajo en progreso. En cada columna se pueden poner un máximo de _work items_ simultáneos. El objetivo de esto es favorecer el foco y la asignación de recursos: si un _work item_ está en una columna de _Doing_ quiere decir que se está trabajando en él. Si una columna está llena, los items en las columnas a la izquierda no se pueden mover. Esto sería señal de que quizá necesitamos más recursos para hacer avanzar los items en la columna llena. O, simplemente, que debemos priorizar el trabajo en los items de esa columna.

En cualquier caso, nos está diciendo que tenemos un problema y que debemos hacer algo para abordar esa situación.

## Limita tu trabajo en curso para reducir tus obstáculos

Para algunas personas limitar el trabajo en progreso puede parecer contra productivo. Sin embargo, es todo lo contrario, ya que nos ayuda a establecer un flujo sostenible y constante, además de identificar cuellos de botella. Esto conecta el uso de Kanban con la teoría de _constraints_ o limitadores. Esta teoría dice que un equipo que no consigue sus objetivos suele estar limitado por un conjunto reducido de obstáculos. Se trataría, pues, de identificar estos obstáculos y tomar medidas para abordarlo, que se agrupan en tres tipos:

* **Exprimir**: Centrar todos los esfuerzos en resolver la limitación, añadiendo recursos o personas, y pospón otros _work items_. Se trata de salir del problema cuanto antes.
* **Subordinar**: Asegurar que otros procesos puedan contribuir a reducir el cuello de botella.
* **Elevar**: Hacer cambios en el sistema para eliminar o reducir la limitación.

En muchos equipos que se quedan atascados en un proyecto, nos hemos encontrado con que se quejan de que les falta tiempo o que tienen que atender múltiples focos. Ambas señales apuntan a un problema de gestión del trabajo en curso.


