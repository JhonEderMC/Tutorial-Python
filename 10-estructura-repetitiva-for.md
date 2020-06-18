---
description: >-
  Una estructura repetitiva  permite ejecutar una instrucción o un conjunto de
  instrucciones varias veces.
---

# 10 - Estructura repetitiva for

Cualquier problema que requiera una estructura repetitiva se puede resolver empleando la estructura while, pero hay 🃏 otra estructura repetitiva _cuyo planteo es más sencillo en ciertas situaciones_ que tenemos que recorrer una lista de datos. 📋 

En general, la estructura repetitiva for se usa en aquellas situaciones en las cuales queremos que una variable vaya tomando un valor de una lista definida de valores.

Veremos con una serie de ejemplos el empleo del for.

#### Ejemplo 1

Realizar un programa que imprima 🖨 en pantalla los números del 0 al 20.

```python
for x in range (21):
    print(x)
    
```

Tenemos primero la palabra clave **for** y seguidamente el nombre de la variable que almacenará en cada vuelta del **for** el valor entero que retorna la función **range**.  
 La función range retorna la primera vez el valor 0 y se almacena en x, luego el 1 y así sucesivamente hasta que retorna el valor que le pasamos a range menos uno \(es decir en nuestro ejemplo al final retorna un 20\) Tengamos en cuenta que este mismo problema resuelto con la estructura while debería ser:

```python
x = 0
while x<21 :
    print(x)
    x+=1
```

#### Ejemplo 2

Realizar un programa que imprima en pantalla los números del 20 al 30.

```python
for x in range (20,31):
    print (x)
```

{% hint style="info" %}
La función **range** puede tener dos parámetros, el **primero** indica el valor inicial que tomará la variable x, cada vuelta del for la variable x toma el valor siguiente hasta llegar al valor indicado por el **segundo** parámetro de la función range menos uno.
{% endhint %}

#### Ejemplo 3

Imprimir todos los números impares que hay entre 1 y 100.

```python
for x in range (1,101,2):
    print(x)
```

{% hint style="info" %}
La función **range** puede tener también _tres parámetros_, el _primero_ indica el valor inicial que tomará la variable x, el _segundo_ parámetro el valor final \(que no se incluye\) y el _tercer_ parámetro indica cuanto se incrementa cada vuelta x.
{% endhint %}

En nuestro ejemplo la primera vuelta ➰ del for x vale 1, en la segunda ➿ vuelta  vale 3 y así sucesivamente hasta el valor 99.

#### Ejemplo 4

Desarrollar un programa que permita la carga de 10 valores por teclado y nos muestre posteriormente la suma de los valores ingresados y su promedio.

```python
# addiction
suma=0
for f in range (10):
    numb=int(input(f"Enter the number{f}: "))
    #acumulate
    suma+=numb
average=suma/10
print(f"The addiction is: {suma}")
print(f"The average is: {average}")
```

Como vemos la variable f del for solo sirve para iterar\(repetir\) las diez veces el bloque contenido en el for. En este ejemplo también para ver en que iteración vamos al ingresar los numeros.

El resultado hubiese sido el mismo 😀 si llamamos a la funcion range con los valores: `for f inrange(1,11)`

#### Ejemplo 5

Escribir un programa que solicite por teclado 10 notas de alumnos y nos informe cuántos tienen notas mayores o iguales a 3 y cuántos menores.

```python
# counter greater
# grade great 3
countGreat=0
for i in range(11):
    grade=float(input(f"Enter grade{i}:"))
    if(grade>=3):
        countGreat+=1
print(f"The number of stundents with greater grade: {countGreat}")
print(f"The number of students with less grade: {10-countGreat}")
```

Nuevamente utilizamos el **for**, ya que sabemos 😏 que el ciclo repetitivo debe repetirse 10 veces. Recordemos que si utilizamos el while debemos llevar un contador  y recordar de incrementarlo en cada vuelta. 🔄 

#### Ejemplo 6

Escribir un programa que lea 10 números enteros y luego muestre cuántos valores ingresados fueron múltiplos de 3 y cuántos de 5.

```python
# Counters
mult3=0
mult5=0
for i in range(1,11):
    number=int(input(f"Enter a number{i}:"))
    if(number%3==0):
        mult3+=1
    if(number%5==0):
        mult5+=1
print(f"Multiple of 3: {mult3}")
print(f"Multiple of 5: {mult5}")
```

{% hint style="info" %}
**%** Nos retorna el módulo o residuo de una división, si este es cero un número es multiplo de otro
{% endhint %}

Si ejecutamos el programa se tiene una salida similar:

![Ejecuci&#xF3;n ejemplo 6](.gitbook/assets/image%20%2824%29.png)

#### Ejemplo 7

Codificar un programa que lea n números enteros y calcule la cantidad de valores mayores o iguales a 1000 \(n se carga por teclado\)

```python
# the amount of number
n=int (input("Enter amount of numbers: "))
#counter
count=0
for i in range (1,n+1):
    number=int(input(f"Enter a number{i}: "))
    if(number>=1000):
        count+=1
print(f"The amount of numbers greater than 1000 are: {count}")
```

### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. El tiempo a dedicar a esta **sección ejercicios propuestos** 👩🏾💻 debe ser mucho mayor que el empleado a la sección de **ejercicios resueltos**.  
 La _experiencia_ dice que debemos dedicar el 80% del tiempo 🕖 a la resolución _individual_ de problemas y el otro 20% al análisis y codificación de problemas ya resueltos 🗃 por otras personas.
{% endhint %}

#### Problema 1

Confeccionar un programa que lea n pares de datos, cada par de datos corresponde a la medida de la base y la altura de un triángulo 📐 . El programa deberá informar: 

* De cada triángulo la medida de su base, su altura y su superficie.
* La cantidad de triángulos cuya superficie es mayor a 12.

#### Problema 2

Desarrollar un programa que solicite la carga de 10 números 🔢 e imprima la suma de los últimos 5 valores ingresados.

#### Problema 3

Confeccionar un programa que permita ingresar un valor del 1 al 10 y nos muestre la tabla de multiplicar del mismo \(los primeros 12 términos\)

#### Problema 4

Realizar un programa que lea los lados de n triángulos, e informar:

*  De cada uno de ellos, qué tipo de triángulo es: equilátero \(tres lados iguales\), isósceles \(dos lados iguales\), o escaleno \(ningún lado igual\).
* Cantidad de triángulos de cada tipo.

#### Problema 5

Escribir un programa que pida ingresar coordenadas \(x,y\) que representan puntos en el [plano cartesiano](https://es.wikipedia.org/wiki/Coordenadas_cartesianas) ➕ . Informar cuántos puntos se han ingresado en el primer, segundo, tercer y cuarto cuadrante. Al comenzar el programa se pide que se ingrese la cantidad de puntos a procesar.

![Plano cartesiano](.gitbook/assets/image%20%2823%29.png)

#### Problema 6

Se cuenta con la siguiente información: Las edades de 5 estudiantes ✍🏽 del turno mañana. Las edades de 6 estudiantes del turno tarde. Las edades de 11 estudiantes del turno noche. Las edades de cada estudiante deben ingresarse por teclado.

* Obtener el promedio de las edades de cada turno \(tres promedios\).
* Imprimir dichos promedios \(promedio de cada turno\).
* Mostrar por pantalla un mensaje que indique cual de los tres turnos tiene un promedio de edades mayor.

#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
#### number of triangles
n=int (input("The number of triangles: "))
# counter greater than 12 area
count=0
for i in range(1,n+1):
    height=float(input(f"The triangle height{i}: "))
    base=float(input(f"The triangle base{i}: "))
    # area
    area=(height*base)/2
    if (area>=12):
        count+=1
print(f"The number of triangles with area greater than 12 are: {count}")
```
{% endtab %}

{% tab title="Problem 2" %}
```python
# acumulate
sum=0
for x in range(10):
    numb=int(input(f"Enter number{x}: "))
    # acmulate
    if (x>=4):
        sum+=numb
print ("Sum: ",sum)
```
{% endtab %}

{% tab title="Problem 3" %}
```python
# input number
number=int(input("Enter a number: "))
for i in range (1,13):
    print(i*number)
```
{% endtab %}

{% tab title="Problem 4" %}
```python
# counters
countEquilateral=0
countIsosceles=0
countScalene=0
# the amount of triangles
n= int (input("Number of triangles: "))
for i in range(n):
    side1=int(input("Enter side1: "))
    side2=int(input("Enter side2: "))
    side3=int(input("Enter side3: "))
    # type of triangle
    if(side1==side2 and side1==side3): #equilateral
        countEquilateral+=1
    elif(side1==side2 or side1==side3 or side1==side3): #isoceles
        countIsosceles+=1
    else: #scalene
        countScalene+=1
print("Equilateral: ",countEquilateral)
print("Isosceles: ",countIsosceles)
print("Scalene: ", countScalene)
```
{% endtab %}

{% tab title="Problem 5" %}
```python
# number of points
n=int(input("Enter the number of points: "))
#counter
quadrantFirst=0
quadrantSecond=0
quadrantThird=0
quadrantFour=0
for i in range (n):
    x=int(input("axis X: "))
    y=int(input("axis Y: "))
    #cartesian plane    
    if(x==0 and y==0):
        print("The point is origin")
    elif(x==0 and y>0):
        print("The point is axis Y positive")
    elif(x==0 and y<0):
        print("The point is axis Y negative")
    elif(x>0 and y==0):
        print("The point is axis X positive")
    elif(x<0 and y==0):
        print("The point is axis X negative")
    elif(x>0 and y>0):
        print("The point is first quadrant")
        quadrantFirst+=1
    elif(x<0 and y>0):
        print("The point is Second quadrant")
        quadrantSecond+=1
    elif(x<0 and y<0):
        print("The point is third quadrant")
        quadrantThird+=1
    elif (x>0 and y<0):
        print("The point is four quadrant")
        quadrantFour+=1
print("\n The number of point in each quadrant")
print("First: ",quadrantFirst)
print("Second: ",quadrantSecond)
print("Third: ",quadrantThird)
print("Four: ",quadrantFour)
```
{% endtab %}

{% tab title="Problem 6" %}
```python
# average stundents
averageMorning=0
averageAfternoon=0
averageEvening=0
#Morning 
print("Morning:")
for f in range(5):
    age=int(input(f"student's age{f+1}: "))
    averageMorning+=age
#afternoon
print("Afternoon:")
for f in range(6):
    age=int(input(f"student's age{f+1}: "))
    averageAfternoon+=age
# evenning
print("Evenning:")
for f in range(11):
    age=int(input(f"student's age{f+1}: "))
    averageEvening+=age
# average
averageMorning=averageMorning//5
averageAfternoon=averageAfternoon//6
averageEvening=averageEvening//11
# print data
print("Morning: ",averageMorning)
print("Afternoon: ",averageAfternoon)
print("Evening: ",averageEvening)   
```
{% endtab %}
{% endtabs %}













