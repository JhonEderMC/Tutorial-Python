# 22 - Listas: eliminación de elementos

Hemos visto que una lista la podemos iniciar por asignación indicando sus elementos.

`lista=[100, 200, 300, 400]`

También podemos agregarle elementos al final mediante el método append:

`lista.append(120)`

Si ahora imprimimos la lista tenemos como resultado:

`lista=[100, 200, 300, 400, 120]`

{% hint style="info" %}
Otra característica fundamental de las listas en Python es que podemos eliminar cualquiera de sus componentes llamando al método _**pop**_ e indicando la posición del elemento a borrar.
{% endhint %}

`lista.pop(0)`

Ahora si imprimimos la lista luego de eliminar el primer elemento el resultado es:

`lista=[200, 300, 400, 120]`



