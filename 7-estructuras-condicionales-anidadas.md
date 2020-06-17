# 7 - Estructuras condicionales anidadas

Estamos en presencia de una estructura condicional anidada cuando por la rama del verdadero ↪↩ o el falso de una estructura condicional hay otra estructura condicional.

![Diagrama de flujo estructura condicional anidada](.gitbook/assets/image%20%285%29.png)

El diagrama de flujo que se presenta contiene dos estructuras condicionales. La principal se trata de una estructura condicional compuesta y la segunda es una estructura condicional simple y está contenida por la rama del falso de la primer estructura.  
 Es muy común que se presenten estructuras condicionales anidadas aún más complejas. 😵 

#### Ejemplo 1

Confeccionar un programa que pida por teclado tres notas de un alumno 👨🏾💻 , calcule el promedio e imprima alguno de estos mensajes: Si el promedio es &gt;=3.5 mostrar "Promocionado". Si el promedio es &gt;=2.8 y &lt;3.5 mostrar "Regular". Si el promedio es &lt;2.8 mostrar "Reprobado". 😕 

```python
#Enter stundent's grade
grade1 = float (input("Enter grade1:"))
grade2 = float (input("Enter grade2:"))
grade3 = float (input("Enter grade3:"))
#average grade
average=(grade1+grade2+grade3)/3
#promoted or not
if(average>= 3.5):
    print("The student's promoved ", average)
elif(average >=2.8 and average <3.5):
    print("The student's regular ", average)
elif(average<=2.8):
    print("The sutudent is no promoved ",average)
```

Analicemos el código anterior: 🔎 

* Se ingresan tres valores por teclado que representan las notas 📋 de un alumno, se obtiene el promedio  sumando los tres valores y dividiendo por 3 dicho resultado \(Tener en cuenta que el resultado es un valor real ya que se utiliza el operador **/**\).
* Primeramente preguntamos si el promedio es superior o igual a 2.8, en caso afirmativo ✅ va por la rama del verdadero de la estructura condicional mostramos un mensaje que indica "….promoved" \(con comillas indicamos un texto que debe imprimirse en pantalla\).
* En caso que la condición nos de falso ❌ , por la rama del falso aparece otra estructura condicional, porque todavía debemos averiguar si el promedio del alumno es mayor igual a 2.8 ****y **\(and\)** menor a 3.5.
* Aquí nos hemos adelantado 🏁 un poco y hemos introducido dos operadores **elif** \(si no\), viene despues de un if, verifica una condición si es verdadera la ejecuta. Segundo el operador lógico **and**  \(y\) que agrupa dos condiciones.

{% hint style="info" %}
No olvidar la identación del código.
{% endhint %}



### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. El tiempo a dedicar a esta **sección ejercicios propuestos** 👩🏾💻 debe ser mucho mayor que el empleado a la sección de **ejercicios resueltos**.  
 La _experiencia_ dice que debemos dedicar el 80% del tiempo 🕖 a la resolución _individual_ de problemas y el otro 20% al análisis y codificación de problemas ya resueltos 🗃 por otras personas.
{% endhint %}

#### Problema 1

Se cargan por teclado tres números distintos. Mostrar por pantalla el mayor de ellos.

#### Problema 2

Se ingresa por teclado un valor entero, mostrar una leyenda que indique si el número es positivo, negativo o nulo \(es decir cero\)

#### Problema 3

Confeccionar un programa que permita cargar un número entero positivo de hasta tres cifras y muestre un mensaje indicando si tiene 1, 2, o 3 cifras. Mostrar un mensaje de error si el número de cifras es mayor.

#### Problema 4

Un postulante a un empleo, realiza un test de capacitación, se obtuvo la siguiente información: cantidad total de preguntas que se le realizaron y la cantidad de preguntas que contestó correctamente. Se pide confeccionar un programa que ingrese los dos datos por teclado e informe el nivel del mismo según el porcentaje de respuestas correctas que ha obtenido, y sabiendo que:

* Nivel máximo: Porcentaje  &gt;=90% 
* Nivel medio: Porcentaje &gt;=75% y&lt;90%
* Nivel regular: Porcentaje &gt;=50% y &lt;75%
* Fuera de nivel: Porcentaje &lt;50%

#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻 
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
#numbers
numb1=int (input("Enter a number1: "))
numb2=int (input("Enter a number2: "))
numb3=int (input("Enter a number3: "))
#greater number
if(numb1>=numb2 and numb1>=numb3):
    print("The greater number is: ",numb1)
elif(numb2>numb1 and numb2>numb3):
    print("The greater number is: ",numb2)
elif(numb3>numb1 and numb3>numb1):
    print("The greater number is: ",numb3)
    
```
{% endtab %}

{% tab title="Problem 2" %}
```python
#number
number = int (input("Enter the number: "))
if(number<0): #negative
    print("The number is negative")
elif(number==0): #zero
    print("The number is zero")
else : #positive
    print("The number is positivo")
```
{% endtab %}

{% tab title="Problem 3" %}
```python
#number
number = int (input("Enter the number"))
if(number<0):
    number=number*-1
if(number>=0 and number<10): # 1 digit
    print("The number has one digit")
elif(number>=10 and number<100): #2 digit
    print("The number has two digits")
elif (number>=100 and number<1000) : # 3 digits
    print("The number has three digits")
elif (number>=1000): #error
    print("Error!")
```
{% endtab %}

{% tab title="Problem 4" %}
```python
#number of questions
num_Questions=int(input("Enter the number of question: "))
num_Correct_Answerns=int(input("number of correct answers: "))
#percentage
percentage=float(num_Correct_Answerns*100)/num_Questions
#level
if(percentage>=90):
    print("max level")
elif (percentage>=75 and percentage<90):
    print("mediun level")
elif (percentage>=50 and percentage<75):
    print ("regular level")
elif(percentage<50):
    print("out level")
print(percentage)

```
{% endtab %}
{% endtabs %}

