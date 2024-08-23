---
layout: page
title: Apuntes
---

* toc
{:toc}

## Presentaciones <img alt="github icon" width="20px" src="./assets/icons/presentacion.svg" />

- [01 Introducción a la materia](https://docs.google.com/presentation/d/18LZeACGdPdkJwaw5dCF8xuCjNNUEUNQOjYyO1hVSVoY)
- [01B Introducción a la ingeniería de software](https://docs.google.com/presentation/d/107ujvnW9BIjqx5uM0TsUKhWi4LfpyJ5e_w_v9vofC08)
- [09 Historia de Smalltalk](https://docs.google.com/presentation/d/1pHV5b4qAAABY70OiPXENHyAtNqfhpekKlDqnl7NxFNY/edit?usp=sharing)
- [09 Intro a Patrones de diseño](https://docs.google.com/presentation/d/1O5P-IxBSvVE4c70EWPeZmTMVnnKZ3nAcCuD8bf-dwKI/edit?usp=sharing)
- [10 TDD](https://docs.google.com/presentation/d/1Zw8MF7GGkyTLGYXlEge4ZYytBC4RLQtLqCRGIrSz9W4/edit?usp=sharing)

<p class="text-muted">Esta sección se irá completando con el correr del cuatrimestre</p>

## Git <img alt="github icon" width="20px" src="https://icongr.am/devicon/git-plain.svg?size=148&color=currentColor" />

- [Apunte del taller de Git](https://docs.google.com/document/d/1VwJUVTMz1psGqdaNR2NJWo8mtPoK2FvDB1cP9xQObcQ/edit?usp=sharing)

### Taller de git <img alt="github icon" width="22px" src="https://icongr.am/clarity/film-strip.svg?size=148&color=currentColor" />

<iframe width="360" height="215" src="https://www.youtube.com/embed/L0RHt3P6S94" title="Taller de git - 20202c" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="360" height="215" src="https://www.youtube.com/embed/OgXfPAw2WoU" title="Taller de git" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Apunte teórico <img alt="github icon" width="20px" src="https://icongr.am/clarity/library.svg?size=128&color=currentColor" />

Conceptos fundamentales
--------

Software:
- Modelo computable de un dominio de problema de la realidad. Dominio = recorte de la realidad.

Desarrollo de software:
- Proceso de aprendizaje
- Iterativo e incremental. Feedback inmediato es fundamental.
- Eje descriptivo	, funcional e implementativo. Foco en eje descriptivo y funcional.

Paradigma de Objetos:
- Objetos que colaboran entre si mediante el envio de mensajes.

Objeto:
- Representación de un ente de la realidad.
- Se define a partir de los mensajes que sabe responder.

Mensaje:
- Define el QUE del objeto (vs Método que define el COMO)
- Define una responsabilidad que tiene el objeto.
- Puede tener múltiples implementaciones asociadas (métodos).

Método:
- Implementación de un mensaje. Define el COMO.
- Conjunto de colaboraciones.

Colaborador:
- También conocido como variable.
- Interno (variable de instancia), externo (parámetro) o temporales (variables).
  - Interno: Lo conozco siempre. Relación de cercanía en cuanto al conocimiento. 
  - Externo: Lo conozco para una colaboración puntual. 
  - Temporal: Lo conozco temporalmente dentro de un conjunto de colaboraciones.

Closure:
- Conjunto de colaboraciones, al igual que un método, pero no está asociado a ningún objeto. No hay mensaje asociado.
- Están bindeados al contexto.
- Closure vs "full" closures. Estos últimos tienen binding del return al contexto de ejecución (ej: Smalltalk, Ruby).

Clase:
- Concepto que aparece en lenguajes OOP con clasificación (vs prototipado, como Self o JS).
- Representa un concepto o idea de la realidad. Ej: "Silla" (clase) vs "esta silla blanca donde estoy sentado (instancia).
- Todo objeto es instancia de una clase.
- Abstracta: No tiene realizaciones concretas. No hay entes de la realidad que puedo relacionar de forma exclusiva con el concepto. Ej: Todo "Numero" es real, entero, fraccionario o imaginario.
  - Tiene al menos un método abstracto.
  - Corolario: No tiene sentido instanciarlo.
- Métodos de instancia vs métodos de clase: Los primeros definen el comportamiento de las instancias, mientras que los segundos, el comportamiento de las clases.

Subclase:
- Especialización. "Se comporta como" (ojo con el ES UN).
- Subclasificación: Forma de organizar conocimiento mediante jerarquías de clases.

Polimorfismo:
-Dos o mas objetos son polimorficos entre si respecto a un conjunto de mensajes <=>
	- Responden de la misma manera / Son semánticamente iguales
	- Mismo nombre del mensaje
	- Misma cantidad y tipo de parametros
	- Mismo tipo de resultado

Heurísticas de diseño
-------------

- Buscar el 1:1 entre objeto - ente
- Favorecer composicion por sobre subclasificación
- Quitar código repetido: Señal de que falta una abstracción.
- No romper encapsulamiento.
- Nombrar a los objetos segun el ROL que cumplen en un determinado contexto
- No subclasificar de clases concretas
- Guiarnos por los aspectos funcionales conducen a mejores modelos
- Favorecer el uso de polimorfismo por sobre ifs.
- Favorecer inmutabilidad
- Crear objetos completos
- Crear objetos validos
- No usar null

Reemplazar if por polimorfismo
-------------------

1. Crear una jerarquia de clases con una clase por cada condicion del if (si no existe)
2. Mover el cuerpo del if de cada condicion a cada abstracción del paso 1) utilizando un mensaje polimorfico.
3. Nombrar el mensaje polifmorfico
4. Nombrar las abstracciones del paso 1)
5. Reemplazar el if por el envio de mensaje polimorfico
6. Buscar el objeto polimorfico (si es necesario)

TDD
---

1. Escribir el test mas sencillo posible que falle.
2. Hacer pasar todos los tests con la implementación más simple posible.
3. Reflexionar. ¿Se puede mejorar?
