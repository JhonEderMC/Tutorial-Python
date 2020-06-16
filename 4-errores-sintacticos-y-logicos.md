# 4 - Errores sintácticos y lógicos

Modificaremos el problema 💡 del concepto anterior y agregaremos adrede una serie de errores  _**tipográficos**_ ✍🏾 . Este tipo de errores siempre son detectados 🔎 por el intérprete de Python, antes de ejecutar el programa.

A los errores tipográficos 📚 , como por ejemplo indicar el nombre incorrecto de la función, nombres de variables incorrectas, falta de paréntesis, palabras claves mal ❌ escritas, etc. los llamamos errores _**sintácticos**_ .

{% hint style="danger" %}
Un programa no se puede ejecutar por completo sin corregir absolutamente todos los errores sintácticos 🚧 
{% endhint %}

  
 Existe otro tipo de errores llamados errores **lógicos**. Este tipo de errores en programas grandes \(miles de líneas\) son más difíciles de localizar 😕 . Por ejemplo un programa que permite hacer la facturación 🤑 pero la salida de datos por impresora 🖨 es incorrecta.

#### Ejemplo anterior

  
 Programa correctamente codificado: 

```python
side = int(input("Enter side:") )
area =side*side
print ("the area is:", area)
```

Programa con error sintáctico 🙊 :

```python
side = int(input("Enter side:") )
area =side*side
print ("the area is:", Area)
```

Es incorrecto \(un error\) la impresión de una variable nunca 😣 inicializada: "Area" \(debemos respetar como la iniciamos en las líneas anteriores\)

![Error sint&#xE1;ctico](.gitbook/assets/image%20%283%29.png)

Programa con error lógico 🙈 :

```python
side = int(input("Enter side:") )
area =side*side*side
print ("the area is:", area)
```

Como podemos observar si ejecutamos el programa no presenta ningún error sintáctico, pero luego de ingresar el valor del lado del cuadrado \(por ejemplo el valor 10\) obtenemos como resultado un valor incorrecto \(imprime el 1000\), esto debido que definimos incorrectamente ⚠ la fórmula para calcular la superficie del cuadrado:

> area = side\*side\*side

 



