---
description: Listas paralelas y su ordenanamiento.
---

# 19 - Listas: ordenamiento con listas paralelas

Cuando se tienen listas paralelas y se ordenan los elementos de una de ellas hay que tener la precaución de intercambiar los elementos de las listas paralelas. ⚠ 

### Ejemplos

#### Ejemplo 1

Confeccionar un programa que permita cargar los nombres de 5 alumnos y sus notas respectivas. Luego ordenar las notas de mayor a menor. Imprimir las notas y los nombres de los alumnos.

Debe quedar claro que cuando intercambiamos las notas para dejarlas ordenadas 📑 de mayor a menor debemos intercambiar los nombres para que las listas continúen paralelas \(es decir que en los mismos subíndices de cada lista continúe la información relacionada\).

```python
# data stundents
listName=[]
listNote=[]
# enter data
for f in range(5):
    listName.append(input(f"Enter student's name{f+1}: "))
    listNote.append(float(input(f"Enter student's note{f+1}: ")))
print("Names: ",listName)    
print("Note: ",listNote)

# ordered greater to minor
for k in range(len(listNote)-1):
    for f in range(len(listNote)-1-k):
        if(listNote[f]<listNote[f+1]):
            auxNote=listNote[f]
            auxName=listName[f]
            listNote[f]=listNote[f+1]
            listName[f]=listName[f+1]
            listNote[f+1]=auxNote
            listName[f+1]=auxName
# print data
print("Names: ",listName)
print("Notes: ",listNote)
```

Definimos y cargamos dos listas con cinco elementos cada una:

> ```python
> listName=[]
> listNote=[]
> for f in range(5):
>     listName.append(input(f"Enter student's name{f+1}: "))
>     listNote.append(float(input(f"Enter student's note{f+1}: ")))
> print("Names: ",listName)    
> print("Note: ",listNote)
> ```

Lo nuevo se presenta cuando ordenamos 🏯 la lista de notas de mayor a menor. La condición dentro de los dos ciclos repetitivos depende de la lista notas, pero en el caso que se verifique verdadera intercambiamos tanto los elementos de la lista notas como el de la lista alumnos con el fin que continúen paralelas:

> ```python
> # ordered greater to minor
> for k in range(len(listNote)-1):
>     for f in range(len(listNote)-1-k):
>         if(listNote[f]<listNote[f+1]):
>             auxNote=listNote[f]
>             auxName=listName[f]
>             listNote[f]=listNote[f+1]
>             listName[f]=listName[f+1]
>             listNote[f+1]=auxNote
>             listName[f+1]=auxName
>                         
> ```

Imprimimos las dos listas:

> print\("Names: ",listName\) print\("Notes: ",listNote\)

![Ejecuci&#xF3;n ejemplo 1](.gitbook/assets/image%20%2829%29.png)

![Salida ejecuci&#xF3;n ejemplo 1](.gitbook/assets/image%20%2830%29.png)

### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. 
{% endhint %}

#### Problema 1

Crear y cargar en un lista los nombres de 5 países 🌎 y en otra lista paralela la cantidad de habitantes del mismo. Ordenar alfabéticamente e imprimir los resultados. Por último ordenar con respecto a la cantidad de habitantes \(de mayor a menor\) e imprimir nuevamente.

#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
# list countriesn and population
listCountry=[]
listPopulation=[]
# enter data
for f in range(5):
    listCountry.append(input(f"Enter country name{f+1}: "))
    listPopulation.append(int(input(f"Enter population of {listCountry[f]}: ")))
# ordered by population
for k in range(len(listCountry)-1):
    for f in range(len(listCountry)-1-k):
        if (listPopulation[f]<listPopulation[f+1]):
            auxPop=listPopulation[f]
            auxCou=listCountry[f]            
            listPopulation[f]=listPopulation[f+1]
            listCountry[f]=listCountry[f+1]
            listPopulation[f+1]=auxPop
            listCountry[f+1]=auxCou
# print list ordered by population
i=0
while i<len(listPopulation):
    print(f"{listCountry[i]}: {listPopulation[i]} ")
    i+=1
```
{% endtab %}
{% endtabs %}

