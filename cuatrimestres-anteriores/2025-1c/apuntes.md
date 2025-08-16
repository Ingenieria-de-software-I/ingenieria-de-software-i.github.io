---
layout: page
title: Apuntes
---

* toc
{:toc}

## Presentaciones <img alt="github icon" width="20px" src="./assets/icons/presentacion.svg" />

[01 Introducción a la materia](https://docs.google.com/presentation/d/1_HzWu0bnRIvB5GHUhpqNm_NVK0-ByPklJzMALT1ggO0/edit?usp=sharing)

[01B Introducción a la ingeniería de Software](https://docs.google.com/presentation/d/1-9n48TRvc4FvYBcNf5FCGFrWO4IXljGnfCjtb47qGhM/edit?usp=sharing)

[12 TDD](https://docs.google.com/presentation/d/1M5ZBUuD_tOSM9JNnmTeqhnZdaKCPHm8ONOz_Y08hBGM/edit?usp=sharing)

<p class="text-muted">Esta sección se irá completando con el correr del cuatrimestre, a pedido de les alumnes.</p>

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

