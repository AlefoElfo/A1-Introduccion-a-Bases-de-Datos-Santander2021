[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 01`](../Readme.md) > `Reto 2`
	
## Reto 2: Estructura básica de una consulta

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Escribir consultas que permitan responder a algunas preguntas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `cursos` (*tienda*), escribe consultas que permitan responder las siguientes preguntas.

- ¿Cuál es el nombre de los empleados con el puesto 4?
~~~
	select nombre
	from empleado
	where id_puesto = 4
	;
~~~
- ¿Qué puestos tienen un salario mayor a $10,000?
~~~
	select nombre
	from puesto
	where salario > 10000
	;
~~~
- ¿Qué artículos tienen un precio mayor a $1,000 y un iva mayor a 100?
~~~
	select nombre
	from articulo
	where precio > 1000
	and iva > 100
	;
~~~
- ¿Qué ventas incluyen los artículos 135 o 963 y fueron hechas por los empleados 835 o 369?
~~~
	select id_venta
	from venta
	where id_articulo in (135, 963)
	and id_empleado in (835, 369)
	;
~~~

<br/>

[`Anterior`](../Ejemplo-03/Readme.md) | [`Siguiente`](../Readme.md)

</div>
