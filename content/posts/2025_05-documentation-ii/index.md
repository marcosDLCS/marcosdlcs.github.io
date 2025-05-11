---
title: "No te olvides de la documentación (II)"
description: "Continuamos desmitificando la documentación de software. En esta segunda parte exploramos qué significa realmente documentar, analizamos sus diversos tipos y cuestionamos los mitos que nos han llevado a rechazarla sistemáticamente."
tags: [ "technology", "spanish" ]
lastmod: 2025-05-11
date: 2025-05-11
categories:
  - "technology"
slug: "2025-05-documentation-ii"
draft: false
---

## 🤷🏽‍♀️ Tenemos claro que no nos gusta pero, ¿qué es documentar?

En la entrada anterior hablé de la visión distorsionada que a veces tenemos sobre la tarea de documentar. Ese doble filo en el que **admitimos su utilidad en momentos clave pero que nos hace rechazarla** por el mero hecho de no tener interiorizadas maneras de trabajar que incluyan su creación y evolución como uno de los pilares de nuestro día a día.

Con el paso de los años he estado en múltiples discusiones al respecto de este tema, pero últimamente me asalta una pregunta: **¿hemos consensuado realmente lo que ES documentar?** Personalmente no tengo una respuesta cien por cien absoluta, por ello en este artículo me centraré en explicar los distintos tipos de documentación que existen y todos aquellos mitos asociados a su creación y mantenimiento.

{{< figure src="images/202505-heisenberg.jpg" alt="Meme en el que aparece Heisenberg de Breaking Bad diciendo que él es la documentación" >}}

## 🩸 Algunos tipos de documentación

Admito que es difícil a veces el "ver más allá" de la documentación pura y dura que podemos consumir en nuestro día a día. Si hago un ejercicio mental simple, lo primero que me viene a la mente al pensar en documentación son páginas y páginas infumables en _Redmine_, de autor desconocido, pero que todos temen eliminar. Lo cierto es que la documentación es mucho más, por ello paso a listar lo que para mi son sus distintos tipos:

- **Gestores de documentación interna**: Normalmente conocidos como "el Notion o el Confluence" este tipo de plataformas se convierten en el punto central de la documentación de un proyecto o empresa. Suelen albergar toda clase de información, desde _onboarding_ hasta arquitecturas y decisiones técnicas, pasando por procedimientos y guías. El problema habitual es que terminan convirtiéndose en cementerios de información desactualizada.

- **Plataforma de gestión de tareas**: Sin lugar a dudas el _software_ de gestión de tareas que usemos en nuestra organización es una fuente de documentación... cuando decidimos agregar información relevante a nuestras historias de usuario o tareas. Aquí reside un tipo de documentación extremadamente valiosa: el contexto, los criterios de aceptación, las decisiones que se tomaron durante el desarrollo. Lamentablemente, muchas veces nos limitamos a títulos escuetos y descripciones austeras.

- **Estándares de documentación técnica**: Herramientas como JavaDoc, OpenAPI/Swagger, AsciiDoc entre otros representan una aproximación controlada a la documentación de código y APIs. Estos estándares permiten generar documentación técnica de forma automatizada, pero requieren un esfuerzo constante de mantenimiento por parte del equipo.

- **Tareas automatizadas**: Los _scripts_, _pipelines_ CI/CD, tests automatizados y Makefiles son formas de documentación ejecutable. Un buen Makefile o un _pipeline_ bien configurado no solo facilita los procesos repetitivos, sino que también documenta cómo se realizan determinadas acciones en el proyecto. Los tests, especialmente los de aceptación o los _e2e_, pueden ser excelentes formas de documentar el comportamiento esperado del sistema.

- **Código**: El propio código es, en sí mismo, una forma de documentación. Los nombres de clases, métodos y variables bien elegidos, la estructura del proyecto y los patrones de diseño aplicados comunican intenciones y decisiones. Un código bien estructurado y con nombres significativos puede reducir la necesidad de documentación adicional. Sin embargo, el código nos dice el "cómo" pero no siempre el "por qué" de las decisiones tomadas.

- **Documentación externa oficial y no oficial**: Las documentaciones de APIs, guías, ejemplos, respuestas en Stack Overflow (mientras dure tras el auge de la IA) o artículos en blogs como Baeldung forman parte de nuestro ecosistema documental día a día. A menudo dependemos más de estos recursos externos que de nuestra propia documentación interna, lo que puede ser problemático cuando nuestro contexto específico difiere del general.
 
- **Herramientas de IA generativa**: En los últimos años, estas herramientas han revolucionado la forma en que interactuamos con la documentación. Pueden ayudarnos a generar, resumir o explicar documentación existente. Sin embargo, también plantean desafíos: ¿Estamos delegando demasiado el conocimiento del día día a sistemas externos?, ¿Realmente entendemos lo que estas herramientas nos explican? A pesar de su utilidad, no deberían reemplazar la creación de documentación contextualizada para nuestros proyectos.

## 🎯 Cazadores de mitos

La pregunta obvia sería, ¿cómo hemos llegado hasta aquí?

En este sentido creo que la industria se ha visto influenciada por opiniones, mitos o creencias que no están del todo fundadas, todo ello bien regado con el sesgo de autoridad que ciertas voces destilan.

### Agile manifesto

Con el tiempo he llegado a la conclusión de que pocas [reuniones en Utah](https://agilemanifesto.org/history.html) han tenido un **impacto tan negativo en una industria mil millonaria** como es la del desarrollo de _software_. Lo que comenzó con una serie de valores y principios necesarios, se ha transformado año tras año en una bola de nieve de convenciones totalmente malinterpretadas.

Dos frases tienen la culpa:

> Working software over comprehensive documentation

> The most efficient and effective method of conveying information to and within a development team is face-to-face conversation.

De manera aislada ambas afirmaciones tienen valor y su esencia es aplicable aún a día de hoy. El verdadero problema es que muchos equipos han interpretado estos principios como "la documentación es mala" o "no documentemos nada, con hablar es suficiente".

Lo que el manifiesto ágil realmente proponía era priorizar el _software_ funcional sobre extensos documentos que nadie lee, y favorecer la comunicación directa como método principal de transmisión de información. Nunca sugirió eliminar la documentación por completo.

La realidad es que necesitamos un equilibrio. La comunicación cara a cara es efímera, se pierde con el tiempo y depende de la memoria humana, que es como mínimo imperfecta. Una documentación concisa, actualizada y contextualizada complementa perfectamente la comunicación directa.

### Clean Code y el código autodocumentado

La otra corriente que nos ha llevado a odiar la documentación es el dogma del código limpio. ¿Eso quiere decir que estoy a favor del _"código sucio"_? En absoluto.

El problema con las reglas que se derivan del movimiento de Clean Code es su aplicación ortodoxa sin considerar el contexto. Una de las máximas más repetidas es que "el buen código se documenta a sí mismo" y que "si tienes que comentar tu código, es que no está bien escrito".

Estas afirmaciones, aunque bien intencionadas, han llevado a muchos desarrolladores a evitar cualquier tipo de comentario o documentación en el código, incluso en ocasiones en las cuales sería beneficioso. El código puede explicar el "cómo" a través de nombres descriptivos y estructura clara, pero rara vez explica el "por qué" detrás de determinadas decisiones.

Un buen equilibrio podría ser:

- Código limpio y autodescriptivo para el "cómo".
- Comentarios estratégicos para explicar el "por qué" cuando no es obvio.
- Documentación externa para visiones más amplias, arquitectura y contexto.

Pero no nos adelantemos.

{{< figure src="images/202505-dog-hurts.jpg" alt="Meme en el que aparece un perro recordando a una persona que probablemente haya olvidado qué hace su propio código por no hbaerlo documentado de alguna manera" >}}

### Hazlo todo al final

Otro mito destructivo es que la documentación debe hacerse al final del proyecto o desarrollo. Este enfoque garantiza prácticamente que la documentación:

1. No se hará nunca (porque siempre hay otra tarea o proyecto esperando)
2. Será incompleta (porque los detalles se han olvidado)
3. Será vista como una carga sin valor real.

La documentación debería ser parte integral del proceso de desarrollo, no un apéndice. Cuando se crea incrementalmente durante el desarrollo, refleja con mayor precisión las decisiones tomadas y el contexto en que se tomaron. Además, este enfoque distribuye la carga de trabajo y hace que la documentación sea menos propensa al rechazo.

Una estrategia efectiva es documentar las decisiones importantes justo cuando se toman, mientras el razonamiento está fresco en la mente. Herramientas como los Registros de Decisiones Arquitectónicas (ADR), de las que hablaremos en otro momento, son perfectas para esto.

### La documentación no evoluciona

Este último mito es quizás el más dañino: la idea de que la documentación es estática, un artefacto inmutable que, una vez creado, permanece igual hasta que se vuelve obsoleto y se descarta.

En realidad, la documentación valiosa evoluciona junto con el código y el producto. Debería ser tratada como un producto vivo que requiere mantenimiento, actualizaciones y ocasionalmente refactorizaciones completas. La documentación desactualizada es a menudo peor que la ausencia de documentación, ya que induce a numerosos errores.

En equipos maduros, la evolución de la documentación debería estar tan automatizada e integrada en el proceso como el propio desarrollo. O al menos esa es mi visión de idealista irredento.

## ➕ En resumen

La documentación no tiene por qué ser un mal necesario o una pesada carga administrativa. Cuando se enfoca correctamente, es una herramienta poderosa que mejora la colaboración, preserva el conocimiento de nuestros proyectos y acelera la incorporación de nuevos miembros al equipo.

Los mitos que nos han llevado a despreciar la documentación son precisamente eso, mitos. El manifiesto ágil no prohíbe documentar, el código limpio no elimina la necesidad de explicar el "por qué", y la documentación no es algo que se hace al final ni permanece estática.

Un enfoque equilibrado hacia la documentación empieza por reconocer su valor como parte fundamental del proceso de desarrollo, no como un complemento opcional. Al igual que cuidamos nuestro código, debemos cuidar nuestra documentación: mantenerla concisa, actualizada y útil.

En la próxima entrada, exploraré algunas estrategias prácticas para integrar la documentación en el flujo de trabajo diario sin que se convierta en una carga. ¿Te apuntas?

### Otras entradas

- [No te olvides de la documentación (I)](https://mdlcs.dev/posts/2024-04-documentation-i/)
