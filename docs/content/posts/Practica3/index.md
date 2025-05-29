+++
draft = false
title = 'Practica 1: Elementos básicos de los lenguajes de programación'
summary = 'Reporte de la Practica 3'
+++

![Logo de la escuela](images/logouabc.png)
![Logo de la facultad](images/logofiad.png)

# Práctica 3: Haskell - Aplicación de Lista de Tareas

## Información General  
**Universidad Autónoma de Baja California**  
**Facultad de Ingeniería, Arquitectura y Diseño**  
**Paradigmas de la Programación**  
**Grupo: 941**  
**Alumno: Paulina Mendoza Quiroz**  
**Matrícula: 372532**  

---

## Instalación  
- **Subsistema de Windows para Linux (WSL)**  
  - Permite ejecutar herramientas de Linux en Windows.  
  - Características: sistemas de archivos, aplicaciones GUI, aceleración de CPU, integración con Docker y VS Code.  

---

## Aplicación de Lista de Tareas en Haskell  

### Funcionalidades  
1. Añadir tareas  
2. Eliminar tareas  
3. Mostrar tarea específica  
4. Editar tareas  
5. Listar todas las tareas  
6. Invertir orden de tareas  
7. Limpiar lista  
8. Salir de la aplicación  

### Estructura del Programa  
- **main.hs**:  
  - Punto de entrada del programa.  
  - Carga variables de entorno desde `.env`.  
  - Si existe `WEBSITE`, abre la URL en el navegador.  
  - Llama a la función `prompt` con lista vacía.  

- **Lib.hs**:  
  - Contiene la lógica principal.  
  - Tareas representadas como `String`.  
  - Funciones:  
    - `putTodo`: Muestra tarea con su índice.  
    - `prompt`: Bucle principal de la interfaz.  
    - `interpret`: Procesa comandos del usuario.  

### Características de Haskell Utilizadas  
- Pureza y IO Monad  
- Inmutabilidad  
- Pattern Matching  
- Recursión  

---

## Conclusión  
La aplicación demuestra los principios de Haskell:  
- Separación clara entre lógica pura y operaciones de I/O.  
- Uso de estructuras inmutables.  
- Implementación de funcionalidades mediante recursión y pattern matching.  