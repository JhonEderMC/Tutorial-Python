---
description: Algunos métodos y conceptos para el manejo de strings
---

# 13 - Procesar cadenas de caracteres

Ya hemos 🔙 visto que podemos cargar una cadena de caracteres tanto por  asignación \(comillas dobles o simples\), como por teclado. Podemos utilizar los [operadores relacionales](https://jhoneder.gitbook.io/tutorial-python/6-estructuras-condicionales-simples-y-compuestas#operadores-relacionales)🔗 para identificar si dos cadenas son iguales, distintas o cual es la mayor alfabéticamente. 🔡 

Como su nombre lo indica una cadena de caracteres está formada generalmente por varios caracteres \(de todos modos podría tener solo un caracter o ser una cadena vacía\) Podemos acceder en forma individual a cada caracter 🇪 del string mediante un subíndice:

```python
nombre='jhon'
print(nombre[0])   #se imprime una j
if nombre[0]=="j": #verificamos si el primer caracter del string es una j
    print(nombre)
    print("comienza con la letra j")
```

Los subíndices comienzan a numerarse a partir del cero.

{% hint style="info" %}
Si queremos conocer la longitud de un _string_ en Python disponemos de una _función_ llamada **len** que retorna la cantidad de caracteres que contiene.
{% endhint %}

```python
nombre= 'jhon'
print(len(nombre))
```

El programa anterior imprime un 4 ya que la cadena nombre almacena 'jhon' que tiene cuatro caracteres.

### Ejemplos 

#### Ejemplo 1

Realizar la carga del nombre de una persona y luego mostrar el primer caracter del nombre y la cantidad de letras que lo componen.

```python
name=input("Enter a name: ")
print(f"The first character of {name} is: {name[0]}")
print(f"The length of {name} is: {len(name)}")
```

#### Ejemplo 2

Solicitar la carga del nombre de una persona en minúsculas. Mostrar un mensaje si comienza con vocal dicho nombre.

```python
#name
name=input("Enter a name: ")
if(name[0]=="a" or name[0]=="e" or name[0]=="i" or name[0]=="o" or name[0]=="u"):
    print(f"{name} begins with a vowel")
else:
    print(f"{name} does not begin with a vowel")
```

{% hint style="info" %}
 Basta con que una de las condiciones del **if** sea verdadera luego se ejecuta el bloque del verdadero.
{% endhint %}

#### Ejemplo 3

Ingresar un mail por teclado. Verificar si el string ingresado contiene solo un caracter "@".

```python
mail=input("Ingrese un mail:")
cantidad=0
x=0
while x<len(mail):
    if mail[x]=="@":
        cantidad=cantidad+1
    x=x+1
if cantidad==1:
    print("Contiene solo un caracter @ el mail ingresado")
else:
    print("Incorrecto")
```

Para analizar cada caracter del _string_ ingresado disponemos una estructura _while_ utilizando un contador llamado _`x`_ que comienza con el valor cero y se repetirá tantas veces como caracteres tenga la cadena \(mediante la función len obtenemos la cantidad de caracteres\).

> while x &lt; len \(mail\):

Dentro del ciclo while verificamos cada caracter mediante un _if_ y contamos la cantidad de caracterers "@":

> if\(mail\[i\]=="@"\):       
>
>         counterArroba+=1

Cuando sale del ciclo while procedemos a verificar si el contador tiene almacenado el valor 1 y mostramos el mensaje respectivo:

> if\(counterArroba==1\):
>
>      print\("The email has one @"\)

{% hint style="danger" %}
Los **string** en Python son inmutables, esto quiere decir que una vez que los inicializamos no podemos modificar su contenido.
{% endhint %}

```python
name="Jhon"
name[0]="m" #esto esta permitido
```

![Error al querer modificar una parte de un string](.gitbook/assets/image%20%2827%29.png)

No hay que confundir 😵 cambiar parte del string con realizar la asignación de otro string a la misma variable, luego si es correcto asignar otro valor a un string:

```python
name="Jhon"
name = "jhon" #esto si esta permitido
```

### Métodos propios de las cadenas de caracteres

Los string tienen una serie de métodos \(funciones aplicables solo a los string\) que nos facilitan 🙂 la creación de nuestros programas.

Los primeros tres métodos que veremos se llaman: lower, upper y capitalize. 🌌 

* **upper\(\)** : devuelve una cadena de caracteres convertida todos sus caracteres a mayúsculas.
* **lower\(\)** : devuelve una cadena de caracteres convertida todos sus caracteres a minúsculas.
* **capitalize\(\)** : devuelve una cadena de caracteres convertida a mayúscula solo su primer caracter y todos los demás a minúsculas.

#### Ejemplo 4

Inicializar un string con la cadena "mAriA" luego llamar a sus métodos upper\(\), lower\(\) y capitalize\(\), guardar los datos retornados en otros string y mostrarlos por pantalla.

```python
text1="mAriA"
#upper case
print(text1)
text2=text1.upper()
print(f"Upper case: {text2}")
#lower case
text2=text1.lower()
print("Lower case: ",text2)
text2=text1.capitalize()
print("Capitalizae case: ",text2)
```

![Ejecuci&#xF3;n ejemplo 4](.gitbook/assets/image%20%2826%29.png)

{% hint style="info" %}
Para llamar a un método del **string** debemos disponer entre el nombre del string y el **método** el caracter punto.
{% endhint %}

> text2 = text1.upper\(\)

### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. El tiempo a dedicar a esta **sección ejercicios propuestos** 👩🏾💻 debe ser mucho mayor que el empleado a la sección de **ejercicios resueltos**.  
 La _experiencia_ dice que debemos dedicar el 80% del tiempo 🕖 a la resolución _individual_ de problemas y el otro 20% al análisis y codificación de problemas ya resueltos 🗃 por otras personas.
{% endhint %}

#### Problema 1

Cargar una oración por teclado. Mostrar luego cuantos espacios en blanco se ingresaron. 

{% hint style="info" %}
Tener en cuenta que un espacio en blanco es igual a " ", en cambio una cadena vacía es ""
{% endhint %}

#### Problem 2

Ingresar una oración que pueden tener letras tanto en mayúsculas como minúsculas. Contar la cantidad de vocales.

#### Problem 3

Solicitar el ingreso de una clave 🗝 por teclado y almacenarla en una cadena de caracteres 🙈 . Controlar que el string ingresado tenga entre 10 y 20 caracteres para que sea válido, en caso contrario mostrar un mensaje de error.

#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
#count blank Space
countBlank=0
text=input("Enter text: ")
for f in range(len(text)):
    if(text[f]==" "):
        countBlank+=1
print("The blanck space: ",countBlank)
```
{% endtab %}

{% tab title="Problem 2" %}
```python
#text (Esto es un texto): 6
text=input("Enter text: ")
#auxiliar text (lower case)
textAuxt=text.lower()
#count vowel
countVowel=0
#scroll text
for f in range(len(textAuxt)):
    x=textAuxt[f]
    # a vowel
    if(x=='a' or x=='e' or x=='i' or x=='o' or x=='u'):
        countVowel+=1
print("The number of vowels: ",countVowel)
```
{% endtab %}

{% tab title="Problem 3" %}
```python
# password
password=""
# The passWord is correct
passWordCorrect=False
while (passWordCorrect!=True):
    password=input("Enter password: ")
    # it should have between 10 and 20 characters
    if(len(password)>=10 and len(password)<=20):
        passWordCorrect=True
    else:
        print("The password should have between 10 and 20 characters")
```
{% endtab %}
{% endtabs %}













