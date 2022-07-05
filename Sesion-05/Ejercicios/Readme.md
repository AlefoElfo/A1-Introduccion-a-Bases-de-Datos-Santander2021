[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 05`](../Readme.md) > `Ejercicios`
	
## Ejercicios Sesión 5

<div style="text-align: justify;">

### 1. Objetivos :dart: 

- Aplicar los conceptos adquiridos durante la sesión.

### 2. Requisitos :clipboard:

1. MongoDB Compass instalado.

### 3. Desarrollo :rocket:

Las consultas se realizarán sobre la base `sample_training`.

Todas las consultas que realices deberás mantenerlas dentro del MongoDB Compass. Para hacer esto, da clic en el botón con los puntos `···` y en `Toogle Query History`. Busca la última consulta y agrégala a favoritos presionando el ícono con la estrella :star:.

1. Obtén los datos de contacto de cada compañía.
```
//Project://
{name: 1, homepage_url: 1, twitter_username: 1, email_address: 1, phone_number: 1}
```
2. Obtén el identificador de la clase de cada calificación.
```
//Project://
{class_id: 1, "scores.score": 1}
```
3. Obtén el nombre de todas las compañias fundadas en octubre.
```
//Filter://
{founded_month: 10}
//Project://
{name: 1}
```
4. Obtén el nombre de todas las compañías fundadas en 2008.
```
//Filter://
{founded_year: 2008}
//Project://
{name: 1}
```
5. Obtén todos los *post* del autor `machine`.
```
//Filter://
{author: "machine"}
//Project://
{title: 1, body: 1}
```
6. Obtén todas las calificaciones provenientes de los grupos `357`, `57` y `465`.
```
//Filter://
{$or: [{class_id: 357, class_id: 57, class_id: 465}]}
//Project://
{class_id: 1, "scores.score": 1}
```
7. Obtén todas las compañías fundadas en octubre del 2008.
```
//Filter://
{$and: [{founded_month: 10, founded_year: 2008}]}
//Project://
{name: 1}
```
8. Obtén todas las compañias con más de 50 empleados. 
```
//Filter://
{number_of_employees: {$gt: 50}}
```
9. Obtén las rutas con un número de paradas entre 1 y 5.
```
//Filter://
{stops: {$in: [1,2,3,4,5]}}
```
10. Obtén la empresa con el menor número de empleados.
```
//Filter://
{number_of_employees: {$ne: null}}
//Sort://
{number_of_employees: 1}
//Limit//
1
```
11. Obtén la empresa con el mayor número de empleados.
```
{number_of_employees: {$ne: null}}
//Sort://
{number_of_employees: -1}
//Limit//
```
12. Obtén el viaje con mayor duración.
```
//Sort://
{tripduration: -1}
```
13. Obtén el viaje con menor duración.
```
//Sort://
{tripduration: 1}
```
**¡¡¡MUCHA SUERTE!!!**

<br/>

[`Anterior`](../Readme.md) | [`Siguiente`](../Readme.md)

</div>

