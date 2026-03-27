<h1 align="center">EJERCICIOS DE BUCLES</h1>

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
	
    Para i <- 700 Hasta 0 Con Paso -7 Hacer;
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

##### Ejercicio 5. Calcular la suma de N números hasta que el usuario presione el número 7
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

##### Ejercicio 6. Diseñar un algoritmo que calcular e imprimir la suma de los números impares y pares hasta el usuario presione el número 2
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

##### Ejercicio 7. Crear un algoritmo que lea 10 números e imprima cuantos de los números ingresado fue un 5
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

##### Ejercicio 8. Crear un algoritmo que lea 10 números, e imprima al final la suma solo de los números mayores a 5 y menores a 50
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

##### Ejercicio 9. Crear un programa que lea el costo de los N productos de un cliente e imprima en pantalla el total a pagar por su compra y el número de productos comprados
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

##### Ejercicio 10. Suponga que tiene usted una tienda y desea registrar las N ventas en una computadora. Crear un programa que lea por cada cliente, el monto total de su compra. Al final del día escriba la cantidad total de las ventas y el número de clientes atendidos
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

##### Ejercicio 11. Crear un algoritmo que lea la edad de n personas e imprima cuantas personas fueron niños (0-13), cuanto fueron jóvenes (14-29) y cuanto adulto (30 o más)
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

##### Ejercicio 12. Crear un algoritmo que lea n calificaciones e imprimir en pantalla el promedio, la calificación más baja y la más alta, el porcentaje de aprobados y el porcentaje de reprobados, validando que el usuario solo pueda ingresar calificaciones entre el 0 y el 10
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

##### Ejercicio 13. Determinar cuántos hombres y cuantas mujeres se encuentran en un grupo de N personas
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

##### Ejercicio 20. Una compañía de seguros tiene contratados a N vendedores. Cada uno hace 3 ventas a la semana. Su política de pagos es que un vendedor recibe un sueldo base, y un 15% extra por comisiones de sus ventas. El gerente de su compañía desea saber cuánto dinero obtendrá en la semana cada vendedor por concepto de comisiones por las 3 ventas realizadas, y cuanto tomando en cuenta su sueldo base y sus comisiones
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

##### Ejercicio 21. Determinar la cantidad semanal de dinero que recibirá cada uno de los N obreros de una empresa. Se sabe que cuando las horas que trabajo un obrero exceden de 40, el resto se convierte en horas extras que se pagan al doble de una hora normal, cuando no exceden de 8; cuando las horas extras exceden de 8 se pagan las primeras 8 al doble de lo que se paga por una hora normal y el resto al triple
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

##### Ejercicio 22. Una persona debe realizar un muestreo con 10 personas para determinar el promedio de peso de los niños, jóvenes, adultos y viejos que existen en su zona habitacional. Se determinan las categorías con base en la siguiente tabla:
| CATEGORIA |   EDAD         |
| :---:     | :---:          |  
| Niños     | 0 - 12         |
| Jóvenes   | 13 - 29        |
| Adultos   | 30 - 59        |
| Viejos    | 60 en adelante |
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