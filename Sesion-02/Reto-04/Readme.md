[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 02`](../Readme.md) > `Reto 4`
	
## Reto 4: Subconsultas

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Escribir consultas que permitan responder a algunas preguntas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `tienda`, escribe consultas que permitan responder las siguientes preguntas.

- ¿Cuál es el nombre de los empleados cuyo sueldo es menor a $100,000?
```sql
select nombre
from empleado
where id_puesto in
	(select id_puesto
	from puesto
	where salario < 100000);
```
- ¿Cuál es la cantidad mínima y máxima de ventas de cada empleado?
```sql
select
	id_empleado, nombre_empleado, min(total), max(total)
from
	(select 
		clave,
		id_empleado, 
		(select nombre from empleado where id_empleado = venta.id_empleado) nombre_empleado,
		count(*) total 
	from venta
	group by clave, id_empleado) vnt
group by id_empleado
;
```
- ¿Cuál es el nombre del puesto de cada empleado?
```sql
select 
	id_empleado,
	nombre,
	apellido_paterno,
	(select nombre from puesto where id_puesto = emp.id_puesto)
		as puesto
from empleado as emp;
```

<br/>

[`Anterior`](../Ejemplo-04/Readme.md) | [`Siguiente`](../Readme.md)            

</div>
