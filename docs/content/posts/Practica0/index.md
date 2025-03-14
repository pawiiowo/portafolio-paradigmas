+++
date = '2025-02-21T10:18:14-08:00'
draft = true
title = 'Practica 0:  Uso de repositorios'
summary = 'Reporte de la practica 0'
+++


<div style="text-align: center;">
  <img src="images/logouabc.png" alt="Logo de la escuela" style="width: 150px; height: auto;">
  <img src="images/logofiad.png" alt="Logo de la facultad" style="width: 150px; height: auto;">

  <h1>Universidad Autónoma de Baja California</h1>
  <h2>Facultad de Ingeniería, Arquitectura y Diseño</h2>
  <h3>Paradigmas de la Programación</h3>

  <p><strong>Nombre del alumno:</strong> Paulina Mendoza Quiroz</p>
  <p><strong>Matrícula:</strong> 372532</p>
  <p><strong>Grupo:</strong> 941</p>
  <p><strong>Fecha:</strong> 14 de Marzo del 2025</p>
</div>

# Práctica 0: Uso de repositorios

## Introducción
Este reporte muestra mi proceso de aprendizaje sobre cómo utilizar Markdown, Hugo, Git y GitHub Actions para crear y desplegar una página web estática. A través de este proceso, he adquirido conocimientos sobre la creación de contenido con Markdown, la gestión de versiones con Git, la generación de sitios web estáticos con Hugo, y la automatización de despliegues con GitHub Actions.

## Aprendiendo Markdown
Markdown es un lenguaje de marcado ligero que permite formatear texto de manera sencilla. Exploré conceptos básicos como encabezados, listas, enlaces, imágenes, código, negritas y cursivas. Estos conceptos me permitieron estructurar el contenido de mi página web de manera clara y eficiente.

## Configuración de Hugo
Hugo es un generador de sitios estáticos rápido y flexible. Primero, instalé Hugo en mi sistema operativo. Luego, usé el comando `hugo new site` para generar la estructura básica del sitio. Después, elegí un tema de Hugo y lo agregué a mi proyecto. Por último, creé contenido usando el comando `hugo new posts/---.md`. Hugo me permitió generar un sitio web estático de manera rápida y sencilla, con la posibilidad de personalizar el diseño y la estructura.

## Uso de Git y GitHub
Git es un sistema de control de versiones que me permitió gestionar los cambios en mi proyecto. Primero, inicialicé un repositorio local con `git init`. Luego, agregué y confirmé cambios usando `git add .` y `git commit -m`. Después, creé una cuenta en GitHub y un repositorio remoto. Finalmente, subí los cambios a GitHub usando `git remote add origin` y `git push -u origin main`.

## Automatización con GitHub Actions
GitHub Actions es una herramienta que permite automatizar tareas como la generación y despliegue de sitios web. Configuré un flujo de trabajo para generar mi sitio estático con Hugo y desplegarlo en GitHub Pages. Primero, creé un archivo YAML en la carpeta `.github/workflows` para definir el flujo de trabajo. El workflow se activa con cada `push` en la rama `main` y ejecuta los siguientes pasos: checkout del código, instalación de Hugo, generación del sitio y despliegue en GitHub Pages. 

## Configuración de SSH Key
Para poder interactuar con GitHub de manera segura, configuré una clave SSH en mi sistema. Primero, generé la clave SSH usando PowerShell con el comando `ssh-keygen`. Luego, copié la clave pública y la agregué en la sección de SSH Keys de mi cuenta de GitHub. Finalmente, verifiqué la conexión usando `ssh -T git@github.com`. Esto me permitió autenticarme de manera segura sin necesidad de ingresar credenciales cada vez que interactuaba con GitHub.

## Creación de Directorios y Archivos con Git Bash
Aprendí a utilizar Git Bash para crear directorios y archivos en mi proyecto. Usé el comando `mkdir nombre-del-directorio` para crear nuevas carpetas y `touch nombre-del-archivo.md` para crear nuevos archivos Markdown. También usé `cd` para moverme entre carpetas y `ls` para listar los archivos. 

## Conclusión
A través de este proceso, he aprendido a utilizar Markdown para crear contenido, Hugo para generar sitios web estáticos, Git para gestionar versiones, y GitHub Actions para automatizar despliegues. 

## Repositorio en GitHub
https://github.com/pawiiowo/paradigmas-portafolio

## Fuentes
- Fazt Code - Markdown, Curso Práctico para principiantes y desarrolladores [https://www.youtube.com/watch?v=oxaH9CFpeEE]
- Introducción a la línea de comando en Windows [https://www.youtube.com/watch?v=Dj5WhV9vV4I]
- Cómo crear directorios (carpetas) y archivos con Git Bash [https://www.youtube.com/watch?v=hNEPN2er1j4]
- Introducción a la línea de comandos Línux.Comandos básicos [https://www.youtube.com/watch?v=2lbCg7UxayU]
- Fazt Code - Git and Github | Practical Course from Scratch [https://www.youtube.com/watch?v=HiXLkL42tMU]
- Quickstart en Hugo [https://gohugo.io/getting-started/quick-start/]
- Quickstart en Gitlab [https://docs.gitlab.com/ee/tutorials/hugo/]
- Generar llave SSH en Windows con PowerShell [https://www.youtube.com/shorts/yyKgiiECefo]