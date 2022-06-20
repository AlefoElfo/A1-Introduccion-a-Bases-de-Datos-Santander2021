[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 02`](../Readme.md) > `Reto 3`
	
## Reto 3: Agrupamientos

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Escribir consultas que permitan responder algunas preguntas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `tienda`, escribe consultas que permitan responder las siguientes preguntas.

- ¿Cuántos registros hay por cada uno de los puestos?
~~~
	select nombre, count(nombre)
	from puesto
	group by nombre
	order by nombre asc;
~~~
- ¿Cuánto dinero se paga en total por puesto?
~~~
	select nombre, sum(salario)
	from puesto
	group by nombre
	order by nombre asc;
~~~
- ¿Cuál es el número total de ventas por vendedor?
~~~
	select id_empleado, count(id_venta)
	from venta
	group by id_empleado
	order by id_empleado asc;
~~~
- ¿Cuál es el número total de ventas por artículo?
~~~
	select id_articulo, count(id_venta)
	from venta
	group by id_articulo
	order by id_articulo asc;
~~~
<br/>

[`Anterior`](../Ejemplo-03/Readme.md) | [`Siguiente`](../Readme.md)         

</div>
