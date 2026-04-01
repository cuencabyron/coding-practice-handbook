<h1 align="center">EJERCICIOS DE CONDICIONALES EN PROGRAMACIÓN</h1>

---

##### Ejercicio 1. Crear un programa que calcule si un número es par o impar
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo ParImpar
    Definir num Como Entero;

    Escribir "Ingresa numero: ";
    Leer num;

    Si num MOD 2 = 0 Entonces
        Escribir "Es par";
    SiNo
        Escribir "Es impar";
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
    int num;
    cout << "Ingresa numero: ";
    cin >> num;

    if(num % 2 == 0)
        cout << "Es par";
    else
        cout << "Es impar";

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
num = int(input("Ingresa numero: "))

if num % 2 == 0:
    print("Es par")
else:
    print("Es impar")
```
</details>

##### Ejercicio 2. Crear un programa que calcule si un número es múltiplo de 2,3 o 4, en el caso contrario imprimir número invalido
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Multiplos
    Definir num Como Entero;

    Escribir "Ingresa numero: ";
    Leer num;

    Si num MOD 2 = 0 Entonces
        Escribir "Multiplo de 2";
    SiNo
        Si num MOD 3 = 0 Entonces
            Escribir "Multiplo de 3";
        SiNo
            Si num MOD 4 = 0 Entonces
                Escribir "Multiplo de 4";
            SiNo
                Escribir "Numero invalido";
            FinSi
        FinSi
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
    int num;
    cout << "Ingresa numero: ";
    cin >> num;

    if(num % 2 == 0)
        cout << "Multiplo de 2";
    else if(num % 3 == 0)
        cout << "Multiplo de 3";
    else if(num % 4 == 0)
        cout << "Multiplo de 4";
    else
        cout << "Numero invalido";

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
num = int(input("Ingresa numero: "))

if num % 2 == 0:
    print("Multiplo de 2")
elif num % 3 == 0:
    print("Multiplo de 3")
elif num % 4 == 0:
    print("Multiplo de 4")
else:
    print("Numero invalido")
```
</details>

##### Ejercicio 3. Crear un programa que lea la altura e imprima en pantalla si la persona tiene una altura promedio, alta o baja. Tomando en cuenta lo siguiente:
| ALTO        |   PROMEDIO    |    BAJO    |
| :---:       |     :---:     |    :--:    |
| 1.80 o mas  |  1.60 a 1.79  |  0 a 1.59  | 
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Estatura
    Definir altura Como Real;

    Escribir "Ingrese altura: ";
    Leer altura;

    Si altura >= 1.80 Entonces
        Escribir "Alto";
    SiNo
        Si altura >= 1.60 Entonces
            Escribir "Promedio";
        SiNo
            Escribir "Bajo";
        FinSi
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
    float altura;
    cout << "Ingresa altura: ";
    cin >> altura;

    if(altura >= 1.80)
        cout << "Alto";
    else if(altura >= 1.60)
        cout << "Promedio";
    else
        cout << "Bajo";

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
altura = float(input("Ingresa altura: "))

if altura >= 1.80:
    print("Alto")
elif altura >= 1.60:
    print("Promedio")
else:
    print("Bajo")
```
</details>

##### Ejercicio 4. Determinar si un alumno aprueba o reprueba un curso, sabiendo que aprobara si su promedio de tres calificaciones es mayor o igual a 7; reprueba en caso contrario
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Aprobado
    Definir cal1, cal2, cal3, promedio Como Real;

    Escribir "Ingrese 3 calificaciones: ";
    Leer cal1, cal2, cal3;

    promedio <- (cal1 + cal2 + cal3) / 3;

    Si promedio >= 7 Entonces
        Escribir "Aprueba";
    SiNo
        Escribir "Reprueba";
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
    float cal1, cal2, cal3, promedio;

    cout << "Ingresa 3 calificaciones: ";
    cin >> cal1 >> cal2 >> cal3;

    promedio = (cal1 + cal2 + cal3) / 3;

    if(promedio >= 7)
        cout << "Aprueba";
    else
        cout << "Reprueba";

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
cal1 = float(input("Nota 1: "))
cal2 = float(input("Nota 2: "))
cal3 = float(input("Nota 3: "))

promedio = (cal1 + cal2 + cal3) / 3

if promedio >= 7:
    print("Aprueba")
else:
    print("Reprueba")
```
</details>

##### Ejercicio 5. Calcular el interés ganado mensualmente si una persona invierte en un banco, y este paga un interés mensual del 2% si la inversión es mayor o igual a 10,000 o un 3% si la inversión es mayor o igual a 20,000 o un 5% si la inversión es mayor o igual a 40,000
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo InteresBanco
    Definir inversion, interes Como Real;

    Escribir "Ingrese monto de inversion: ";
    Leer inversion;

    Si inversion >= 40000 Entonces
        interes <- inversion * 0.05;
    SiNo
        Si inversion >= 20000 Entonces
            interes <- inversion * 0.03;
        SiNo
            Si inversion >= 10000 Entonces
                interes <- inversion * 0.02;
            SiNo
                interes <- 0;
            FinSi
        FinSi
    FinSi

    Escribir "Interes: ", interes;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float inversion, interes;

    cout << "Ingresa inversion: ";
    cin >> inversion;

    if(inversion >= 40000)
        interes = inversion * 0.05;
    else if(inversion >= 20000)
        interes = inversion * 0.03;
    else if(inversion >= 10000)
        interes = inversion * 0.02;
    else
        interes = 0;

    cout << "Interes: $" << interes;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
inversion = float(input("Ingresa inversion: "))

if inversion >= 40000:
    interes = inversion * 0.05
elif inversion >= 20000:
    interes = inversion * 0.03
elif inversion >= 10000:
    interes = inversion * 0.02
else:
    interes = 0

print("Interes:", interes)
```
</details>

##### Ejercicio 6. En un almacén se hace un 5% de descuento a los clientes cuya compra supere los $6,000.00 o un 10% si la compra supera los $8,000.00 ¿Cuál será la cantidad que pagara una persona por su compra y cuál es su descuento?
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

##### Ejercicio 7. Un obrero necesita calcular su salario semanal, el cual se obtiene de la siguiente manera:
- Si trabaja 40 horas o menos se le paga $16 por hora
- Si trabaja más de 40 horas se le paga $20 por hora extra trabajada.
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo SalarioObrero
    Definir horas, salario Como Real;

    Escribir "Horas trabajadas: ";
    Leer horas;

    Si horas <= 40 Entonces
        salario <- horas * 16;
    SiNo
        salario <- 40 * 16 + (horas - 40) * 20;
    FinSi

    Escribir "Salario: ", salario;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float horas, salario;

    cout << "Horas trabajadas: ";
    cin >> horas;

    if(horas <= 40)
        salario = horas * 16;
    else
        salario = 40 * 16 + (horas - 40) * 20;

    cout << "Salario: $" << salario;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
horas = float(input("Horas trabajadas: "))

if horas <= 40:
    salario = horas * 16
else:
    salario = 40 * 16 + (horas - 40) * 20

print("Salario:", salario)
```
</details>

##### Ejercicio 8. Programa que lea dos números y los imprima en forma ascendente.
- Ejemplo:
    - 1
    - 5
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Ordenar
    Definir num1, num2 Como Entero;

    Escribir "Ingrese dos numeros: ";
    Leer num1, num2;

    Si num1 < num2 Entonces
        Escribir num1, num2;
    SiNo
        Escribir num2, num1;
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
    int a, b;

    cout << "Ingresa dos numeros: ";
    cin >> num1 >> num2;

    if(num1 < num2)
        cout << num1 << " " << num2;
    else
        cout << num2 << " " << num1;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
num1 = int(input("Numero 1: "))
num2 = int(input("Numero 2: "))

if num1 < b:
    print(num1, num2)
else:
    print(num2, num1)
```
</details>

##### Ejercicio 9. Hacer un programa que calcule el total a pagar por la compra de camisas. Si se compran tres camisas o más se aplica un descuento del 20% sobre el total de la compra y si son menos de tres camisas un descuento del 10%
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Camisas
    Definir cantidad, precio, total, descuento Como Real

    Escribir "Cantidad de camisas: ";
    Leer cantidad;
    Escribir "Precio por camisa: ";
    Leer precio;

    total <- cantidad * precio;

    Si cantidad >= 3 Entonces
        descuento <- total * 0.20;
    SiNo
        descuento <- total * 0.10;
    FinSi

    Escribir "Total a pagar: ", total - descuento;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int cantidad;
    float precio, total, descuento;

    cout << "Cantidad de camisas: ";
    cin >> cantidad;
    cout << "Precio por camisa: ";
    cin >> precio;

    total = cantidad * precio;

    if(cantidad >= 3)
        descuento = total * 0.20;
    else
        descuento = total * 0.10;

    cout << "Total a pagar: $" << total - descuento;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
cantidad = int(input("Cantidad de camisas: "))
precio = float(input("Precio por camisa: "))

total = cantidad * precio

if cantidad >= 3:
    descuento = total * 0.20
else:
    descuento = total * 0.10

print("Total a pagar:", total - descuento)
```
</details>

##### Ejercicio 10. Calcular el total que una persona debe pagar en una llantera, si el precio de cada llanta es de $ 800 si se compran menos de 5 llantas y de $700 si se compran 5 o más
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

##### Ejercicio 11. En un almacén se hace un 20% de descuento a los clientes cuya compra supere los $1000 ¿Cuál será la cantidad que pagara una persona por su compra?
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo AlmacenDescuento
    Definir total, descuento Como Real;

    Escribir "Total de compra: ";
    Leer total;

    Si total > 1000 Entonces
        descuento <- total * 0.20;
    SiNo
        descuento <- 0;
    FinSi

    Escribir "Total a pagar: ", total - descuento;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float total, descuento;

    cout << "Total de compra: ";
    cin >> total;

    if(total > 1000)
        descuento = total * 0.20;
    else
        descuento = 0;

    cout << "Total a pagar: $" << total - descuento;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
total = float(input("Total de compra: "))

if total > 1000:
    descuento = total * 0.20
else:
    descuento = 0

print("Total a pagar:", total - descuento)
```
</details>

##### Ejercicio 12. Calcular el total que una persona debe pagar en una librería, si se realiza una compra mayor a $5,000.00 se realizara un descuento del 5% además si la persona es estudiante se le otorgara un descuento extra del 3%
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Libreria
    Definir total, descuento Como Real;
    Definir esEstudiante Como Caracter;

    Escribir "Total de compra: ";
    Leer total;

    descuento <- 0

    Si total > 5000 Entonces
        descuento <- descuento + total * 0.05;
    FinSi

    Escribir "Es estudiante? (S/N): ";
    Leer esEstudiante;

    Si esEstudiante = "S" Entonces
        descuento <- descuento + total * 0.03;
    FinSi

    Escribir "Total a pagar:", total - descuento;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float total, descuento = 0;
    char estudiante;

    cout << "Total de compra: ";
    cin >> total;

    if(total > 5000)
        descuento += total * 0.05;

    cout << "Es estudiante? (S/N): ";
    cin >> estudiante;

    if(estudiante == 'S' || estudiante == 's')
        descuento += total * 0.03;

    cout << "Total a pagar: $" << total - descuento;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
total = float(input("Total de compra: "))
descuento = 0

if total > 5000:
    descuento += total * 0.05

estudiante = input("Es estudiante? (S/N): ").lower()

if estudiante == "s":
    descuento += total * 0.03

print("Total a pagar:", total - descuento)
```
</details>

##### Ejercicio 13. Una tienda ofrece galletas a 10 pesos el kilo, pero comprando más de 100 kilos, se ofrece un 10 % de descuento. Hacer un programa que calcule el total a pagar
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Galletas
    Definir kilos, total, descuento Como Real;

    Escribir "Kilos a comprar: ";
    Leer kilos;

    total <- kilos * 10;

    Si kilos > 100 Entonces
        descuento <- total * 0.10;
    SiNo
        descuento <- 0;
    FinSi

    Escribir "Total a pagar: ", total - descuento;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float kilos, total, descuento;

    cout << "Kilos a comprar: ";
    cin >> kilos;

    total = kilos * 10;

    if(kilos > 100)
        descuento = total * 0.10;
    else
        descuento = 0;

    cout << "Total a pagar: $" << total - descuento;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
kilos = float(input("Kilos a comprar: "))

total = kilos * 10

if kilos > 100:
    descuento = total * 0.10
else:
    descuento = 0

print("Total a pagar:", total - descuento)
```
</details>

##### Ejercicio 14. En una fábrica de calzado pagan 20 pesos por cada par empaquetado. Si se empaquetan más de 500 zapatos, los pares extras se pagan a 30 pesos. Hacer un programa que calcule el sueldo de un trabajador con base en el número de pares empaquetados
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Zapatos
    Definir pares, salario Como Real;

    Escribir "Pares empaquetados: "
    Leer pares;

    Si pares <= 500 Entonces
        salario <- pares * 20;
    SiNo
        salario <- 500 * 20 + (pares - 500) * 30;
    FinSi

    Escribir "Salario: ", salario;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int pares;
    float salario;

    cout << "Pares empaquetados: ";
    cin >> pares;

    if(pares <= 500)
        salario = pares * 20;
    else
        salario = 500 * 20 + (pares - 500) * 30;

    cout << "Salario: $" << salario;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
pares = int(input("Pares empaquetados: "))

if pares <= 500:
    salario = pares * 20
else:
    salario = 500 * 20 + (pares - 500) * 30

print("Salario:", salario)
```
</details>

##### Ejercicio 15. Un maestro desea evaluar dando equivalencia con letras, de 8.5 a 10 equivale a MB, de 7 a 8.4 equivale a B, de 6 a 6.9 equivale a S, de 0 a 5.9 equivale a NA. Crear un programa que realice la equivalencia
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Calificacion
    Definir nota Como Real;

    Escribir "Ingrese calificacion: ";
    Leer nota;

    Si nota >= 8.5 Entonces
        Escribir "MB";
    SiNo
        Si nota >= 7 Entonces
            Escribir "B";
        SiNo
            Si nota >= 6 Entonces
                Escribir "S";
            SiNo
                Escribir "NA";
            FinSi
        FinSi
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
    float nota;

    cout << "Ingresa calificacion: ";
    cin >> nota;

    if(nota >= 8.5)
        cout << "MB";
    else if(nota >= 7)
        cout << "B";
    else if(nota >= 6)
        cout << "S";
    else
        cout << "NA";

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
nota = float(input("Ingresa calificacion: "))

if nota >= 8.5:
    print("MB")
elif nota >= 7:
    print("B")
elif nota >= 6:
    print("S")
else:
    print("NA")
```
</details>

##### Ejercicio 16. Determinar la cantidad semanal de dinero que recibirá cada uno de los obreros de una empresa. Se sabe que cuando las horas que trabajo un obrero exceden de 40, el resto se convierte en horas extras que se pagan al doble de una hora normal, cuando no exceden de 8; cuando las horas extras exceden de 8 se pagan las primeras 8 al doble de lo que se paga por una hora normal y el resto al triple
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

##### Ejercicio 17. En una fábrica de computadoras se planea ofrecer a los clientes un descuento que dependerá del número de computadoras que compre. Si las computadoras son menos de cinco se les dará un 10% de descuento sobre el total de la compra; si el número de computadoras es mayor o igual a cinco, pero menos de diez se le otorga un 20% de descuento; y si son 10 o más se les da un 40% de descuento
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

##### Ejercicio 18. En un juego de preguntas a las que se responde “Si” o “No” gana quien responda correctamente las tres preguntas. Si se responde mal a cualquiera de ellas ya no se pregunta la siguiente y termina el juego. Las preguntas son:
- ¿Colon descubrió América?
- ¿La independencia de México fue en el año 1810?
- ¿The Doors fue un grupo de rock americano?
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

##### Ejercicio 19. Un proveedor de estéreos ofrece un descuento del 10% sobre el precio sin IVA, de algún aparato si esta cuesta $2000 o más. Además, independientemente de esto, ofrece un 5% de descuento si la marca es “sony”. Determinar cuánto pagara, con IVA incluido, un cliente cualquiera por la compra de su aparato
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

##### Ejercicio 20. Una frutería ofrece las manzanas con descuento según la siguiente tabla:
| NUM. DE KILOS COMPRADOS    |    % DESCUENTO    |
| :---:                      |     :--:          |
|        0 - 2               |       0%          | 
|      2.01 - 5              |      10%          | 
|      5.01 - 10             |      15%          | 
|  10.01 en adelante         |      20%          | 
##### Determinar cuánto pagara una persona que compre manzanas es esa frutería
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

##### Ejercicio 21. Una fábrica de sillas vende al público en general al mayoreo con un precio de $200 y menudeo con un precio de $300 por silla, para que un cliente obtenga el precio de mayoreo debe comprar más de 10 sillas, calcular el total a pagar por la compra de sillas
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

##### Ejercicio 22. Una escuela ofrece una beca a los alumnos cuyo promedio sea mayor o igual 9.0 y curse el primer o segundo año, desarrollar un algoritmo que muestre si los alumnos obtienen o no la beca estudiantil
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