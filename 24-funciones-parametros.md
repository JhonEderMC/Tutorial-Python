# 24 - Funciones: parámetros

Vimos en el concepto anterior que una función resuelve una parte de nuestro algoritmo. Tenemos por un lado la declaración de la función por medio de un nombre y el algoritmo de la función seguidamente. Luego para que se ejecute la función la llamamos desde el bloque principal de nuestro programa.

Ahora veremos que una función puede tener **parámetros** para _recibir datos_. Los parámetros nos permiten comunicarle algo a la función y la hace más flexible.

### Ejemplos

#### Ejemplo 1

Confeccionar una aplicación que muestre una presentación 👩🏽🎨 en pantalla del programa. Solicite la carga de dos valores y nos muestre la suma. Mostrar finalmente un mensaje de despedida del programa.

```python
# function message
def message(msg):
    print(msg)
    print("**************************")

# function sum of two values
def suma(val1,val2):
    v=val1+val2;
    print("Sum: ",v)

# main
msg=("welcome to this program!")
# call function
message(msg)
val1=int(input("Enter a number1: "))
val2=int(input("Enter a number2: "))
# cal function
suma(val1,val2)
msg=("thank you by uses this program")
# call function
message(msg)
```

![Salida ejecuci&#xF3;n ejemplo 1](.gitbook/assets/image%20%2840%29.png)

Ahora para resolver este pequeño problema hemos planteado una función llamada _message_ que recibe como parámetro un string \(cadena de caracteres\) y lo muestra en pantalla.

{% hint style="info" %}
Los parámetros van seguidos del nombre de la función encerrados entre paréntesis \(y en el caso de tener más de un parámetro los mismos deben ir separados por coma\)
{% endhint %}

```python
def message(msg):
    print(msg)
    print("**************************")
```

Un parámetro podemos imaginarlo como una variable que solo se puede utilizar dentro de la función. ⚠ 

Ahora cuando llamamos a la función _message_ desde el bloque principal de nuestro programa debemos pasar una variable string o un valor de tipo string:

> ```python
> message("El programa calcula la suma de los dos valores ingresados por teclado.")
> ```

El string que le pasamos: "El programa calcula la suma de dos valores ingresados por teclado." lo recibe el parámetro de la función.

Una función con parámetros nos hace más flexible 🥳 la misma para utilizarla en distintas circunstancias. En nuestro problema la función _message_ la utilizamos tanto para la presentación inicial de nuestro programa como para mostrar el mensaje de despedida. Si no existieran los parámetros estaríamos obligados 😞 a implementar dos funciones como el concepto anterior.

#### Ejemplo 2

Confeccionar una función que reciba tres enteros y nos muestre el mayor de ellos. La carga de los valores hacerlo por teclado.

```python
# function greater of three number
def greater_number(v1,v2,v3):
    if (v1>=v2 and v1>=v3):
        greater=v1
    elif(v2>=v1 and v2>=v3):
        greater=v2
    else:
        greater=v3
    return greater

# main 
v1=int(input("Enter a number1: "))
v2=int(input("Enter a number2: "))
v3=int(input("Enter a number3: "))
print("greater number: ",greater_number(v1,v2,v3))
```

Es importante notar que un programa en Python no ejecuta en forma lineal las funciones definidas en el archivo _\*.py_ sino que arranca en la zona del bloque principal. En nuestro ejemplo se llama primero a la función "_greater\_number\(\)_". Esta función recibe los tres parametros v1, v2 y v3 para luego retornar el mayor de ellos.

#### Ejemplo 3

