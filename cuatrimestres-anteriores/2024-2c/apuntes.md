---
layout: page
title: Apuntes
---

* toc
{:toc}

## Presentaciones <img alt="github icon" width="20px" src="./assets/icons/presentacion.svg" />

- [01 Introducción a la materia](https://docs.google.com/presentation/d/1eB3SIUu4lrOvCYqXKT9Ka1Fd1L2QxrvAdQpl8p7M_Ao/edit#slide=id.p)
- [01B Introducción a la ingeniería de software](https://docs.google.com/presentation/d/1uKQQEr8lx1Q5rrhrbwCVV67BFOv_S0ONOpX7z0wJL1I/edit#slide=id.p)
- [01C Introduccion a la ingenieria de software](https://docs.google.com/presentation/d/187YcvvkAbXzn-b6efBPLMTTaIAg3GZTilX5vmGRKdIk/edit#slide=id.g2206af7cf7d_0_0)
- [10 TDD](https://docs.google.com/presentation/d/1Brr2Z1-qxEfBBEHYIRXN4jIjK4vcexD-Xl-9zuvWE9k/edit?usp=sharing)

<p class="text-muted">Esta sección se irá completando con el correr del cuatrimestre</p>

## Git <img alt="github icon" width="20px" src="https://icongr.am/devicon/git-plain.svg?size=148&color=currentColor" />

- [Apunte del taller de Git](https://docs.google.com/document/d/1VwJUVTMz1psGqdaNR2NJWo8mtPoK2FvDB1cP9xQObcQ/edit?usp=sharing)

### Taller de git <img alt="github icon" width="22px" src="https://icongr.am/clarity/film-strip.svg?size=148&color=currentColor" />

<iframe width="360" height="215" src="https://www.youtube.com/embed/L0RHt3P6S94" title="Taller de git - 20202c" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="360" height="215" src="https://www.youtube.com/embed/OgXfPAw2WoU" title="Taller de git" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Apunte teórico <img alt="github icon" width="20px" src="https://icongr.am/clarity/library.svg?size=128&color=currentColor" />

Objeto: Representación de un ente de la realidad. Se define a partir de los mensajes que sabe responder.
Mensaje: Representa el QUE de los objetos. Define una responsabilidad. Puede tener múltiples implentaciones.
Método: Es la implementación de un mensaje. Representa el COMO. Conjunto de colaboraciones.
Colaborador: Variable. Puede ser interno (variable de instancia), externo (parámetro) o temporal.

Clase: Representa un concepto de la realidad.
Subclase: Especialización. "Se comporta como". Forma de organizar el conocimiento mediante jerarquias.

Buscar el 1:1 entre objeto-ente

### Heuristicas de diseño
- Favorecer composición sobre subclasificación.
- No subclasificar de clases concretas.
- Codigo repetido: Señal de que me falta una abstracción.
- Evitar romper encapsulamiento
- Favorcer polimorfismo por sobre ifs
- Nombrar objetos segun el ROL que cumplen en el dominio de problema.
- Guiarnos por aspectos funcionales conduce a mejores modelos.
- Crear objetos compĺetos
- Crear objetos válidos
- Favorecer objetos inmutables
- No usar nil/null

### Quitar código repetido
1. Copiar lo repetido a "algun lugar"
2. Parametrizar lo que cambia
3. Nombrar la abstraccion
4. Reemplazar lo repetido x la nueva abstracción

### Reemplazar if por polimorfismo
1. Crear una jerarquia de clases con una clase por cada condicion del if (si no existe)
2. Mover el cuerpo del if de cada condicion a cada abstracción del paso 1) utilizando un mensaje polimorfico.
3. Nombrar el mensaje polifmorfico
4. Nombrar las abstracciones del paso 1)
5. Reemplazar el if por el envio de mensaje polimorfico
6. Buscar el objeto polimorfico (si es necesario)

### TDD
1. Escribir el test mas simple posible que falle
2. Hacer pasar los tests con la implementacion mas simple posible
3. Reflexionar, ¿refactorizar?
