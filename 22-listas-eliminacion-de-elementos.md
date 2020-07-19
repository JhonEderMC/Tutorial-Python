---
description: Eliminación de elementos de una lista.
---

# 22 - Listas: eliminación de elementos

Hemos visto que una lista la podemos iniciar por asignación indicando sus elementos.

`lista=[100, 200, 300, 400]`

También podemos agregarle elementos al final mediante el método append:

`lista.append(120)`

Si ahora imprimimos la lista tenemos como resultado:

`lista=[100, 200, 300, 400, 120]`

{% hint style="info" %}
Otra característica fundamental de las listas en Python es que podemos eliminar cualquiera de sus componentes llamando al método _**pop**_ e indicando la posición del elemento a borrar.
{% endhint %}

`lista.pop(0)`

Ahora si imprimimos la lista luego de eliminar el primer elemento el resultado es:

`lista=[200, 300, 400, 120]`

Otra cosa que hay que hacer notar ``⚠ que cuando un elemento de la lista se elimina no queda una posición vacía, sino se desplazan todos los elementos de la derecha una posición.

{% hint style="info" %}
El método pop retorna el valor almacenado en la lista en la posición indicada, aparte de borrarlo.
{% endhint %}

`lista=[200, 300, 400, 120]` 

`print(lista.pop(0)) # imprime un 200`

### Ejemplos

#### Ejemplo 1

Crear una lista 📋 por asignación con 5 enteros. Eliminar el primero, el tercero y el último de la lista.

```python
list1=[10, 20, 30, 40, 50]
# print list
print(list1)
#delete first
list1.pop(0)
print(list1)
# delete third
list1.pop(1)
print(list1)
# deleted last
list1.pop(2)
print(list1)
```

Parecería que con esas tres llamadas al método pop se eliminan los tres primeros elementos pero no es así, 🤔 si imprimimos cada vez que borramos uno veremos que estamos borrando el primero, tercero y quinto.

> ```python
> list1=[10, 20, 30, 40, 50]
> print(list1)
> # se imprime [10, 20, 30, 40, 50]
> list1.pop(0)
> print(list1)
> # se imprime [20, 30, 40, 50]
> list1.pop(1)
> print(list1)
> # se imprime [20, 40, 50]
> list1.pop(2)
> print(list1)
> # se imprime [20, 40]
> ```

#### Ejemplo 2

Crear una lista y almacenar 10 enteros pedidos por teclado. Eliminar todos los elementos que sean iguales al número entero 5.

```python
#list
list1=[]
# enter data
for f in range(10):
    list1.append(int(input(f"Enter a number{f+1}: ")))
#print list
print("List: ",list1)
# deleted number 5
#counter number o deleted (left Shift)
i=0
for f in range(len(list1)-i):
    #if it's number five
    #left shift, 
    x=f-i
    if(list1[x]==5):
        #deleted
        list1.pop(x)
        i+=1
#print list
print("List: ",list1)
```

![Salida ejecuci&#xF3;n ejemplo 1](.gitbook/assets/image%20%2837%29.png)

Mediante un for cargamos 10 elementos en la lista:

> ```python
> list1=[]
> for f in range(10):
>     list1.append(int(input(f"Enter a number{f+1}: ")))
> ```

Para eliminar los elementos de la lista utilizamos un _for,_ donde _"i "_ es un contador de la cantidad de 5 eliminados:

> ```python
> i=0
> for f in range(len(list1)-i):
> ```

Se resta la cantidad de elementos eliminados __❌ al tamaño de lista, debido a que cada vez que se elimina un elemento esta se desplaza una posición a la izquierda.

_"x"_ es la nueva posición del elemento desplazado en la lista.

> ```python
> x=f-i
> ```

Se utiliza un condicional para verificar si el número es igual a cinco, si es verdadero eliminar dicho número de la lista, luego se aumenta el contador:

> ```python
> if(list1[x]==5):
>     list1.pop(x)
>     i+=1
> ```

Resolviendo el mismo problema pero ahora utilizando en vez de _for_ un _while:_

```python
# list
list1=[]
# enter data
for f in range(10):
    list1.append(int(input(f"Enter a number{f+1}: ")))
#print list
print("List: ",list1)
# counter deleted
i=0
while i<len(list1):
    if(list1[i]==5):
        list1.pop(i)
    else:
        i+=1
print("List: ",list1)
```

Llevamos un contador llamado "_i_" que nos indica que elemento de la lista estamos verificando en el _if_, en el caso que se debe borrar llamamos al método _pop_ pasando el contador y no incrementamos en uno el contador "_i_" ya que los elementos de la derecha se desplazan una posición a izquierda. En el caso que no se debe borrar se incrementa en uno el contador "i" para analizar el siguiente elemento de la lista en la próxima vuelta del ciclo.

### Nota: otra forma de eliminar elementos de una lista

Para eliminar elementos de una lista también es empleada la función "**del**" pasando como parámetro la referencia de la componente a eliminar:

```python
lista=[10, 20, 30, 40, 50]
print(lista)
del(lista[0])
del(lista[1])
del(lista[2])
print(lista) # 20 40
```

### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. 
{% endhint %}

#### Problema 1

Crear dos listas paralelas. En la primera ingresar los nombres de empleados 👩🏽🏭 y en la segunda los sueldos de cada empleado. Ingresar por teclado cuando inicia el programa la cantidad de empleados de la empresa. Borrar luego todos los empleados que tienen un sueldo mayor a 10000 🤑 \(tanto el sueldo como su nombre\).

#### Problema 2

Crear una lista de 5 enteros y cargarlos por teclado. Borrar los elementos mayores o iguales a 10 y generar una nueva lista con dichos valores.

#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
## list 
# employees name
listName=[]
# employees Salary
listSalary=[]
# the number of employee
n=int(input("The number of employee: "))
# enter employee data
for f in range(n):
    # add empy
    listName.append([])
    # add employee name
    listName[f].append(input(f"Enter the employee name{f+1}: "))
    # add empty
    listSalary.append([])
    # add employee salary
    listSalary[f].append(int(input(f"Enter {listName[f][0]}'s salary: ")))
    
# print data
print ("Employees data:  ")
for f in range (len(listName)):
    print(f"Name: {listName[f][0]} -- Salary: ${listSalary[f][0]}")

# deleted employees whose salary is greater than 1000i
# counter
i=0
while i<len(listSalary):
    # compare if employee is greater than 1000
    if (listSalary[i][0]>1000):
        # elimined this employee
        listName.pop(i)
        listSalary.pop(i)
        # the list is moved to the left one position(length (list)-1)
    else:
        #increase counter
        i+=1
# print data        
print ("Employees data:  ")
for f in range (len(listName)):
    print(f"Name: {listName[f][0]} -- Salary: ${listSalary[f][0]}")
```
{% endtab %}

{% tab title="Poblem 2" %}
```python
# list numbers
listNumb=[]
# list of numbers deleted
listNumbDeleted=[]
# enter numbers
for f in range(5):
    listNumb.append(int(input(f"Enter a number{f+1}: ")))

# new list
#listNumbDeleted=listNumb
listNumbDeleted=listNumb.copy()
# deleted numbers are greater than 10
#counter 
i=0
while i<len(listNumbDeleted):
    # this number is greater
    if(listNumbDeleted[i]>10):
        # deleted number
        listNumbDeleted.pop(i)
        # the list is moved to the left one position
    #counter   
    else:
        i+=1
print("List:",listNumb)
print("list deleted:", listNumbDeleted)
```
{% endtab %}
{% endtabs %}

