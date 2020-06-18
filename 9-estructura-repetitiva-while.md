---
description: >-
  Una estructura repetitiva  permite ejecutar una instrucción o un conjunto de
  instrucciones varias veces.
---

# 9 - Estructura repetitiva while

  
Hasta ahora hemos empleado estructuras **secuenciales** y **condicionales**. Existe 🤖 otro tipo de estructuras tan importantes como las anteriores que son las estructuras **repetitivas.**

Una estructura repetitiva ➿ permite ejecutar una instrucción o un conjunto de instrucciones varias veces.

Una estructura repetitiva se caracteriza por:

{% hint style="info" %}
* La sentencia o las sentencias que se repiten.
* El test o prueba de condición antes de cada repetición, que motivará que se repitan o no las instrucciones.
{% endhint %}

### Estructura repetitiva while

![Diagrama de flujo estructura repetitica while](.gitbook/assets/image%20%2820%29.png)

⚠ No debemos confundir la representación gráfica de la estructura repetitiva **while** \(Mientras\) con la estructura condicional **if** \(Si\)

  
 **Funcionamiento:**

* En primer lugar se verifica la condición, si la misma resulta verdadera se ejecutan las operaciones ⚙ que indicamos por la rama del Verdadero**.**
* A la rama del verdadero la graficamos en la parte inferior de la condición. Una línea al final del bloque de repetición la conecta con la parte superior de la estructura repetitiva.
* En caso que la condición sea _falsa_ continúa por la rama del _falso_ y sale de la estructura repetitiva para continuar con la ejecución del algoritmo. ⏭ 

{% hint style="warning" %}
El bloque se repite **mientras** la condición sea verdadera.
{% endhint %}

{% hint style="danger" %}
 **Importante:** Si la condición siempre retorna verdadero estamos en presencia de un ciclo repetitivo infinito .♾ Dicha situación es un error de programación lógico, nunca finalizará el programa.
{% endhint %}

#### Ejemplo 1

Realizar un programa que imprima en pantalla los números del 1 al 100. 🖨 

Sin conocer las estructuras repetitivas podemos resolver el problema empleando una estructura secuencial. Iniciamos una variable con el valor 1, luego imprimimos la variable, incrementamos nuevamente la variable y así sucesivamente. 😓 

![Diagrama de flujo estructura sencuencial ejemplo 1](.gitbook/assets/image%20%2821%29.png)

Si continuamos con el diagrama veríamos que es una forma ineficiente y casi interminable. 🤕   
 Emplear una estructura secuencial para resolver este problema produce un diagrama de flujo y un programa en Python muy largo. 😫 

Ahora veamos la solución empleando una estructura repetitiva while:

![Diagrama de flujo estructura while ejemplo 1](.gitbook/assets/image%20%2817%29.png)

Es muy importante analizar este diagrama: 🕵🏾♂ 

*  La primera operación inicializa la variable x en 1, seguidamente comienza la estructura repetitiva while y disponemos la siguiente condición \( x &lt;= 100\), se lee **mientras** la variable x sea menor o igual a 100.
*  Al ejecutarse la condición retorna **verdadero** porque el contenido de `x = 1` es menor o igual a 100. Al ser la condición _verdadera_ se ejecuta el bloque de instrucciones que contiene la estructura _while._
* El bloque de instrucciones contiene una salida y una operación. Se imprime el contenido de `x` y seguidamente se incrementa la variable `x` en uno. `x = x+1` 
* Es decir, si x contiene 1 luego de ejecutarse esta operación se almacenará en x un 2.

{% hint style="info" %}
* Al finalizar el bloque de instrucciones que contiene la estructura repetitiva se verifica nuevamente 🔙 la condición de la estructura repetitiva y se repite el proceso explicado anteriormente.
* Mientras la condición retorne verdadero ✅ se ejecuta el bloque de instrucciones; al retornar falso ❌ la verificación de la condición se sale de la estructura repetitiva y continua el algoritmo, en este caso \(ejemplo 1\) finaliza el programa.
{% endhint %}

Lo más difícil es la definición de la condición de la estructura _while_ y que bloque de instrucciones se van a repetir. Observar que si, por ejemplo, disponemos la condición `x >=100` \( si x es mayor o igual a 100\) no provoca ningún _error sintáctico_ pero estamos en presencia de un _error lógico_ porque al evaluarse por primera vez la condición retorna falso ❌ y no se ejecuta el bloque de instrucciones que queríamos repetir 100 veces. 🤦🏾♀ 

{% hint style="info" %}
No existe una **receta** para definir una condición de una estructura repetitiva, sino que se logra con una práctica continua 💪🏾 solucionando problemas. ✍🏾 
{% endhint %}

Una vez planteado el diagrama debemos verificar si el mismo es una solución válida al problema \(en este caso se debe imprimir los números del 1 al 100 en pantalla\), para ello podemos hacer un seguimiento del flujo del diagrama y los valores que toman las variables a lo largo de la ejecución:

```text
x
	1
	2
	3
	4
	.
	.
  100
  101  Cuando x vale 101 la condición de la estructura repetitiva retorna falso, 
       en este caso finaliza el diagrama.
```

{% hint style="danger" %}
* Podemos observar que el bloque repetitivo puede _no ejecutarse_ ninguna vez si la condición retorna falso la primera vez. 
* La variable a verificar en la condición debe estar inicializada con algún valor antes que se ejecute la condición, en caso contrario aparece un error en el interprete.
* Es importante notar que seguido de la palabra clave **while** disponemos la condición y finalmente los dos puntos. Todo el código contenido en la estructura repetitiva debe estar _indentado_ \(normalmente a cuatro espacios\)
{% endhint %}

```python
x=1
while x<=100:
    print(x)  
    x+=1
```

Probemos algunas modificaciones de este programa y veamos que cambios se deberían hacer para:

> 1. Imprimir los números del 1 al 500.
> 2. Imprimir los números del 50 al 100.
> 3. Imprimir los números del -50 al 0.
> 4. Imprimir los números del 2 al 100 pero de 2 en 2 \(2,4,6,8 ....100\).

{% hint style="info" %}
Tomate unos momentos para pensar 🤔 que tendrías que cambiar en el código o programa para lograr imprimir los números anteriores.
{% endhint %}

Respuestas:

> 1. Debemos cambiar la condición del while con `x<=500`.
> 2. Debemos inicializar `x` con el valor 50.
> 3. Inicializar `x` con el valor -50 y fijar la condición `x<=0`.
> 4. Inicializar a `x` con el valor 2 y dentro del bloque repetitivo incrementar a `x` en 2
>
>        `( x = x + 2 )`

#### Ejemplo 2

Codificar un programa que solicite la carga de un valor positivo y nos muestre desde 1 hasta el valor ingresado de uno en uno.

{% hint style="info" %}
Es de **fundamental** importancia analizar 🧠 los diagramas de flujo y la posterior codificación en Python ⚕ de los ejemplos y posteriores problemas que codificaras, en varios ejemplos y problemas se presentan otras situaciones no vistas en el ejercicios anteriores.
{% endhint %}

![Diagrama de flujo ejemplo 2](.gitbook/assets/image%20%2819%29.png)

Podemos observar que se ingresa por teclado la variable n. El operador 👲🏼 puede cargar cualquier valor. Si el usuario carga 10 el bloque repetitivo se ejecutará 10 veces, ya que la condición es “Mientras x&lt;=n ”, es decir “mientras x sea menor o igual a 10”; pues x comienza en uno y se incrementa en uno cada vez que se ejecuta el bloque repetitivo. ➿ 

La prueba del diagrama la podemos realizar dándole valores a las variables; por ejemplo, si ingresamos 5 el seguimiento es el siguiente:

> n        x
>
> 5        1  \(Se imprime el contenido de x\)
>
>         2 "                  "
>
>         3 "                  "
>
>         4 "                  "
>
>         5 "                  "
>
>         6 \(Sale del while porque 6 no es menor o igual a 5\)

```python
# Number
n= int (input("Enter the number: "))
x=1
while (x<=n):
    print(x)
    x+=1
```

{% hint style="info" %}
La variable x recibe el nombre de **contador**. Un contador es un tipo especial de variable que se _incrementa_ ⬆ o _disminuye_ ⬇  con valores constantes durante la ejecución del programa. 
{% endhint %}

El contador x nos indica en cada momento la cantidad de valores impresos en pantalla.

#### Ejemplo 3

Desarrollar un programa que permita la carga de 10 valores por teclado y nos muestre posteriormente la suma de los valores ingresados y su promedio.

![Diagrama de flujo ejemplo 3](.gitbook/assets/image%20%2818%29.png)

En este problema, a semejanza de los anteriores, tenemos un **contador** llamado x que nos sirve para contar las vueltas que debe repetir el while.  
 También aparece el concepto de **acumulador** \(un acumulador es un tipo especial de variable que se incrementa o disminuye con valores variables durante la ejecución del programa\).

Hemos dado el nombre 🃏 de suma a nuestro acumulador. Cada ciclo que se repita la estructura repetitiva, la variable suma se incrementa con el contenido ingresado en la variable valor `(suma=suma+valor)`

La prueba del diagrama se realiza dándole valores a las variables:

> valor            suma           x           promedio
>
>      0                    0
>
> \(Antes de entrar a la estructura repetitiva estos son los valores\).
>
>  5                5                1
>
> 16                21                2
>
>  7                28                3
>
> 10                38                4
>
>  2                40                5
>
> 20                60                6
>
>  5                65                7
>
>  5                70                8
>
> 10                80                9
>
>  2                82             10
>
>  8                90             11
>
>                                                     9

Este es un seguimiento del diagrama planteado. Los números que toma la variable valor dependerá de qué cifras cargue el operador durante la ejecución del programa.  
El promedio se calcula al salir de la estructura repetitiva \(es decir primero sumamos los 10 valores ingresados y luego los dividimos por 10\)

Hay que tener en cuenta que cuando en la variable valor se carga el primer valor \( 5\) al cargarse el segundo valor \(16\) el valor anterior 5 se pierde, por ello la necesidad de ir almacenando 💾 en la variable suma los valores ingresados.

```python
# count
i=(int)(1) 
# acumulate
sum=0
while i<=10:
    x=int(input(r"Enter a number:" ))
    sum+=x
    i+=1
#average
prom=sum/10    
print(f"The addiction is {sum} and the average is {prom} ")
```

El resultado del promedio es un número real. Si queremos que el resultado de la división solo retorne la parte entera del promedio debemos utilizar el operador `//`

`prom = sum / 10`

El interprete de Python sabe que el promedio se calcula al finalizar el while ya que se encuentra codificado en la columna 1. Las tres instrucciones contenidas en el while están indentadas.

#### Ejemplo 4

Una planta que fabrica perfiles de hierro ⛏ posee un lote de n piezas. Confeccionar un programa que pida ingresar por teclado la cantidad de piezas a procesar y luego ingrese la longitud de cada perfil; sabiendo que la pieza cuya longitud esté comprendida en el rango de 1.20 y 1.30 son aptas. Imprimir por pantalla la cantidad de piezas aptas que hay en el lote.

![Diagrama de flujo ejemplo 4](.gitbook/assets/image%20%2822%29.png)

  
Podemos observar que dentro de una estructura repetitiva puede haber estructuras condicionales \(inclusive puede haber otras estructuras repetitivas que veremos más adelante\).

En este problema hay que cargar inicialmente la cantidad 🔢 de piezas a ingresar \( n \), seguidamente se cargan n valores de largos de piezas.  
 Cada vez que ingresamos un largo de pieza \(piece\) verificamos si es una medida correcta \(debe estar entre 1.20 y 1.30 el largo para que sea correcta\), en caso de ser correcta la **contamos** \(incrementamos la variable cantidad en 1\)

Al contador de cantidad \(amount\) lo inicializamos en cero porque inicialmente no se ha cargado ningún largo de pieza.  
 Cuando salimos de la estructura repetitiva porque se han cargado n largos de piezas mostramos 🖥 por pantalla el contador amount \(que representa la cantidad de piezas aptas\)

El contador \(i\) cuenta la cantidad de piezas ingresadas.

```python
# number of pieces in the lot
n=int(input("Enter the number of pieces in the lot: "))
# counters
# while
i=1 
# good pieces
amount=0
while (i<=n):
    # lenght of piece
    piece=float(input("Enter the piece: "))
    # count good pieces
    if (piece>=1.20 and piece<=1.30):
        amount+=1
    # increase counter    
    i+=1
print(f"The good pieces is {amount}")
```

{% hint style="warning" %}
Para ingresar o convertir un número real se utilziar **float** en vez de int
{% endhint %}

### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. El tiempo a dedicar a esta **sección ejercicios propuestos** 👩🏾💻 debe ser mucho mayor que el empleado a la sección de **ejercicios resueltos**.  
 La _experiencia_ dice que debemos dedicar el 80% del tiempo 🕖 a la resolución _individual_ de problemas y el otro 20% al análisis y codificación de problemas ya resueltos 🗃 por otras personas.
{% endhint %}

#### Problema 1

Escribir un programa que solicite ingresar 10 notas de alumnos y nos informe cuántos tienen notas mayores o iguales a 3 y cuántos menores.

#### Problema 2

Se ingresan un conjunto de n alturas de personas por teclado. Mostrar la altura promedio de las personas.

#### Problema 3

En una empresa trabajan n empleados cuyos sueldos 💵 oscilan entre $100 y $500, realizar un programa que lea los sueldos que cobra cada empleado e informe cuántos empleados cobran entre $100 y $300 y cuántos cobran más de $300. Además el programa deberá informar el importe que gasta la empresa en sueldos al personal.

#### Problema 4

Realizar un programa que imprima 25 términos de la serie 11 - 22 - 33 - 44, etc. \(No se ingresan valores por teclado\).

#### Problema 5

Mostrar los múltiplos de 8 hasta el valor 500. Debe aparecer en pantalla 8 - 16 - 24, etc.

#### Problema 6

Desarrollar un programa que permita cargar n números enteros 🔢 y luego nos informe cuántos valores fueron pares y cuántos impares.



#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
i=1
# counter greater
countGreater=0
while (i<=10):
    # grades
    grade=float(input("Enter grade:"))
    # if it is greater than 3.5
    if(grade>=3.5):
        # acumulate
        countGreater+=1
    # increase count    
    i+=1
print(f"the number of stundts with greater grade: {countGreater}")
print(f"The number of stundets with less grade: {10-countGreater} ")
```
{% endtab %}

{% tab title="Problem 2" %}
```python
# number of people
n=int (input("Enter the number of people:"))
# count
i=1
# acumualte heights
addiHeight=0
while i<=n:
    height=float (input ("The person's height: "))
    #acumulate
    addiHeight+=height
    # increase counter
    i+=1
# average heights
averageHeight=addiHeight/n
print(f"The average heigth is: {averageHeight}")
```
{% endtab %}

{% tab title="Problem 3" %}
```python
# number of employeer
n = int(input("Enter the number of employee: "))
# counters
i=1 # while
count100and300=0 #salaries in range
countGreat300=0
while (i<=n):
    # input salary
    salary=int(input())   
    if(salary>=100 and salary <=300):
        count100and300+=1
    elif (salary>300):
        countGreat300+=1
    # increase counter while
    i+=1
print(f"The number of employee with salary between 100 and 300: {count100and300}")
print(f"The number of employee with salary greater than 300: {countGreat300}")
```
{% endtab %}

{% tab title="Problem 4" %}
```python
i=1
while i<=25:
    print(f"{11*i}")
    i+=1
```
{% endtab %}

{% tab title="Problem 5" %}
```python
i=1
x=0
while (x<500):
    x=8*i
    print(x)
    i+=1    
```
{% endtab %}

{% tab title="Problem 6" %}
```python
# The amount of number
n=int(input("Enter amount of numbers: "))
# counters
# while
i=1
# odd numbers
oddNumbers=0
# even numbers
evenNumbers=0
while (i<=n):
    # input number
    number=int (input("Enter a number:"))
    #if it is a even number
    if(number%2==0):
        evenNumbers+=1
    else:
        oddNumbers+=1
    #increase counter while
    i+=1
print (f"The amount of even numbers: {evenNumbers}")
print (f"The amount of odd numbers: {oddNumbers}")

```
{% endtab %}
{% endtabs %}

