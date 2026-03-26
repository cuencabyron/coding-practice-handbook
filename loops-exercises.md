<h1 align="center">EJERCICIOS DE BUCLES</h1>

---

##### Ejercicio 1. Crear un programa que lea 10 números e imprima el Doble de la suma de los números
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

##### Ejercicio 2. Escribir todos los números del 700 al 0, de 7 en 7
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_2
	Definir Num Como Entero
	Num <- 700;
	Escribir "---PROGRAMA QUE CALCULA LOS NUMEROS DEL 700 AL 0, DE 7 EN 7---";
	Mientras (Num >= 0) Hacer
		Escribir Num;
		Num <- Num - 7;
	FinMientras
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void DecrementarNumeros()
{
	int num = 700;
	cout<<"\t---PROGRAMA QUE CALCULA LOS NUMEROS DEL 700 AL 0, DE 7 EN 7---"<<endl;
	do
	{
		cout<<"\n"<<num;
		num -=  7;
	}while(num >= 0);	
}
int main()
{
	system("color 0A");
	DecrementarNumeros();
	return 0;
}

```
</details>

##### Ejercicio 3. Leer 10 números e imprimir el número mayor ingresado
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_3
	Definir x, myr, num Como Entero
	x <- 1;
	myr <- 0;
	num <- 0;
	Escribir "---PROGRAMA QUE CALCULA EL NUMERO MAYOR INGRESADO---";
	Mientras (x <= 10) Hacer
		Escribir "Ingrese el número ",x,": ";
		Leer num;
		Si (num > myr) Entonces
			myr <- num;
		FinSi
		x <- x + 1;
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El numero mayor ingresado es: ",myr;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void MayorIngresado()
{
	int x = 1, myr = 0, num = 0;
	cout<<"\t---PROGRAMA QUE CALCULA EL NUMERO MAYOR INGRESADO---"<<endl;
	do
	{
		cout<<"Ingrese el numero "<<x<<": ";
		cin>>num;
		if(num > myr)
		myr = num;
		x += 1;
	}while(x <= 10);
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"EL NUMERO MAYOR INGRESADO ES: "<<myr;
}
int main()
{
	system("color 0A");
	MayorIngresado();
	return 0;
}
```
</details>


##### Ejercicio 4. Leer 10 números e imprimir el número menor ingresado
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_4
	Definir x, mnr, num Como Entero
	x <- 1;
	mnr <- 0;
	num <- 0;
	Escribir "---PROGRAMA QUE CALCULA EL NUMERO MENOR INGRESADO---";
	Mientras (x <= 10) Hacer
		Escribir "Ingrese el n�mero ",x,": ";
		Leer num;
		Si (x == 1) Entonces
			mnr <- num;
		FinSi
		Si (num < mnr) Entonces
			mnr <- num;
		FinSi
		x <- x + 1;
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El número menor ingresado es: ",mnr;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void MenorIngresado()
{
	int x = 1, mnr = 0, num = 0;
	cout<<"\t---PROGRAMA QUE CALCULA EL NUMERO MENOR INGRESADO---"<<endl;
	do
	{
		cout<<"Ingrese el numero "<<x<<": ";
		cin>>num;
		if(x == 1)
		mnr = num;
		if(num < mnr)
		mnr = num;
		x += 1;
	}while(x <= 10);
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"EL NUMERO MENOR INGRESADO ES: "<<mnr;
}
int main()
{
	system("color 0A");
	MenorIngresado();
	return 0;
}
```
</details>

##### Ejercicio 5. Calcular la suma de N números hasta que el usuario presione el número 7
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_5
	Definir num, suma Como Entero
	num <- 0;
	suma <- 0;
	Escribir "---PROGRAMA QUE CALCULA LA SUMA DE N NUMEROS---";
	Mientras (num <> 7) Hacer
		Escribir "Ingrese un numero: ";
		Leer num; 
		suma <- suma + num; 
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El resultado por la suma de N numeros es de: ",suma;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void SumaNnumeros()
{
	int num = 0, suma = 0;
	cout<<"\t---PROGRAMA QUE CALCULA LA SUMA DE N NUMEROS---"<<endl;
	do
	{
		cout<<"Ingrese un numero: ";
		cin>>num;
		suma += num;
	}while(num != 7);
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"LA SUMA DE N NUMEROS ES: "<<suma;	
}
int main()
{
	system("color 0A");
	SumaNnumeros();
	return 0;
}
```
</details>

##### Ejercicio 6. Diseñar un algoritmo que calcular e imprimir la suma de los números impares y pares hasta el usuario presione el número 2
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_6
	Definir num, pares, impares Como Entero
	num <- 1;
	pares <- 0;
	impares <- 0;
	Escribir "---PROGRAMA QUE CALCULA LA SUMA DE LOS NUMEROS PARES E IMPARES---";
	Mientras (num <> 0) Hacer
		Escribir "Ingrese un número: "
		Leer num;
		Si (num % 2 == 0) Entonces
			pares <- num + pares;
		SiNo
			impares <- num + impares;
		FinSi
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "La suma de los pares es: ",pares;
	Escribir "La suma de los impares es: ",impares;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void SumaParesImpares()
{
	int num = 1, pares = 0, impares = 0;
	cout<<"\t---PROGRAMA QUE CALCULA LA SUMA DE LOS NUMEROS PARES E IMPARES---"<<endl;
	do
	{
		cout<<"Ingrese un numero: ";
		cin>>num;
		if(num % 2 == 0)
		pares += num;
		else
		impares += num;
	}while(num != 0);
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"SUMA DE LOS PARES: "<<pares<<endl;
	cout<<"SUMA DE LOS IMPARES: "<<impares<<endl;	
}
int main()
{
	system("color 0A");
	SumaParesImpares();
	return 0;
}
```
</details>

##### Ejercicio 7. Crear un algoritmo que lea 10 números e imprima cuantos de los números ingresado fue un 5
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_7
	Definir x, num, total Como Entero
	x <- 1;
	num <- 0;
	total <- 0;
	Escribir "---PROGRAMA QUE CALCULA CUANTOS NUMEROS 5 FUERON INGRESADOS---";
	Mientras (x <= 10) Hacer
		Escribir "Ingrese el número ",x,": ";
		Leer num; 
		Si (num == 5) Entonces
			total <- total + 1;
		FinSi
		x <- x + 1;
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El total de números 5 ingresados fue de: ",total;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void Numeros5()
{
	int x = 1, num = 0, total = 0;
	cout<<"\t---PROGRAMA QUE CALCULA CUANTOS NUMEROS 5 FUERON INGRESADOS---"<<endl;
	do
	{
		cout<<"Ingrese el numero "<<x<<": ";
		cin>>num;
		if(num == 5)
		total += 1;
		x += 1;
	}while(x <= 10);
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"EL TOTAL DE NUMEROS 5 INGRESADOS FUE DE: "<<total;
}
int main()
{
	system("color 0A");
	Numeros5();
	return 0;
}
```
</details>

##### Ejercicio 8. Crear un algoritmo que lea 10 números, e imprima al final la suma solo de los números mayores a 5 y menores a 50
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_8
	Definir x, num, suma Como Entero 
	x <- 1;
	num <- 0;
	suma <- 0;
	Escribir "---PROGRAMA QUE CALCULA LA SUMA DE LOS NUMEROS MAYORES A 5 Y MENORES A 50---";
	Mientras (x <= 10) Hacer
		Escribir "Ingrese el numero ",x,": ";
		Leer num;
		Si (num >= 5 y num <= 50) Entonces
			suma <- suma + num;
		FinSi
		x <- x + 1;
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "La suma de los numeros mayores a 5 y menores a 50 es: ",suma;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void SumaMyr5Mnr50()
{
	int x = 1, num = 0, suma = 0;
	cout<<"\t---PROGRAMA QUE CALCULA LA SUMA DE LOS NUMEROS MAYORES A 5 Y MENORES A 50---"<<endl;
	do
	{
		cout<<"Ingrese el numero "<<x<<": ";
		cin>>num;
		if(num >= 5 && num <= 50)
		suma += num;
		x += 1;
	}while(x <= 10);
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"LA SUMA DE LOS NUMEROS MAYORES A 5 Y MENORES A 50 ES: "<<suma;	
}
int main()
{
	system("color 0A");
	SumaMyr5Mnr50();
	return 0;
}

```
</details>

##### Ejercicio 9. Crear un programa que lea el costo de los N productos de un cliente e imprima en pantalla el total a pagar por su compra y el número de productos comprados
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_9
	Definir costo,total,productos Como Entero
	costo <- 1;
	total <- 0;
	productos <- 0;
	Escribir "---PROGRAMA QUE CALCULA EL COSTO DE N PRODUCTOS---";
	Mientras (costo <> 0) Hacer
		Escribir "Ingresa el costo del producto: ";
		Leer costo;
		Si (costo <> 0) Entonces
			total <- total + costo;
			productos <- productos + 1;
		FinSi
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El total a pagar es de: $",total;
	Escribir "El total de productos comprados es de: ",productos;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void ProductosCliente()
{
	int costo = 1, total = 0, prdcts = 0;
	cout<<"\t---PROGRAMA QUE CALCULA EL COSTO DE N PRODUCTOS---"<<endl;
	while(costo != 0)
	{
		cout<<"Ingrese el costo de producto: ";
		cin>>costo;
		if(costo != 0)
		{
			total += costo;
		    prdcts += 1;
		}
	}
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"EL TOTAL A PAGAR ES DE: $"<<total<<endl;
	cout<<"TOTAL DE PRODUCTOS COMPRADOS: "<<prdcts;	
}
int main()
{
	system("color 0A");
	ProductosCliente();
	return 0;
}
```
</details>

##### Ejercicio 10. Suponga que tiene usted una tienda y desea registrar las N ventas en una computadora. Crear un programa que lea por cada cliente, el monto total de su compra. Al final del día escriba la cantidad total de las ventas y el número de clientes atendidos
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_10
	Definir x, clts, ctv, mt Como Entero
	x <- 1;
	clts <- 0;
	ctv <- 0;
	mt <- 0;
	Escribir "---PROGRAMA QUE CALCULA LA CANTIDAD TOTAL DE VENTAS Y LOS CLIENTES ATENDIDOS---";
	Escribir "Ingrese la cantidad de clientes: ";
	Leer clts;
	Mientras (x <= clts) Hacer
		Escribir "Ingrese el monto total del cliente: ";
		Leer mt;
		ctv <- ctv + mt;
		x <- x + 1;
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "La cantidad total de las ventas es de: $",ctv;
	Escribir "El número de clientes atendidos es de: ",clts;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void ClientesAtendidos()
{
	int clts = 0, ctv = 0, mt = 0;
	cout<<"\t---PROGRAMA QUE CALCULA LA CANTIDAD TOTAL DE VENTAS Y LOS CLIENTES ATENDIDOS---"<<endl;
	cout<<"Ingrese la cantidad de clientes: ";
	cin>>clts;
	for(int x = 1; x <= clts; x++)
	{
		cout<<"Ingrese el monto total del cliente "<<x<<": $";
		cin>>mt;
		ctv += mt;
	}
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"CANTIDAD TOTAL DE LAS VENTAS: $"<<ctv<<endl;	
	cout<<"CLIENTES ATENDIDOS: "<<clts;
}
int main()
{
	system("color 0A");
	ClientesAtendidos();
	return 0;
}
```
</details>

##### Ejercicio 11. Crear un algoritmo que lea la edad de n personas e imprima cuantas personas fueron niños (0-13), cuanto fueron jóvenes (14-29) y cuanto adulto (30 o más)
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_11
	Definir x, numper, infantes, jovenes, adultos, edad Como Entero
	x <- 1;
	numper <- 0;
	infantes <- 0;
	jovenes <- 0;
	adultos <- 0;
	edad <- 0;
	Escribir "---PROGRAMA QUE CALCULA CUANTAS PERSONAS HAY DE DIEFRENTES EDADES---";
	Escribir "Ingrese la cantidad de personas que va a registrar: ";
	Leer numper;
	Mientras (x <= numper) Hacer
		Escribir "Ingrese una edad: ";
		Leer edad;
		Si (edad >= 0 y edad <= 13) Entonces
			infantes <- infantes + 1;
		FinSi
		Si (edad >= 14 y edad <= 29) Entonces
			jovenes <- jovenes + 1;
		FinSi
		Si (edad >= 30) Entonces
			adultos <- adultos + 1;
		FinSi
		x <- x + 1;
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El total de infantes fueron: ",infantes;
	Escribir "El total de jovenes fueron: ",jovenes;
	Escribir "El total de adultos fueron: ",adultos;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void EdadPersonas()
{
	int x = 1, numper = 0, infantes = 0, jovenes = 0, adultos = 0, edad = 0;
	cout<<"\t---PROGRAMA QUE CALCULA CUANTAS PERSONAS HAY DE DIEFRENTES EDADES---"<<endl;
	cout<<"Personas a registrar: ";
	cin>>numper;
	while(x <= numper)
	{
		cout<<"Ingrese la edad "<<x<<": ";
		cin>>edad;
		if(edad >= 0 && edad <= 13)
		infantes += 1;
		if(edad >= 14 && edad <= 29)
		jovenes += 1;
		if(edad >= 30)
		adultos += 1;
		
		x += 1;
	}
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"TOTAL DE INFANTES FUERON: "<<infantes<<endl;
	cout<<"TOTAL DE JOVENES FUERON: "<<jovenes<<endl;
	cout<<"TOTAL DE ADULTOS FUERON: "<<adultos<<endl;
}
int main()
{
	system("color 0A");
	EdadPersonas();
	return 0;
}
```
</details>

##### Ejercicio 12. Crear un algoritmo que lea n calificaciones e imprimir en pantalla el promedio, la calificación más baja y la más alta, el porcentaje de aprobados y el porcentaje de reprobados, validando que el usuario solo pueda ingresar calificaciones entre el 0 y el 10
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_12
	Definir x, numcal, calif, suma, baja, alta, conAprob, conReprob Como Entero
	Definir prom, aprob, reprob Como Real;
	x <- 1;
	numcal <- 0;
	calif <- 0;
	suma <- 0;
	baja <- 10; 
	alta <- 0;
	conAprob <- 0;
	conReprob <- 0;
	aprob <- 0;
	reprob <- 0;
	prom <- 0;
	Escribir "---PROGRAMA QUE CALCULA LA CALIFICACIÓN BAJA Y ALTA LOS APROBADOS Y REPROBADOS---";
	Escribir "Ingrese las calificaciones que va a registrar: ";
	Leer numcal;
	Mientras (x <= numcal) Hacer
		Escribir "Ingrese la califcación ",x,": ";
		Leer calif;
		Si (calif >= 0 y calif <= 10) Entonces
			x <- x + 1;
			suma <- suma + calif;
		    Si (calif > alta) Entonces
				alta <- calif;
			FinSi
			Si (calif < baja) Entonces
				baja <- calif;
			FinSi
			Si (calif >= 6) Entonces
				conAprob <- conAprob + 1;
			FinSi
			Si (calif <= 6) Entonces
				conReprob <- conReprob + 1;
			FinSi
		SiNo
			Escribir "La calificación que ingresaste debe estar entre 0 y 10";
		FinSi
	FinMientras;
	prom <- suma / (x - 1);
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El promedio es: ",prom;
	Escribir "La calificación alta fue: ",alta;
	Escribir "La calificación baja fue: ",baja;
	aprob <- conAprob * 100 / (conAprob + conReprob);
	reprob <- conReprob * 100 / (conAprob + conReprob);
	Escribir "El porcentaje de aprobados es de: ",aprob,"%";
	Escribir "El porcentaje de reprobados es de: ",reprob,"%";
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void Calificaciones()
{
	int x = 1, numcal = 0, calif = 0, suma = 0, baja = 10, alta = 0, conAprob = 0, conReprob = 0;
	float prom = 0, aprob = 0, reprob = 0;
	cout<<"\t---PROGRAMA QUE CALCULA LA CALIFICACI�N BAJA Y ALTA LOS APROBADOS Y REPROBADOS---"<<endl;
	cout<<"Calificaciones a registrar: ";
	cin>>numcal;
	while(x <= numcal)
	{
		cout<<"Ingrese la calificacion "<<x<<": ";
		cin>>calif;
		if(calif >= 0 && calif <= 10)
		{
			x += 1;
			suma += calif;
			if(calif > alta)
			alta = calif;
			if(calif < baja)
			baja = calif;
			if(calif >= 6)
			conAprob += 1;
			if(calif <= 6)
			conReprob += 1;
		}
		else
		{
			cout<<"CALIFICACION INVALIDA"<<endl;
		    cout<<"!!!INGRESE UNA CALIFICACION ENTRE EL 0 Y 10!!!"<<endl;	
		}
	}
	prom = suma / (x - 1);		
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
    cout<<"EL PROMEDIO ES: "<<prom<<endl;	
	cout<<"CALIFICACION ALTA: "<<alta<<endl;	
	cout<<"CALIFICACION BAJA: "<<baja<<endl;
	aprob = conAprob * 100 / (conAprob + conReprob);
	reprob = conReprob * 100 / (conAprob + conReprob);
	cout<<"PORCENTAJE DE APROBADOS: "<<aprob<<"%"<<endl;
	cout<<"PORCENTAJE DE REPROBADOS: "<<reprob<<"%"<<endl;
}
int main()
{
	system("color 0A");
	Calificaciones();
	return 0;
}
```
</details>

##### Ejercicio 13. Determinar cuántos hombres y cuantas mujeres se encuentran en un grupo de N personas
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_13
	Definir x,numpers,sexo,hombres,mujeres Como Entero
	x <- 1;
	numpers <- 0;
	sexo <- 0;
	hombres <- 0;
	mujeres <- 0;
	Escribir "---PROGRAMA QUE CALCULA CUANTOS HOMBRES Y MUJERES HAY EN GRUPO DE N PERSONAS---";
	Escribir "Ingrese el número de personas: ";
	Leer numpers;
	Mientras (x <= numpers) Hacer
		Escribir "Persona ",x,": ";
		Escribir "Eliga un número de acuerdo a tu sexo: ";
		Escribir "1 = HOMBRE";
		Escribir "2 = MUJER";
		Leer sexo;
		Si (sexo == 1) Entonces
			hombres <- hombres + 1;
		SiNo
			Si (sexo == 2) Entonces
				mujeres <- mujeres + 1;
			SiNo
				Escribir "!!!NO SE ENCONTRO EL NúMERO INGRESADO!!!";
				Escribir "INGRESE UN NúMERO EN EL RANGO CORRECTO";
				x <- x - 1;
			FinSi
		FinSi
		x <- x + 1;
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "La cantidad de hombres que hay en el grupo es de: ",hombres;
	Escribir "La cantidad de mujeres que hay en el grupo es de: ",mujeres;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void GrupoHmbMjr()
{
	int x = 1, numpers = 0, masc = 0, fem = 0, sexo = 0;
	cout<<"\t---PROGRAMA QUE CALCULA CUANTOS HOMBRES Y MUJERES HAY EN GRUPO DE N PERSONAS---"<<endl;
	cout<<"Ingrese la cantidad de personas: ";
	cin>>numpers;
	while(x <= numpers)
	{
		cout<<"PERSONA "<<x<<": "<<endl;
		cout<<"1 = HOMBRE"<<endl;
		cout<<"2 = MUJER"<<endl;
		cout<<"Eliga un numero de acuerdo a tu sexo: ";
		cin>>sexo;
		//system("cls");
		if(sexo == 1)
		masc += 1;
		else
		{
			if(sexo == 2)
	        fem += 1;
	        else
	        {
	        	cout<<"!!!NO SE ENCONTRO NUMERO INGRESADO!!!"<<endl;
		        cout<<"INGRESE UN NUMERO EN EL RANGO CORRECTO"<<endl;
		        x -= 1;
			}
		}
		x += 1;
	}
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
    cout<<"CANTIDAD HOMBRES EN EL GRUPO: "<<masc<<endl;	
	cout<<"CANTIDAD MUJERES EN EL GRUPO: "<<fem<<endl;			
}
int main()
{
	system("color 0A");
	GrupoHmbMjr();
	return 0;
}
```
</details>

##### Ejercicio 14. Una compañía de seguros tiene contratados a N vendedores. Cada uno hace 3 ventas a la semana. Su política de pagos es que un vendedor recibe un sueldo base, y un 15% extra por comisiones de sus ventas. El gerente de su compañía desea saber cuánto dinero obtendrá en la semana cada vendedor por concepto de comisiones por las 3 ventas realizadas, y cuanto tomando en cuenta su sueldo base y sus comisiones
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_14
	Definir x, n Como Entero
	Definir sueldo, comision, venta1, venta2, venta3 Como Real
	x <- 1;
	n <- 0;
	sueldo <- 0;
	comision <- 0;
	venta1 <- 0;
	venta2 <- 0;
	venta3 <- 0;
	Escribir "---PROGRAMA QUE CALCULA LA CANTIDAD DE DINERO OBTENIDAD DE TRES VENTAS REALIZADAS---";
	Escribir "Ingrese la cantidad de trabajadores en la compañia: ";
	Leer n;
	Mientras (x <= n) Hacer
		Escribir "Ingrese el sueldo base del trabajador: ";
		Leer sueldo;
		Escribir "Ingrese las ventas del mes: ";
		Leer venta1,venta2,venta3;
		comision <- (venta1+venta2+venta3) * 0.15;
		Escribir "------RESULTADOS OBTENIDOS------";
		Escribir "El sueldo mensual es de: $",sueldo;
		Escribir "La comisión del mes es de: $",comision;
		Escribir "El suelso total con la comisión incluida es de: $",sueldo + comision;
		x <- x + 1;
	FinMientras
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void EmpresaSeguros()
{
	int numtrab = 0;
	float sueldo = 0, comision = 0, venta1 = 0, venta2 = 0, venta3 = 0;
	cout<<"\t---PROGRAMA QUE CALCULA LA CANTIDAD DE DINERO OBTENIDAD DE TRES VENTAS REALIZADAS---"<<endl;
	cout<<"Cantidad de trabajadores en la empresa: ";
	cin>>numtrab;
	for(int x = 1; x <= numtrab; x++)
	{
		cout<<"Sueldo base del trabajador: $";
		cin>>sueldo;
		cout<<"Ventas del mes: ";
		cin>>venta1;
		cout<<"Ventas del mes: ";
		cin>>venta2;
		cout<<"Ventas del mes: ";
		cin>>venta3;
		comision = (venta1 + venta2 + venta3) * 0.15;
		cout<<"\t---RESULTADOS OBTENIDOS---"<<endl<<endl;
        cout<<"SUELDO MENSUAL: $"<<sueldo<<endl<<endl;	
	    cout<<"COMISION DEL MES: $"<<comision<<endl<<endl;	
	    cout<<"SUELDO TOTAL CON LA COMISION INCLUIDA: $"<<sueldo + comision<<endl<<endl;
	}
}
int main()
{
	system("color 0A");
	EmpresaSeguros();
	return 0;
}
```
</details>

##### Ejercicio 15. Obtener la suma y el promedio de calificaciones de un grupo de N alumnos
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_15
	Definir x, numcal Como Entero
	Definir calif, suma, prom Como Real
	x <- 1;
	numcal <- 0;
	calif <- 0;
	suma <- 0;
	prom <- 0;
	Escribir "---PROGRAMA QUE CALCULA EL PROMEDIO DE CALIFICACIONES DE UN GRUPO DE N PERSONAS---";
	Escribir "Ingresa la cantidad de alumnos: ";
	Leer numcal;
	Mientras (x <= numcal) Hacer
		Escribir "Ingrese la califcación ",x,": ";
		Leer calif;
		suma <- suma + calif;
		prom <- suma / numcal;
		x <- x + 1;
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El promedio del grupo es de: ",prom;
	Escribir "La suma de ",numcal," calificaciones ingresadas del grupo es de: ",suma;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void PromedioAlumnos()
{
	int x = 1, numalum = 0;
	float calif = 0, suma = 0, prom = 0;
	cout<<"\t---PROGRAMA QUE CALCULA EL PROMEDIO DE CALIFICACIONES DE UN GRUPO DE N PERSONAS---"<<endl;
	cout<<"Cantidad de alumnos: ";
	cin>>numalum;
	while(x <= numalum)
	{
		cout<<"Ingrese la calificacion "<<x<<": ";
		cin>>calif;
		suma += calif;
		prom = suma / numalum;
		x += 1;
	}
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"PROMEDIO DEL GRUPO: "<<prom<<endl;
	cout<<"LA SUMA DE LAS CALIFICACIONES ES: "<<suma<<endl;
}
int main()
{
	system("color 0A");
	PromedioAlumnos();
	return 0;
}
```
</details>

##### Ejercicio 16. Leer 10 calificaciones de un grupo de alumnos. Calcule y escriba el porcentaje de reprobados y porcentaje de aprobados. Tomando en cuenta que la calificación mínima aprobatoria es de 6
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_16
	Definir x, aprobados, reprobados Como Entero
	Definir calif Como Real
	x <- 1;
	calif <- 0;
	aprobados <- 0;
	reprobados <- 0;
	Escribir "---PROGRAMA QUE CALCULA EL PORCENTAJE DE APROBADOS Y REPROBADOS---";
	Mientras (x <= 10) Hacer
		Escribir "Ingresa la calificacion ",x,": ";
		Leer calif;
		si (calif <= 6) Entonces
			reprobados <- reprobados + 1;
		SiNo
			aprobados <- aprobados + 1;
		FinSi
		x <- x + 1;
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El total de alumnos aprobados es: ",aprobados;
	Escribir "El total de alumnos reprobados es: ",reprobados;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void AprobReprob()
{
	int aprob = 0, reprob = 0;
	float calif = 0;
	cout<<"\t---PROGRAMA QUE CALCULA EL PORCENTAJE DE APROBADOS Y REPROBADOS---"<<endl;
	for(int x = 1; x <= 10; x++)
	{
		cout<<"Ingrese la calificacion "<<x<<": ";
		cin>>calif;
		if(calif <= 6)
		reprob += 1;
		else
		aprob += 1;
	}
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"TOTAL DE ALUMNOS APROBADOS: "<<aprob<<endl;
	cout<<"TOTAL DE ALUMNOS REPROBADOS: "<<reprob<<endl;	
}
int main()
{
	system("color 0A");
	AprobReprob();
	return 0;
}
```
</details>


##### Ejercicio 17. Encontrar el promedio, el valor menor y mayor de un conjunto de 15 números leídos por el usuario
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_17
	Definir x, num, myr, mnr, suma Como Entero
	Definir prommyr, prommnr Como Real	
	x <- 1;
	num <- 0;
	suma <- 0;
	prommyr <- 0;
	myr <- 0;
	prommnr <- 0;
	mnr <- 0;
	Escribir "---PROGRAMA QUE CALCULA EL PROMEDIO DEL VALOR MENOR Y MAYOR DE UN CONJUNTO DE NUMEROS---";
	Mientras  (x <= 15) Hacer
		Escribir "Ingrese el número ",x,": ";
		Leer num;
		Si (x == 1) Entonces
			myr <- num;
			mnr <- num;
		SiNo
			Si (num > myr) Entonces
				myr <- myr + num;
			FinSi
			Si (num < mnr) Entonces
				mnr <- mnr + num;
			FinSi
		FinSi
		x <- x + 1;
	FinMientras
	prommyr <- myr / 15;
	prommnr <- mnr / 15;
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El promedio mayor del conjunto de 15 numeros ingresados es: ",prommyr;
	Escribir "El promedio menor del conjunto de 15 numeros ingresados es: ",prommnr;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void PromMnrMyr()
{
	int num = 0, myr = 0, mnr = 0, suma = 0;
	float prommyr = 0, prommnr = 0;
	cout<<"\t---PROGRAMA QUE CALCULA EL PROMEDIO DEL VALOR MENOR Y MAYOR DE UN CONJUNTO DE NUMEROS---"<<endl;
	for(int x = 1; x<= 15; x++)
	{
		cout<<"Ingrese el numero "<<x<<": ";
		cin>>num;
		if( x == 1)
		{
			myr = num;
			mnr = num;
		}
		else
		if(num > myr)
		myr += num;
		if(num < mnr)
		mnr += num;
	}
	prommyr = myr / 15;
	prommnr = mnr / 15;
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"PROMEDIO MAYOR DE 15 NUMEROS INGRESADOS: "<<prommyr<<endl;	
	cout<<"PROMEDIO MENOR DE 15 NUMEROS INGRESADOS: "<<prommnr<<endl;		
}
int main()
{
	system("color 0A");
	PromMnrMyr();
	return 0;
}
```
</details>

##### Ejercicio 18. Determinar cuántos hombres y cuantas mujeres se encuentran en un grupo de 25 personas
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_18
	Definir x,numpers,sexo,hombres,mujeres Como Entero
	x <- 1;
	numpers <- 0;
	sexo <- 0;
	hombres <- 0;
	mujeres <- 0;
	Escribir "---PROGRAMA QUE CALCULA CUANTOS HOMBRES Y MUJERES HAY EN GRUPO DE 25 PERSONAS---";
	Mientras (x <= 25) Hacer
		Escribir "Persona ",x,": ";
		Escribir "Eliga un numero de acuerdo a tu sexo: ";
		Escribir "1 = HOMBRE";
		Escribir "2 = MUJER";
		Leer sexo;
		Si (sexo == 1) Entonces
			hombres <- hombres + 1;
		SiNo
			Si (sexo == 2) Entonces
				mujeres <- mujeres + 1;
			SiNo
				Escribir "!!!NO SE ENCONTRO EL NUMERO INGRESADO!!!";
				Escribir "INGRESE UN NUMERO EN EL RANGO CORRECTO";
				x <- x - 1;
			FinSi
		FinSi
		x <- x + 1;
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "La cantidad de hombres que hay en el grupo es de: ",hombres;
	Escribir "La cantidad de mujeres que hay en el grupo es de: ",mujeres;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void GrupoHmbMjr()
{
	int masc = 0, fem = 0, sexo = 0;
	cout<<"\t---PROGRAMA QUE CALCULA CUANTOS HOMBRES Y MUJERES HAY EN GRUPO DE 25 PERSONAS---"<<endl;
	for(int x = 1; x <= 25; x++)
	{
		cout<<"PERSONA "<<x<<": "<<endl;
		cout<<"1 = HOMBRE"<<endl;
		cout<<"2 = MUJER"<<endl;
		cout<<"Eliga un numero de acuerdo a tu sexo: ";
		cin>>sexo;
		if(sexo == 1)
		masc += 1;
		else
		{
			if(sexo == 2)
	        fem += 1;
	        else
	        {
	        	cout<<"!!!NO SE ENCONTRO NUMERO INGRESADO!!!"<<endl;
		        cout<<"INGRESE UN NUMERO EN EL RANGO CORRECTO"<<endl;
		        x -= 1;
			}
		}
	}
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
    cout<<"CANTIDAD HOMBRES EN EL GRUPO: "<<masc<<endl;	
	cout<<"CANTIDAD MUJERES EN EL GRUPO: "<<fem<<endl;
}
int main()
{
	system("color 0A");
	GrupoHmbMjr();
	return 0;
}
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
Algoritmo EJERCICIO_19
	Definir x Como Entero
	Definir numautos, autsamarillo, autsrosa, autsrojo, autsverde, autsazul, autcolor Como Real
	x <- 1;
	numautos <- 0;
	autsamarillo <- 0;
	autsrosa <- 0;
	autsrojo <- 0;
	autsverde <- 0;
	autsazul <- 0;
	autcolor <- 0;
	Escribir "---PROGRAMA QUE CALCULA LA CANTIDAD DE AUTOS QUE HAY SEGUN SU PLACA---";
	Escribir "Ingrese el número de autos a registrar: ";
	Leer numautos;
	Mientras (x <= numautos) Hacer
		Escribir "!!!DE ACUERDO A LA SIGUIENTE LISTA CON EL ULTIMO DIGITO DE SU PLACA SE PUEDE DETERMINAR EL COLOR!!!";
		Escribir "1 ó 2 -> Amarillo";
		Escribir "3 ó 4 -> Rosa";
		Escribir "5 ó 6 -> Roja";
		Escribir "7 ó 8 -> Verde";
		Escribir "9 ó 0 -> Azul";
		Escribir "Ingrese el ultimo número de acuerdo a su placa: ";
		Leer autcolor;
		Si (autcolor == 1 o autcolor == 2) Entonces
			autsamarillo <- autsamarillo + 1;
		FinSi
		Si (autcolor == 3 o autcolor == 4) Entonces
			autsrosa <- autsrosa + 1;
		FinSi
		Si (autcolor == 5 o autcolor == 6) Entonces
			autsrojo <- autsrojo + 1;
		FinSi
		Si (autcolor == 7 o autcolor == 8) Entonces
			autsverde <- autsverde + 1;
		FinSi
		Si (autcolor == 9 o autcolor == 0) Entonces
			autsazul <- autsazul + 1;
		FinSi
		x <- x + 1;
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "El total de automóviles con calcomanía amarilla es de: ",autsamarillo;
	Escribir "El total de automóviles con calcomanía rosa es de: ",autsrosa;
	Escribir "El total de automóviles con calcomanía roja es de: ",autsrojo;
	Escribir "El total de automóviles con calcomanía verde es de: ",autsverde;
	Escribir "El total de automóviles con calcomanía azul es de: ",autsazul;
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void DeptoPlacas()
{
	int numautos = 0, autcolor = 0, autsamarillo = 0, autsrosa = 0, autsrojo = 0, autsverde = 0, autsazul = 0;
	cout<<"\t---PROGRAMA QUE CALCULA LA CANTIDAD DE AUTOS QUE HAY SEGUN SU PLACA---"<<endl;
	cout<<"Ingrese el numero de autos a registrar: ";
	cin>>numautos;
	for(int x = 1; x <= numautos; x++)
	{
		cout<<"!!!DE ACUERDO A LA SIGUIENTE LISTA CON EL ULTIMO DIGITO DE SU PLACA SE PUEDE DETERMINAR EL COLOR!!!"<<endl;
		cout<<"1 o 2 -> Amarillo"<<endl;
		cout<<"3 o 4 -> Rosa"<<endl;
		cout<<"5 o 6 -> Roja"<<endl;
		cout<<"7 o 8 -> Verde"<<endl;
		cout<<"9 o 0 -> Azul"<<endl;
		cout<<"Ingrese el ultimo numero de acuerdo a su placa: ";
		cin>>autcolor;
		if(autcolor == 1 || autcolor == 2)
		autsamarillo += 1;
		if(autcolor == 3 || autcolor == 4)
		autsrosa += 1;
		if(autcolor == 5 || autcolor == 6)
		autsrojo += 1;
		if(autcolor == 7 || autcolor == 8)
		autsverde += 1;
		if(autcolor == 9 || autcolor == 0)
		autsazul += 1;
	}
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"TOTAL DE AUTOS CON CALCOMANIA AMARILLA: "<<autsamarillo<<endl;	
	cout<<"TOTAL DE AUTOS CON CALCOMANIA ROSA: "<<autsrosa<<endl;	
	cout<<"TOTAL DE AUTOS CON CALCOMANIA ROJA: "<<autsrojo<<endl;	
	cout<<"TOTAL DE AUTOS CON CALCOMANIA VERDE: "<<autsverde<<endl;
	cout<<"TOTAL DE AUTOS CON CALCOMANIA AZUL: "<<autsazul;		
}
int main()
{
	system("color 0A");
	DeptoPlacas();
	return 0;
}
```
</details>

##### Ejercicio 20. Una compañía de seguros tiene contratados a N vendedores. Cada uno hace 3 ventas a la semana. Su política de pagos es que un vendedor recibe un sueldo base, y un 15% extra por comisiones de sus ventas. El gerente de su compañía desea saber cuánto dinero obtendrá en la semana cada vendedor por concepto de comisiones por las 3 ventas realizadas, y cuanto tomando en cuenta su sueldo base y sus comisiones
<details>
<summary>Pseudocódigo</summary>

```
Algoritmo EJERCICIO_20
	Definir x, hrstrab, hrsextras, hrstriple, numobr Como Entero
	Definir pagohrs, sueldo Como Real
	x <- 1;
	hrstrab <- 0;
	hrsextras <- 0;
	hrstriple <- 0;
	numobr <- 0;
	pagohrs <- 0;
	sueldo <- 0;
	Escribir "------PROGRAMA QUE CALCULA LA CANTIDAD SEMANAL DE DINERO------";
	Escribir "Ingrese la cantidad de obreros: ";
	Leer numobr;
	Mientras (x <= numobr) Hacer
		Escribir "Obrero ",x,": ";
		Escribir "Ingrese sus horas trabajadas: ";
		Leer hrstrab;
		Escribir "Ingrese el pago por hora: ";
		Leer pagohrs;
		Si (hrstrab > 40) Entonces
			hrsextras <- hrstrab - 40;
			Si (hrsextras > 8) Entonces
				hrstriple <- hrsextras - 8;
				sueldo <- (40 * pagohrs) + (8 * pagohrs * 2) + (hrstriple * pagohrs * 3);
			SiNo
				sueldo <- (40 * pagohrs) + (hrsextras * pagohrs * 2);
			FinSi
		SiNo
			sueldo <- hrstrab * pagohrs;
		FinSi
		x <- x + 1;
	FinMientras
	Escribir "------RESULTADOS OBTENIDOS------";
	Escribir "La cantidad semanal de dinero que recibiran ",numobr," obreros por las horas trabajadas es de: $",sueldo; 
FinAlgoritmo
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void SalarioObrero()
{
	int hrstrab = 0, hrsextras = 0, hrstriple = 0, numsobr = 0;
	float pagohrs = 0, sueldo = 0;
	cout<<"\t---PROGRAMA QUE CALCULA LA CANTIDAD SEMANAL DE DINERO---"<<endl;
	cout<<"Ingrese la cantidad de obreros: ";
	cin>>numsobr;
	for(int x = 1; x <= numsobr; x++)
	{
		cout<<"Obrero "<<x<<": "<<endl;
		cout<<"Ingrese sus horas trabajadas a la semana: ";
	    cin>>hrstrab;
	    cout<<"Ingrese el pago por hora: $";
	    cin>>pagohrs;
	    system("cls");
	    if(hrstrab > 40)
	    {
		    hrsextras = hrstrab - 40;
		    if(hrsextras > 8)
		    {
			    hrstriple = hrsextras - 8;
		        sueldo = (40 * pagohrs) + (8 * pagohrs * 2) + (hrstriple * pagohrs * 3);
		    }
		    else
		    sueldo = (40 * pagohrs) + (hrsextras * pagohrs * 2);
	    }
	    else
	    sueldo = hrstrab * pagohrs;		
	}
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"LA CANTIDAD SEMANAL DE DINERO A RECIBIR POR "<<hrstrab<<" HORAS TRABAJADAS ES DE: $"<<sueldo;
}
int main()
{
	system("color 0A");
	SalarioObrero();
	return 0;
}
```
</details>

##### Ejercicio 21. Determinar la cantidad semanal de dinero que recibirá cada uno de los N obreros de una empresa. Se sabe que cuando las horas que trabajo un obrero exceden de 40, el resto se convierte en horas extras que se pagan al doble de una hora normal, cuando no exceden de 8; cuando las horas extras exceden de 8 se pagan las primeras 8 al doble de lo que se paga por una hora normal y el resto al triple
<details>
<summary>Pseudocódigo</summary>

```
Proceso EJERCICIO_21
	Definir x, edad Como Entero
	Definir peso, prominfan, promjoven, promadul, promviejos Como Real
	x <- 1;
	edad <- 0;
	peso <- 0;
	prominfan <- 0;
	promjoven <- 0;
	promadul <- 0;
	promviejos <- 0;
	Para x <- 1 Hasta 10 Con Paso 1 Hacer
		Escribir "Persona ",x,": ";
		Escribir "Ingresa su edad: ";
		Leer edad;
		Escribir "Ingresa su peso: ";
		Leer peso;
		Si (edad >= 0 y edad <= 12) Entonces
			prominfan <- prominfan + peso;
		FinSi
		Si (edad >= 13 y edad <= 29) Entonces
			promjoven <- promjoven + peso;
		FinSi
		Si (edad >= 30 y edad <= 59) Entonces
			promadul <- promadul + peso;
		FinSi
		Si (edad >= 60) Entonces
			promviejos <- promviejos + peso;
		FinSi
	FinPara
	prominfan <- 100.0 * (prominfan / 10);
	promjoven <- 100.0 * (promjoven / 10);
	promadul <- 100.0 * (promadul / 10);
	promviejos <- 100.0 * (promviejos / 10);
	Escribir "El promedio de los adultos: ", promadul;
	Escribir "El promedio de los jovenes: ", promjoven;
	Escribir "El promedio de los infantes: ", prominfan;
	Escribir "El promedio de los adultos mayores: ", promviejos;
FinProceso
```
</details>

<details>
<summary>C++</summary>

```c++
#include<iostream>
using namespace std;
void MuestreoPeso()
{
	int edad = 0;
	float peso = 0, prominfan = 0, promjoven = 0, promadul = 0, promviejos = 0;
	cout<<"\t---PROGRAMA QUE CALCULA EL PROMEDIO DE PESO---"<<endl;
	for(int x = 1; x <= 10; x++)
	{
		cout<<"Persona "<<x<<": "<<endl;
	    cout<<"Ingrese su edad: ";
	    cin>>edad;
		cout<<"Ingrese su peso: ";	
		cin>>peso;
		if(edad >= 0 && edad <= 12)
		prominfan += peso;
		if(edad >= 13 && edad <= 29)
		promjoven  += peso;
		if(edad >= 30 && edad <= 59)
		promadul += peso;
		if(edad >= 60)
		promviejos += peso;
	}
	prominfan = 100.0 * (prominfan / 10);
	promjoven = 100.0 * (promjoven / 10);
	promadul = 100.0 * (promadul / 10);
	promviejos = 100.0 * (promviejos / 10);
	system("cls");
	cout<<"\t---RESULTADOS OBTENIDOS---"<<endl;
	cout<<"PROMEDIO DE LOS INFANTES: "<<prominfan<<endl;
	cout<<"PROMEDIO DE LOS JOVENES: "<<promjoven<<endl;
	cout<<"PROMEDIO DE LOS ADULTOS: "<<promadul<<endl;
	cout<<"PROMEDIO DE LOS ADULTOS MAYORES: "<<promviejos;
}
int main()
{
	system("color 0A");
	MuestreoPeso();
	return 0;
}
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

```c++

```
</details>