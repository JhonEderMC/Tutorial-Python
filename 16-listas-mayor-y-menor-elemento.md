---
description: >-
  Es una actividad muy común la búsqueda  del mayor y menor elemento de una
  lista.
---

# 16 - Listas: mayor y menor elemento

Es una actividad muy común la búsqueda 🔍 del mayor y menor elemento de una lista. **Es necesario que la lista tenga valores del mismo tipo** por ejemplo enteros. Pueden ser de tipo cadenas de caracteres y se busque cual es mayor o menor alfabéticamente, pero **no podemos buscar el mayor o menor si la lista tiene enteros y cadenas de caracteres al mismo tiempo**.

### Ejemplos 

#### Ejemplo 1

Crear y cargar una lista con 5 enteros. Implementar un algoritmo 📝 que identifique el mayor valor de la lista.

```python
# list of numbers
#empty list
listNumbers=[]
# enter list
for numb in range(5):
    listNumbers.append(int(input("Enter a number: ")))
print("list: ",listNumbers)
# great Number
# number auxiliar (it's take as greater)
greatNumb=listNumbers[0]
for f in range(1,len(listNumbers)):
    # if it is greater
    if(listNumbers[f]>greatNumb):
        greatNumb=listNumbers[f]
print("The greater number: ",greatNumb)      

```

Primero procedemos a cargar por teclado los 5 valores en la lista:

> for numb in range\(5\):
>
>     listNumbers.append\(int\(input\("Enter a number: "\)\)\)
>
> print\("list: ",listNumbers\)

Para identificar el mayor de una lista primero tomamos como referencia el primer elemento 🧮 , considerando a este en principio como el mayor de la lista:

> greatNumb= listNumbers\[0\]

Seguidamente disponemos un _for_ que se repita 4 veces esto debido a que no debemos controlar el primer elemento de la lista \(recordar que la primer vuelta del for x toma el valor 1, luego el 2 y así sucesivamente hasta el 4\):

> for f in range\(1,len\(listNumbers\)\):

Dentro del for mediante una estructura condicional verificamos si el elemento de la posición `f` de la lista es mayor al que hemos considerado hasta este momento como mayor:

> if\(listNumbers\[f\]&gt;greatNumb\): 
>
>             greatNumb=listNumbers\[f\]

Como vemos en las dos líneas anteriores 🔙 si el if se verifica verdadero ✅ actualizamos la variable mayor con el elemento de la lista que estamos analizando.Cuando finaliza el for procedemos a mostrar el contenido de la variable "greatNumb" que tiene almacenado el mayor elemento de la lista.

> print\("The greater number: ",greatNumb\)

#### Ejemplo 2

Crear y cargar una lista con 5 enteros 🔢 por teclado. Implementar un algoritmo que identifique el menor valor de la lista y la posición donde se encuentra.

```python
# list of numbers
#empty list
listNumbers=[]
# enter list
for numb in range(5):
    listNumbers.append(int(input("Enter a number: ")))
print("list: ",listNumbers)
# min Number
# number auxiliar (it's take as greater)
minNumb=listNumbers[0]
position=0
for f in range(1,len(listNumbers)):
    # if it is greater
    if(listNumbers[f]<minNumb):
        minNumb=listNumbers[f]
        position=f
print("The minor number: ",minNumb, "in the position: ",position)      
```

Iniciamos una lista vacía y cargamos 5 elementos enteros:

> ```python
> listNumbers=[]
> for numb in range(5):
>     listNumbers.append(int(input("Enter a number: ")))
> print("list: ",listNumbers)
> ```

Para identificar 🔍 el menor y la posición de dicho valor en la lista definimos dos variables. La primera le cargamos el primer elemento de la lista, que es el que consideramos como menor hasta este momento, por otro en la segunda variable almacena un cero que es la posición donde se encuentra el menor hasta este momento:

> minNumb=listNumbers\[0\]
>
>  position=0

Seguidamente ⏭ disponemos un for que se repita el tamaño de la lista menos 1 \(len -1\) veces \(que son la cantidad de elementos que nos faltan analizar de la lista\):

> for f in range\(1,len\(listNumbers\)\):

Dentro del for mediante un _if_ verificamos si el elemento que estamos analizando de la lista es menor a la variable "minNumb":

> if\(listNumbers\[f\]&lt;minNumb\):

En caso que sea un número menor al que hemos considerado como "menor" hasta este momento procedemos a actualizar la variable "minNumb" con el nuevo valor y también actualizamos la variable "position" con el valor del contador del _for_ que nos indica que posición de la lista estamos analizando.

> minNumb=listNumbers\[f\] 
>
> position=f

  
Por ultimo solo faltaría mostrar la lista y el menor número.

> print\("The minor number: ",minNumb, "in the position: ",position\)

### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. El tiempo a dedicar a esta **sección ejercicios propuestos** 👩🏾💻 debe ser mucho mayor que el empleado a la sección de **ejercicios resueltos**.  
 La _experiencia_ dice que debemos dedicar el 80% del tiempo 🕖 a la resolución _individual_ de problemas y el otro 20% al análisis y codificación de problemas ya resueltos 🗃 por otras personas.
{% endhint %}

#### Problema 1

Ingresar por teclado los nombres de 5 personas y almacenarlos en una lista. Mostrar el nombre de persona menor en orden alfabético.

#### Problema 2

Cargar una lista con 5 elementos enteros. Imprimir el mayor y un mensaje si se repite dentro de la lista \(es decir si dicho valor se encuentra en 2 o más posiciones en la lista\).

#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
# list names
listNames=[]
# enter list
i=0
while i<5:
    listNames.append(input("Enter a name:"))
    i+=1
print("List: ",listNames)
# it is take as minor
minorName=listNames[0]
i=1
while i<5:
    if(listNames[i]<minorName):
        minorName=listNames[i]
    i+=1
print("The minor alphabetic name is: ",minorName)

```
{% endtab %}

{% tab title="Problem 2" %}
```python
# list of numbers
#empty list
listNumbers=[]
# enter list
for numb in range(5):
    listNumbers.append(int(input("Enter a number: ")))
print("list: ",listNumbers)
# great Number
# number auxiliar (it's take as greater)
greatNumb=listNumbers[0]
for f in range(1,len(listNumbers)):
    # if it is greater
    if(listNumbers[f]>greatNumb):
        greatNumb=listNumbers[f]
# count repeat        
countRepeat=0
for numb in listNumbers:
    if(numb==greatNumb):
        countRepeat+=1
# repeat
if(countRepeat>1):
    print("it's repeat")
else:
    print("it is not repeat")
```
{% endtab %}

{% tab title="Free Bonus" %}
```python
'''Esto se me ocurrio en el momento de hacer este modulo y podría ser
un poco mas complicado. Consiste en ordenear una lista de menor a mayor
y reorganizandola en dicho orden'''
# list of numbers
#empty list
listNumbers=[]
# enter list
for numb in range(5):
    listNumbers.append(int(input("Enter a number: ")))
print("List: ",listNumbers)
# list ordering
# number auxiliar
# auxNumb=listNumbers[0]
for i in range (len(listNumbers)-1):
    for f in range(len(listNumbers)-i-1):
        # if it is not ordered
        if(listNumbers[f]>listNumbers[f+1]):
            auxNumb=listNumbers[f]
            listNumbers[f]=listNumbers[f+1]
            listNumbers[f+1]=auxNumb
print("List Ordered: ",listNumbers) 


```
{% endtab %}
{% endtabs %}









