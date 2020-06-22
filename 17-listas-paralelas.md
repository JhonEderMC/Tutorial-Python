---
description: >-
  Dos listas son paralelas cuando hay una relación entre las componentes de
  igual subíndice (misma posición) de una lista y otra
---

# 17 - Listas paralelas

Podemos decir que dos listas son paralelas cuando hay una relación entre las componentes de igual subíndice \(misma posición\) de una lista y otra.

| Juan | Daniela | Cristian | Isabel |
| :--- | :--- | :--- | :--- |
| 15 | 21 | 24 | 19 |

 Si tenemos dos listas 📋 que ya hemos inicializado con 4 elementos cada una. En una se almacenan los nombres de personas en la otra las edades de dichas personas. Decimos que la lista nombres es paralela a la lista edades si en la componente 0 de cada lista se almacena 🗄 información relacionada a una persona \(Juan - 15 años\).

Es decir hay una relación entre cada componente de las dos listas.

{% hint style="info" %}
Esta relación la conoce únicamente el programador y se hace para facilitar el desarrollo de algoritmos que procesen los datos almacenados en las estructuras de datos.
{% endhint %}

#### Ejemplo 1

Desarrollar un programa que permita cargar 5 nombres de personas y sus edades respectivas. Luego de realizar la carga por teclado de todos los datos imprimir los nombres de las personas mayores de edad \(mayores o iguales a 18 años\).

```python
# Enter data
listName=[]
listAge=[]
for f in range(5):
    listName.append(input(f"Enter the person name{f+1}: "))
    listAge.append(int(input(f"Enter the person age{f+1}: ")))
print("The people are of age: ")
#persons are of age
for f in range(5):
    if(listAge[f]>=18):
        print(listName[f]) 
```

Definimos dos listas para almacenar los nombres y las edades de las personas respectivamente:

> listName=\[\]
>
> listAge=\[\]

Mediante un for cargamos en forma simultanea un elemento de cada lista, es decir un nombre de persona y la edad de dicha persona.

> for f in range\(5\): 
>
>          listName.append\(input\(f"Enter the person name{f+1}: "\)\)
>
>          listAge.append\(int\(input\(f"Enter the person age{f+1}: "\)\)\)

Para imprimir los nombres de la personas mayores de edad procedemos a analizar dentro de un _for_ y mediante un if cada una de las edades almacenadas en la lista de "edades", en el caso que su valor sea mayor o igual a 18 mostramos el elemento de la lista nombres de la misma posición:

> for f in range\(5\):
>
>     if\(listAge\[f\]&gt;=18\):
>
>         print\(listName\[f\]\)

### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. 
{% endhint %}

#### Problema  1

Crear y cargar dos listas con los nombres de 5 productos en una y sus respectivos precios 💷 en otra. Definir dos listas paralelas. Mostrar cuantos productos tienen un precio mayor al primer producto ingresado.

#### Problema 2

En un curso de 4 alumnos 👨🏾🏫 se registraron las notas de sus exámenes y se deben procesar de acuerdo a lo siguiente:

* Ingresar nombre y nota de cada alumno \(almacenar los datos en dos listas paralelas\).
* Realizar un listado que muestre los nombres, notas y condición del alumno. En la condición, colocar "Muy Bueno" 😊 si la nota es mayor o igual a 4, "Bueno" 🙂 si la nota está entre 3.3 y 4, y colocar "Insuficiente" 😞 si la nota es inferior a 3.3.
* Imprimir cuantos alumnos tienen la leyenda “Muy Bueno”.

#### Problema 3

Realizar un programa que pida la carga de dos listas numéricas enteras de 4 elementos cada una. Generar una tercer lista que surja de la suma de los elementos de la misma posición de cada lista. Mostrar esta tercer lista.

#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
# lists
listProductName=[]
listProductPrice=[]
# enter data
for f in range (5):
    listProductName.append(input(f"Enter the product name{f+1}: "))
    listProductPrice.append(float(input(f"Enter the produce price{f+1}: $")))
print(f"Products with a price ($) greater than {listProductName[0]}: ")
# print greaters
i=1
while i<5:
    if(listProductPrice[i]>listProductPrice[0]):
        print(listProductName[i])
    # increase counter
    i+=1
```
{% endtab %}

{% tab title="Problem 2" %}
```python
# list student data
listName=[]
listNote=[]
listState=[]

#Enter data
for f in range (4):
    listName.append(input(f"Enter stundent's name{f+1}: "))
    listNote.append(float(input(f"Enter stundet's note{f+1}: ")))

#list state
for f in range(4):
    listState.append(listName[f])
    listState.append(listNote[f])
    # very good
    if(listNote[f]>=4):
        listState.append("very good")
    # good
    elif(listNote[f]>=3.3 and listNote[f]<4):
        listState.append("good")
    # insufficient
    elif(listNote[f]<3.3):
        listState.append("insufficient")
print("List State: ",listState)

#print very good
print("Stundents Very good: ")
i=0
while i<4:
    if(listNote[i]>=4):
        print(listName[f])
    #increase counter
    i+=1
```
{% endtab %}

{% tab title="Problem 3" %}
```python
# list numbers 
listNumber1=[]
listNumber2=[]
listNumber3=[]

# enter numbers
print("list number 1:")
for f in range(4):
    listNumber1.append(int(input(f"Enter the number{f+1}: ")))
print("list number 2:")
for f in range(4):
    listNumber2.append(int(input(f"Enter the number{f+1}: ")))

# sum list
i=0
while i<4:
    listNumber3.append(int(listNumber1[i]+listNumber2[i]))
    # increase counter
    i+=1

#print
print("list 1: ",listNumber1)
print("list 2: ",listNumber2)
print("list 3: ",listNumber3)
```
{% endtab %}
{% endtabs %}



