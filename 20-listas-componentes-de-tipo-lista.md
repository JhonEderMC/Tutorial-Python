---
description: Manejo de componenentes de una lista
---

# 20 - Listas: componentes de tipo lista

Hasta ahora hemos trabajado 😎 con listas cuyos componentes son de tipo:

> Enteros
>
> Flotantes
>
> Cadena de caracteres

Un ejemplo de estos:

> `notas=[7, 3, 4]`
>
> `alturas = [1.23, 1.27, 0.94]`
>
> `dias = ["miercoles", "jueves", "viernes"]`

{% hint style="info" %}
Lo que hace tan **flexible** a esta estructura de datos es que podemos almacenar componentes de tipo **lista.**
{% endhint %}

> nota =\[\[3, 4\], \[2, 5\], \[1, 3\]\]

En la línea anterior 🔙 hemos definido una lista de tres elementos de tipo lista, el primer elemento de la lista es otra lista de dos elementos de tipo entero. De forma similar los otros dos elementos de la lista notas son listas de dos elementos de tipo entero.

### Ejemplos

#### Ejemplo 1

Crear una lista 📋 por asignación. La lista tiene que tener cuatro elementos. Cada elemento debe ser una lista de 3 enteros. Imprimir sus elementos accediendo de diferentes modos.

```python
# list
list1=[[1,2,3],[4,5,6],[7,8,9]]
print("len: ",len(list1))
# print full list
print("\nFull list:")
print(list1)
print("-------------------------------")

# print full sublist
print("\nPrint full sublist: ")
for x in list1:
    print(x)
print("-------------------------------")

# print first element each sublist
print("\nprint first element each sublist: ")
for f in range (len(list1)):
    print(list1[f][0])
print("-------------------------------")  

# print first sublist
print("\nprint first sublist:")
for f in range (len(list1[0])):
    print(list1[0][f])
print("-------------------------------")      

# print the last sublits:
print("\nPrint the last sublist: ")
for f in range (len(list1[2])):
    print(list1[2][f])
print("-------------------------------")      

# print full list
print("\nPrint full list: ")
for f in range (len(list1)):
    for i in range(len(list1[f])):
                print(list1[f][i])
```

![](.gitbook/assets/image%20%2831%29.png)

![Ejecucion ejemplo 1](.gitbook/assets/image%20%2834%29.png)

Al principio puede complicarse 😵 trabajar con listas de listas pero a medida que practiquemos esta estructura de datos veremos que podemos desarrollar algoritmos más complejos.

Para definir y crear por asignación una lista de listas tenemos:

> list1=\[\[1,2,3\],\[4,5,6\],\[7,8,9\]\]

Queda claro 👨🏫 que el primer elemento de lista es:

> \[1,2,3\]

El segundo elemento de la variable lista es \(y así sucesivamente\):

> \[4,5,6\]

La función print si le pasamos como parámetro el nombre de la lista nos muestra la lista completa por pantalla:

> print\(list1\)

Aparece:

> \[\[1,2,3\],\[4,5,6\],\[7,8,9\]\]

Cuando pasamos a la función print el primer elemento de la lista:

> print\(list1\[0\]\)

Nos muestra la lista contenida en la primer componente de la lista principal:

> \[1,2,3\]

Si queremos acceder al primer entero almacenado en la lista contenida en la primer componente de la lista principal:

> print\(list1\[0\]\[0\]\)

Nos muestra:

> 1

Para acceder mediante un for a todos los elementos de la lista contenida en la primer componente de la lista principal debemos codificar:

```python
for f in range (len(list1)):
    print(list1[f][0])
```

Recordemos ◀ que la función len retorna la cantidad de elementos que contiene una lista. En este caso le pasamos como parámetro list1\[0\] que hace referencia a la primer componente de la lista principal.

El resultado de _len_\(list1\[0\]\) es un 3 que es la cantidad de elementos que tiene la lista contenida en la primer componente de la lista principal.

Cada ciclo del for accedemos a: lista\[0\]\[0\] cuando x vale 0, lista\[0\]\[1\] cuando x vale 1 y lista\[0\]\[2\] cuando x vale 2.

Mediante este ciclo podemos acceder a cada elemento y procesarlo.

Por último con el ciclo anidado _f_  podemos acceder a cada elemento de la lista principal y mediante el _for_ interno acceder a cada elemento entero de las listas contenidas en la lista principal:

```python
for f in range (len(list1)):
    for i in range(len(list1[f])):
                print(list1[f][i])
```

#### Ejemplo 2

Crear una lista por asignación. La lista tiene que tener 2 elementos. Cada elemento debe ser una lista de 5 enteros. Calcular 📲 y mostrar la suma de cada lista contenida en la lista principal.

```python
# list
list2=[[1,1,1,1,1], [2,2,2,2,2]]
sum1=list2[0][0]+list2[0][1]+list2[0][2]++list2[0][3]+list2[0][4]
sum2=list2[1][0]+list2[1][1]+list2[1][2]+list2[1][3]+list2[1][4]
print("Sum1: ",sum1)
print("Suma2: ",sum2)
print("--------------------------")

# with for
sum1=0
sum2=0
for f in range(len(list2[0])):
    sum1+=list2[0][f]
    sum2+=list2[1][f]
print("Sum1: ",sum1)
print("Suma2: ",sum2)
print("--------------------------")
sumall=0
for f in range(len(list2)):
    for k in range(len(list2[f])):
                   sumall+=list2[f][k]
print("Sum: ",sumall)
```

Hemos resuelto el problema de tres formas.

La primer forma es acceder a cada elemento en forma secuencial, esto se resuelve de esta forma si tenemos que acceder a un pequeño número de elementos, es decir si la lista es pequeña:

> list2=\[\[1,1,1,1,1\], \[2,2,2,2,2\]\]
>
> sum1=list2\[0\]\[0\]+list2\[0\]\[1\]+list2\[0\]\[2\]++list2\[0\]\[3\]+list2\[0\]\[4\]
>
> sum2=list2\[1\]\[0\]+list2\[1\]\[1\]+list2\[1\]\[2\]+list2\[1\]\[3\]+list2\[1\]\[4\]

La segunda forma es utilizar una estructura repetitiva para sumar todos los elementos de una lista \(el primer subíndice siempre es 0 y el segundo varía con la variable _f_ \):

```python
for f in range(len(list2[0])):
    sum1+=list2[0][f]
    sum2+=list2[1][f]    
```

La última forma planteada es utilizar una estructura repetitiva anidada que suma cada fila, el _for_ externo \(f\) se repite 2 veces que es el tamaño de la variable "list2":

```python
for f in range(len(list2)):
    for k in range(len(list2[f])):
                   sumall+=list2[f][k]
print("Sum: ",sumall)
```

{% hint style="info" %}
Es importante notar que el acumulador suma lo iniciamos en 0 cada vez que comenzamos a sumar una nueva lista.
{% endhint %}

#### Ejemplo 3

Crear una lista por asignación. La lista tiene que tener 5 elementos. Cada elemento debe ser una lista, la primera lista tiene que tener un elemento, la segunda dos elementos, la tercera tres elementos y así sucesivamente. Sumar todos los valores de las listas.

```python
# list
list3=[[1], [1,2], [1,2,3], [1,2,3,4], [1,2,3,4,5]]
# acumulate
suma=0
# external for
for k in range(len(list3)):
    #internal for
    for f in range (len(list3[k])):
        suma+=list3[k][f]
print("Sum: ",suma)
```

Lo primero que es importante notar 🔎 que las listas contenidas en las lista principal no tienen porque ser del mismo tamaño.

La forma más sencilla es utilizar dos ciclos repetitivos. El primero se repite tantas veces como elementos tenga la lista principal:

> for k in range\(len\(list3\)\):

El segundo ciclo nos sirve para recorrer y acceder a cada elemento entero de cada lista:

> for f in range \(len\(list3\[k\]\)\): 
>
>        suma+=list3\[k\]\[f\]

La cantidad de veces que se repite el for interno depende de la cantidad de elementos que tiene la lista que estamos sumando en ese momento.



### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. 
{% endhint %}

#### Problema 1

Se tiene la siguiente lista:

`lista=[[200,7,85,8], [4,8,56,40], [67,90,21,1], [75,57]]`

Imprimir🖨 la lista. Luego fijar con el valor cero todos los elementos mayores a 50 del primer elemento de "lista". Volver a imprimir la lista.

#### Problema 2

Se tiene la siguiente lista:

`lista=[[4,12,5,66], [14,6,25], [3,4,5,67,89,23,1], [78,56]]`

Imprimir la lista. Luego fijar con el valor cero todos los elementos mayores a 10 contenidos en todos los elementos de la variable "lista". Volver a imprimir la lista.

#### Problema 3

Crear una lista por asignación con la cantidad de elementos de tipo lista que usted desee. Luego imprimir el último elemento de la lista principal.

#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
list4=[[4,12,5,66], [14,6,25], [3,4,5,67,89,23,1], [78,56]]
print("List: ",list4)
for k in range(len(list4)):
    for f in range(len(list4[k])):
        if(list4[k][f]>50):
            list4[k][f]=0
print("new list: ",list4)
```
{% endtab %}

{% tab title="Problem 2" %}
```python
list4=[[4,12,5,66], [14,6,25], [3,4,5,67,89,23,1], [78,56]]
print("List: ",list4)
for k in range(len(list4)):
    for f in range(len(list4[k])):
        if(list4[k][f]>10):
            list4[k][f]=0
print("new list: ",list4)
```
{% endtab %}

{% tab title="Problem 3" %}
```python
list4=[[4,12,5,66], [14,6,25], [3,4,5,67,89,23,1], [78,56]]
#The last component
print(len(list4[len(list4)-1])-1)
print("Last: ",list4[len(list4)-1][len(list4[len(list4)-1])-1])
```
{% endtab %}
{% endtabs %}

