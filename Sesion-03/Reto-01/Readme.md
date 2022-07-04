[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 03`](../Readme.md) > `Reto 1`
	
## Reto 1: Agrupamientos y subconsultas

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Escribir consultas que permitan responder a algunas preguntas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `tienda`, escribe consultas que permitan responder las siguientes preguntas.

- ¿Cuál es el nombre de los empleados que realizaron cada venta?
~~~sql
	select id_venta, e.nombre, e.apellido_paterno
	from venta v
	join empleado e
	on v.id_empleado = e.id_empleado
	order by id_venta
	;
~~~
- ¿Cuál es el nombre de los artículos que se han vendido?
~~~sql
	select id_venta, a.id_articulo, a.nombre
	from articulo a
	join venta v
	on a.id_articulo = v.id_articulo
	order by id_venta
	;
~~~
- ¿Cuál es el total de cada venta?
~~~sql
	select id_venta, sum(a.precio)
	from venta v
	join articulo a
	on v.id_articulo = a.id_articulo
	group by id_venta
	order by id_venta
	;
~~~

<br/>

[`Anterior`](../Ejemplo-01/Readme.md) | [`Siguiente`](../Readme.md)

</div>
