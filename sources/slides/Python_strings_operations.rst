:title: Python Strings
:author: Juan Alvarado
:description: String and operations in python.
:keywords: strings, python, operations
:css: C:/GitHub/StaticPages/juan-alvarado-uk.github.io/css/itesm.css
:data-transition-duration: 1000
:skip-help: true

.. header::

    .. image:: C:/GitHub/StaticPages/juan-alvarado-uk.github.io/images/ITESM.png

.. footer::

   Pensamiento computacional para las ingenierías - Juan Alvarado


Presentación con el tema de cadenas en python



.. title: Cadenas en Python

----

Cadenas
=======================

.. code:: python


    "Yo soy una cadena..."

    'Yo también soy una cadena...'


----


Operaciones con cadenas
=======================

El tipo de datos cadena (str) de Python es un tipo de "objeto" que permite varias operaciones.


Aquí se presentan algunas de estas operaciones.


----

.. code:: python

    # el operador in devuelve True si x está contenido 
    # en s, False en otro caso
    x in s

    # el operador in funciona igual que el ejemplo anterior
    # el operador not niega (invierte) el valor de verdad obtenido
    x not in s

    # Concatena (une) las dos cadenas s y t
    s + t


----


.. code:: python

    # El operador * replica la cadena s, n veces. 
    # n debe ser mayor o igual a cero
    s * n

    # sirve para obtener el i-ésimo (índice) caracter de la cadena s, 
    # Las cadenas tienen índices desde 0 hasta (longitud de cadena)-1
    s[i]

    # sirve para obtener una subcadena de la cadena s
    # la subcadena empieza en i, termina en j (sin incluirlo) y 
    # avanza en k saltos.
    s[i:j:k]


----


.. code:: python

    ''' Método que devuelve una copia de la cadena s 
    con su primer carácter en mayúscula y el resto en minúscula.''' 
    s.capitalize()

    'abcdef'.capitalize()
    'Abcdef'

    ''' Método que devuelve una copia de la cadena s en donde 
    el primer carácter de cada palabra inicia con una letra 
    mayúscula y el resto de las letras están en minúscula.'''
    s.title()


    # Método que devuelve una copia de la cadena s
    # con todas sus letras convertidas a minúsculas.
    s.lower()

    # Método que devuelve una copia de la cadena s
    # con todas sus letras convertidas a mayúsculas.
    s.upper()



----


.. code:: python

    ''' Método que devuelve el número de veces que 
    aparece x dentro de la secuencia s. ''' 
    s.count(x)

    'Erase una vez en un reino...'.count('e')


    '''Método que devuelve True si la cadena s termina con el sufijo t, 
    de lo contrario, devuelve False. '''
    s.endswith(t)

    '''Método que devuelve True si la cadena s empieza con el prefijo t, 
    de lo contrario, devuelve False. '''
    s.startswith(t)


----


.. code:: python

    ''' Métodos que devuelven el índice de la cadena s 
    donde se encuentra la primera ocurrencia de la subcadena t 
    dentro de la rebanada s[i:j]. Devuelve -1 si no se encuentra t.
    ''' 

    s.find(t)
    s.find(t,i)
    s.find(t,i,j)

    s = 'abcdefghijklmnopqrst'
    s.find("ghi")
    s.find("ghi", 8)
    s.find("ghi", 3)
    s.find("ghi", 3, 6)
    s.find("ghi", 3, 10)



----


.. code:: python

    ''' Métodos que devuelven el índice de la cadena s donde se encuentra 
    la última ocurrencia de la subcadena t dentro de la rebanada s[i:j]. 
    Devuelve -1 si no se encuentra t.
    ''' 

    s.rfind(t)
    s.rfind(t,i)
    s.rfind(t,i,j)


----



.. code:: python

    # Método que devuelve el índice en el que aparece por primera vez x
    s.index(x)

    # Método que devuelve True si todos los caracteres de s 
    # son alfabéticos (letras) y len(s) ≥ 1
    s.isalpha()


----

.. code:: python

    # Método que devuelve True si todos los caracteres de s 
    # son dígitos del 0 al 9 y len(s)≥1. 
    s.isdigit()

    # Método que devuelve True si todas las letras contenidas en s
    # son minúsculas y len(s)≥1.
    s.islower()

    # Método que devuelve True si todas las letras contenidas en s
    # son mayúsculas y len(s)≥1.
    s.isupper()


----

.. code:: python
 
    ''' Método que devuelve una copia de la cadena s 
    pero eliminando todos los caracteres en blanco 
    (espacios, tabuladores y saltos de línea) que 
    aparecen al inicio (left strip). '''
    s.lstrip()

    # Lo mismo pero eliminando los caracteres en blanco al final
    s.rstrip()
    
    # Lo mismo pero eliminando los caracteres en blanco 
    # al inicio y al final
    s.strip()



----

.. code:: python

    # Devuelve una cadena de caracteres cuyo código Unicode es x.
    chr(x)

    chr(65)
    chr(128578)

    # Devuelve el código de Unicode del carácter contenido en la cadena x.
    ord(x)
    ord('A')

    # Devuelve la logitud de la cadena s
    len(s)

    # Convierte x en representación de cadena
    str(x)




----

.. code:: python


    '''Método que devuelve una lista con las palabras contenidas en s 
    delimitadas por x. Si se omite x considera como delimitador a 
    cualquier sequencia consecutiva de caracteres en blanco 
    (espacios, tabuladores y saltos de línea).'''
    s.split(x)

    '''Método que devuelve una copia de la cadena s
    en donde todas las ocurrencias de la subcadena t
    son reemplazadas por u. '''
    s.replace(t,u)


----

.. code:: python

    '''Función que devuelve un objeto iterable con todos los 
    elementos de la secuencia s pero en orden inverso. '''
    reversed(s)

    '''Función que devuelve una nueva lista con todos los 
    elementos contenidos en la secuencia s en orden ascendente. 
    Se utiliza orden lexicográfico para comparar los elementos de s.'''
    sorted(s)

