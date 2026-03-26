<h1 align="center">LÓGICA DE PROGRAMACIÓN BÁSICA</h1>

Este repositorio contiene una colección de ejercicios básicos de programación implementados en:

- Pseudocódigo
- C++
- Python

**Contenido**
Los ejercicios incluyen:
- Operaciones básicas
- Porcentajes
- Conversiones
- Interés simple
- Promedios
- Problemas clásicos de lógica

**Objetivo**
Reforzar la lógica de programación y comparar la implementación en diferentes lenguajes.

---

##### Ejercicio 1. Crear un algoritmo que lea 3 números e imprima el doble y la mitad de los mismos
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo DobleMitad
    Definir num1, num2, num3 Como Real;
    Definir doble1, doble2, doble3 Como Real;
    Definir mitad1, mitad2, mitad3 Como Real;

    Escribir "Ingresa 3 numeros: ";
    Leer num1, num2, num3;

    doble1 <- num1 * 2;
    doble2 <- num2 * 2;
    doble3 <- num3 * 2;

    mitad1 <- num1 / 2;
    mitad2 <- num2 / 2;
    mitad3 <- num3 / 2;

    Escribir "Dobles:", doble1, doble2, doble3;
    Escribir "Mitades:", mitad1, mitad2, mitad3;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float num1, num2, num3;

    cout << "Ingresa 3 numeros: ";
    cin >> num1 >> num2 >> num3;

    cout << "Dobles: " << num1*2 << ", " << num2*2 << ", " << num3*2 << endl;
    cout << "Mitades: " << num1/2 << ", " << num2/2 << ", " << num3/2 << endl;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
n1, n2, n3 = map(float, input("Ingresa 3 numeros: ").split())

print("Dobles:", n1*2, n2*2, n3*2)
print("Mitades:", n1/2, n2/2, n3/2)
```
</details>


##### Ejercicio 2. Crear un algoritmo que lea desde teclado 3 números e imprima en pantalla el producto de los números ingresados
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Producto
    Definir num1, num2, num3 Como Real;

    Escribir "Ingresa 3 numeros: ";
    Leer num1, num2, num3;

    producto <- num1 * num2 * num3;

    Escribir "Producto:", producto;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float n1, n2, n3;

    cout << "Ingresa 3 numeros: ";
    cin >> num1 >> num2 >> num3;

    cout << "Producto: " << num1*num2*num3;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
num1, num2, num3 = map(float, input("Ingresa 3 numeros: ").split())

print("Producto:", n1*n2*n3)
```
</details>

##### Ejercicio 3. Crear un algoritmo que calcule el cuadrado de un número ingresado desde el teclado
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Cuadrado
    Definir num Como Real;

    Escribir "Ingresa un numero: ";
    Leer num;

    cuadrado <- num * num;

    Escribir "Cuadrado:", cuadrado
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float num;

    cout << "Ingresa numero: ";
    cin >> num;

    cout << "Cuadrado: " << num * num;

    return 0;
}
```
</details> 

<details>
<summary>Python</summary>

```Python
num = float(input("Ingresa numero: "))

print("Cuadrado:", num**2)
```
</details>

##### Ejercicio 4. Crear un algoritmo que lea el costo de un producto y obtenga como resultado el descuento del 15%
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Descuento15
    Definir costo, descuento, total Como Real

    Escribir "Ingresa el costo del producto: ";
    Leer costo;

    descuento <- costo * 0.15;
    total <- costo - descuento;

    Escribir "Descuento:", descuento;
    Escribir "Total a pagar:", total;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float costo, descuento, total;

    cout << "Ingresa el costo: ";
    cin >> costo;

    descuento = costo * 0.15;
    total = costo - descuento;

    cout << "Descuento: $" << descuento << endl;
    cout << "Total: $" << total;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
costo = float(input("Ingresa el costo: "))

descuento = costo * 0.15
total = costo - descuento

print("Descuento:", descuento)
print("Total a pagar:", total)
```
</details>

##### Ejercicio 5. ¿Cuál será el costo de un producto si el tiendero recibe $4 de ganancia lo cual es el 25% del costo real?
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo CostoReal
    Definir costo Como Real;

    costo <- (4 * 100) / 25;

    Escribir "Costo real:", costo;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float costo;

    costo = (4 * 100) / 25;

    cout << "Costo real: $" << costo;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
costo = (4 * 100) / 25

print("Costo real:", costo)
```
</details>

##### Ejercicio 6. Crear un algoritmo que calcule cuanto pagara una persona por la compra 3 computadoras si el costo de las computadoras son diferentes
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo CompraPC
    Definir pc1, pc2, pc3, total Como Real;

    Escribir "Ingresa precios: ";
    Leer pc1, pc2, pc3;

    total <- pc1 + pc2 + pc3;

    Escribir "Total a pagar:", total;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float p1, p2, p3, total;

    cout << "Ingresa precios: ";
    cin >> pc1 >> pc2 >> pc3;

    total = pc1 + pc2 + pc3;

    cout << "Total: $" << total;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
pc1 = float(input("Precio 1: "))
pc2 = float(input("Precio 2: "))
pc3 = float(input("Precio 3: "))

total = pc1 + pc2 + pc3

print("Total a pagar:", total)
```
</details>

##### Ejercicio 7. ¿Cuanto pagara una persona por la compra de un televisor con un costo de $8,000. Si este tiene un descuento del 10%?
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Televisor
    Definir precio, descuento, total Como Real;

    precio <- 8000;
    descuento <- precio * 0.10;
    total <- precio - descuento;

    Escribir "Total a pagar:", total;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float precio = 8000;
    float descuento = precio * 0.10;
    float total = precio - descuento;

    cout << "Total a pagar: $" << total;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
precio = 8000
descuento = precio * 0.10
total = precio - descuento

print("Total a pagar:", total)
```
</details>

##### Ejercicio 8. Crear un algoritmo que calcule el salario semanal de una persona en donde el trabajador labora un número variable de días a la semana y gana $200.00 diarios
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Salario
    Definir dias, salario Como Entero;

    Escribir "Ingresa dias trabajados: ";
    Leer dias;

    salario <- dias * 200;

    Escribir "Salario semanal:", salario;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int dias;
    cout << "Ingresa dias trabajados: ";
    cin >> dias;

    int salario = dias * 200;

    cout << "Salario: $" << salario;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
dias = int(input("Ingresa dias trabajados: "))

salario = dias * 200

print("Salario semanal:", salario)
```
</details>

##### Ejercicio 9. Convertir segundos a minutos y horas
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Tiempo
    Definir seg, min, hrs Como Entero;

    Escribir "Ingresa segundos: ";
    Leer seg;

    min <- seg / 60;
    hrs <- seg / 3600;

    Escribir "Minutos:", min;
    Escribir "Horas:", hrs;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int seg;
    cout << "Ingrese segundos: ";
    cin >> seg;

    int min = seg / 60;
    int hrs = seg / 3600;

    cout << "Minutos: " << min << endl;
    cout << "Horas: " << hrs;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
seg = int(input("Ingresa segundos: "))

minutos = seg // 60
horas = seg // 3600

print("Minutos:", minutos)
print("Horas:", horas)
```
</details>

##### Ejercicio 10. Un joven estudia en una escuela particular y la escuela le otorga un descuento del 35%, solicitar el costo real de la colegiatura e imprimir en pantalla el descuento y el total a pagar ya con el descuento aplicado
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Colegiatura
    Definir costo, descuento, total Como Real;

    Escribir "Ingresa costo de colegiatura: ";
    Leer costo;

    descuento <- costo * 0.35;
    total <- costo - descuento;

    Escribir "Descuento:", descuento;
    Escribir "Total a pagar:", total;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float costo, descuento, total;

    cout << "Ingresa costo: ";
    cin >> costo;

    descuento = costo * 0.35;
    total = costo - descuento;

    cout << "Descuento: $" << descuento << endl;
    cout << "Total: $" << total;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
costo = float(input("Ingresa costo de colegiatura: "))

descuento = costo * 0.35
total = costo - descuento

print("Descuento:", descuento)
print("Total a pagar:", total)
```
</details>

##### Ejercicio 11. Una tienda ofrece un descuento del 40% sobre el total de la compra y un cliente desea saber cuánto deberá pagar finalmente por su compra y el descuento.
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Tienda
    Definir compra, descuento, total Como Real;

    Escribir "Ingrese total de la compra: ";
    Leer compra;

    descuento <- compra * 0.40;
    total <- compra - descuento;

    Escribir "Descuento:", descuento;
    Escribir "Total a pagar:", total;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float compra, descuento, total;

    cout << "Ingresa compra: ";
    cin >> compra;

    descuento = compra * 0.40;
    total = compra - descuento;

    cout << "Descuento: $" << descuento << endl;
    cout << "Total: $" << total;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
compra = float(input("Ingresa total de la compra: "))

descuento = compra * 0.40
total = compra - descuento

print("Descuento:", descuento)
print("Total a pagar:", total)
```
</details>

##### Ejercicio 12. Diseñar un algoritmo que lea el valor correspondiente a una distancia en millas y las escriba expresadas en metros. Sabiendo que 1 milla equivale a 1852 metros
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Millas
    Definir millas, metros Como Real;

    Escribir "Ingrese millas: ";
    Leer millas;

    metros <- millas * 1852;

    Escribir "Metros:", metros;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float millas;
    cout << "Ingresa millas: ";
    cin >> millas;

    float metros = millas * 1852;

    cout << "Metros: " << metros;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
millas = float(input("Ingresa millas: "))

metros = millas * 1852

print("Metros:", metros)
```
</details>

##### Ejercicio 13. Diseñar un algoritmo que reciba como entrada una medida expresada en centímetros la convierta en pulgadas (1 pulgada = 2.54 centímetros)
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Conversion
    Definir cm, pulgadas Como Real;

    Escribir "Ingresa centimetros: ";
    Leer cm;

    pulgadas <- cm / 2.54;

    Escribir "Pulgadas:", pulgadas;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float cm;
    cout << "Ingresa centimetros: ";
    cin >> cm;

    float pulgadas = cm / 2.54;

    cout << "Pulgadas: " << pulgadas;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
cm = float(input("Ingresa centimetros: "))

pulgadas = cm / 2.54

print("Pulgadas:", pulgadas)
```
</details>

##### Ejercicio 14. Suponga que un individuo desea invertir su capital en un banco y desea saber cuánto dinero ganara después de un mes, el banco paga a razón de 2% mensual
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Interes
    Definir capital, interes, total Como Real;

    Escribir "Ingresa el capital: ";
    Leer capital;

    interes <- capital * 0.02;
    total <- capital + interes;

    Escribir "Ganancia:", interes;
    Escribir "Total:", total;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float capital, interes, total;

    cout << "Ingresa capital: ";
    cin >> capital;

    interes = capital * 0.02;
    total = capital + interes;

    cout << "Ganancia: $" << interes << endl;
    cout << "Total: $" << total;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
capital = float(input("Ingresa capital: "))

interes = capital * 0.02
total = capital + interes

print("Ganancia:", interes)
print("Total:", total)
```
</details>

##### Ejercicio 15. Calcular la ganancia de una inversión con un interés del 35% anual en un periodo de 10 meses
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo InteresMeses
    Definir capital, interes, total Como Real
    Definir meses Como Entero

    Escribir "Ingresa capital: "
    Leer capital
    Escribir "Ingresa meses: "
    Leer meses

    interes <- capital * 0.02 * meses
    total <- capital + interes

    Escribir "Interes:", interes
    Escribir "Total:", total
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float capital, interes, total;
    int meses;

    cout << "Ingresa capital: ";
    cin >> capital;
    cout << "Ingresa meses: ";
    cin >> meses;

    interes = capital * 0.02 * meses;
    total = capital + interes;

    cout << "Interes: $" << interes << endl;
    cout << "Total: $" << total;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
capital = float(input("Ingresa capital: "))
meses = int(input("Ingresa meses: "))

interes = capital * 0.02 * meses
total = capital + interes

print("Interes:", interes)
print("Total:", total)
```
</details>

##### Ejercicio 16. Una tienda desea calcular lo siguiente: el monto de la compra, el IVA (16%), el total (monto más iva) y el cambio del cliente
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo IVA
    Definir precio_prdct, pago_prdctiva, cambio, iva, monto_iva Como Real

    Escribir "Ingresa precio: ";
    Leer precio_prdct;
    Escribir "Ingrese el pago: ";
	Leer pago_prdct;

    iva <- precio_prdct * 0.16;
    monto_iva <- precio_prdct + iva;
    cambio = precio_prdct - pago_prdct;

    Escribir "El iva a pagar es de: $",iva;
	Escribir "El total a pagar ya con el iva incluido es de: $",monto_iva;
	Escribir "Su cambio es de: $", cambio;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float precio, iva, total;

    cout << "Ingresa precio: ";
    cin >> precio;

    iva = precio * 0.16;
    total = precio + iva;

    cout << "IVA: $" << iva << endl;
    cout << "Total: $" << total;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
precio = float(input("Ingresa precio: "))

iva = precio * 0.16
total = precio + iva

print("IVA:", iva)
print("Total:", total)
```
</details>

##### Ejercicio 17. Suponga que un individuo desea invertir su capital en un banco y desea saber cuánto dinero tendrá en el mismo después de 3 años, el banco paga a razón de 3% mensual
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

##### Ejercicio 18. Un vendedor recibe un sueldo base más un 10% extra por comisión de sus ventas, el vendedor desea saber cuánto dinero obtendrá por concepto de comisiones por las tres ventas que realiza en la semana y el total que recibirá en la semana tomando en cuenta su sueldo base y comisiones
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Inversiones
    Definir i1, i2, i3, total Como Real
    Definir p1, p2, p3 Como Real

    Escribir "Ingresa inversiones: "
    Leer i1, i2, i3

    total <- i1 + i2 + i3

    p1 <- (i1 * 100) / total
    p2 <- (i2 * 100) / total
    p3 <- (i3 * 100) / total

    Escribir p1, p2, p3
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float i1, i2, i3, total;

    cout << "Ingresa inversiones: ";
    cin >> i1 >> i2 >> i3;

    total = i1 + i2 + i3;

    cout << "Porcentaje 1: " << (i1*100)/total << endl;
    cout << "Porcentaje 2: " << (i2*100)/total << endl;
    cout << "Porcentaje 3: " << (i3*100)/total;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
i1 = float(input("Inversion 1: "))
i2 = float(input("Inversion 2: "))
i3 = float(input("Inversion 3: "))

total = i1 + i2 + i3

print("Porcentaje 1:", (i1*100)/total)
print("Porcentaje 2:", (i2*100)/total)
print("Porcentaje 3:", (i3*100)/total)
```
</details>

##### Ejercicio 19. Un maestro desea saber qué porcentaje de hombres y que porcentaje de mujeres hay en un grupo de estudiantes, recibiendo como entrada el número de hombres y mujeres del grupo
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Grupo
    Definir hombres, mujeres, total Como Entero
    Definir ph, pm Como Real

    Escribir "Ingrese numero de hombres:"
    Leer hombres
    Escribir "Ingrese numero de mujeres:"
    Leer mujeres

    total <- hombres + mujeres

    ph <- (hombres * 100) / total
    pm <- (mujeres * 100) / total

    Escribir "% Hombres:", ph
    Escribir "% Mujeres:", pm
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    int hombres, mujeres, total;
    float ph, pm;

    cout << "Hombres: ";
    cin >> hombres;
    cout << "Mujeres: ";
    cin >> mujeres;

    total = hombres + mujeres;

    ph = (hombres * 100.0) / total;
    pm = (mujeres * 100.0) / total;

    cout << "% Hombres: " << ph << endl;
    cout << "% Mujeres: " << pm;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
hombres = int(input("Hombres: "))
mujeres = int(input("Mujeres: "))

total = hombres + mujeres

ph = (hombres * 100) / total
pm = (mujeres * 100) / total

print("% Hombres:", ph)
print("% Mujeres:", pm)
```
</details>

##### Ejercicio 20. Tres personas deciden invertir su dinero para fundar una empresa. Cada una de ellas invierte una cantidad distinta. Obtener el porcentaje que cada quien invierte con respecto a la cantidad total invertida
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo PrecioFinal
    Definir precio, desc, iva, total Como Real

    Escribir "Ingresa precio: "
    Leer precio

    desc <- precio * 0.10
    precio <- precio - desc

    iva <- precio * 0.16
    total <- precio + iva

    Escribir "Total:", total
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float precio, desc, iva, total;

    cout << "Precio: ";
    cin >> precio;

    desc = precio * 0.10;
    precio = precio - desc;

    iva = precio * 0.16;
    total = precio + iva;

    cout << "Total: $" << total;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
precio = float(input("Precio: "))

precio -= precio * 0.10
total = precio + (precio * 0.16)

print("Total:", total)
```
</details>

##### Ejercicio 21. Una embotelladora de agua ofrece por aniversario un descuento del 25% en compara de agua, si el garrafón de agua tiene un costo de $12. Calcular el total a pagar por la compra de uno o más garrafones
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo Promedio
    Definir nu1, num2, num3, prom Como Real

    Leer num1, num2, num3

    prom <- (num1 + num2 + num3) / 3

    Escribir "Promedio:", prom
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```C++
#include<iostream>
using namespace std;

int main() {
    float n1, n2, n3;

    cin >> n1 >> n2 >> n3;

    float prom = (n1 + n2 + n3) / 3;

    cout << "Promedio: " << prom;

    return 0;
}
```
</details>

<details>
<summary>Python</summary>

```Python
n1 = float(input())
n2 = float(input())
n3 = float(input())

print("Promedio:", (n1+n2+n3)/3)
```
</details>

##### Ejercicio 22. Calcular la calificación final de juan si esta se compone de los siguientes porcentajes:
| PROMEDIO DE SUS TRES CALIFICACIONES PARCIALES |  EXAMEN FINAL   |   PROYECTO FINAL   |
| :---:                                         |     :---:       |    :--:            |
|              50%                              |     30%         |     20%            | 
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