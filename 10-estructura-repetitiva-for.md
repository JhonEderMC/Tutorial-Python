# 10 - Estructura repetitiva for

Cualquier problema que requiera una estructura repetitiva se puede resolver empleando la estructura while, pero hay 🃏 otra estructura repetitiva _cuyo planteo es más sencillo en ciertas situaciones_ que tenemos que recorrer una lista de datos. 📋 

En general, la estructura repetitiva for se usa en aquellas situaciones en las cuales queremos que una variable vaya tomando un valor de una lista definida de valores.

Veremos con una serie de ejemplos el empleo del for.

#### Ejemplo 1

Realizar un programa que imprima 🖨 en pantalla los números del 0 al 20.

```python
for x in range (21):
    print(x)
    
```

Tenemos primero la palabra clave **for** y seguidamente el nombre de la variable que almacenará en cada vuelta del **for** el valor entero que retorna la función **range**.  
 La función range retorna la primera vez el valor 0 y se almacena en x, luego el 1 y así sucesivamente hasta que retorna el valor que le pasamos a range menos uno \(es decir en nuestro ejemplo al final retorna un 20\) Tengamos en cuenta que este mismo problema resuelto con la estructura while debería ser:

```python
x = 0
while x<21 :
    print(x)
    x+=1
```

#### Ejemplo 2

Realizar un programa que imprima en pantalla los números del 20 al 30.

```python
for x in range (20,31):
    print (x)
```

{% hint style="info" %}
La función **range** puede tener dos parámetros, el **primero** indica el valor inicial que tomará la variable x, cada vuelta del for la variable x toma el valor siguiente hasta llegar al valor indicado por el **segundo** parámetro de la función range menos uno.
{% endhint %}



