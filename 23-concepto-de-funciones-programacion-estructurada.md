# 23 - Concepto de funciones - Programación estructurada

Hasta ahora hemos trabajado ✍🏾 con una metodología de programación lineal. Todas las instrucciones de nuestro archivo \*.py se ejecutan en forma secuencial de principio a fin. Esta forma de organizar un programa solo puede ser llevado a cabo si el mismo es muy pequeño \(decenas de líneas\).

Cuando los problemas a resolver tienden a ser más grandes la metodología de programación lineal se vuelve ineficiente 🤕 y compleja. El segundo paradigma de programación que veremos 😁 es la **programación estructurada**.

La programación 🤖 estructurada busca dividir o descomponer un problema complejo en pequeños problemas. La solución de cada uno de esos pequeños problemas nos trae la solución del problema complejo. En Python  el planteo de esas pequeñas soluciones al problema complejo se hace dividiendo el programa en funciones.

Una **función** es un conjunto de instrucciones en Python que resuelven un problema específico.

El lenguaje Python ya tiene incorporada algunas funciones básicas. Algunas de ellas ya las utilizamos 👨🏽🔧 en conceptos anteriores como son las funciones: _print_, _len_ y _range_.

Veamos ahora como crear nuestras propias funciones.

{% hint style="info" %}
El tema de funciones en un principio puede presentar dificultades para entenderlo 😵 y ver sus ventajas ante la metodología de programación lineal que veníamos trabajando en conceptos anteriores.
{% endhint %}

Los primeros problemas que presentaremos nos puede parecer que sea más conveniente utilizar programación lineal en vez de programación estructurada por funciones.

A medida que avancemos veremos que si un programa empieza a ser más complejo \(cientos de líneas, miles de líneas o más\) la división en pequeñas funciones nos permitirá tener un programa más ordenado y fácil  de entender 👨🏾🏫 y por lo tanto en mantener.

### Ejemplos

#### Ejemplo 1

Confeccionar una aplicación que muestre una presentación en pantalla 🖥 del programa. Solicite la carga de dos valores y nos muestre la suma. Mostrar finalmente un mensaje de despedida del programa. Implementar estas actividades en tres funciones.

```python
# program

# function: presentation of program
def presentation():
    print("Welcome, this program that allows prompt two values by keyBoard")    
    print("it shows the result of sum")
    print("*****************************")

# function: loading data and sum
def loading_operation():
    val1=int(input("Ente value1: "))
    val2=int(input("Ente value2: "))
    suma=val1+val2
    print("Sum: ",suma)

# goodbye
def goodbye():
    print("thank you for uses this program")
    print("*******************************")
    print("goodbye")

# main program
presentation()
loading_operation()
goodbye() 
```

La forma de organizar nuestro programa cambia en forma radical. El programa ahora no empieza a ejecutarse en la línea 1.

El programa principal comienza a ejecutarse luego del comentario "main program" \(programa principal\).

> ```python
> # main program
> presentation()
> loading_operation()
> goodbye() 
> ```

Primero declaramos las tres funciones llamadas _presentation_, _loading\_operation_ y _goodbye_.

La sintaxis para declarar una función es mediante la palabra clave **def** seguida por el nombre de la función.

{% hint style="danger" %}
El nombre de la función _no puede_ tener espacios en blanco, comenzar con un número y el único caracter especial permitido es el "\_"
{% endhint %}

Luego del nombre de la función deben ir entre _paréntesis_ los datos que llegan o de entrada \(parametros\), si no llegan datos como es el caso de nuestras tres funciones solo se disponen paréntesis abierto y cerrado. Al final disponemos los "**:"** \(dos puntos\).

{% hint style="warning" %}
Todo el bloque de la función se indenta cuatro espacios como venimos trabajando cuando definimos estructuras condicionales o repetitivas.
{% endhint %}

Dentro de una función implementamos el algoritmo que pretendemos que resuelva esa función, por ejemplo la función _presentatation\(\)_ tiene por objetivo mostrar en pantalla el objetivo del programa:

> ```python
> def presentation():
>     print("Welcome, this program that allows prompt two values by keyBoard")    
>     print("it shows the result of sum")
>     print("*****************************")
> ```

La función _loading\_operation\(\)_ permite ingresar dos enteros por teclado, sumarlos y mostrarlos en pantalla:

> ```python
> def loading_operation():
>     val1=int(input("Ente value1: "))
>     val2=int(input("Ente value2: "))
>     suma=val1+val2
>     print("Sum: ",suma)
> ```

La función _goodbye\(\)_ tiene por objetivo mostrar un mensaje que muestre al operador que el programa finalizó:

> ```python
> def goodbye():
>     print("thank you for uses this program")
>     print("*******************************")
>     print("goodbye")
> ```

Luego de definir las funciones tenemos al final de nuestro archivo \*.py las llamadas de las funciones:

> ```python
> presentation()
> loading_operation()
> goodbye() 
> ```

Si no hacemos las llamadas a las funciones los algoritmos que implementan las funciones nunca se ejecutarán.

Cuando en el bloque del programa principal se llama una función hasta que no finalice no continua con la llamada a la siguiente función \( se ejecutan todas las lineas de la función\).

![C&#xF3;digo ejemplo 1](.gitbook/assets/image%20%2838%29.png)

![Salida ejecuci&#xF3;n ejemplo 1](.gitbook/assets/image%20%2839%29.png)

{% hint style="info" %}
El orden en que llamamos a las funciones es muy importante. 
{% endhint %}

Supongamos que nuestro bloque del programa principal llamamos las funciones en este orden:

> ```python
> goodbye()
> loading_operation()
> presentation()
> ```

Veremos que primero muestra el mensaje de finalización, luego la carga y suma de datos y finalmente aparece por pantalla los mensajes de presentación de nuestro programa.

#### Ejemplo 2

Confeccionar una aplicación 🤖 que solicite la carga de dos valores enteros y muestre su suma. Repetir la carga e impresion de la suma 5 veces. Mostrar una línea separadora después de cada vez que cargamos dos valores y su suma.

```python
#function for loading values
#keyBoard inpt
def input_values():    
    val1=int(input("Ente value1: "))
    val2=int(input("enter value2:"))
    suma=val1+val2
    print("sum: ",suma)

# separator
def separator():
    print("**********************")
# main
for f in range(5):
    input_values()
    separator()
```

Luego de ejectuar el programa anterior tenemos:

![Salida ejecuci&#xF3;n ejemplo 2](.gitbook/assets/image%20%2841%29.png)

Hemos declarado dos funciones, una que permite cargar dos enteros sumarlos y mostrar el resultado:

> ```python
> def input_values():    
>     val1=int(input("Ente value1: "))
>     val2=int(input("enter value2:"))
>     suma=val1+val2
>     print("sum: ",suma)
> ```

Y otra función que tiene por objetivo mostrar una línea separadora con asteriscos:

> ```python
> def separator():
>     print("**********************")
> ```

Ahora nuestro bloque principal del programa, recordemos 👨🏾🏫 que estas líneas son las primeras que se ejecutarán cuando iniciemos el programa:

> ```python
> # main
> for f in range(5):
>     input_values()
>     separator()
> ```

Como vemos podemos llamar a la función input\_values\(\) y separator\(\) muchas veces en nuestro caso en particular 5 veces.

Lo nuevo que debe quedar claro es que la llamada a las funciones desde el bloque principal de nuestro programa puede hacerse múltiples veces \(esto es lógico, 🤓 recordemos que print es una función ya creada en Python y la llamamos múltiples veces dentro de nuestro algoritmo\).

### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. 
{% endhint %}

#### Problema 1

Desarrollar un programa con dos funciones. La primer solicite el ingreso de un entero y muestre el cuadrado de dicho valor. La segunda que solicite la carga de dos valores y muestre el producto de los mismos. LLamar ☎ desde el bloque del programa principal a ambas funciones.

#### Problema 2

Desarrollar un programa que solicite la carga de tres valores y muestre el menor. Desde el bloque principal del programa llamar 2 veces a dicha función \(sin utilizar una estructura repetitiva\)



#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
# squaring a number
def squaring():
    val1=int(input("Enter a number: "))
    val1=val1**2
    print("squaring: ",val1)
    print("**************************")

# multiplication two numbers
def multiplication():
    val1=int(input("Enter a number1: "))
    val2=int(input("Enter a number: "))
    m=val1*val2
    print("multiplication: ",m)

#main 
squaring()
multiplication()
```
{% endtab %}

{% tab title="Problem 2" %}
```python
# lower number
def lower_number():
    v1=int(input("Enter a number1: "))
    v2=int(input("Enter a number2: "))
    v3=int(input("Enter a number3: "))
    #lower
    if(v1<=v2 and v1<=v3):
        m=v1
    elif(v2<v1 and v2<v3):
        m=v2
    else:
        m=v3
    print("minor: ",m)
    print("***********************************")
    
#main
lower_number()
lower_number()
```
{% endtab %}
{% endtabs %}

