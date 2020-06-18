---
description: Estructura condicional if y else.
---

# 6 - Estructuras condicionales simples y compuestas

No todos los problemas pueden resolverse empleando estructuras secuenciales 🙅🏾♂ . Cuando hay que tomar una decisión 🤔 aparecen las estructuras condicionales:

* ¿Elijo la carrera A o la carrera B 📋 ? 
* ¿Me pongo este pantalón 👖 ? 
* Para ir al trabajo, ¿Elijo el camino A 🛣 o el camino B 🛤 ?

Es común que en un problema se combinan estructuras secuenciales y condicionales.

### Estructura condicional simple

Es cuando tenemos la opción de realizar una actividad o no realizar ninguna.

![Diagrama de flujo estructura condicional simple](.gitbook/assets/image%20%2813%29.png)

**Podemos observar:**

* El rombo representa la condición 🚦 
* Hay dos opciones que se pueden tomar ⏯ . Si la condición da verdadera se sigue el camino del verdadero ✅ , o sea el de la derecha, si la condición da falsa ❎ se sigue el camino de la izquierda donde no hay ninguna actividad.
* Se trata de una estructura **condional simple** porque por el camino del verdadero hay actividades 👾 y por el camino del falso no hay actividades.
* Por el camino del verdadero pueden existir varias operaciones, entradas y salidas, inclusive ya veremos ⏳ que puede haber otras estructuras condicionales.

#### Ejemplo 1

Ingresar el sueldo de una persona en dólares, si este supera los $ 3000 mostrar un mensaje en pantalla indicando que debe abonar \(pagar\) impuestos

![Diagrama de flujo estructura ejemplo 1](.gitbook/assets/image%20%2816%29.png)

Podemos observar 👁🗨 lo siguiente: Siempre se hace la carga del sueldo, pero si el sueldo que ingresamos supera 3000 dolares 🤑 se mostrará por pantalla el mensaje "Esta persona debe abonar impuestos", en caso que la persona cobre 3000 o menos no aparece nada por pantalla.

```python
salary = float (input ("Enter worker salary: $"))
if (salary>=3000) :
    print("you must pay taxes")
```

{% hint style="info" %}
* La palabra clave " **if "** indica que estamos en presencia de una estructura condicional; seguidamente disponemos la condición y finalizamos la línea con el caracter dos puntos     \(" **: "**\).
* La actividad dentro del **if** se _**indenta**_ generalmente a 4 espacios hacia la ➡ derecha .
{% endhint %}

{% hint style="danger" %}
La **indentación** es una característica obligatoria 👮🏾♂ del lenguaje Python para codificación de las estructuras condicionales, de esta forma el intérprete de Python puede identificar donde finalizan las instrucciones contenidas en la rama verdadera del if.
{% endhint %}

Ejecutando ▶  el programa, si ingresamos un sueldo mayor o igual a $ 3000. Podemos observar como aparece en pantalla el mensaje "Esta persona debe abonar impuestos", ya que la condición del if es verdadera:

![Salida c&#xF3;digo ejemplo 1 \(Jupyter\)](.gitbook/assets/image%20%2810%29.png)

Si  volvemos a ejecutar e ingresamos un valor inferior a $ 3000 podemos observar que la instrucción que se encuentra por la rama del verdadero del if no se ejecuta:

![Salida c&#xF3;digo ejemplo 1 \(Jupyter\)](.gitbook/assets/image%20%281%29.png)

### Estructura condicional compuesta

Cuando se presenta una elección 🤔 donde tenemos la opción de realizar una actividad u otra 📋 . Es decir tenemos actividades por el verdadero y por el falso de la condición.

{% hint style="info" %}
Lo más importante que hay que tener en cuenta que se realizan las actividades de la rama del verdadero o las del falso, **nunca** se realizan las actividades de las dos ramas 🎋 
{% endhint %}

![Diagrama flujo estructura condicional compuesta](.gitbook/assets/image%20%2812%29.png)

En una estructura condicional compuesta hay actividades tanto por la rama del verdadero como por la rama del falso.

#### Ejemplo 2

Realizar un programa que solicite ingresar dos números 🔢 distintos y muestre por pantalla 🖥 el mayor de ellos.

![Diagrama de flujo ejemplo 2](.gitbook/assets/image%20%2811%29.png)

Se hace la entrada de num1 y num2 por teclado ⌨ . Para saber cual variable tiene un valor mayor preguntamos si el contenido de num1 **es mayor \(&gt;\)** que el contenido de num2, si la respuesta es verdadera ✅ vamos por la rama de la derecha e imprimimos num1, en caso que la condición sea falsa ❌ vamos por la rama de la izquierda \(Falsa\) e imprimimos num2.

Nunca se imprimen num1 y num2 simultáneamente. Estamos en presencia de una estructura condicional compuesta ya que tenemos actividades por la rama del verdadero y del falso.

```python
number1=int (input("Enter number1:"))
number2= int (input("Enter number2:"))
if(number1>number2):
    print("The greater number is:",number1)
else(number1<number2):
    print("The greater number is:",number2)
```

Cotejemos el diagrama de flujo 🔎 y la codificación y observemos que el primer bloque después del if representa la rama del verdadero y el segundo bloque después de la palabra clave **else** representa la rama del falso.

Ejecutamos el programa, si hubo errores sintácticos corrijamos y carguemos dos valores, como por ejemplo:

![Salida c&#xF3;digo ejemplo 2](.gitbook/assets/image%20%287%29.png)

{% hint style="info" %}
Cuando a un programa le corregimos todos los errores 📋 sintácticos y lógicos ha terminado nuestra tarea y podemos entregar 📩 el mismo al _usuario_ 🧔🏽 que  nos lo solicitó.
{% endhint %}

### Operadores 🛠 

En una condición deben disponerse en únicamente variables, valores constantes y operadores relacionales.

#### Operadores relacionales 👩🔬 

> * Igualdad:   ==
> * Desigualdad:   !=
> * Menor:   &lt;
> * Menor igual:    &lt;=
> * Mayor:    &gt;
> * Mayor igual:    &gt;=

#### Operadores mátematicos 👨🔬 

> * Suma:   +
> * Resta:    -
> * Multiplicación:    \*
> * División flotantes:    /
> * División enteros:     //
> * Resto de una división:    %
> * Exponenciación:    \*\*

Hay que tener en cuenta que al disponer una condición debemos seleccionar que operador relacional se adapta a la pregunta.

#### Ejemplos

1. Ingresar un número y multiplicarlo por 5 si es distinto de cero.         \(!=\)
2. Se ingresan dos números, mostrar una advertencia si son iguales.    \(==\)

{% hint style="info" %}
Los problemas que se pueden presentar son infinitos y la correcta elección del operador solo se alcanza con la práctica intensiva en la resolución de problemas 💪🏾 
{% endhint %}

### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. El tiempo a dedicar a esta **sección ejercicios propuestos** 👩🏾💻 debe ser mucho mayor que el empleado a la sección de **ejercicios resueltos**.  
 La _experiencia_ dice que debemos dedicar el 80% del tiempo 🕖 a la resolución _individual_ de problemas y el otro 20% al análisis y codificación de problemas ya resueltos 🗃 por otras personas.
{% endhint %}

#### Problema 1

Realizar un programa 📇 que solicite la carga por teclado de dos números, si el primero es mayor al segundo informar su suma y diferencia, en caso contrario informar el producto y la división del primero respecto al segundo.

#### Problema 2

Se ingresan tres notas 🗒 de un alumno, si el promedio es mayor o igual a siete mostrar un mensaje "Promocionado"

#### Problema 3

Se ingresa por teclado un número positivo de uno o dos dígitos \(1..99\) mostrar un mensaje indicando si el número tiene uno 7⃣ o dos dígitos 🔟 . \(Tener en cuenta que condición debe cumplirse para tener dos dígitos un número entero\)

#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻 
{% endhint %}



{% tabs %}
{% tab title="Problem 1" %}
```python
number1=int (input("Enter number1:"))
number2= int (input("Enter number2:"))
if(number1>number2):
    suma= number1 + number2
    subtraction= number1 - number1
    print("Sum:",suma)
    print("Sub:", subtraction)
else(number1<number2):
    multiplication=number1*number2
    division = number1 / number2
    print("Mult:",multiplication)
    print("Div:", division)
```
{% endtab %}

{% tab title="Problem 2" %}
```python
#student's grade
note1= float(input("Enter the student's grade1:"))
note2= float(input("Enter the student's grade2:"))
note3= float(input("Enter the student's grade3:"))
#average grade
average=(note1+note2+note3)/3
#if the student is promoted
if(average>=2.96):
    print("The student's promoted ",average)
else :
    print("The student is not promoted",average)
```
{% endtab %}

{% tab title="Problem 3" %}
```python
number=int (input("Enter the number"))
# Negative number
if(number<0):
    number=-1*number;
#Digits
if(number>=0 and number<10):
    print("The number has one digit")
elif (number>=10 and number<100):
    print("The number has two digit")
else:
    print("The number has three or more digits")
```
{% endtab %}
{% endtabs %}









