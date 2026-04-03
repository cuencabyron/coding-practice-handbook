<h1 align="center">
EJERCICIOS DE BASE DE DATOS<br>
(TIENDA INFORMÁTICA)
</h1>

---

##### CREAR LA BASE DE DATOS
<details>
<summary>Solución</summary>

```sql
CREATE DATABASE tienda_informatica;
```
</details>

##### MOSTRAR LA BASE DE DATOS
<details>
<summary>Solución</summary>

```sql
SHOW DATABASE;
```
</details>

##### USAR LA BASE DE DATOS
<details>
<summary>Solución</summary>

```sql
USE tienda_informatica;
```
</details>

##### CREAR LA TABLA Y SUS CAMPOS
<details>
<summary>Solución</summary>

```sql
CREATE TABLE fabricante (
    fabricante_id INT             NOT NULL,
    nombre VARCHAR(30)            NOT NULL,
    PRIMARY KEY (fabricante_id)
)ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

CREATE TABLE articulo (
    articulo_id INT           NOT NULL,
    nombre VARCHAR(30)        NOT NULL,
    precio DECIMAL(10,2)      NOT NULL,
    PRIMARY KEY (articulo_id),
    CONSTRAINT fk_articulo_fabricante
        FOREIGN KEY (fabricante_id) REFERENCES fabricante(fabricante_id)
)ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
```
</details>


##### MOSTRAR LAS TABLAS
<details>
<summary>Solución</summary>

```sql
SHOW TABLES;
```
</details>


##### MOSTRAR LOS ATRIBUTOS DE LA TABLA
<details>
<summary>Solución</summary>

```sql
DESCRIBE fabricante;
DESCRIBE articulo;
```
</details>

##### INSERCIÓN DE REGISTROS
<details>
<summary>Solución</summary>

```sql
INSERT INTO fabricante (fabricante_id, nombre) VALUES (1, 'Kingston'), (2, 'Adata'), (3, 'Logitech'), (4, 'Lexar'), (5, 'Seagate');

INSERT INTO articulo (articulo_id, nombre, precio, fabricante_id) VALUES (1, 'Teclado', 100.00, 3), (2, 'Disco Duro 300 GB', 500.00, 5), (3, 'Mouse', 80.00, 3), 
(4, 'Memoria USB', 140.00, 4), (5, 'Memoria RAM', 290.00, 1), (6, 'Disco Duro Extraible 250 GB', 650.00, 5), (7, 'Memoria USB', 279.00, 1), 
(8, 'DVD-ROM', 450.00, 2), (9, 'CD-ROM', 200.00, 2), (10, 'Tarjeta de Red', 180.00, 3);
```
</details>

---

<h1 align="center">CONSULTAS</h1>

##### Ejercicio 1. Obtener todos los datos de los artículos de la tienda  
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 2.Obtener los nombres de los artículos de la tienda 
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 3. Obtener los nombres y precio de los artículos de la tienda 
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 4. Obtener los nombres de los artículos sin repeticiones 
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 5. Obtener todos los datos del artículo cuyo id sea "5"
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 6. Obtener todos los datos del artículo cuyo nombre del producto es "Teclado"
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 7. Obtener todos los datos de la memoria RAM y memorias USB
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 8. Obtener todos los datos de los artículos que empiezan con "M"
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 9. Obtener el nombre de los artículos donde el precio sea $100 
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 10. Obtener el nombre de los artículos donde el precio sea mayor a $200
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 11. Obtener todos los datos de los artículos cuyo precio este entre $100 y $350
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 12. Obtener el precio medio de todos los artículos
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 13. Obtener el precio medio de los artículos cuyo id de fabricante sea 2 
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 14. Obtener el nombre y precio de los artículos ordenados por nombre 
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 15. Obtener todos los datos de los artículos ordenados descendentemente por precio
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 16. Obtener el nombre y precio de los artículos cuyo precio sea mayor a $250 y ordenarlos descendentemente por nombre
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 17. Obtener un listado completo de los artículos, incluyendo por cada artículo sus datos asi como los del fabricante
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 18. Obtener el id del artículo, nombre del artículo y nombre del fabricante de todos los productos en venta
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 19. Obtener el nombre y precio de los artículos donde el fabricante sea "Logitech" ordenados alfabéticamente por nombre del artículo
<details>
<summary>Solución</summary>

```sql

```
</details>

##### Ejercicio 20. Obtener el nombre, precio y nombre del fabricante de los artículos que son marca "Lexar" o "Kingston" ordenados descendentemente por precio 
<details>
<summary>Solución</summary>

```sql

```
</details>