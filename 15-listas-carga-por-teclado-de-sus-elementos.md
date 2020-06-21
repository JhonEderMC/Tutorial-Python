---
description: Cargaremos los elementos de una lista mediante una entrada por teclado.
---

# 15 - Listas: carga por teclado de sus elementos

{% hint style="info" %}
Una lista 📋 en Python es una estructura mutable \(es decir puede ir cambiando durante la ejecución del programa\).
{% endhint %}

  
Hemos visto que podemos definir una lista por asignación indicando entre corchetes los valores a almacenar:

> lista=\[10, 15, 20\]

Una lista luego de definida podemos agregarle 🛒 nuevos elementos. La primera forma que veremos para que nuestra lista crezca es utilizar el método **append** que tiene la lista y pasar como parámetro el nuevo elemento:

> lista=\[5,10,15\]  \# se define una lista de 3 elementos
>
> print\(len\(lista\)\) \# imprime el número 3
>
> lista.append\(20\) \# agrega el 20 al final de la lista
>
> print\(len\(lista\)\) \# imprime el número 4
>
> print\(lista\[0\]\) \# imprime el número 5
>
> print\(lista\[3\]\) \# imprime el número 20

Agregamos una nuevo elemento al final de la lista llamando al método append:

`lista.append(20)`

### Ejemplos 

#### Ejemplo 1

Definir una lista vacía y luego solicitar la carga de 5 enteros por teclado y añadirlos a la lista. Imprimir la lista generada.

```python
#list empty
list1=[]
i=0
#enter five elements
while i<5:
    list1.append(int(input("Enter a number: ")))
    # increase counter
    i+=1
# print list
print("List is: ",list1)

```

El algoritmo propuesto crea primero una lista vacía \(debemos asignar los corchetes de apertura y cerrado sin contenido\):

> list1=\[\]

Luego mediante un while \(podemos utilizar un for si queremos 🤠 \) solicitamos en forma sucesiva la carga de un entero por teclado y procedemos a agregarlo al final de la lista llamando al método append:

> while i&lt;5:
>
>       list1.append\(int\(input\("Enter a number: "\)\)\)
>
>       \# increase counter
>
>        i+=1

#### Ejemplo 2

Realizar la carga de valores enteros por teclado, almacenarlos en una lista. Finalizar la carga 🛑 de enteros al ingresar el cero. Mostrar finalmente el tamaño de la lista.

```python
# list empty
list1=[]
# Stop with zero
stop=False
while stop!=True:
    #input number
    number=int(input("Enter a number: "))    
    if(number!=0):
        #add list end list1
        list1.append(number)
    else: #stop
        stop=True
print("List: ",list1)
print("Length:",len(list1))
```

En este problema 🦠 se agregaran valores a la lista hasta que el operador ingrese el valor cero.

Dentro del ciclo while procedemos a agregar al final de la lista el valor ingresado y solicitar la carga del siguiente valor.

{% hint style="info" %}
Cada valor agregado utilizando el método addend\(\) queda al final de la lista. Por lo tanto, el ultimo valor agregado es el ultimo y el anterior a este el penúltimo en la lista.
{% endhint %}

> ```python
> stop = False
> while stop!=True:
> #input number
>     number=int(input("Enter a number: "))    
>     if(number!=0):
>         #add list end list1
>         list1.append(number)
>     else: #stop
>         stop=True
> ```

Cuando salimos del ciclo repetitivo procedemos a imprimir la lista y el tamaño de la misma.

> print\("List: ",list1\)
>
> print\("Length:",len\(list1\)\)

### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas.
{% endhint %}

#### Problema 1

Almacenar en una lista los sueldos \(valores float\) de 5 operarios. Imprimir la lista y el promedio de sueldos.

#### Problema 2

Cargar por teclado y almacenar en una lista las alturas de 5 personas 👨👩👧👦 \(valores float\) Obtener el promedio de las mismas. Contar cuántas personas son más altas que el promedio y cuántas más bajas.

#### Problema 3

Una empresa 🏭 tiene dos turnos \(mañana y tarde\) en los que trabajan 8 empleados \(4 por la mañana y 4 por la tarde\) Confeccionar un programa que permita almacenar los sueldos de los empleados agrupados en dos listas. Imprimir las dos listas de sueldos.

#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
#list salary
salary=[]
# enter salary
suma=0
for sal in range(5):
    salary.append(float(input("Enter a worker salary: $")))
    suma+=salary[sal]
print("Worker salaries: ",salary)
print("Worker average: ",suma/5) 
```
{% endtab %}

{% tab title="Problem 2" %}
```python
# list Heights
listHeight=[]
suma=0
for x in range(5):
    listHeight.append(float(input("Enter a height: ")))
    # acumulate height
    suma+=listHeight[x]
#average 
averageHeight=suma/5
# count greater height
countGeat=0
for x in listHeight:
    # greater average height
    if(x>averageHeight):
        countGeat+=1
print("average height: ",averageHeight)
print("The amount of people greater than average: ",countGeat)
```
{% endtab %}

{% tab title="Problem 3" %}
```python
## list of salaries 
listSalaryMorning=[]
listSalaryAfternoon=[]

# morning
for f in range(4):
    listSalaryMorning.append(float(input(f"Enter worker{f}'s salry in the morning: $")))
# afternoon
for f in range(4):
    listSalaryAfternoon.append(float(input(f"Enter worker{f}'s salry in the afternoon: $")))
# print list
print("Morning: ",listSalaryMorning)
print("Afternoon: ",listSalaryAfternoon)
    
```
{% endtab %}
{% endtabs %}







