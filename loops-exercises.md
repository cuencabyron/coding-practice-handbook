<h1 align="center">EJERCICIOS DE BUCLES EN PROGRAMACIÓN</h1>

Este repositorio contiene una colección de ejercicios enfocados exclusivamente en el uso de estructuras repetitivas (bucles), implementados en:

- Pseudocódigo
- C++
- Python

**Contenido**

Los ejercicios incluyen:
- Lectura de múltiples datos
- Suma de valores (acumuladores)
- Conteo de ocurrencias (contadores)
- Uso de valores centinela
- Procesamiento de datos en secuencia
- Cálculo de promedios
- Clasificación de datos dentro de un ciclo

**Tipos de Bucles Utilizados**

- Para ```(for)```
Se utiliza cuando se conoce la cantidad de repeticiones.
- Mientras ```(while)```
Se utiliza cuando no se conoce cuántas veces se repetirá el proceso.
- Repetir ```(do-while)```
Se utiliza cuando el bloque debe ejecutarse al menos una vez.

**Conceptos Clave**

Durante estos ejercicios se aplican:
- Acumuladores ```(suma = suma + valor)```
- Contadores ```(contador = contador + 1)```
- Condiciones dentro de bucles
- Validación de datos
- Control de flujo

**Objetivo**

Fortalecer la lógica de programación mediante el uso de bucles para:
- Repetir procesos
- Procesar múltiples datos
- Resolver problemas de manera estructurada

**Nota**

Todos los ejercicios mantienen la misma lógica en los tres lenguajes, cambiando únicamente la sintaxís.

---

##### Ejercicio 1. Crear un programa que lea 10 números e imprima el Doble de la suma de los números
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo DobleSuma
    Definir num, suma, i Como Entero;

    suma <- 0;

    Para i <- 1 Hasta 10 Hacer
        Escribir "Ingresa numero: "
        Leer num
        suma <- suma + num
    FinPara

    Escribir "Doble de la suma:", suma * 2
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int num, suma = 0;

    for(int i = 1; i <= 10; i++) {
        cout << "Ingresa numero: ";
        cin >> num;
        suma += num;
    }

    cout << "Doble de la suma: " << suma * 2;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
suma = 0

for i in range(10):
    num = int(input("Ingresa numero: "))
    suma += num

print("Doble de la suma:", suma * 2)
```
</details>

##### Ejercicio 2. Escribir todos los números del 700 al 0, de 7 en 7
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Descendente7
    Definir i Como Entero;
	
    Para i <- 700 Hasta 0 Con Paso -7 Hacer
        Escribir i;
    FinPara
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    for(int i = 700; i >= 0; i -= 7) {
        cout << i << endl;
    }
    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
for i in range(700, -1, -7):
    print(i)
```
</details>

##### Ejercicio 3. Leer 10 números e imprimir el número mayor ingresado
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo MayorNumero
    Definir num, mayor, i Como Entero;

    i <- 1;

    Escribir "Ingresa numero: ";
    Leer num;
    mayor <- num;

    Mientras i < 10 Hacer;
        Escribir "Ingresa numero: ";
        Leer num;

        Si num > mayor Entonces
            mayor <- num;
        FinSi

        i <- i + 1;
    FinMientras

    Escribir "Mayor:", mayor;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int num, mayor, i = 1;

    cout << "Ingresa numero: ";
    cin >> num;
    mayor = num;

    while(i < 10) {
        cout << "Ingresa numero: ";
        cin >> num;

        if(num > mayor)
            mayor = num;

        i++;
    }

    cout << "Mayor: " << mayor;
    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
i = 1

num = int(input("Ingresa numero: "))
mayor = num

while i < 10:
    num = int(input("Ingresa numero: "))
    
    if num > mayor:
        mayor = num
    
    i += 1

print("Mayor:", mayor)
```
</details>

##### Ejercicio 4. Leer 10 números e imprimir el número menor ingresado
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo MenorNumero
    Definir num, menor, i Como Entero;

    i <- 1;

    Escribir "Ingresa numero: ";
    Leer num;
    menor <- num;

    Repetir
        Escribir "Ingrese numero: ";
        Leer num;

        Si num < menor Entonces
            menor <- num;
        FinSi

        i <- i + 1;
    Hasta Que i = 10;

    Escribir "Menor: ", menor;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int num, menor, i = 1;

    cout << "Ingresa numero: ";
    cin >> num;
    menor = num;

    do {
        cout << "Ingresa numero: ";
        cin >> num;

        if(num < menor)
            menor = num;

        i++;
    } while(i < 10);

    cout << "Menor: " << menor;
    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
i = 1

num = int(input("Ingresa numero: "))
menor = num

while True:
    num = int(input("Ingresa numero: "))
    
    if num < menor:
        menor = num
    
    i += 1
    
    if i == 10:
        break

print("Menor: ", menor)
```
</details>

##### Ejercicio 5. Calcular la suma de N números hasta que el usuario presione el número 7
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo SumaHasta7
    Definir num, suma Como Entero;

    suma <- 0;

    Escribir "Ingresa un número (7 para salir): ";
    Leer num;

    Mientras num <> 7 Hacer
        suma <- suma + num;

        Escribir "Ingresa un numero: ";
        Leer num;
    FinMientras

    Escribir "Suma total: ", suma;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int num, suma = 0;

    cout << "Ingresa un número (7 para salir): ";
    cin >> num;

    while(num != 7) {
        suma += num;

        cout << "Ingresa un numero: ";
        cin >> num;
    }

    cout << "Suma total: " << suma;
    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
suma = 0

num = int(input("Ingresa  un numero (7 para salir): "))

while num != 7:
    suma += num
    num = int(input("Ingresa un numero: "))

print("Suma total: ", suma)
```
</details>

##### Ejercicio 6. Diseñar un algoritmo que calcular e imprimir la suma de los números impares y pares hasta el usuario presione el número 2
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo ParesImpares
    Definir num, sumaP, sumaI Como Entero;

    sumaP <- 0;
    sumaI <- 0;

    Repetir
        Escribir "Ingrese numero (2 para salir): ";
        Leer num;

        Si num MOD 2 = 0 Entonces
            sumaP <- sumaP + num;
        SiNo
            sumaI <- sumaI + num;
        FinSi

    Hasta Que num = 2;

    Escribir "Suma pares:", sumaP;
    Escribir "Suma impares:", sumaI;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int num, sumaP = 0, sumaI = 0;

    do {
        cout << "Ingresa numero (2 para salir): ";
        cin >> num;

        if(num % 2 == 0)
            sumaP += num;
        else
            sumaI += num;

    } while(num != 2);

    cout << "Suma pares: " << sumaP << endl;
    cout << "Suma impares: " << sumaI;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
sumaP = 0
sumaI = 0

while True:
    num = int(input("Ingresa numero (2 para salir): "))

    if num % 2 == 0:
        sumaP += num
    else:
        sumaI += num

    if num == 2:
        break

print("Suma pares: ", sumaP)
print("Suma impares: ", sumaI)
```
</details>

##### Ejercicio 7. Crear un algoritmo que lea 10 números e imprima cuantos de los números ingresado fue un 5
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo ContarCinco
    Definir num, contador, i Como Entero;

    contador <- 0;

    Para i <- 1 Hasta 10 Hacer
        Escribir "Ingresa numero: ";
        Leer num;

        Si num = 5 Entonces
            contador <- contador + 1;
        FinSi
    FinPara

    Escribir "Cantidad de numeros 5: ", contador;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int num, contador = 0;

    for(int i = 1; i <= 10; i++) {
        cout << "Ingresa numero: ";
        cin >> num;

        if(num == 5)
            contador++;
    }

    cout << "Cantidad de numeros 5: " << contador;
    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
contador = 0

for i in range(10):
    num = int(input("Ingresa numero: "))
    
    if num == 5:
        contador += 1

print("Cantidad de numeros 5: ", contador)
```
</details>

##### Ejercicio 8. Crear un algoritmo que lea 10 números, e imprima al final la suma solo de los números mayores a 5 y menores a 50
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo SumaRango
    Definir num, suma, i Como Entero;

    suma <- 0;
    i <- 1:

    Mientras i <= 10 Hacer
        Escribir "Ingresa numero: ";
        Leer num;

        Si num > 5 Y num < 50 Entonces
            suma <- suma + num;
        FinSi

        i <- i + 1;
    FinMientras

    Escribir "Suma: ", suma;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int num, suma = 0, i = 1;

    while(i <= 10) {
        cout << "Ingresa numero: ";
        cin >> num;

        if(num > 5 && num < 50)
            suma += num;

        i++;
    }

    cout << "Suma: " << suma;
    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
suma = 0
i = 1

while i <= 10:
    num = int(input("Ingresa numero: "))
    
    if num > 5 and num < 50:
        suma += num
    
    i += 1

print("Suma:", suma)
```
</details>

##### Ejercicio 9. Crear un programa que lea el costo de los N productos de un cliente e imprima en pantalla el total a pagar por su compra y el número de productos comprados
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo CompraCliente
    Definir n, i Como Entero;
    Definir costo, total Como Real;

    total <- 0;

    Escribir "Ingresa cantidad de productos: ";
    Leer n;

    Para i <- 1 Hasta n Hacer
        Escribir "Ingresa costo del producto: ";
        Leer costo;
        total <- total + costo;
    FinPara

    Escribir "Total a pagar: ", total;
    Escribir "Numero de productos:", n;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int n;
    float costo, total = 0;

    cout << "Cantidad de productos: ";
    cin >> n;

    for(int i = 1; i <= n; i++) {
        cout << "Costo del producto: ";
        cin >> costo;
        total += costo;
    }

    cout << "Total a pagar: $" << total << endl;
    cout << "Numero de productos: " << n;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
n = int(input("Cantidad de productos: "))

total = 0

for i in range(n):
    costo = float(input("Costo del producto: "))
    total += costo

print("Total a pagar:", total)
print("Numero de productos:", n)
```
</details>

##### Ejercicio 10. Suponga que tiene usted una tienda y desea registrar las N ventas en una computadora. Crear un programa que lea por cada cliente, el monto total de su compra. Al final del día escriba la cantidad total de las ventas y el número de clientes atendidos
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo VentasDia
    Definir monto, totalDia Como Real;
    Definir clientes Como Entero;

    totalDia <- 0;
    clientes <- 0;

    Escribir "Ingresa monto de compra (0 para terminar): ";
    Leer monto;

    Mientras monto <> 0 Hacer
        totalDia <- totalDia + monto;
        clientes <- clientes + 1;

        Escribir "Ingresa monto de compra: ";
        Leer monto;
    FinMientras

    Escribir "Total de ventas:", totalDia;
    Escribir "Clientes atendidos:", clientes;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float monto, totalDia = 0;
    int clientes = 0;

    cout << "Ingresa monto (0 para terminar): ";
    cin >> monto;

    while(monto != 0) {
        totalDia += monto;
        clientes++;

        cout << "Ingresa monto: ";
        cin >> monto;
    }

    cout << "Total ventas: $" << totalDia << endl;
    cout << "Clientes atendidos: " << clientes;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
total_dia = 0
clientes = 0

monto = float(input("Ingresa monto (0 para terminar): "))

while monto != 0:
    total_dia += monto
    clientes += 1

    monto = float(input("Ingresa monto: "))

print("Total ventas:", total_dia)
print("Clientes atendidos:", clientes)
```
</details>

##### Ejercicio 11. Crear un algoritmo que lea la edad de n personas e imprima cuantas personas fueron niños (0-13), cuanto fueron jóvenes (14-29) y cuanto adulto (30 o más)
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo ClasificarEdades
    Definir n, edad, i Como Entero;
    Definir ninos, jovenes, adultos Como Entero;

    ninos <- 0;
    jovenes <- 0;
    adultos <- 0;

    Escribir "Ingrese cantidad de personas: ";
    Leer n;

    Para i <- 1 Hasta n Hacer
        Escribir "Ingrese edad: ";
        Leer edad;

        Si edad >= 0 Y edad <= 13 Entonces
            ninos <- ninos + 1;
        SinoSi edad <= 29 Entonces
            jovenes <- jovenes + 1;
        SiNo
            adultos <- adultos + 1;
        FinSi
    FinPara

    Escribir "Niños: ", ninos;
    Escribir "Jovenes: ", jovenes;
    Escribir "Adultos: ", adultos;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int n, edad;
    int ninos = 0, jovenes = 0, adultos = 0;

    cout << "Cantidad de personas: ";
    cin >> n;

    for(int i = 1; i <= n; i++) {
        cout << "Edad: ";
        cin >> edad;

        if(edad >= 0 && edad <= 13)
            ninos++;
        else if(edad <= 29)
            jovenes++;
        else
            adultos++;
    }

    cout << "Niños: " << ninos << endl;
    cout << "Jovenes: " << jovenes << endl;
    cout << "Adultos: " << adultos;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
n = int(input("Cantidad de personas: "))

ninos = jovenes = adultos = 0

for i in range(n):
    edad = int(input("Edad: "))

    if 0 <= edad <= 13:
        ninos += 1
    elif edad <= 29:
        jovenes += 1
    else:
        adultos += 1

print("Niños:", ninos)
print("Jovenes:", jovenes)
print("Adultos:", adultos)
```
</details>

##### Ejercicio 12. Crear un algoritmo que lea n calificaciones e imprimir en pantalla el promedio, la calificación más baja y la más alta, el porcentaje de aprobados y el porcentaje de reprobados, validando que el usuario solo pueda ingresar calificaciones entre el 0 y el 10
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Calificaciones
    Definir n, i Como Entero;
    Definir nota, suma, promedio Como Real;
    Definir mayor, menor Como Real;
    Definir aprobados, reprobados Como Entero;

    suma <- 0;
    aprobados <- 0;
    reprobados <- 0;
    i <- 1;

    Escribir "Cantidad de calificaciones: ";
    Leer n;

    Mientras i <= n Hacer

        Repetir
            Escribir "Ingresa calificacion (0-10): ";
            Leer nota;
        Hasta Que nota >= 0 Y nota <= 10;

        Si i = 1 Entonces
            mayor <- nota;
            menor <- nota;
        SiNo
            Si nota > mayor Entonces
                mayor <- nota;
            FinSi
            Si nota < menor Entonces
                menor <- nota;
            FinSi
        FinSi

        suma <- suma + nota;

        Si nota >= 6 Entonces
            aprobados <- aprobados + 1;
        SiNo
            reprobados <- reprobados + 1;
        FinSi

        i <- i + 1;
    FinMientras

    promedio <- suma / n;

    Escribir "Promedio:", promedio;
    Escribir "Mayor:", mayor;
    Escribir "Menor:", menor;
    Escribir "% Aprobados:", (aprobados*100)/n;
    Escribir "% Reprobados:", (reprobados*100)/n;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int n, i = 1;
    float nota, suma = 0, promedio;
    float mayor, menor;
    int aprobados = 0, reprobados = 0;

    cout << "Cantidad de calificaciones: ";
    cin >> n;

    while(i <= n) {

        do {
            cout << "Ingresa nota (0-10): ";
            cin >> nota;
        } while(nota < 0 || nota > 10);

        if(i == 1) {
            mayor = menor = nota;
        } else {
            if(nota > mayor) mayor = nota;
            if(nota < menor) menor = nota;
        }

        suma += nota;

        if(nota >= 6)
            aprobados++;
        else
            reprobados++;

        i++;
    }

    promedio = suma / n;

    cout << "Promedio: " << promedio << endl;
    cout << "Mayor: " << mayor << endl;
    cout << "Menor: " << menor << endl;
    cout << "% Aprobados: " << (aprobados*100.0)/n << endl;
    cout << "% Reprobados: " << (reprobados*100.0)/n;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
n = int(input("Cantidad de calificaciones: "))

i = 1
suma = 0
aprobados = 0
reprobados = 0

while i <= n:

    while True:
        nota = float(input("Ingresa nota (0-10): "))
        if 0 <= nota <= 10:
            break

    if i == 1:
        mayor = menor = nota
    else:
        if nota > mayor:
            mayor = nota
        if nota < menor:
            menor = nota

    suma += nota

    if nota >= 6:
        aprobados += 1
    else:
        reprobados += 1

    i += 1

promedio = suma / n

print("Promedio:", promedio)
print("Mayor:", mayor)
print("Menor:", menor)
print("% Aprobados:", (aprobados*100)/n)
print("% Reprobados:", (reprobados*100)/n)
```
</details>

##### Ejercicio 13. Determinar cuántos hombres y cuantas mujeres se encuentran en un grupo de N personas
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo ContarGenero
    Definir n, i Como Entero;
    Definir genero Como Caracter;
    Definir hombres, mujeres Como Entero;

    hombres <- 0;
    mujeres <- 0;
    i <- 1;

    Escribir "Ingresa cantidad de personas: ";
    Leer n;

    Mientras i <= n Hacer
        Escribir "Ingrese genero (H/M): ";
        Leer genero;

        Si genero = "H" Entonces
            hombres <- hombres + 1;
        SiNo
            mujeres <- mujeres + 1;
        FinSi

        i <- i + 1;
    FinMientras

    Escribir "Hombres: ", hombres;
    Escribir "Mujeres: ", mujeres;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int n, i = 1, hombres = 0, mujeres = 0;
    char genero;

    cout << "Cantidad de personas: ";
    cin >> n;

    while(i <= n) {
        cout << "Genero (H/M): ";
        cin >> genero;

        if(genero == 'H' || genero == 'h')
            hombres++;
        else
            mujeres++;

        i++;
    }

    cout << "Hombres: " << hombres << endl;
    cout << "Mujeres: " << mujeres;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
n = int(input("Cantidad de personas: "))

i = 1
hombres = 0
mujeres = 0

while i <= n:
    genero = input("Genero (H/M): ").lower()

    if genero == "h":
        hombres += 1
    else:
        mujeres += 1

    i += 1

print("Hombres: ", hombres)
print("Mujeres: ", mujeres)
```
</details>

##### Ejercicio 14. Una compañía de seguros tiene contratados a N vendedores. Cada uno hace 3 ventas a la semana. Su política de pagos es que un vendedor recibe un sueldo base, y un 15% extra por comisiones de sus ventas. El gerente de su compañía desea saber cuánto dinero obtendrá en la semana cada vendedor por concepto de comisiones por las 3 ventas realizadas, y cuanto tomando en cuenta su sueldo base y sus comisiones
<details>
<summary>Pseudocódigo</summary>

```

```
</details>

<details>
<summary>C++</summary>

```C++

```
</details>

<details>
<summary>Python</summary>

```Python

```
</details>

##### Ejercicio 15. Obtener la suma y el promedio de calificaciones de un grupo de N alumnos
<details>
<summary>Pseudocódigo</summary>

```

```
</details>

<details>
<summary>C++</summary>

```C++

```
</details>

<details>
<summary>Python</summary>

```Python

```
</details>

##### Ejercicio 16. Leer 10 calificaciones de un grupo de alumnos. Calcule y escriba el porcentaje de reprobados y porcentaje de aprobados. Tomando en cuenta que la calificación mínima aprobatoria es de 6
<details>
<summary>Pseudocódigo</summary>

```

```
</details>

<details>
<summary>C++</summary>

```C++

```
</details>

<details>
<summary>Python</summary>

```Python

```
</details>

##### Ejercicio 17. Encontrar el promedio, el valor menor y mayor de un conjunto de 15 números leídos por el usuario
<details>
<summary>Pseudocódigo</summary>

```

```
</details>

<details>
<summary>C++</summary>

```C++

```
</details>

<details>
<summary>Python</summary>

```Python

```
</details>

##### Ejercicio 18. Determinar cuántos hombres y cuantas mujeres se encuentran en un grupo de 25 personas
<details>
<summary>Pseudocódigo</summary>

```

```
</details>

<details>
<summary>C++</summary>

```C++

```
</details>

<details>
<summary>Python</summary>

```Python

```
</details>

##### Ejercicio 19. El Departamento de Seguridad Publica y Transito del D.F. desea saber, de los n autos que entran a la Ciudad de México, cuantos entran con calcomanía de cada color. Conociendo el último dígito de la placa de cada automóvil se puede determinar el color de la calcomanía utilizando la sig. relación:
| DÍGITO |   COLOR  |
| :---:  | :---:    |  
| 1 o 2  | amarilla |
| 3 o 4  | rosa     |
| 5 o 6  | roja     |
| 7 o 8  | verde    |
| 9 o 0  | azul     |

<details>
<summary>Pseudocódigo</summary>

```

```
</details>

<details>
<summary>C++</summary>

```C++

```
</details>

<details>
<summary>Python</summary>

```Python

```
</details>

##### Ejercicio 20. Determinar la cantidad semanal de dinero que recibirá cada uno de los N obreros de una empresa. Se sabe que cuando las horas que trabajo un obrero exceden de 40, el resto se convierte en horas extras que se pagan al doble de una hora normal, cuando no exceden de 8; cuando las horas extras exceden de 8 se pagan las primeras 8 al doble de lo que se paga por una hora normal y el resto al triple
<details>
<summary>Pseudocódigo</summary>

```

```
</details>

<details>
<summary>C++</summary>

```C++

```
</details>

<details>
<summary>Python</summary>

```Python

```
</details>

##### Ejercicio 21. Una persona debe realizar un muestreo con 10 personas para determinar el promedio de peso de los niños, jóvenes, adultos y viejos que existen en su zona habitacional. Se determinan las categorías con base en la siguiente tabla:
| CATEGORIA |   EDAD         |
| :---:     | :---:          |  
| Niños     | 0 - 12         |
| Jóvenes   | 13 - 29        |
| Adultos   | 30 - 59        |
| Viejos    | 60 en adelante |
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo PromedioPesos
    Definir edad Como Entero;
    Definir peso Como Real;
    Definir i Como Entero;
	
    Definir sumaN, sumaJ, sumaA, sumaV Como Real;
    Definir contN, contJ, contA, contV Como Entero;
	
    sumaN <- 0; sumaJ <- 0; sumaA <- 0; sumaV <- 0;
    contN <- 0; contJ <- 0; contA <- 0; contV <- 0;
	
    Para i <- 1 Hasta 10 Hacer
		
		Escribir "Edad: ";
		Leer edad;
		Escribir "Peso: ";
		Leer peso;
		
		Si edad >= 0 Y edad <= 12 Entonces
			sumaN <- sumaN + peso;
			contN <- contN + 1;
			
		SiNo
			Si edad <= 29 Entonces
				sumaJ <- sumaJ + peso;
				contJ <- contJ + 1;
				
			SiNo
				Si edad <= 59 Entonces
					sumaA <- sumaA + peso;
					contA <- contA + 1;
					
				SiNo
					sumaV <- sumaV + peso;
					contV <- contV + 1;
				FinSi
			FinSi
		FinSi
		
	FinPara
	
    Si contN > 0 Entonces
        Escribir "Promedio niños: ", sumaN / contN;
    FinSi
    Si contJ > 0 Entonces
        Escribir "Promedio jovenes:", sumaJ / contJ;
    FinSi
    Si contA > 0 Entonces
        Escribir "Promedio adultos:", sumaA / contA;
    FinSi
    Si contV > 0 Entonces
        Escribir "Promedio viejos:", sumaV / contV;
    FinSi
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int edad;
    float peso;

    float sumaN=0, sumaJ=0, sumaA=0, sumaV=0;
    int contN=0, contJ=0, contA=0, contV=0;

    for(int i = 1; i <= 10; i++) {
        cout << "Edad: ";
        cin >> edad;
        cout << "Peso: ";
        cin >> peso;

        if(edad >= 0 && edad <= 12) {
            sumaN += peso;
            contN++;
        }
        else if(edad <= 29) {
            sumaJ += peso;
            contJ++;
        }
        else if(edad <= 59) {
            sumaA += peso;
            contA++;
        }
        else {
            sumaV += peso;
            contV++;
        }
    }

    if(contN > 0) cout << "Promedio niños: " << sumaN/contN << endl;
    if(contJ > 0) cout << "Promedio jovenes: " << sumaJ/contJ << endl;
    if(contA > 0) cout << "Promedio adultos: " << sumaA/contA << endl;
    if(contV > 0) cout << "Promedio viejos: " << sumaV/contV << endl;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
sumaN = sumaJ = sumaA = sumaV = 0
contN = contJ = contA = contV = 0

for i in range(10):
    edad = int(input("Edad: "))
    peso = float(input("Peso: "))

    if 0 <= edad <= 12:
        sumaN += peso
        contN += 1
    elif edad <= 29:
        sumaJ += peso
        contJ += 1
    elif edad <= 59:
        sumaA += peso
        contA += 1
    else:
        sumaV += peso
        contV += 1

if contN > 0:
    print("Promedio niños:", sumaN/contN)
if contJ > 0:
    print("Promedio jovenes:", sumaJ/contJ)
if contA > 0:
    print("Promedio adultos:", sumaA/contA)
if contV > 0:
    print("Promedio viejos:", sumaV/contV)
```
</details>