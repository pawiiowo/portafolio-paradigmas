+++
draft = false
title = 'Practica 1: Elementos básicos de los lenguajes de programación'
summary = 'Reporte de la Practica 2'
+++

![Logo de la escuela](images/logouabc.png)
![Logo de la facultad](images/logofiad.png)

# Programa de Biblioteca

## Introducción  
El programa implementa un sistema de gestión de biblioteca que permite:  
- Administrar libros (físicos y digitales) y miembros.  
- Realizar préstamos y devoluciones.  
- Gestionar la memoria utilizada.  

**Módulos principales**:  
1. `biblioteca.py` (lógica central)  
2. `biblioteca_web.py` (interfaz web con Flask)  
3. `memory_management.py` (seguimiento de memoria)  

---

## Estructura y Funcionamiento  

### Clases `Book` y `DigitalBook`  
- **`Book`**:  
  - Representa libros físicos.  
  - Atributos: `title`, `author`, `id`, etc.  
  - Métodos: `to_dict()`, `from_dict()`.  

- **`DigitalBook`** (hereda de `Book`):  
  - Añade atributo `file_format`.  

### Gestión de Memoria  
- Actualiza contadores en `__init__` (creación) y `__del__` (destrucción).  

### Clase `Member`  
- Atributos: `name`, `member_id`, `issued_books` (lista de libros prestados).  
- Registra asignaciones/liberaciones de memoria.  

### Clase `Library`  
**Funcionalidades**:  
- Agregar/mostrar libros y miembros.  
- Préstamos (`issue_book`) y devoluciones (`return_book`) con validaciones.  
- Persistencia en JSON:  
  - `save_library_to_file()`  
  - `load_library_from_file()`  

---

## Interfaz Web (`biblioteca_web.py`)  
**Tecnología**: Flask (API REST).  

**Endpoints**:  
- `/books`: GET/POST (listar/agregar libros).  
- `/members`: GET/POST (gestionar miembros).  
- `/issue_book`: POST (préstamos).  
- `/return_book`: POST (devoluciones).  

---

## Gestión de Memoria (`memory_management.py`)  
**Clase `MemoryManagement`**:  
- Rastrea:  
  - `heap_allocations` (asignaciones).  
  - `heap_deallocations` (liberaciones).  
- Método: `display_memory_usage()` (muestra uso actual).  

---

## Conclusión  
- **POO**: Uso de clases y herencia (`Book`/`DigitalBook`).  
- **Persistencia**: Almacenamiento en JSON.  
- **Modularidad**: Separación clara entre lógica, interfaz web y memoria.  

**Repositorio**:  
[https://github.com/pawiiowo/portafolio-paradigmas](https://github.com/pawiiowo/portafolio-paradigmas)  