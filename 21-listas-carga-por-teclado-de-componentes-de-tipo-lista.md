# 21 - Listas: carga por teclado de componentes de tipo lista

En el concepto anterior vimos que fácilmente podemos definir por asignación una lista cuyas componentes sean también listas:

> lista=\[\[1,2,3\] , \[4,5\], \[5,7\]\]

En muchas situaciones debemos crear una nueva 🆕 lista ingresando los datos por teclado o por operaciones del mismo programa.

### Ejemplos

#### Ejemplo 1

Crear y cargar una lista con los nombres de tres alumnos. ✍🏾 Cada alumno tiene dos notas, almacenar las notas en una lista paralela. Cada componente de la lista paralela debe ser también una lista con las dos notas. Imprimir luego cada nombre y sus dos notas.

Si cargáramos los datos por asignación sería algo parecido a esto:

> estudiantes=\["Arbey", "Ana", "Luisa"\]
>
> notas=\[\[3,4\], \[2,4\],\[3,5\] \]

En la componente 0 de la lista estudiantes tenemos almacenado 🗳 el nombre "Arbey" y como son listas paralelas en la componente 0 de la lista notas tenemos almacenado una lista con las dos notas 3 y 4.

Nuestro objetivo como lo pide el problema es cargar los datos por teclado.

```python
# list
listName=[]
listNote=[]
# enter data
for f in range(3):
    listName.append(input(f"Enter stundent's name{f+1}: "))
    note1=float(input(f"Enter {listName[f]} note1: "))
    note2=float(input(f"Enter {listName[f]} note2: "))
    listNote.append([note1,note2])
# print data
for f in range(3):
    print(f"{listName[f]}: {listNote[f]}")
```

![Salida ejecuci&#xF3;n ejemplo 1](.gitbook/assets/image%20%2835%29.png)

La creación de las dos listas no difiere una de otra:

> `listName=[]`
>
> `listNote=[]`

En la estructura repetitiva for procedemos a cargar un nombre y agregarlo a la lista en forma similar como lo hemos hecho en conceptos anteriores:

> `for f in range(3):` 
>
>       `listName.append(input(f"Enter stundent's name{f+1}: "))`

Lo nuevo 🥳 se presenta cuando queremos añadir elementos a la lista notas, lo hacemos con el mismo método **append** pero le pasamos como parámetro una lista con dos elementos:

> `note1=float(input(f"Enter {listName[f]} note1: ")) note2=float(input(f"Enter {listName[f]} note2: "))`

#### Ejemplo 2

Se tiene que cargar la siguiente información: · Nombres de 3 empleados. 👳🏽♂ Ingresos en concepto de sueldo, 🤑 cobrado por cada empleado, en los últimos 3 meses. Confeccionar el programa para:

* Realizar la carga de los nombres de empleados y los tres sueldos por cada empleado.
* Generar una lista que contenga el ingreso acumulado en sueldos en los últimos 3 meses para cada empleado.
* Mostrar por pantalla 🖥 el total pagado en sueldos a cada empleado en los últimos 3 meses.
* Obtener el nombre del empleado que tuvo el mayor ingreso 💰 acumulado.

En este problema definiremos tres listas:

1. Una lista para almacenar los nombres de los empleados: `nombres = ["juan", "estiven", "sara"]`
2. Una lista paralela a la anterior para almacenar los sueldos en los últimos tres meses por cada empleado: `sueldos =[[300,400,500], [600,600,700], [200,400,800]]`
3. Otra lista paralela donde almacenamos el total de sueldos cobrados por cada empleado que resulta de sumar los tres sueldos de cada empleado contenidos en la lista sueldos: `totalsueldos=[[1200],[1900],[1400] ]`

Es importante ⚠ notar que estos datos no los cargaremos por asignación sino los cargaremos por teclado a las dos primeras listas y la tercera la generaremos extrayendo los datos de la lista sueldos.

```python
# employee list
listName=[]
listSalary=[]
listTotalSalary=[]
# enter data
for f in range(3):
    # enter employee name
    listName.append(input(f"Enter the employe name{f+1}: "))    
    #enter employee salary
    sal1=int(input(f"Enter {listName[f]} salary{f+1}: "))
    sal2=int(input(f"Enter {listName[f]} salary{f+1}: "))
    sal3=int(input(f"Enter {listName[f]} salary{f+1}: "))
    # save salary
    listSalary.append([sal1,sal2,sal3])

# total salary the last three month
(print("total salary the last three month: "))
for f in range(len(listSalary)):
    sume=0    
    for k in range(len(listSalary[f])):
        sume+=listSalary[f][k]
    listTotalSalary.append(sume)
    
# print and greater salary
great=0
position=0
for f in range(len(listName)):
    print(f"{listName[f]}: {listTotalSalary[f]}")
    if(listTotalSalary[f]>great):
        great=listTotalSalary[f]
        position=f
print("The employe with greater salary is: ",listName[position])
```

Definimos 3 listas:

> `listName=[]`
>
> `listSalary=[]`
>
> `listTotalSalary=[]`

En el primer _for_ realizamos la carga de cada nombre de empleado y sus tres últimos sueldos, en la lista nombres añadimos _strings_ y en la lista sueldos añadimos otra lista con tres enteros que representan los sueldos:

> ```python
> for f in range(3):
>     listName.append(input(f"Enter the employe name{f+1}: "))    
>     sal1=int(input(f"Enter {listName[f]} salary{f+1}: "))
>     sal2=int(input(f"Enter {listName[f]} salary{f+1}: "))
>     sal3=int(input(f"Enter {listName[f]} salary{f+1}: "))
>     listSalary.append([sal1,sal2,sal3])    
> ```

En el segundo ciclo repetitivo generamos automáticamente la lista de total sueldos \(es decir no cargamos por teclado\), este valor resulta de sumar los tres sueldos de cada empleado que se encuentran en cada una de las listas contenidas en la lista sueldos:

> > ```python
> > for f in range(len(listSalary)):
> >     sume=0    
> >     for k in range(len(listSalary[f])):
> >         sume+=listSalary[f][k]
> >     listTotalSalary.append(sume) 
> > ```

Imprimimos 🖨 ahora el nombre del empleado seguido por el ingreso total en sueldos de los últimos tres meses:

> ```python
> for f in range(len(listName)):
>     print(f"{listName[f]}: {listTotalSalary[f]}")
> ```

Finalmente el problema requiere mostrar el nombre del empleado que recaudó más en sueldos en los últimos tres meses. Iniciamos dos variables previas al _for_ indicando en una la posición de importe en sueldos mayor y en otra dicho importe. Hacemos la suposición antes de ingresar al _for_ que el mayor está en la posición 0:

> ```python
> if(listTotalSalary[f]>great):
>         great=listTotalSalary[f]
>         position=f
> print("The employe with greater salary is: ",listName[position])
> ```

#### Ejemplo 3



