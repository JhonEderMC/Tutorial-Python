# 18 - Listas: ordenamiento de sus elementos

Otro algoritmo 🤖 muy común que debe conocer y entender un programador es el ordenamiento de una lista de datos.

El ordenamiento de una lista se logra intercambiando las componentes de manera que:  
 lista\[0\] &lt;= lista\[1\] &lt;= lista\[2\] etc. El contenido de la componente lista\[0\] sea menor o igual al contenido de la componente lista\[1\] y así sucesivamente.  
 Si se cumple lo dicho anteriormente decimos que la lista **está ordenado de menor a mayor**. Igualmente podemos ordenar una lista de **mayor a menor.**

Tengamos en cuenta que la **estructura de datos lista en** _**Python**_ **es mutable**, eso significa que podemos modificar sus elementos por otros. Se puede ordenar tanto listas con componentes de tipo int, float como cadena de caracteres. En este último caso el ordenamiento es alfabético. ****🔡 

### Ejemplos 

#### Ejemplo 1

Se debe crear y cargar una lista donde almacenar 5 sueldos. Desplazar el valor mayor de la lista a la última posición.

La primera aproximación para llegar en el próximo problema al ordenamiento completo de una lista tiene por objetivo analizar 🧠 los intercambios de elementos dentro de la lista y dejar el mayor en la última posición.

El algoritmo consiste en comparar si la primera componente es mayor a la segunda, en caso que la condición sea verdadera ✅ , intercambiamos los contenidos de las componentes.

Vamos a suponer que se ingresan los siguientes valores por teclado:

> 1200
>
> 750
>
> 820
>
> 550 
>
> 490

En este ejemplo 🚏 :

* ¿es 1200 mayor a 750? La respuesta es verdadera, por lo tanto intercambiamos el contenido de la componente 0 con el de la componente 1. 🔜 
* Luego comparamos el contenido de la componente 1 con el de la componente 2: ¿Es 1200 mayor a 820? La respuesta es verdadera entonces intercambiamos. 🔜 
* Si hay 5 componentes hay que hacer 4 comparaciones, por eso el for se repite 4 veces. Generalizando: si la lista tiene N componentes hay que hacer N-1 comparaciones. 🔙 

```text
Cuando		x = 0		x = 1		x  = 2		x = 3
		
		      750		  750		   750	   750
		      1200		820		   820		 820
		      820		  1200		 550	   550
		      550		  550   	 1200    490
		      490 		490  		 490     1200
```

```python
# enter salary
listSalary=[]
for f in range(5):
    listSalary.append(float(input(f"Enter Salary{f+1}: $")))
print("Salary: ",listSalary)
# ordered (N-1 iterations)
for f in range (5-1):
    if(listSalary[f]>listSalary[f+1]):
        auxSal=listSalary[f]
        listSalary[f]=listSalary[f+1]
        listSalary[f+1]=auxSal
print("Salary",listSalary)
```

![Ejecuci&#xF3;n ejemplo 1](.gitbook/assets/image%20%2828%29.png)

#### Ejemplo 2

Se debe crear y cargar una lista donde almacenar 5 sueldos. Ordenar de menor a mayor la lista.

Ahora bien como vimos en el problema anterior con los 4 elementos que nos quedan podemos hacer el mismo proceso visto anteriormente, con lo cual quedará ordenado otro elemento de la lista. Este proceso lo repetiremos hasta que quede ordenado por completo la lista.

Como debemos repetir el mismo algoritmo podemos englobar todo el bloque en otra estructura repetitiva.

Realicemos una prueba del siguiente algoritmo:

```text
Cuando k = 0
		x = 0		x = 1		x = 2		x = 3
		    750		750		750		750
		    1200		820		820		820
		    820		1200		550		550
		    550		550		1200		490
		    490		490		490		1200
		
Cuando k = 1
		x = 0		x = 1		x = 2		x = 3
		    750		750		750		750	
		    820		550		550		550
		    550		820		490		490
		    490		490		820		820
		    1200		1200		1200		1200

Cuando k = 2
		x = 0		x = 1		x  = 2		x = 3
		    550		550		550		550
		    750		490		490		490
		    490		750		750		750
		    820		820		820		820
		    1200		1200		1200		1200


Cuando k = 3
		x = 0		x = 1		x  = 2		x = 3
		   490		490		490		490
		   550		550		550		550
		   750		750		750		750
		   820		820		820		820
```

```python
# enter salary
listSalary=[]
for f in range(5):
    listSalary.append(float(input(f"Enter Salary{f+1}: $")))
print("Salary: ",listSalary)
# ordered (N-1 iterations)
for k in range (4):
    for f in range(4-k):        
        if(listSalary[f]>listSalary[f+1]):
            auxSal=listSalary[f]
            listSalary[f]=listSalary[f+1]
            listSalary[f+1]=auxSal
print("Salary",listSalary)
```

¿Porque repetimos 4 veces el for externo?  
 Como sabemos cada vez que se repite en forma completa el for interno queda ordenada una componente de la lista. A primera vista diríamos que deberíamos repetir el for externo la cantidad de componentes de la lista 📋 , en este ejemplo la lista sueldos tiene 5 componentes. Si observamos, cuando quedan dos elementos por ordenar, al ordenar uno de ellos queda el otro automáticamente ordenado \(podemos imaginar que si tenemos una lista con 2 elementos no se requiere el for externo, porque este debería repetirse una única vez\).

{% hint style="info" %}
Se necesitan N-1 iteracciones para ordenar una lista \(N, tamaño de lista\).
{% endhint %}

Una última consideración a este **algoritmo** de ordenamiento es que los elementos que se van ordenando continuamos comparándolos.

  
Para plantear un algoritmo mas eficiente, como sabemos que cada que paso 👣 del for externo quedan organizados dos elementos, entonces hay una iteración menos \(k-1\) en el interno. 

