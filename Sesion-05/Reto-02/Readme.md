[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 05`](../Readme.md) > `Reto 2`
	
## Reto 2: Filtros básicos

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Proyectar columnas sobre distintos documentos para repasar algunos conceptos.

### 2. Requisitos :clipboard:

1. MongoDB Compass instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `sample_mflix`, agrega proyeccciones, filtros, ordenamientos y límites que permitan contestar las siguientes preguntas:

- ¿Qué comentarios ha hecho Greg Powell?
~~~mongodb
//Filter://
{name: /Greg Powell/}
//Project://
{name: 1, text: 1}
~~~
- ¿Qué comentarios han hecho Greg Powell o Mercedes Tyler?
~~~mongodb
//Filter://
{$or: [{name: /Greg Powell/}, {name: /Mercedes Tyler/}]}
//Project://
{name: 1, text: 1}
~~~
- ¿Cuál es el máximo número de comentarios en una película?
~~~mongodb
//Project://
{num_mflix_comments: 1}
//Sort://
{num_mflix_comments: -1}
//Limit://
1
~~~
- ¿Cuál es título de las cinco películas más comentadas?
~~~mongodb
//Project://
{title: 1, num_mflix_comments: 1}
//Sort://
{num_mflix_comments: -1}
//Limit://
5
~~~

<br/>

[`Anterior`](../Ejemplo-02/Readme.md) | [`Siguiente`](../Readme.md)

</div>
