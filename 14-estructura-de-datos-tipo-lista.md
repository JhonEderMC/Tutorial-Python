---
description: >-
  Conoceremos y abordaremos la estructura de datos tipo lista y su carga por
  asignación.
---

# 14 - Estructura de datos tipo lista

Hasta ahora hemos trabajado ✍🏾 con variables que permiten almacenar un único valor:

> age= 17
>
> height= 1.82
>
> name = "Arbey"

En Python existe un tipo de variable que permite almacenar una colección de datos 🗂 y luego acceder por medio de un subíndice \(similar a los string\).

### Creación de la lista por asignación

Para crear 🆕 una lista por asignación debemos indicar sus elementos encerrados entre corchetes y separados por coma:

> lista1=\[10, 5, 3\]                                        \# lista de enteros
>
> lista2=\[1.78, 2.66, 1.55, 89,4\]                \# lista de valores float
>
> lista3=\["lunes", "martes", "miercoles"\] \# lista de string
>
> lista4=\["juan", 45, 1.92\]                          \# lista con elementos de  distinto tipo

Si queremos conocer la cantidad de elementos de una lista podemos llamar a la función len:

> lista1=\[10, 5, 3\]   \# lista de enteros
>
> print\(len\(lista1\)\)  \# imprime un 3

### Ejemplos

#### Ejemplo 1

Definir una lista que almacene 5 enteros. Sumar todos sus elementos y mostrar dicha suma.

```python
# list
list1=[1,2,3,4,5]
# sum
suma=0
print("List: ",list1)
for number in list1:
    suma+=number
print("sum: ",suma)
# with a while
print("With a while: ")
suma=0
i=0
while i<len(list1):
    suma+=list1[i]
    #increase counter
    i+=1
print("sum: ",suma)
```

![Ejecuci&#xF3;n ejemplo 1](.gitbook/assets/image%20%2825%29.png)

Primero definimos una lista por asignación con 5 elementos:

> list1=\[1,2,3,4,5\]

Definimo un acumulador \(suma\) 

> suma=0

En el ciclo _for_  en __ number, se  obtiene cada elemento de la lista para acumularlo en suma.

> for number in list1: 
>
>       suma+=number 
>
> print\("sum: ",suma\)

Mediante un ciclo while es similar a lo anterior, solo diferimos que necesitamos un contador \(i\) para indicar la posición de la lista.

> i=0
>
> while i&lt;len\(list1\):
>
>     suma+=list1\[i\]
>
>     \#increase counter
>
>     i+=1
>
> print\("sum: ",suma\)

#### Ejemplo 2

Definir una lista por asignación que almacene los nombres de los primeros cuatro meses 🗓 de año. Mostrar el primer y último elemento de la lista solamente.

```python
#list
list1=["January","Febrary","March","April"]
print(list1[0])
print(list1[3])
```

Como queremos imprimir solo el primer y último elemento de la lista indicamos entre corchetes la posición de la lista del cual queremos rescatar el valor.

Si llamamos a print y pasamos solo el nombre de la lista luego se nos muestra todos los elementos.

> print\(list1\) \# se muestra \["January", "Febrary","March";April"\]

#### Ejemplo 3

Definir una lista por asignación que almacene en el primer componente el nombre de un alumno y en los dos siguientes sus notas. 📔 Imprimir luego el nombre y el promedio de las dos notas.

```python
# Stundent list
studentList=["Diana", 4.2,3.7]
print(f"{studentList[0]} with average grade: {(studentList[1]+studentList[2])/2}")
```

{% hint style="info" %}
Los elementos de una lista pueden ser de distinto tipo \(int, float, string...\).
{% endhint %}

### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. 
{% endhint %}

#### Problema 1

Definir por asignación una lista con 8 elementos enteros. Contar cuantos de dichos valores almacenan un valor superior a 100.

#### Problema 2

Definir una lista por asignación con 5 enteros. Mostrar por pantalla solo los elementos con valor iguales o superiores a 7.

#### Problema 3

Definir una lista que almacene por asignación los nombres de 5 personas. Contar cuantos de esos nombres tienen 5 o más caracteres.

#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
# list
list1=[1,20,3,40,500,6,700,9,100]
# count greater than 100
countGreat=0
for numb in list1:
    if(numb>100):
        countGreat+=1
print("The amount of numbers greater than 100 are: ",countGreat)  
```
{% endtab %}

{% tab title="Problem 2" %}
```python
# list
list1=[1,4,10,7,9]
for numb in list1:
    if(numb>=7):
        print(numb)
```
{% endtab %}

{% tab title="Problem 3" %}
```python
# list
text=["Jhon","Leidy","Arbey","Camila","Valentina"]
# count number of characters
countCh=0
for name in text:
    if(len(name)>=5):
        countCh+=1
print("The amount: ",countCh)

#With while
countCh=0
i=0
while i<len(text):
    if(len(text[i])>=5):
        countCh+=1
    # increase counter    
    i+=1
print("The amount: ",countCh)
```
{% endtab %}
{% endtabs %}







