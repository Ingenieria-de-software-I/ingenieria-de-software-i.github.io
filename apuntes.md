---
layout: page
title: Apuntes
---

* toc
{:toc}

## Presentaciones <img alt="github icon" width="20px" src="./assets/icons/presentacion.svg" />

- [01 Introducción a la materia](https://docs.google.com/presentation/d/1srLq5Cm9e9FiFUZommX4_70tSROogv-9KFlIhRHIGyA/edit?usp=sharing)
- [01B Introducción a la ingeniería de Software](https://docs.google.com/presentation/d/1ErPs_ZQg6m3KZrOn-voLt-JikSx5le90QM8m9spPKCE/edit?usp=sharing)
- [06 Organización de conocimiento](https://docs.google.com/presentation/d/1gaAlimn_3CL7OKDg3qr0bj0jeXAr2_x6F1By26rlcxg/edit?usp=sharing)
- [07 Historia de Smalltalk](https://docs.google.com/presentation/d/1FRYjfV0M_NbK39uNgbTs9xMj910o0wJ5a9LjxT02a3E/edit?usp=sharing)
- [12 TDD](https://docs.google.com/presentation/d/1AWzAIAxxvB7IElcBowbZHMBHWu5Qn_jWmdpyIQsQUIk/edit?usp=sharing)
- [16 Intro a Patrones de diseño](https://docs.google.com/presentation/d/1d2e_lJOw993-fN5C1yHvAv356jCnCOarocBFyQcB9-A/edit?usp=sharing)

## Git <img alt="github icon" width="20px" src="https://icongr.am/devicon/git-plain.svg?size=148&color=currentColor" />

- [Apunte del taller de Git](https://docs.google.com/document/d/1VwJUVTMz1psGqdaNR2NJWo8mtPoK2FvDB1cP9xQObcQ/edit?usp=sharing)

### Taller de git <img alt="github icon" width="22px" src="https://icongr.am/clarity/film-strip.svg?size=148&color=currentColor" />

<iframe width="360" height="215" src="https://www.youtube.com/embed/L0RHt3P6S94" title="Taller de git - 20202c" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="360" height="215" src="https://www.youtube.com/embed/OgXfPAw2WoU" title="Taller de git" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Apunte teórico <img alt="github icon" width="20px" src="https://icongr.am/clarity/library.svg?size=128&color=currentColor" />

Conceptos que exploramos
- Objeto
- Mensaje vs Método
- Igualdad vs Identidad
- Closures
- Acoplamiento y cohesión
- Encapsulamiento
- Polimorfismo
- Prototipado vs Clasificacion
- Clase y jerarquías de conocimiento.

Heurísticas de diseño
-------------

Hasta ahora…

- Buscamos 1:1 entre objeto y ente de la realidad. Separación de responsabilidades.
- Nombrar a los objetos (clases y colaboradores) según el ROL que cumplen de acuerdo al contexto / al dominio de problema.
- Guiarnos por el aspecto funcional conduce a buenos diseños.
- Evitar romper encapsulamiento.
- Código repetido: Señal de que falta una abstracción.
- Favorecer polimorfismo por sobre ifs.
- Favorecer inmutabilidad
- Crear objetos completos
- Crear objetos validos
- Evitar subclasificar de clases concretas.
- Favorecer composición por sobre subclasificación.

Técnicas que vimos:
- Algoritmo para quitar código repetido
- Algoritmo para quitar el if [*]
- Switch dinámico

[*]

1. Crear una jerarquia de clases con una clase por cada condicion del if (si no existe)
2. Mover el cuerpo del if de cada condicion a cada abstracción del paso 1) utilizando un mensaje polimorfico.
3. Nombrar el mensaje polifmorfico
4. Nombrar las abstracciones del paso 1)
5. Reemplazar el if por el envio de mensaje polimorfico
6. Buscar el objeto polimorfico (si es necesario)

---
TDD

1. Escribir un test que falle
2. Hacer pasar todos los test
3. Reflexionar
