# 12 - Variables enteras, flotantes y cadenas de caracteres

 Hemos visto como definir variables enteras y flotantes. Realizar su carga por asignación y por teclado.

Para iniciarlas por asignación utilizamos el operador **`=`**

> \#definición de una variable entera
>
> cantidad=20
>
> \#definición de una variable flotante 
>
> altura=1.92

{% hint style="info" %}
El intérprete de Python diferencia una variable flotante de una variable entera por la presencia del carácter punto.
{% endhint %}

Para realizar la carga por teclado ⌨ utilizando la función input debemos llamar a la función _int_ o _float_ para convertir el dato devuelto por input \(retorna un cadena de caracteres o string\):

```python
cantidad=int(input("Ingresar la cantidad de personas:"))
altura=float(input("Ingresar la altura de la persona en metros ej:1.70:"))
```

A estos dos tipos de datos fundamentales \(int y float\) se suma un tipo de dato muy utilizado 🙂 que son las **cadenas de caracteres**.

Una **cadena de caracteres** está compuesta por uno o más caracteres. 🔤 También podemos iniciar una cadena de caracteres por asignación o ingresarla por teclado. Inicialización de una cadena por asignación:

```python
#definición e inicio de una cadena de caracteres
day="Monday"
# o tambien
day = 'Monday' 
```

{% hint style="info" %}
En Python podemos definir una cadena de caracteres tanto en comillas dobles como en comillas simples.
{% endhint %}

Como mencionamos previamente ⏮ , para la carga por teclado de una cadena de caracteres utilizamos la función input que retorna una cadena de caracteres:

```python
name = input ("Enter a name: ")
```

#### Ejemplo 1

Realizar la carga por teclado del nombre, edad y altura de dos personas. Mostrar por pantalla el nombre de la persona con mayor altura.

```python
# people data
name1=input("Enter person's name: ")
#age
age1=int(input("Enter person's age: "))
# heigth
height1=float(input("Enter person's heigth: "))
name2=input("Enter person's name: ")
age2=int(input("Enter person's age: "))
height2=float(input("Enter person's heigth: "))
# greater height
if(height1>height2):
    print("Graeter height is: ",name1)
elif(height2>height1):
    print("Graeter height is: ",name2)
else:
    print("Graeter height is: ",name1," - ",name2)
```

Es importante notar que  el dato devuelto por la función input  es una cadena de caracteres, la cual se lo pasamos a la función _int_ que tiene por objetivo convertirlo a entero. Similarmente para la altura con la fluncion _float_ para convertirlo en un número real.

> age1 = int \(input\("Enter person's age: "\)\)
>
> heigth1= float\(input\("Enter person's heigth: "\)\)

El nombre de la persona 👩🏽✈ es retornado directamente como una cadena de caracteres.

> name1= input\("Enter person's name: "\)

#### Ejemplo 2

Realizar la carga de dos nombres por teclado. Mostrar cual de los dos es mayor alfabéticamente o si son iguales.

```python
# name
name1=input("Enter name1: ")
name2=input("Enter name1: ")
if(name1>name2):
    print(f"The {name1} is alphabetic greater than {name2}")
elif(name2>name1):
    print(f"The {name2} is alphabetic greater than {name1}")
elif(name1==name2):
    print("The names are alphabetic equals")
```

Cuando trabajamos con cadenas de caracteres al utilizar el operador `>` estamos verificando si una cadena es mayor alfabéticamente 🔤 a otra \(esto es distinto a cuando trabajamos con enteros o flotantes\)

Por ejemplo 'luis' es mayor a 'carlos' porque la 'l' se encuentra más adelante en el abecedario que la 'c'.

#### Ejemplo 3

Realizar la carga de enteros por teclado. Preguntar después que ingresa el valor si desea cargar otro valor debiendo el operador ingresar la cadena 'si' o 'no' por teclado. Mostrar la suma de los valores ingresados.

```python
# default
option="yes"
sum=0
while(option!="no"):    
    number=int(input("Enter a number: "))
    sum+=number
    option=input("Do you want to load and other number(yes/no): ")
print(f"\nThe sum was: {sum}")
```

Para resolver este problema hemos inicializado una variable de tipo cadena de caracteres \(también se las llama variables de tipo string\) con el valor "si"\(“yes”\), esto hace que la condición del while se verifique verdadera la primera vez. Dentro del while luego de cargar el valor entero se pide la carga por teclado que confirme si desea cargar otro valor.

El ciclo se corta cuando el operador carga un string distinto a "no".

Es importante notar que el string "yes"  es distinto al string "Yes", es decir las mayúsculas no tienen el mismo valor alfabético que las minúsculas \(después veremos que podemos convertir mayúsculas a minúsculas y viceversa\).

