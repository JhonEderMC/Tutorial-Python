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

### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. El tiempo a dedicar a esta **sección ejercicios propuestos** 👩🏾💻 debe ser mucho mayor que el empleado a la sección de **ejercicios resueltos**.  
 La _experiencia_ dice que debemos dedicar el 80% del tiempo 🕖 a la resolución _individual_ de problemas y el otro 20% al análisis y codificación de problemas ya resueltos 🗃 por otras personas.
{% endhint %}

#### Problema 1

Se ingresan por teclado tres números, si todos los valores ingresados son menores a 10, imprimir 🖥 en pantalla la leyenda "Todos los números son menores a diez".

#### Problema 2

Se ingresan por teclado tres números, si al menos uno de los valores ingresados es menor a 10, imprimir en pantalla la leyenda "Alguno de los números es menor a diez".

#### Problema 3

Escribir un programa que pida ingresar la coordenada de un punto en el plano, es decir dos valores enteros x e y \(distintos a cero\). Posteriormente imprimir en pantalla en que cuadrante se ubica dicho punto. \(1º Cuadrante si x &gt; 0 Y y &gt; 0 , 2º Cuadrante: x &lt; 0 Y y &gt; 0, etc.\)

#### Problema 4

De un operario se conoce su sueldo y los años de antigüedad. Se pide confeccionar un programa que lea los datos de entrada e informe: 

* Si el sueldo es inferior a 500 y su antigüedad es igual o superior a 10 años, otorgarle un aumento del 20 %, mostrar el sueldo a pagar. 
* Si el sueldo es inferior a 500 pero su antigüedad es menor a 10 años, otorgarle un aumento de 5 %. 
* Si el sueldo es mayor o igual a 500 mostrar el sueldo en pantalla sin cambios.

#### Problema 5

Escribir un programa en el cual: dada una lista de tres valores numéricos distintos se calcule e informe su rango de variación \(debe mostrar el mayor y el menor de ellos\)

#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻 
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
#numbers
numb1= int (input("Number1: "))
numb2= int (input("Number2: "))
numb3= int (input("Number3: "))
if(numb1<=10 and numb2<=10 and numb3<=10):
    print ("The numbers are less equals than 10")

```
{% endtab %}

{% tab title="Problem 2" %}
```python
#numbers
numb1= int (input("Number1: "))
numb2= int (input("Number2: "))
numb3= int (input("Number3: "))
if(numb1<=10 or numb2<=10 or numb3<=10):
    print ("The some numbers are less equals than 10")
```
{% endtab %}

{% tab title="Problem 3" %}
```python
# axis
x=int(input("Enter axis X: "))
y=int(input("Enter axis X: "))
#origin
print("the point is: ")
if(x==0 and y==0):
    print("origin")
# Y axis    
elif(x==0):
    if(y>0):
        print("positive Y axis")
    elif(y<0):
        print("negative y axis")
# X axis
elif(y==0):
    if(x>0):
        print("positive X axis")
    elif(x<0):
        print("negative X axis")
# first and four quadrant        
elif(x>0):
    if(y>0):
        print("first quadrant")
    else:
        print("four quadrant")
#second and third
elif(x<0):
    if(y>0):
        print("second quadrant")
    else:
        print("third quadrant")
```
{% endtab %}

{% tab title="Problem 4" %}
```python
#data
antiquity=int (input("Enter worker's antiquity: "))
salary=int(input("Enter worker's salary: $"))
# salary increase
if(salary<500):
    if(antiquity>=10):
        salary=salary+salary*0.2
    else:
        salary=salary+salary*0.05
print("Salary: $",salary)
    
```
{% endtab %}

{% tab title="Problem 5" %}
```python
#numbers
numb1= int (input("Number1: "))
numb2= int (input("Number2: "))
numb3= int (input("Number3: "))
#Greater
if(numb1>=numb2 and numb1>=numb3):
    print ("Greater number: ",numb1)
elif(numb2>numb1 and numb2>numb3):
    print ("Greater number: ",numb2)
elif(numb3>numb1 and numb3>numb2):
    print ("Greater number: ",numb3)
#Minor
if(numb1<=numb2 and numb1<=numb3):
    print ("Minor number: ",numb1)
elif(numb2<numb1 and numb2<numb3):
    print ("Minor number: ",numb2)
elif(numb3<numb1 and numb3<numb2):
    print ("Minor number: ",numb3)
```
{% endtab %}
{% endtabs %}







