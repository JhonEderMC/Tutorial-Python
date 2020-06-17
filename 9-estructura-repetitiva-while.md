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
 También aparece el concepto de **acumulador** \(un acumulador es un tipo especial de variable que se incrementa o disminuye con valores variables durante la ejecución del programa\)



