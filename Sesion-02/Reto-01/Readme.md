[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 02`](../Readme.md) > `Reto 1`
	
## Reto 1: Agrupamientos y subconsultas

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Escribir consultas que permitan responder algunas preguntas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `tienda`, escribe consultas que permitan responder las siguientes preguntas.

- ¿Qué artículos incluyen la palabra `Pasta` en su nombre?
~~~
	select nombre
	from articulo
	where nombre
	like '%Pasta%'
	;
~~~
- ¿Qué artículos incluyen la palabra `Cannelloni` en su nombre?
~~~
	select nombre
	from articulo
	where nombre
	like '%Cannelloni%'
	;
~~~
- ¿Qué nombres están separados por un guión (`-`) por ejemplo `Puree - Kiwi`?
~~~
	select nombre
	from articulo
	where nombre
	like '% - %' #Espacio entre guiones para evitar guiones internos
	;
~~~
	
<br/>

[`Anterior`](../Ejemplo-01/Readme.md) | [`Siguiente`](../Readme.md#funciones-de-agrupamiento)   


</div>
