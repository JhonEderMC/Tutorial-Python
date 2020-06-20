---
description: Como realizar comentarios en el código fuente.
---

# 11 - Definición de comentarios en el código fuente

Un programa en Python puede definir además del algoritmo propiamente dicho una serie de comentarios en el código fuente que sirvan para aclarar los objetivos de ciertas partes del programa.

Tengamos en cuenta que un programa puede requerir mantenimiento del mismo en el futuro. Cuando hay que implementar cambios es bueno encontrar en el programa comentarios sobre el objetivo de las distintas partes del algoritmo, sobretodo si es complejo.

Existen dos formas de definir comentarios en Python:

{% hint style="info" %}
 Comentarios de una sola línea, se emplea el caracter **\#**     
{% endhint %}

```python
# Definimos contadores
contad1=0
contad2=0
contad3=0   
```

Comentarios de varias líneas:

```python
""" Definimos tres contadores """
''' Definimos tres contadores'''
contad1=0
contad2=0
contad3=0  
```

{% hint style="info" %}
Se deben utilizar tres comillas simples o dobles seguidas al principio y al final del comentario.
{% endhint %}

{% hint style="danger" %}
Todo lo que disponemos como comentario  no se ejecuta.
{% endhint %}

### Ejemplos 

#### Ejemplo 1

Mostrar la tabla de multiplicar del 5 empleando primero el while y seguidamente de nuevo empleando el for.

```python
"""
Mostrar la tabla de 5 con las estructuras repetitivas:
  while
  y
  for
"""

#utilizando el while
print("Tabla del 5 empleando el while")
x=5
while x<=50:
    print(x)
    x=x+5

#utilizando el for
print("Tabla del 5 empleando el for")
for x in range(5,51,5):
    print(x)    
```



### Problemas propuestos 📚 

{% hint style="info" %}
Ha llegado una parte fundamental 😀 , que es el momento donde uno desarrolla individualmente un algoritmo ✍🏾 para la resolución de problemas. 
{% endhint %}

#### Problema 1

Realizar un programa que solicite la carga de valores enteros por teclado y los sume. Finalizar la carga al ingresar el valor -1. Dejar como comentario dentro del código fuente el enunciado del problema.

#### Solución 🆘 

{% hint style="info" %}
**Nota :** 👩🏫 Inténtalo tu mism@, esta es la mejor forma de aprender 📈  o si quieres ver 👀 otro algoritmo para solucionar el mismo problema. 👨💻
{% endhint %}

{% tabs %}
{% tab title="Problem 1" %}
```python
"""
Realizar un programa que solicite la carga de valores enteros 
por teclado y los sume. Finalizar la carga al ingresar el valor -1. 
Dejar como comentario dentro del código fuente el enunciado del problema.
"""
# stop with -1
number=0
sum=0
while number!=-1:
    number=int(input("Number(Stopt with -1):"))
    if( number!=-1):
        #acumulate
        sum+=number
print("Sum: ",sum)
```
{% endtab %}
{% endtabs %}





