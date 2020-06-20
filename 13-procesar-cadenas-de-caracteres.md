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





