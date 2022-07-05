[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 05`](../Readme.md) > `Reto 1`
	
## Reto 1: Colecciones, Documentos y Proyecciones

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Proyectar columnas sobre distintos documentos para repasar algunos conceptos.

### 2. Requisitos :clipboard:

1. MongoDB Compass instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `sample_mflix`, proyecta los datos que se solicitan.

- Fecha, nombre y texto de cada comentario.
~~~mongodb
{date: 1, name: 1, text: 1, _id: 0}
~~~
- Título, elenco y año de cada película.
~~~mongodb
{titel: 1, cast: 1, year: 1, _id: 0}
~~~	
- Nombre y contraseña de cada usuario.
~~~mongodb
{name: 1, password: 1, _id: 0}
~~~

<br/>

[`Anterior`](../Ejemplo-01/Readme.md) | [`Siguiente`](../Readme.md)

</div>
