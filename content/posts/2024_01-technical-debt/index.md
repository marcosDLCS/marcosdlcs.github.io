---
title: "El problema de la deuda (técnica)"
description: "Tras unos cuantos años en el sector puedo decir que uno de los conceptos que siempre te acompaña es el de la deuda técnica. La pregunta que me hago siempre es: ¿sabemos realmente lo que ES y cómo identificarla?"
tags: [ "technology", "management", "spanish" ]
lastmod: 2024-01-31
date: 2024-01-31
categories:
  - "technology"
  - "management"
slug: "2024-01-tech-debt"
draft: false
---

_**Nota**: Se trata de un artículo de opinión basado únicamente en mis conocimientos y experiencias a día de hoy (inicios de 2024). Mi perspectiva sobre el mundo y el desarrollo de software cambia con el tiempo. Es un ejercicio de reflexión que no busca ofrecer soluciones concretas, sino presentar una visión del problema._

## 🎬 Introducción

Nos encanta hablar de **deuda técnica**. Es un concepto propio, de nuestro nicho de conocimiento.

Pertenezcas a la empresa a la que pertenezcas, sea cual sea el evento IT al que asistas, las conversaciones sobre deuda técnica están ahí, a la vuelta de la esquina, acechando, esperando atraparte.

Se tiende a pensar que algo que está en boca de todos es materia conocida, bien definida y de dominio público. Pero en realidad con este término ocurre todo lo contrario, hay tantas cosas que podrían ser deuda técnica que el concepto ha ido perdiendo su esencia, enmascarando otros problemas reales que muchas veces nos avergüenza reconocer.

{{< figure src="images/202401-banner-tech-debt.png" alt="Figura con gorro de copa y monóculo con los brazos levantados. Rótulo que reza: let's talk about technical debt" >}}

## 🙅‍♀️ Todo lo que NO es deuda técnica

Me encanta intentar definir conceptos desechando al principio características probablemente asumidas por todos, pero que se alejan del significado real de la expresión. Por ello, y siempre bajo mi opinión, paso a enumerar las cosas que considero fuera de los límites de la deuda técnica.

### 🪳 Bugs

Me atrevería a afirmar que esta es la parte que suscita más consenso. Los _bugs_, errores, incidencias o cómo quiera que los llames nunca son deuda técnica.

Incluso la existencia de muchos errores tampoco es deuda técnica. Posiblemente pueda ser una consecuencia de ello, pero no más.

**Un fallo de nuestro sistema es por definición inconsciente, no buscado. Por lo tanto, no lo podemos añadir a nuestra mochila de mejoras o propósitos**. Arréglalo y pon los medios necesarios para que no vuelva a suceder.

### 🔄 Actualización de dependencias

Algunas de las tareas clásicas en cualquier tablero o _backlog_ de deuda técnica son las de actualización de dependencias, librerías o _frameworks_.

Entonces, si son tan habituales, ¿por qué considero que no deberían asociarse al concepto mencionado?

El mundo del desarrollo de _software_ es bastante relativista, antes o después alguien te dirá la palabra "depende" aludiendo a que las decisiones son dependientes del contexto y que en el ámbito tecnológico no hay respuestas absolutas o técnicas infalibles. Sin entrar de lleno en la veracidad o no de esta afirmación, lo que puedo decir es que **en la programación, como en la vida, hay alguna que otra regla casi inviolable y una de ellas es que _"el software evoluciona y se degenera con el tiempo"_**.

Todo el mundo sabe (espero) que cuando comienzas un nuevo proyecto tendrás que mantenerlo: los lenguajes avanzarán, los _frameworks_ quedarán obsoletos o descubrirán vulnerabilidades en tus librerías.

Por ello, tu estrategia de mantenimiento debería ser un pilar fundamental de tu organización. Si omites deliberadamente estos procesos de actualización con la típica frase de _"si funciona no lo toques"_ pero luego apresuras a tu equipo a actualizar vuestros servicios porque _"dice AWS que dejará de dar soporte a la tecnología X"_, el problema no es de deuda técnica, sino de cultura y modos de trabajo.

{{< figure src="images/202401-banner-phone.png" alt="Conversación entre el equipo técnico y negocio en la que los primeros alertan de temas técnicos que arreglar y los segundos quieren hablar del ROI asociado" >}}

### 🎁 Código heredado

En mi opinión, surge una controversia al calificar como deuda técnica al código de proyectos que, en ocasiones, nos asignan y que no ha sido desarrollado por nuestro equipo.

Frecuentemente, lo que recibimos no cumple con las expectativas de calidad, es difícil de entender y presenta obstáculos al agregar nuevas funcionalidades. Esta situación es común y, además, genera estrés y tensión innecesarios en las personas.

No obstante, estas circunstancias no cumplen con la definición clásica de deuda técnica, ya que no podemos asumir responsabilidad directa por las acciones y el contexto vivido por otros. **Además, estos momentos pueden desembocar en un bloqueo operativo que no puede abordarse en pequeños incrementos durante nuestras iteraciones habituales**.

Es esencial afrontar la calidad y el rendimiento de estos proyectos, pero asignar recursos de manera más específica, como la creación de grupos de trabajo para tareas de refactorización o la extracción puntual de funcionalidades hacia otros servicios, puede ser más efectivo.

### 💾 Mejoras que quedaron en el olvido

Otro de los grandes males que asolan a la industria es el exceso de optimismo sobre el tiempo que tendremos para modernizar nuestros productos. Podría apostar contigo, sin posibilidad de perder, que has estado en algún proyecto en cuyo _backlog_, muy en el fondo, residían tareas de mejora que nunca nadie tuvo tiempo de acometer.

Todos tenemos en mente esos ambiciosos _"Improve performance"_ o _"Revamp persistence layer"_ que normalmente tienen unos números de tarea en Jira extremadamente bajos y que creó una heroína desconocida para ti, la cual abandonó la empresa hace año y medio.

¿Es eso deuda técnica? Me temo que no.

**Sin contexto y cercanía temporal, las propuestas de mejora no tienen valor**. Mi consejo es que te armes de voluntad, dejes el apego irracional a un lado y permitas que esas tareas se acomoden tranquilamente en el bulevar de tus sueños rotos. Elimínalas y re-analiza el problema sobre la base de las circunstancias actuales. _Farewell!_

### 🤝 Adaptación de nuevos acuerdos de equipo

Como último punto quiero destacar como antipatrón de deuda técnica todas aquellas tareas que nacen de cambios en los acuerdos de equipo.

¿En serio has propuesto una mejora sin evaluar el impacto y el coste de cambio en tu base de código actual? Si la respuesta es afirmativa, deberías repensar tu estrategia.

**Todo cambio en las convenciones internas que nos damos nosotros mismos tendría que tener en cuenta su coste de adopción**.

Y la justificación para alejar estas tareas del término "deuda técnica" es simple: en muchos casos dichas convenciones son una recomendación para mejorar la uniformidad del código (elección entre librerías similares, modo de diseñar una API, convenciones de nombres, capas y responsabilidades de la arquitectura), acciones que no presentan una mejora técnica per se, sino más bien una preferencia para dotar a nuestros proyectos de una mayor cohesión.

{{< figure src="images/202401-banner-usual-suspects.png" alt="Imagen que muestra un muñeco de palo por cada una de las 5 secciones de listadas arriba. En la parte inferior hay una línea de puntos y un texto que dice: usual suspects" >}}

## 🧐 Entonces, ¿qué es la deuda técnica?

Si tuviese que dar una definición concisa para mi visión del concepto de deuda técnica, sería la que sigue:

> Decisión de desarrollo u organización que se toma, de manera **deliberada**, como un **atajo** o solución de contingencia a un **problema concreto y acotado** y con la que **adquirimos un compromiso** de resolución real y **fijado en el tiempo**.

Ahora vayamos punto por punto repasando cada una de las características:

- **Voluntaria o deliberada**: Bajo mi prisma, no existe la deuda técnica externa. Para que la podamos considerar como tal debe provenir de nosotros mismos en un ejercicio de aceptación voluntaria. Por el mismo motivo, no puedo considerar deuda técnica a algo impuesto por un equipo o departamento externo ajeno a responsabilidades técnicas.
- **Conocida y aceptada**: En el momento de crear la deuda técnica debemos analizar el problema, aceptar la solución a tomar como poco adecuada y sobre todo conocer la manera óptima de realizarlo en el futuro (o al menos una propuesta). No podemos admitir como deuda técnica la falta de conocimiento o contexto en un momento pasado.
- **Compromiso de solución**: El punto más odiado. No hay deuda técnica si no existe un compromiso cierto de devolución de esa deuda. Como mencionaba antes, si en el fondo de tu _backlog_ se acumulan tareas y más tareas de mejora, no tienes un problema de deuda técnica. Hazme caso, es otra cosa.
- **De ámbito reducido**: La deuda tiene que ser concreta para que su resolución sea accesible e incluso posible. No podemos considerar como deuda técnica un conjunto de servicios o proyectos completos.

El análisis de las características de la deuda técnica es importante, ya que de esa manera podremos anticiparnos a sus causas y encontrar soluciones. Tras reflexionar considero que hay tres orígenes comunes para este problema y tres soluciones obvias a dichas circunstancias:

{{< figure src="images/202401-banner-problem-solution.png" alt="Diagrama que expone 3 problemas: falta de conocimiento, falta de tiempo y percepción de valor. Y tres soluciones: formación, mejoras organizativas y cultura de empresa" >}}

Mi objetivo es exponer el problema y crear un marco de comunicación, no aportar estrategias detalladas. Queda de tu mano y de la de tu equipo definir e impulsar las acciones y prácticas necesarias para no caer en el pozo de la deuda técnica.

## 🤔 ¿Por qué es importante llamar a las cosas por su nombre?

Asignar con precisión los conceptos nos conduce a descubrir soluciones más efectivas para los desafíos cotidianos que enfrentamos.

Al revisar la lista anterior de situaciones distintas a la deuda técnica, podemos notar que cada elemento presenta peculiaridades únicas y requiere enfoques diferentes:

- **Errores (Bugs)**: Encarar eficazmente los errores recurrentes implica contar con un sólido **sistema de monitorización u observabilidad** que alerte de manera oportuna sobre incidencias, proyectos con una **buena batería de tests** y fomentar la **simplicidad** en nuestro dominio.
- **Actualización de dependencias**: En la actualidad, existen herramientas que facilitan enormemente esta tarea, desde **_bots_ que nos alertan sobre nuevas versiones** de nuestras dependencias, hasta sistemas de **detección estática y dinámica de vulnerabilidades**. Es esencial conocer a fondo las tecnologías que utilizamos y **evitar incluir _software_ de terceros** a menos que sea verdaderamente necesario.
- **Código heredado**: No hay soluciones mágicas en este punto. Si el código heredado es problemático, debemos abordarlo de manera rápida y precisa desde el principio, **asignando todos los recursos disponibles**. No esperes lograr frutos sorprendentes con pequeñas mejoras. Los proyectos heredados de baja calidad son una carga para el equipo y pueden dar como resultado la pérdida de talento en la empresa. La decisión está en tus manos.
- **Deuda técnica antigua**: Si las tareas son tan antiguas que desconoces su origen o la persona que reportó la incidencia, mi recomendación sería **eliminarlas** directamente, **reconsiderar** la situación actual y **crear** nuevas tareas con el contexto actualizado.
- **Nuevos acuerdos**: En el ámbito de los nuevos acuerdos, siempre es efectivo implementar medidas que dificulten su incumplimiento. Esto puede lograrse mediante la creación de **tests de arquitectura**, el uso de **herramientas de _linting_** correctamente configuradas, la promoción de técnicas de trabajo como el **_pair/mob programming_**, o la adopción de una **cultura de refactorización** que no requiera la creación explícita de tareas para su realización.

## ➕ En resumen

El concepto **"deuda técnica"** en el desarrollo de _software_ ha perdido su esencia. Durante mucho tiempo se ha utilizado sistemáticamente de manera incorrecta para describir problemas que no son compromisos propios.

Considero que los errores, las actualizaciones de dependencias, las mejoras pendientes, el código heredado o los cambios en acuerdos de equipo no son deuda técnica. Y propongo una definición más precisa: **una decisión voluntaria que implica un compromiso fijado en el tiempo para resolver un problema específico**. Catalogar correctamente los conceptos es crucial para encontrar soluciones adecuadas y evitar malentendidos en el desarrollo de _software_.

Por último, y ya que al tratar sobre estos conceptos siempre se usan símiles económicos, me gustaría acabar con una cita de **David Graeber** de su libro _En deuda_, que al hablar sobre su cancelación dice:

> ... recordarnos a nosotros mismos que el dinero no es inefable, que pagar las deudas no es la esencia de la moral, que todo esto son cosas que hemos decidido hacer de determinada manera los humanos y que, si algo significa la democracia, es la capacidad de ponernos de acuerdo entre todos para hacer las cosas de otra manera.

Espero que te haya gustado. Si es así, estamos en deuda.
