---
layout: post
title:  Modelos de Ciclo de Vida
date:   2019-06-10 18:17:20 +0300
description: Métodos para construir software confiable. # Add post description (optional)
img: whiteboard-planning.jpg # Add image post (optional)
tags: [Blog, Programming, Analisis, Sistemas]
author: Joaquin Ipar # Add name author (optional)
---
##Ciclos de Vida

Contenidos

7.1 Pure Waterfall
7.2 Code-and-Fix
7.3 Spiral
7.4 Modified Waterfalls
7-5 Evolutionary Prototyping
7.6 Staged Delivery
7.7 Design-to-Schedule
7.8 Evolutionary Delivery
7.9 Design-to-Tools
7.10 Commercial Off-the-Shelf Software
7.11 Choosing the Most Rapid Lifecycle for Your Project

##7.1 Pure Waterfall (Cascada)
Es el ciclo de vida más viejo. En el ciclo de vida de cascada, un proyecto progresa a través de una secuencia ordenada de pasos desde el concepto de software inicial a través de pruebas del sistema. El proyecto realiza una reseña al final de cada fase para determina si está listo para avanzar a la próxima fase. Si el proyecto determina que no está listo para avanzar a la próxima fase, se queda en la fase actual hasta que esté listo.
El ciclo de vida de cascada funciona con documentos, lo que significa que los productos de trabajo que van pasando por las fases son documentos.
El ciclo de visa de cascada funciona bien para ciclos de producto donde hay una definición estable del producto y se trabaja con buen entendimiento de las metodologías técnicas. Este ciclo ayuda a detectar errores en etapas tempranas (de bajo costo de tiempo) de un proyecto. 
El ciclo de vida de cascada puede ser la decisión correcta para un desarrollo rápido en situaciones como:
•	Si se está construyendo un mantenimiento bien definido de un producto existente o un port de un producto existente a una nueva plataforma.
•	Para proyectos que son bien comprendidos pero complejos, debido a que se puede beneficiar abordando la complejidad en una forma ordenada.
•	Si se trabaja con un equipo técnicamente débil o inexperto, porque dota al proyecto con una estructura que ayuda a minimizar el malgasto de tiempo y esfuerzo.
Este ciclo de vida tiene desventajas como:
•	Necesita que se especifiquen la totalidad de los requerimientos al principio del proyecto, antes de que se diseñe algo y antes de la etapa de programación.
•	El cliente puede no ser un experto en computación, y puede olvidar algo hasta que ven el producto funcionando. Si se está usando un ciclo de vida de cascada, olvidar algo puede resultar en un error muy caro, ya que recién se encontrarán en el testeo de los sistemas los requerimientos faltantes o erróneos.
•	Por lo tanto, el ciclo de vida de cascada no es flexible, lo que va en contra a las necesidades de negocios modernos, en los cuales se recompensa al desarrollador que puede implementar más funcionalidades en las últimas etapas del proyecto.
•	Para un proyecto de desarrollo rápido, el modelo de cascada tener una cantidad excesiva de documentación.
•	Genera pocas señales de progreso hasta el final del desarrollo, lo que genera una percepción de lentitud (aunque no sea verdad).

##7.2 Code-and-Fix
El modelo Code-and-Fix es raramente útil, pero es muy común. Si no se ha elegido explícitamente un ciclo de vida, probablemente se estará usando Code-and-Fix.
Cuando se utiliza Code-and-fix, se comienza con una idea general de lo que hay que construir. Con una especificación formal, o no. Por lo tanto, se utiliza cualquier combinación de diseño informal, programación, debug y metologías de testeo hasta que se considere que el producto está listo.
Este modelo tiene ventajas:
•	No tiene gastos general, no se gasta tiempo en planear, documentar, aseguración de calidad, o otras actividades que no sean programar.
•	Señales de progreso inmediato
•	Requiere muy poca experiencia, cualquiera que haya tenido experiencia con la programación puede usarlo.
Es útil para proyectos con poca vida, para demostraciones o prototipos descartables.
Para el resto de los proyectos, este modelo es peligroso. Tendrá menores gastos generales, pero no se puede asegurar el progreso. Solamente se programa hasta que se termina, no se puede asegurar calidad o identificar riesgos. Si se encuentra un error en etapas tardías, el diseño va a estar problemas fundamentales y se va a tener que empezar a diseñar desde cero.
En otros modelos, se podría detectar tal error en etapas tempranas, y sería más barato de corregirlo.

##7.3 Spiral
El modelo espiral es un ciclo de vida orientado al riesgo, que divide al software en pequeños proyectos. Cada pequeño proyecto se encarga de uno o más riesgos principales hasta que todos los riesgos se eliminen. Podemos entender a riesgo como requerimientos pobremente entendidos, arquitectura pobremente entendida, potenciales problemas de rendimiento, entre otros. Luego que los riesgos principales hayan sido solucionados, se utiliza un método de cascada.

Se empieza en pequeña escala en el medio de la espiral, explora los riesgos, y hace un plan de como contenerlos, luego avanzar a la próxima iteración. Cada iteración amplia el proyecto a una escala superior.
Cada iteración incluye seis casos, ilustrados en los bordes de la espiral.
1.	Determinar objetivos, alternativas y restricciones.
2.	Identificar y resolver riesgos.
3.	Evaluar alternativas.
4.	Desarrollar las entregas de esa iteración y verificar que sean correctas.
5.	Planear la próxima iteración.
6.	Comprometerse con un enfoque para la próxima iteración (si hay una próxima iteración)

En un modelo de espiral, las iteraciones tempranas son las más baratas. No necesariamente el proyecto debe seguir exactamente los 6 casos, es dependiente del proyecto.
Ventajas del modelo Espiral:
•	Como los costos (tiempo y dinero) aumentan, los riesgos disminuyen. Lo que cualquier proyecto de rápido desarrollo busca.
•	Este modelo da tanto control de administración como uno de cascada. Los controles a final de cada fase siguen presentes.
•	Como el modelo es orientado a riesgos, te da indicaciones tempranas de riesgos insuperables. Si un proyecto no puede ser hecho por causas técnicas o otras razones, te darás cuenta temprano por lo tanto no te costará mucho (tiempo y dinero).
La única desventaja del modelo Espiral es que es complicado, necesita una administración consciente, atenta y con amplios conocimientos. Puede resultar difícil definir objetivos y verificar que se está listo para avanzar a la próxima iteración. A veces no es necesario un modelo tan demandante de tiempo porque ya se sabe que los riesgos del proyecto son moderados.


##7.4 Modified Waterfalls

#Sashimi (Waterfall with Overlapping Phases)
Este modelo sugiere el uso de solapación entre etapas. Es decir que la etapa siguiente puede comenzar incluso antes que la anterior haya terminado. Esto permite más flexibilidad porque permite modificar algo en etapas posteriores.

#Waterfall with Subprojects
Un problema del modelo Pure Waterfall en un punto de vista de desarrollo rápido, es que se supone que se debe terminar el diseño de la arquitectura antes de empezar con el desarrollo del sistema. Hay áreas que suelen tener sorpresas en el diseño, pero otras con la experiencia han mostrado que no tienen sorpresas en el diseño. ¿Para qué retrasar el desarrollo de las áreas fáciles de desarrollar porque están esperando a un área más difícil?.
 Aquí entra en juego los subproyectos, si a la arquitectura se la divide en diferentes proyectos independientes, se pueden separar y trabajar a su propio ritmo. 

#Waterfall with Risk Reduction
Otra debilidad de el modelo Pure Waterfall es que necesita que definas los requerimientos antes de comenzar con el diseño de la Arquitectura. Se puede agregar un espiral de Reducción de Riesgo en el principio de la cascada para solucionar eso.

##7.5 Evolutionary Prototyping (Prototipos Evolutivos)
Es un ciclo de vida en el cual se desarrolla el concepto del sistema mientras se mueve a través del proyecto. Usualmente se comienza por desarrollar los aspectos más visibles del sistema, los cuales se muestran al cliente y se continua desarrollando el prototipo según el feedback del cliente. En algún momento el cliente y el desarrollador se ponen de acuerdo en que el prototipo es bueno. En ese momento se realiza el trabajo restante en el sistema y se lanza el prototipo como el producto final.
Este sistema es útil cuando:
•	Los requerimientos del cliente cambian rápidamente.
•	Cuando el cliente se niega a comprometerse a ciertos requerimientos.
•	Cuando ni el usuario ni el desarrollador entiende el área de aplicación bien.
•	Cuando el desarrollador no está seguro de la arquitectura óptima o que algoritmos usar.
Los prototipos evolutivos producen signos de progreso estables, que puede ser útil cuando se demanda un desarrollo rápido.
La mayor desventaja de este tipo de modelo, es que es imposible de saber cuanto va a tomar crear un producto aceptable, no sabrás ni siquiera cuantas iteraciones serán necesarias para que el prototipo sea aceptado. Aunque esta desventaja pasa desapercibido gracias a que los clientes podrán ver el progreso del proyecto.
Otra desventaja es que este modelo puede ser una excusa para realizar un desarrollo Code-and-Fix. Un prototipo evolutivo real incluye análisis de requerimientos, diseño real y código mantenible. 

##7.6 Staged Delivery
En este modelo de ciclo de vida, se muestra el software al cliente en sucesivas etapas refinadas. Al contrario de Evolutionary Prototyping, en este modelo se conoce exactamente lo que se va a crear. Lo que hace especial a este modelo, es que no se entrega el proyecto una vez que está completo, sino que se entrega en sucesivas etapas a través del proyecto.
Con este ciclo, se usa el modelo cascada de definir el Software Concept, el análisis de requerimientos y crear el diseño de la arquitectura del programa que se va a crear.
Luego, se procede con el diseño detallado, programación, debugging y testeo por cada etapa.
Ventajas del Staged Delivery:
•	Permite poner funcionalidades útiles en las manos de los clientes más temprano que si lo entregaras cuando se completa el proyecto. Si se planea las etapas correctamente, se puede enviar las funcionalidades más temprano y los clientes pueden empezar a usarlas desde ese momento.
•	Este modelo de ciclo de vida también provee de signos de progreso tangibles más temprano que otros modelos. Dichos signos de progreso pueden ser valiosos en mantener la presión de tiempos a un nivel manejable.
La primer desventaja de Staged Delivery es que no funcionará sin un planeamento cuidadoso, tanto en niveles administrativos como técnicos. En un nivel administrativo, hay que tener en cuenta que las etapas que planees tengan sentido para le cliente y que distribuyas el trabajo al personal de una manera que puedan completar la etapa en fecha. En un nivel técnico, hay que estar seguro que has tomado en cuenta todas las dependencias entre los diferentes componentes del producto.   
       
##7.7 Design-to-Schedule
Este ciclo de vida es similar al Staged Delivery, pero en este modelo no se sabe si llegarás al último lanzamiento. Podrás tener cinco etapas planeadas, pero solo llegar a la tercera debido a que tienes una fecha de entrega inamovible. 
Ventajas del Design-to-Schedule:
•	Puede ser útil para asegurar de lanzar un producto en una fecha particular.
•	Puede ser útil para desarrollar partes que no quieres en el camino crítico. Deja a las características de menor prioridad para después, si la fecha de entrega llega antes de que hayas completado todas las etapas, no dejarás de lado a las características críticas porque has gastado tiempo en implementar las menos importantes.
Desventajas del Design-to-Schedule:
•	Una desventaja es si usted no realiza todas las etapas, habrá perdido tiempo especificando, diseñando características que no va a entregar. Si no hubiese gastado tiempo en características incompletas que no va a entregar, podría haber tenido tiempo para realizar alguna característica más. 
La decisión de usar este ciclo de vida se basará en la confianza en tus capacidades de calendarización. Si confía en que podrá llegar a las fechas de entrega, usar este ciclo de vida será muy ineficiente.

##7.8 Evolutionary Delivery
En este modelo se desarrolla una versión del producto, se lo muestra al cliente y se redefine el producto basado en el feedback del cliente.
La principal diferencia entre Evolutionary Prototyping y Evolutionary Delivery es el énfasis.
En Evolutionary Prototyping se pone énfasis en los aspectos visibles del sistema, luego se realiza el trabajo fundamental del sistema.
En Evolutionary Delivery, se pone énfasis inicialmente en el núcleo del sistema, en funciones de bajo nivel del sistema que probablemente no cambien con el feedback del cliente.

##7.9 Design-to-Tools
En este ciclo de vida, ha sido usado solamente en ambientes sensibles al tiempo. La idea detrás de Design-to-Tools es trabajar en tu producto solamente si está soportado por herramientas de software existentes. Si no está soportado, se lo deja de lado. Se le llama herramientas de software a librerías, generadores de código, lenguajes de rápido desarrollo, y otras herramientas que puedan reducir el tiempo de implementación.
Ventajas de Design-to-Tools:
•	Se puede combinar con modelos de ciclo de vida flexibles.
•	Probablemente, todas las funcionalidades que este buscando no estén disponibles por las herramientas, pero si elige sus herramientas cuidadosamente, puede implementar la mayoría de sus funcionalidades rápidamente.
•	Provoca un tiempo de desarrollo excepcionalmente rápido.
Desventajas:
•	Se pierde mucho control del producto desarrollado.
•	Es posible que no puedas implementar todas las características que necesitas, y será posible que no puedas implementar las características de la manera que querés.
•	Te vuelve dependiente en los productores de software comercial.

##7.10 Commercial Off-the-Shelf Software
Una alternativa puede ser comprar software listo para el uso. Este tipo de software raramente va a satisfacer las necesidades, pero tiene las siguientes ventajas:
•	Está disponible inmediatamente.
•	En el tiempo que compras el software listo, ya se le puede dar a los clientes algunas capacidades. Pueden aprender a trabajar con el producto, ver sus limitaciones. En ese tiempo se debería estar trabajando en el software modificado.





