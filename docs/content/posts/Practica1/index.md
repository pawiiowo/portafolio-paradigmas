+++
date = '2025-02-21T10:18:14-08:00'
draft = true
title = 'Practica 1: Elementos básicos de los lenguajes de programación'
summary = 'Reporte de la practica 1'
+++

![Logo de la escuela](images/logouabc.png){width=150px}
![Logo de la facultad](images/logofiad.png){width=150px}

# Universidad Autónoma de Baja California
## Facultad de Ingeniería, Arquitectura y Diseño
### Paradigmas de la Programación

**Nombre del alumno:** Paulina Mendoza Quiroz  
**Matrícula:** 372532  
**Grupo:** 941  
**Fecha:** 14 de Marzo del 2025

## Introducción
Este reporte tiene como objetivo identificar los elementos básicos de los lenguajes de programación en los archivos que nos dieron (`biblioteca.c`, `memory_management.c`, y `memory_management.h`). Vamos a ver cosas como nombres, objetos, entornos, bloques, alcance, manejo de memoria, expresiones, comandos, secuencia, selección, iteración, recursión, subprogramas y tipos de datos.

---

## 1. Nombres
Los nombres son como etiquetas que usamos para referirnos a variables, funciones o tipos de datos. En el código, hay varios ejemplos. Por ejemplo, en `biblioteca.c`, usamos nombres como `library`, `members`, `bookCount` y `memberCount`. En `memory_management.c`, hay nombres como `heap_allocations`, `heap_deallocations`, `stack_allocations` y `stack_deallocations`. También en `memory_management.h`, está el nombre `MEMORY_MANAGEMENT_DISPLAY`.

---

## 2. Objetos
Los objetos son como instancias de algo, por ejemplo, una variable o una estructura. En `biblioteca.c`, creamos objetos como `book_t *new_book` y `member_t *new_member`. En `memory_management.c`, usamos el objeto `MemoryRecord *record` para manejar registros de memoria.

---

## 3. Entornos
El entorno es como el lugar donde vive una variable o función. Por ejemplo, en `biblioteca.c`, dentro de la función `main`, tenemos variables como `library`, `members`, `bookCount` y `memberCount`. En `memory_management.c`, dentro de la función `addMemoryRecord`, está la variable `record`.

---

## 4. Bloques
Un bloque es un pedazo de código que está entre llaves `{}`. En `biblioteca.c`, el bloque de la función `main` tiene todo el código que se ejecuta cuando el programa empieza. En `memory_management.c`, el bloque de la función `addMemoryRecord` dice cómo se agregan registros de memoria.

---

## 5. Alcance (Scope)
El alcance es como el área donde una variable puede ser usada. Por ejemplo, en `biblioteca.c`, la variable `current` dentro de `findBookById` solo existe dentro de esa función. En cambio, en `memory_management.c`, la variable `heap_memory_records` puede ser usada en cualquier parte del programa porque es global.

---

## 6. Administración de Memoria
Esto es cómo se maneja la memoria en el programa. En `biblioteca.c`, usamos `malloc` para pedir memoria y `free` para liberarla cuando ya no la necesitamos. En `memory_management.c`, las funciones `incrementHeapAllocations` y `incrementHeapDeallocations` ayudan a llevar la cuenta de cuánta memoria se ha usado y liberado.

---

## 7. Expresiones
Las expresiones son como fórmulas que combinan valores, variables y operadores. En `biblioteca.c`, un ejemplo es `new_book->id = bookID`, donde le damos un valor al ID de un libro. En `memory_management.c`, la expresión `heap_allocations++` aumenta el contador de memoria asignada.

---

## 8. Comandos
Los comandos son instrucciones que hacen algo, como asignar un valor o llamar a una función. En `biblioteca.c`, un comando común es `library = new_book`, que agrega un nuevo libro a la biblioteca. En `memory_management.c`, el comando `fclose(file)` cierra un archivo después de usarlo.

---

## 9. Secuencia
La secuencia es el orden en que se ejecutan las cosas. En `biblioteca.c`, dentro de la función `main`, todo se ejecuta en orden dentro del bucle `do-while`. Esto hace que el programa siga un flujo lógico.

---

## 10. Selección
La selección es como tomar decisiones en el código. En `biblioteca.c`, usamos `if (bookFound && memberFound)` en la función `issueBook` para ver si un libro y un miembro existen antes de hacer algo. También usamos `switch (choice)` en `main` para manejar las opciones del menú.

---

## 11. Iteración
La iteración es repetir algo varias veces. En `biblioteca.c`, el bucle `while (current_book)` en `findBookById` busca un libro por su ID. También está el bucle `for (int i = 0; i < current->issued_count; i++)` en `displayMembers`, que muestra los libros que ha pedido un miembro.

---

## 12. Recursión
La recursión es cuando una función se llama a sí misma. En `biblioteca.c`, la función `displayBooksRecursive` usa recursión para mostrar todos los libros. Se llama a sí misma con `displayBooksRecursive(library->next)`.

---

## 13. Subprogramas (Funciones)
Los subprogramas son funciones que hacen algo específico. En `biblioteca.c`, funciones como `addBook`, `findBookById` y `displayBooks` se encargan de gestionar la biblioteca. En `memory_management.c`, las funciones `addMemoryRecord` y `removeMemoryRecord` manejan los registros de memoria.

---

## 14. Tipos de Datos
Los tipos de datos son como categorías que definen qué tipo de valor puede tener una variable. En `biblioteca.c`, usamos tipos como `int`, `char`, `book_t` y `member_t`. En `memory_management.c`, está el tipo `MemoryRecord` para guardar información de la memoria.

---

## Conclusión
Este análisis nos ayudó a identificar los elementos básicos de los lenguajes de programación en los archivos que revisamos. Cada concepto está presente en diferentes partes del código, y ahora sabemos cómo se estructuran y funcionan los programas en C. Esto es útil para entender mejor cómo se hacen las cosas en programación.

## Repositorio en Github
https://github.com/pawiiowo/paradigmas-portafolio

## Fuentes
- GeeksforGeeks. (n.d.). *Memory Layout of C Programs*. Recuperado de https://www.geeksforgeeks.org/memory-layout-of-c-program/
- TutorialsPoint. (n.d.). *C Programming - Data Types*. Recuperado de https://www.tutorialspoint.com/cprogramming/c_data_types.htm
- Programiz. (n.d.). *Dynamic Memory Allocation in C*. Recuperado de https://www.programiz.com/c-programming/c-dynamic-memory-allocation