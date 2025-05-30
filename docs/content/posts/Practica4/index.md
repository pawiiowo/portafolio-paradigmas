+++
draft = false
title = 'Práctica 4: Paradigma Lógico - Prolog'
summary = 'Reporte de la Práctica 4'
+++

![Logo de la escuela](images/logouabc.png)
![Logo de la facultad](images/logofiad.png)

# Práctica 4: Introducción a las Bases de Conocimiento

## Información General  
**Universidad Autónoma de Baja California**  
**Facultad de Ingeniería, Arquitectura y Diseño**  
**Paradigmas de la Programación**  
**Grupo: 941**  
**Alumno: Paulina Mendoza Quiroz**  
**Matrícula: 372532**  

---

## Introducción a las Bases de Conocimiento
Una **base de conocimiento (BC)** es una tecnología utilizada para almacenar información compleja derivada y utilizada por sistemas de inteligencia artificial. Consiste en un conjunto de **hechos** (datos explícitos) y **reglas** (sentencias lógicas que permiten inferir nuevos hechos a partir de los existentes). Las bases de conocimiento son fundamentales en áreas como los sistemas expertos, la representación del conocimiento y la programación lógica. A través de **consultas**, se puede interrogar a la base de conocimiento para obtener respuestas o derivar nueva información.

---

## Ejemplos de Bases de Conocimiento

### Base de Conocimiento 1: Hechos Simples sobre Personas
Esta base de conocimiento contiene hechos directos sobre individuos.

**Declaraciones:**
* Se declara que Priya, Natasha y Jasmin son niñas:
    * `girl(priya)`
    * `girl(natasha)`
    * `girl(jasmin)`
* Se establece que Priya puede cocinar:
    * `can_cook(priya)`

**Consultas realizadas:**
* Al preguntar si Priya es `girl`: devuelve `true`
* Al preguntar si Natasha puede cocinar (`can_cook(natasha)`): devuelve `false`

### Base de Conocimiento 2: Hechos y Reglas Lógicas
Esta base de conocimiento incluye tanto hechos como reglas lógicas para inferir nueva información.

**Hechos:**
* Ana canta canciones: `sing_a_song(ana)`
* Rodrigo escucha música: `listens_to_music(rodrigo)`

**Reglas:**
* Si alguien canta, entonces escucha música:
    * `listens_to_music(X) :- sing_a_song(X)`
    * Ejemplo aplicado: `listens_to_music(ana) :- sing_a_song(ana)`
* Si alguien canta, es feliz:
    * `happy(X) :- sing_a_song(X)`
    * Ejemplo aplicado: `happy(ana) :- sing_a_song(ana)`
* Si alguien escucha música, es feliz:
    * `happy(X) :- listens_to_music(X)`
    * Ejemplo aplicado: `happy(rodrigo) :- listens_to_music(rodrigo)`
* Si Rodrigo escucha música, entonces toca guitarra:
    * `plays_guitar(rodrigo) :- listens_to_music(rodrigo)`

### Base de Conocimiento 3: Hechos y Relaciones
Esta base de conocimiento contiene hechos y reglas que definen relaciones entre entidades.

**Hechos sobre quiénes pueden cocinar (`can_cook/1`):**
* `can_cook(priya)`
* `can_cook(jasmin)`
* `can_cook(timoteo)`

**Reglas de preferencia:**
* A Priya le gusta Jasmin si Jasmin puede cocinar:
    * `like(priya, jasmin) :- can_cook(jasmin)`
* A Priya le gusta Timoteo si Timoteo puede cocinar:
    * `like(priya, timoteo) :- can_cook(timoteo)`

**Consultas realizadas:**
* `can_cook(X)` → encuentra tres soluciones: `priya`, `jasmin` y `timoteo`.
* `like(priya, X)` → devuelve `jasmin` y `timoteo` como soluciones.

### Conceptos Clave Ilustrados
Los ejemplos anteriores demuestran varios conceptos fundamentales de las bases de conocimiento y la programación lógica:
-   **Hechos (Facts)**: Proposiciones elementales que se asumen verdaderas (ej. `girl(priya)`, `can_cook(priya)`).
-   **Reglas (Rules)**: Sentencias condicionales que permiten inferir nuevos hechos a partir de hechos existentes (ej. `listens_to_music(X) :- sing_a_song(X)`).
-   **Consultas (Queries)**: Preguntas formuladas a la base de conocimiento para recuperar información o verificar proposiciones (ej. `can_cook(natasha)`, `like(priya,X)`).
-   **Inferencia Lógica**: El proceso mediante el cual el sistema deriva conclusiones (respuestas a consultas) basándose en los hechos y reglas almacenados.
-   **Predicados y Átomos**: Las relaciones y propiedades se expresan mediante predicados (ej. `girl/1`, `can_cook/1`, `like/2`). Un átomo es un predicado aplicado a términos (constantes o variables).

---

## Conclusión
Las bases de conocimiento, como se ilustra en los ejemplos, proporcionan un mecanismo estructurado para representar información y razonar sobre ella.
-   La **Base de Conocimiento 1** destaca la simplicidad de almacenar y consultar hechos directos.
-   La **Base de Conocimiento 2** introduce el poder de las reglas lógicas para expandir el conocimiento implícito a partir de datos explícitos, mostrando cómo se pueden derivar nuevas conclusiones.
-   La **Base de Conocimiento 3** demuestra cómo se pueden modelar relaciones más complejas y preferencias mediante la combinación de hechos y reglas, permitiendo consultas que exploran estas interconexiones.

Estos ejemplos sientan las bases para comprender sistemas más sofisticados basados en conocimiento, relevantes en la inteligencia artificial y la programación declarativa. La capacidad de definir hechos, establecer reglas y realizar consultas es central para construir sistemas que puedan "razonar".