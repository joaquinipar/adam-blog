---
layout: post
title:  Método del Camino Crítico
date:   2021-01-31 15:30:00 +0300
description: Algoritmo para el calculo de tiempo en un proyecto. # Add post description (optional)
img: project-management.jpg # Add image post (optional)
tags: [Blog, Programming, Sistemas, Systems]
author: Joaquin Ipar # Add name author (optional)
---

## Critical Path Method

Este método sirve para:

- Identificar las eventos críticas de un proyecto.

- Visualizar el avance de un proyecto.

- Visualizar e identiciar las dependencias las tareas.

- Determinar la duración total del proyecto.

## Elementos

### Nodo
![nodo](https://github.com/joaquinipar/blog/blob/gh-pages/assets/img/node.png?raw=true)

Punto que indica el principio y el final del evento.

### Fecha Temprana
![nodo temprano](https://github.com/joaquinipar/blog/blob/gh-pages/assets/img/node_temprano.png?raw=true)

Es la fecha más próxima de ocurrencia del evento.

### Fecha Tardía
![nodo temprano](https://github.com/joaquinipar/blog/blob/gh-pages/assets/img/node_tardia.png?raw=true)

Es la fecha más lejana de ocurrencia del evento.

### Tarea
![tarea](https://github.com/joaquinipar/blog/blob/gh-pages/assets/img/flecha.png?raw=true)

Indica consumo de tiempo

### Tarea Ficticia
![tarea](https://github.com/joaquinipar/blog/blob/gh-pages/assets/img/flecha_punteada.png?raw=true)

Es una tarea que no consume tiempo. Solo sirve para crear dependencias.

## Lista de Actividades

| Tarea | Duración | Dependencias |
| ----------- | ----------- | ----------- |
| A | 3 | - |
| B | 2 | A |

![tarea](https://github.com/joaquinipar/blog/blob/gh-pages/assets/img/ejemplo_npm.png?raw=true)

## Intervalo de Flotamiento

Cantidad de tiempo que se puede demorar una tarea sin afectar la fecha de finalización del proyecto.

IF = Fecha Tardía - Fecha Temprana

## Margen Total

Tiempo límite que una tarea podría retrasarse para no afectar los tiempos límites del proyectos

MT = Fecha Tardía(Nodo 2) - Fecha Temprana(Nodo 1) - Duración

## Tarea Crítica

Si se retrasa esta tarea se atrasa el proyecto completamente. Una tarea es crítica cuando se encuentra entre dos nodos críticos y su margen total es igual a cero.
Básicamente se tiene que cumplir que :
    - MT = 0
    - IF = 0

En todo CPM debe haber al menos un camino crítico.

## Camino Crítico

Un camino crítico es un conjunto de tareas críticas

- Cada tarea esta representada por una flecha
- Para cada tarea existe un único nodo inicial y final.

### Otras maneras de representar tareas...

## Diagrama de Gantt

![diagrama de gannt](https://upload.wikimedia.org/wikipedia/en/thumb/5/59/Pranjal%27s_Master%27s_Project_Timeline.png/800px-Pranjal%27s_Master%27s_Project_Timeline.png)

Nos permite ver la duración de las tareas, pero a diferencia del CPM, este diagrama no permite visualizar las dependencias de las tareas.

## PERT

Es muy similar al CPM, pero este método es probabilístico(No se explicará a fondo en este post).
