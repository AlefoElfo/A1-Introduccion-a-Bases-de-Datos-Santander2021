[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 06`](../Readme.md) > `Reto 1`
	
## Reto 1: Expresiones regulares

<div style="text-align: justify;">

### 1. Objetivos :dart: 

- Poner en práctica el uso de expresiones regulares.

### 2. Requisitos :clipboard:

1. MongoDB Compass instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `sample_airbnblistingsAndReviews`, realiza los siguientes filtros:

- Propiedades que no permitan fiestas.
```
//Filter://
{house_rules: /.*no partie.*/i}
```
- Propiedades que admitan mascotas.
```
//Este resultado da un falso positivo pues incluye "no pets"//
//Filter://
{house_rules: /.*pet.*/i}
```
- Propiedades que no permitan fumadores.
```
//Filter://
{house_rules: /.*no smoking.*/i}
```
- Propiedades que no permitan fiestas ni fumadores.
```
//Filter://
{$and: [{house_rules: /.*no smoking.*/i}, {house_rules: /.*no partie.*/i }]}
```

<br/>

[`Anterior`](../Ejemplo-01/Readme.md) | [`Siguiente`](../Readme.md)

</div>
