<h1 align="center">
EJERCICIOS DE BASE DE DATOS<br>
(EMPRESA TELEFÓNICA)
</h1>

---

##### CREAR LA BASE DE DATOS
```sql
CREATE DATABASE empresa_telefonica;
```

##### MOSTRAR LA BASE DE DATOS
```sql
SHOW DATABASE;
```

##### USAR LA BASE DE DATOS
```sql
USE empresa_telefonica;
```

##### CREAR LA TABLA Y SUS CAMPOS
```sql
CREATE TABLE user (
    user_id INT AUTO_INCREMENT  NOT NULL,
    username VARCHAR(20)        NOT NULL,
    nombre VARCHAR(20)            NOT NULL,
    sexo VARCHAR(1)             NOT NULL,
    nivel TINYINT               NOT NULL,
    email VARCHAR(50)           NOT NULL, 
    telefono VARCHAR(20)        NOT NULL, 
    marca VARCHAR(20)           NOT NULL, 
    compania VARCHAR(20)        NOT NULL,
    saldo FLOAT                 NOT NULL,
    activo BOOLEAN              NOT NULL,
    PRIMARY KEY (user_id)
)ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
```

##### MOSTRAR LA TABLA
```sql
SHOW TABLE;
```

##### MOSTRAR LAS CARACTERÍSTICAS DE LA TABLA
```sql
DESCRIBE user;
```

##### INSERCIÓN DE REGISTROS

```sql
INSERT INTO user (username, nombre, sexo, nivel, email, telefono, marca, compania, saldo, activo)
VALUES ('BRE2271','BRENDA','M',2,'brenda@live.com','655-330-5736','SAMSUNG','IUSACELL',100,1),
('OSC4677','OSCAR','H',3,'oscar@gmail.com','655-143-4181','LG','TELCEL',0,1),
('JOS7086','JOSE','H',3,'francisco@gmail.com','655-143-3922','NOKIA','MOVISTAR',150,1),
('LUI6115','LUIS','H',0,'enrique@outlook.com','655-137-1279','SAMSUNG','TELCEL',50,1),
('LUI7072','LUIS','H',1,'luis@hotmail.com','655-100-8260','NOKIA','IUSACELL',50,0),
('DAN2832','DANIEL','H',0,'daniel@outlook.com','655-145-2586','SONY','UNEFON',100,1),
('JAQ5351','JAQUELINE','M',0,'jaqueline@outlook.com','655-330-5514','BLACKBERRY','AXEL',0,1),
('ROM6520','ROMAN','H',2,'roman@gmail.com','655-330-3263','LG','IUSACELL',50,1),
('BLA9739','BLAS','H',0,'blas@hotmail.com','655-330-3871','LG','UNEFON',100,1),
('JES4752','JESSICA','M',1,'jessica@hotmail.com','655-143-6861','SAMSUNG','TELCEL',500,1),
('DIA6570','DIANA','M',1,'diana@live.com','655-143-3952','SONY','UNEFON',100,0),
('RIC8283','RICARDO','H',2,'ricardo@hotmail.com','655-145-6049','MOTOROLA','IUSACELL',150,1),
('VAL6882','VALENTINA','M',0,'valentina@live.com','655-137-4253','BLACKBERRY','AT&T',50,0),
('BRE8106','BRENDA','M',3,'brenda2@gmail.com','655-100-1351','MOTOROLA','NEXTEL',150,1),
('LUC4982','LUCIA','M',3,'lucia@gmail.com','655-145-4992','BLACKBERRY','IUSACELL',0,1),
('JUA2337','JUAN','H',0,'juan@outlook.com','655-100-6517','SAMSUNG','AXEL',0,0),
('ELP2984','ELPIDIO','H',1,'elpidio@outlook.com','655-145-9938','MOTOROLA','MOVISTAR',500,1),
('JES9640','JESSICA','M',3,'jessica2@live.com','655-330-5143','SONY','IUSACELL',200,1),
('LEX4015','LETICIA','M',2,'leticia@yahoo.com','655-143-4019','BLACKBERRY','UNEFON',100,1),
('LUI1076','LUIS','H',3,'luis2@live.com','655-100-5085','SONY','UNEFON',150,1),
('HUG5441','HUGO','H',2,'hugo@live.com','655-137-3935','MOTOROLA','AT&T',500,1);
```

---

<h1 align="center">CONSULTAS</h1>

##### Ejercicio 1. Listar los nombres de los usuarios
<details>
<summary>Solución</summary>

```sql
SELECT nombre FROM user;
```
</details>

##### Ejercicio 2. Calcular el saldo máximo de los usuarios de sexo "Mujer"
<details>
<summary>Solución</summary>

```sql
SELECT MAX(saldo) FROM user WHERE sexo = 'M';
```
</details>

##### Ejercicio 3. Listar nombre y teléfono de los usuarios con teléfono NOKIA, BLACKBERRY o SONY
<details>
<summary>Solución</summary>

```sql
SELECT nombre, telefono 
FROM user
WHERE marca IN ('NOKIA', 'BLACKBERRY', 'SONY');
```
</details>

##### Ejercicio 4. Contar los usuarios sin saldo o inactivos
<details>
<summary>Solución</summary>

```sql
SELECT COUNT(*) 
FROM user 
WHERE saldo = 0 OR activo = 0;
```
</details>

##### Ejercicio 5. Listar el username de los usuarios con nivel 1, 2 o 3
<details>
<summary>Solución</summary>

```sql
SELECT username 
FROM user
WHERE nivel IN (1, 2, 3);
```
</details>

##### Ejercicio 6. Listar los números de teléfono con saldo menor o igual a $300
<details>
<summary>Solución</summary>

```sql
SELECT telefono 
FROM user
WHERE saldo <= 300;
```
</details>

##### Ejercicio 7. Calcular la suma de los saldos de los usuarios de la compañía telefónica NEXTEL
<details>
<summary>Solución</summary>

```sql
SELECT SUM(saldo) 
FROM user 
WHERE compania = 'NEXTEL';
```
</details>

##### Ejercicio 8. Contar el número de usuarios por compañía telefónica
<details>
<summary>Solución</summary>

```sql
SELECT compania, COUNT(*) 
FROM user
GROUP BY compania;
```
</details>

##### Ejercicio 9. Contar el número de usuarios por nivel
<details>
<summary>Solución</summary>

```sql
SELECT nivel, COUNT(*) 
FROM user
GROUP BY nivel;
```
</details>

##### Ejercicio 10. Listar el username de los usuarios con nivel 2
<details>
<summary>Solución</summary>

```sql
SELECT username
FROM user 
WHERE nivel = 2;
```
</details>

##### Ejercicio 11. Mostrar el email de los usuarios que usan gmail
<details>
<summary>Solución</summary>

```sql
SELECT email 
FROM user
WHERE email LIKE '%@gmail.com';
```
</details>

##### Ejercicio 12. Listar nombre y teléfono de los usuarios con teléfono LG, SAMSUNG o MOTOROLA
<details>
<summary>Solución</summary>

```sql
SELECT nombre, telefono 
FROM user
WHERE marca IN ('LG', 'SAMSUNG', 'MOTOROLA');
```
</details>

##### Ejericio 13. Contar el número de usuarios por marca de teléfono
<details>
<summary>Solución</summary>

```sql
SELECT marca, COUNT(*) 
FROM user
GROUP BY marca;
```
</details>

##### Ejercicio 14. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG
<details>
<summary>Solución</summary>

```sql
SELECT nombre, telefono 
FROM user
WHERE marca <> 'LG';
```
</details>

##### Ejercicio 15. Listar las diferentes compañías en orden alfabético ascendentemente
<details>
<summary>Solución</summary>

```sql
SELECT DISTINCT compania 
FROM user
ORDER BY compania ASC;
```
</details>

##### Ejercicio 16. Calcular la suma de los saldos de los usuarios de la compañía telefónica UNEFON
<details>
<summary>Solución</summary>

```sql
SELECT SUM(saldo) 
FROM user
WHERE compania = 'UNEFON';
```
</details>

##### Ejercicio 17. Mostrar el email de los usuarios que usan hotmail
<details>
<summary>Solución</summary>

```sql
SELECT email 
FROM user
WHERE email LIKE '%@hotmail.com';
```
</details>

##### Ejercicio 18. Listar los nombres de los usuarios sin saldo o inactivos
<details>
<summary>Solución</summary>

```sql
SELECT nombre 
FROM user
WHERE saldo = 0 OR activo = 0;
```
</details>

##### Ejericio 19. Listar el username y teléfono de los usuarios con compañía telefónica IUSACELL o TELCEL
<details>
<summary>Solución</summary>

```sql
SELECT usuario, telefono 
FROM user
WHERE compania IN ('IUSACELL', 'TELCEL');
```
</details>

##### Ejercicio 20. Listar las diferentes marcas de celular en orden alfabético ascendentemente
<details>
<summary>Solución</summary>

```sql
SELECT DISTINCT marca 
FROM user
ORDER BY marca ASC;
```
</details>

##### Ejercicio 21. Listar las diferentes marcas de celular en orden alfabético aleatorio
<details>
<summary>Solución</summary>

```sql
SELECT DISTINCT marca 
FROM user
ORDER BY RAND();
```
</details>

##### Ejercicio 22. Listar el username y teléfono de los usuarios con compañía telefónica IUSACELL o UNEFON
<details>
<summary>Solución</summary>

```sql
SELECT usuario, telefono 
FROM user
WHERE compania IN ('IUSACELL', 'UNEFON');
```
</details>

##### Ejercicio 23. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca MOTOROLA o NOKIA
<details>
<summary>Solución</summary>

```sql
SELECT nombre, telefono 
FROM user
WHERE marca NOT IN ('MOTOROLA', 'NOKIA');
```
</details>

##### Ejercicio 24. Calcular la suma de los saldos de los usuarios de la compañia telefónica TELCEL
<details>
<summary>Solución</summary>

```sql
SELECT SUM(saldo) 
FROM user
WHERE compania = 'TELCEL';
```
</details>

##### Ejericio 25. Muestra todos los datos de los usuarios que tengan un celular de la marca MOTOROLA 
<details>
<summary>Solución</summary>

```sql
SELECT *
FROM user
WHERE marca = 'MOTOROLA';
```
</details>

##### Ejericio 26. Muestra los siguientes datos: nombre del usuario, email, teléfono de los usuarios de la compañia MOVISTAR
<details>
<summary>Solución</summary>

```sql
SELECT nombre, email, telefono, compania
FROM user
WHERE compania = 'MOVISTAR';
```
</details>

##### Ejericio 27. Muestra todos los datos del usuario 10
<details>
<summary>Solución</summary>

```sql
SELECT *
FROM user
WHERE username = 10;
```
</details>

##### Ejericio 28. Muestra el nombre y saldo de los usuarios con saldo mayor o igual a $200
<details>
<summary>Solución</summary>

```sql
SELECT nombre, saldo
FROM user
WHERE saldo >= 200;
```
</details>

##### Ejericio 29. Muestra el nombre y teléfono de los usuarios que son solo mujeres
<details>
<summary>Solución</summary>

```sql
SELECT nombre, telefono
FROM tblUsuarios
WHERE sexo = 'M';
```
</details>

##### Ejericio 30. Muestra el nombre de la persona y su sexo cuyo sean hombres y su saldo este entre $100 y $200  
<details>
<summary>Solución</summary>

```sql
SELECT nombre, sexo
FROM tblUsuarios
WHERE saldo BETWEEN 100 AND 200;
```
</details>