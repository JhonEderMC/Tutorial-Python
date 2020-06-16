# 8 - Condiciones compuestas con operadores lógicos

Hasta ahora hemos visto los operadores:

> * Relacionales: \(&gt; , &lt;  , &gt;= , &lt;= , == , !=\)
> * Mátematicos: \(+ , - , \* , / , // , \*\*\)

Pero nos están faltando otros operadores imprescindibles 👁🗨 :

> * Lógicos: \(and y or\)

Estos dos operadores se emplean fundamentalmente en las estructuras condicionales para agrupar varias condiciones simples.

#### Operador and  🇦🇳🇩 

![Diagrama de flujo operador and](.gitbook/assets/image%20%2815%29.png)

{% hint style="info" %}
* En español se traduce como "**y**".
* Si ambas condiciones son verdaderas, se ejecuta la rama de verdadero.
* Si una de las condiciones es falsa, se ejecuta la rama de falso.
{% endhint %}

La utilización de operadores lógicos permiten en muchos casos plantear algoritmos más cortos y comprensibles. 🤓 

#### Ejemplo 1

Confeccionar un programa que lea por teclado tres números enteros distintos y nos muestre el mayor 🖥 .

![](.gitbook/assets/image%20%289%29.png)

Este ejercicio se puede resolver sin operadores lógicos pero el utilizarlos nos permite que sea mas simple la solución. 🤓 

La primera estructura condicional es una _estructura condicional compuesta con una condición compuesta._ Similarmente la segunda pero con _una condición simple_.

Si una de las condiciones simples da falso la condición compuesta da falso y continúa por la rama del falso. Es decir que se mostrará el contenido de num1 si y sólo si num1 &gt; num2 y num1 &gt; num3.  En caso de ser falsa la condición, analizamos el contenido de num2 y num3 para ver cual tiene un valor mayor.  
 En esta segunda estructura condicional no se requieren operadores lógicos al haber una condición simple. 👨🏾💻 

```python
#numbers
numb1= int (input("Number1: "))
numb2= int (input("Number2: "))
numb3= int (input("Number3: "))
#greater number
print ("the greater number is: ")
if(numb1>=numb2 and numb1>=numb3):
    print (numb1)
elif(numb2>numb1 and numb2>numb3):
    print(numb2)
else :
    print(numb3)    
```

### Operador or 🇴 🇷 

![Diagrama de flujo operador or](.gitbook/assets/image%20%288%29.png)



{% hint style="info" %}
* En español se traduce como "**O**".
* Si una de las condiciones es verdaderas, se ejecuta la rama de verdadero.
* Si ambas condiciones son falsas, se ejecuta la rama de falso.
{% endhint %}

#### Ejemplo 2

Se carga una fecha \(día, mes y año\) por teclado. Mostrar un mensaje si corresponde al primer trimestre del año \(enero, febrero o marzo\) Cargar por teclado el valor numérico del día, mes y año. Ejemplo: dia:10 mes:2 año:2020

![Diagrama de flujo ejemplo 2](.gitbook/assets/image%20%284%29.png)

La carga de una fecha se hace por partes, ingresamos las variables dia, mes y año. Mostramos el mensaje "Corresponde al primer trimestre" en caso que el mes ingresado por teclado sea igual a 1, 2 ó 3. En la condición no participan las variables dia y año.

```python
#day
day=int(input("Day: "))
month=int(input("Month: "))
year=int(input("Year: "))
if(month==0 or month==1 or month==2 or month==3):
    print("The first trimester")
```







