[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 02`](../Readme.md) > `Reto 2`
	
## Reto 2: Funciones de agrupamiento

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Escribir consultas que permitan responder a algunas preguntas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `tienda`, escribe consultas que permitan responder las siguientes preguntas.

- ¿Cuál es el promedio de salario de los puestos?
	select avg(salario)
	from puesto;
- ¿Cuántos artículos incluyen la palabra `Pasta` en su nombre?
	select nombre
	from articulo
	where nombre like '%pasta%';
- ¿Cuál es el salario mínimo y máximo?
	select min(salario), max(salario)
	from puesto;
- ¿Cuál es la suma del salario de los últimos cinco puestos agregados?
	select sum(salario)
	from 
		(select id_puesto, salario
		from puesto
		order by id_puesto desc
		limit 5) as finales;


<br/>

[`Anterior`](../Ejemplo-02/Readme.md) | [`Siguiente`](../Readme.md)      

</div> 
