# 3 - Codificación del diagrama de flujo en Python

El diagrama de flujo es nuestra herramienta 🛠 para poder plantear una solución a nuestro problema.

Para poder probar nuestra solución propuesta a un problema mediante un diagrama de flujo lo debemos codificar seguidamente en Python.

#### Ejemplo 1

Hallar la superficie de un cuadrado 🔲 conociendo el valor de un lado.

![](.gitbook/assets/image%20%282%29.png)

Utilizando cualquiera de los editores recomendados\(mirar tutoriales basicos para su uso con Python\) o el por defecto en Python guardando un archivo .py codificamos la siguiente solución al diagrama de flujo:

```python
text = input("Enter side:") 
side= int(text)
area =side*side
print ("the area is:", area)
```

Si ejecutamos el programa "Run"  podemos comprobar que se solicita el ingreso por teclado ⌨ de la medida del lado del cuadrado y seguidamente nos muestra la superficie dependiendo del valor ingresado.

Para el ingreso de un dato por teclado y mostrar un mensaje se utiliza la función input, esta función retorna todos los caracteres 🔡 escritos por el operador del programa 🤖 :

`text = input ("Enter side:")`

La variable `side` guarda 💾 todos los caracteres ingresados por teclado pero no en formato numérico, si no en texto,  para esto debemos llamar a la función  `int` para convertir el texto a un número entero.

`side = int(text)`

Ahora se vuelve a guardar en la variable `side` el valor que ingresó el operador pero en formato entero que posibilita hacer operaciones matemáticas 👩🔬 con el mismo.

Un formato simplificado para ingresar un valor entero por teclado y evitarnos escribir las dos líneas anteriores es 🤓 : 

> side  = int \(input\("Enter side:"\)\)

Procedemos a efectuar el cálculo 📚 de la superficie o área luego de ingresar el dato por teclado y convertirlo a entero:

`area = side*side`

Para mostrar un mensaje por pantalla 🖥 tenemos la función print 🖨 que le pasamos como parámetro una cadena de caracteres a mostrar que debe estar entre comillas simples \(" ejm"\) o   dobles\('ejm'\):

`print ("The area is:", area)`

### Algunas consideraciones

{% hint style="warning" %}
* Python ⚠ es sensible  a mayúsculas y minúsculas, no es lo mismo llamar a la función input que con la sintaxis: Input
* Los nombres de variables también son ☢ sensibles  a mayúsculas y minúsculas. Son dos variables distintas si en un lugar iniciamos  la variable "area" y luego hacemos referencia a "Area"
* Los nombres de variable no pueden tener ❌ espacios en blanco, caracteres especiales y empezar con un número
* Todo el código debe ⚖ escribirse en la misma columna 📐 , estará incorrecto si escribimos:

```python
text = input("Enter side:") 
    side= int(text)
    area =side*side
print ("the area is:", area)
```
{% endhint %}

Hay más restricciones que iremos aprendiendo a medida que avance el curso 🔜 .



