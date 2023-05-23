---
marp: true
---


# Taller intensivo de Python
## 4 Horas
### Mexicali, B.C, 2013
 ---
 # Temario
 * Tipos de datos básicos.
* Operadores matemáticos y
logicos.
* Todo es un objeto.
* Estructuras de control.
* Clases, métodos y funciones.
* Las baterías ya vienen
incluidas.
* La letra chiquita del contrato.
* Módulos.
* The cheeseshop: Pypi, eggs y Virtualenv.
* ¿Dónde encontrar más ayuda?
--- 
# Taller Intensivo De Phython
## Vista Rapida
---
# Lenguaje multi-propósito
* POO.
* Scripting / Guiones.
* Algo de programación funcional.
* Tipo de datos dinámico.
* Administración automática de memoria.
---
# Otros detallitos
* Funcionalidad y sintaxis sencilla. Readability counts
* Una gran comunidad de entusiastas, usuarios y programadores.
---
# Multi-propósito
* Administración de servidores (scripting y granjas de servidores).
* Sistemas distribuidos.
* Paralelismo (Hilos, multiprocesos y SMP).
* Interfaz con hardware y drivers (C, C++).
* Interfaces gráficas (Gtk+, QT, Windows,MacOS)
* Sistemas empotrados
---
# Multi-propósito
* Web
* Zope, Plone, Grok
* Pyramid / TurboGears/ Repoze BFG
* Django
* CherryPy
* Werkzeug, Bootlepy, Flask
* XML-RPC, REST, HTTP, FTP, Sockets, etc..
* Multimedia (GStreamer, Blender)
---
# Multi plataforma
* Windoze
* Linux
* FreeBSD, NetBSD, OpenBSD
* Java (Jython)
* .NET (IronPython)
* MacOS, Haiku (BeOS)
* Python (Python sobre python - PyPy)
---
# ¿Quién usa Python?
---
# Versiones
* Python 2.0 en 2000.
* Python < 2.7 = obsoleto. (Aunque algunos usan
* Python 2.4 aún).
* Python 3 alias Python 3k ya ha salido, pero aún no se encuentra en uso masivo.
---
# El zen de Python
```
>>> import this
The Zen of Python, by Tim Peters
Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
>>>
```
---
# Taller intensivo de Python
## Tipos de datos básicos
---
# Tipos de datos básicos: números
## bool
```
>>> True = bool(True)
True
>>> True == bool(False)
False
```
---
# float
```
>>> 100.1 == float (100.1)
True
>>> 100.0 == 100
True
```
---
# int
```
>>> 100 == int(100)
True
```
---
# long
```
>>> 10L == long (10)
True
>>> 10 == 10.0 == 10L
True
```
---
# Tipos de datos básicos: números
# oct
```
>>> 010 == 0o10 == 0O10
True
>>> 10 == 10.0 == 10L ==  012 == 0o12
True
```
---
# complex
```
>>> 1 + 2j == (1 + 2j) == complex(1,2)
True
>>> 10 == 10.0 == 10L == 0o12 == 0x0a == 
(10 +0j)
True
```
---
# hex
```
>>> 0x0a == 0x0A == 0X0a == 0X0A
True
>>> 10 == 10.0 == 10L == 0o12 == 0x0a
True
```
---
# bin
```
>>> 0b1010 == 0B1010
True
>>> 10 == 10.0 == 10L == 0o12 == 0x0a == 
(10 +0j) == 0b1010
True
```
---
# Tipos de datos básicos: números
* Oops!
* oct() y hex()
* regresan una representación del número en formato string.
---
```

>>> 0o10 == oct(8)
False
>>> oct(8)
'010'
>>> 0x0a == hex(10)
False
>>> hex(10)
'0xa'
```
---
# Tipos de datos básicos: secuencias
* Una secuencia es una lista ordenada deobjetos o eventos.
---
# Tipos de datos básicos: secuencias
* Una secuencia es una lista ordenada de objetos o eventos.
---
# Tipos de datos básicos: secuencias (tuplas)
* Tupla: es una lista con un número limitado de objetos.
* En python, una tupla es una secuencia devalores u objetos separados por comas.
---
```
>>> 1 , 12.9, 0x0fe, 0b10001
(1, 12.9, 254, 17)
>>> (1, 2, 3, 4)
(1, 2, 3, 4)
>>> (1, 2, 3, 4, (1 , 12.9), 0b10001 )
(1, 2, 3, 4, (1, 12.9), 17)
```
---
# Tipos de datos básicos: secuencias (tuplas)
* Rebanadas e índices
```
>>> t = (1, 2, 3, 4)
>>> t[0]
1
>>> t[3]
4
>>> t[1:3]
(2, 3)
>>> t [­1]
4
>>> t [­3:­1]
(2,3
>>> t[2:]
(3, 4)
>>> t[2:][­1]
4
```
---
# Tipos de datos básicos: secuencias (listas)
* Lista: es una lista con un número ilimitado de objetos.
* En python, una lista es una secuencia de valores u objetos separados por comas y delimitadas por corchetes.
---
```
>>> [1 , 12.9, 0x0fe, 0b10001]
[1, 12.9, 254, 17]
>>> [1, 2, 3, 4]
(1, 2, 3, 4)
>>> [1, 2, 3, 4, (1 , 12.9), 0b10001 ]
[1, 2, 3, 4, (1, 12.9), 17]
```
--- 
# Tipos de datos básicos: secuencias (listas)
* Rebanadas e índices
```
>>> t = [1, 2, 3, 4]
>>> t[0]
1
>>> t[3]
4
>>> t[1:3]
(2, 3)
>>> t [­1]
4
>>> t [­3:­1]
(2,3)
>>> t[2:]
(3, 4)
>>> t[2:][­1]
4
```
---
# Tipos de datos básicos: secuencias (tuplas vs listas)
* Tuplas
* Secuencia
* Contiene cualquier tipo de valor
* Delimitado por paréntesis
* No es mutable.
* La posición es importante.
---
* Lista
* Secuencia
* Contiene cualquier tipo de valor.
* Delimitado por corchetes.
* Mutable
---
# Tipos de datos básicos: secuencias (tuplas vs listas)
## Inmutable
```
>>> t = (1, 2, 3, 4)
>>> t[1] = 27
Traceback ...
```
---
# Mutable
```
>>> t = [1, 2, 3, 4]
>>> t[1] = 27
>>> t
[1, 27, 3, 4]
>>> t.append(33)
>>> t
[1, 27, 3, 4, 33]
>>> t.insert(2, 400)
>>> t
[1, 27, 400, 3, 4, 33]
```
---
# Tipos de datos básicos: secuencias (tuplas vs listas)
## Inmutable
```
>>> t = (1, 2, 3, 4)
>>> t[1] = 27
Traceback ...
```
---
### Mutable
```
>>> t = [1, 27, 400, 3, 4, 33]
>>> t.pop()
33
>>> t
[1, 27, 400, 3, 4]
>>> t.remove(27)
[1, 400, 3, 4]
>>> t.sort()
>>> t
[1, 3, 4, 400]
>>> t.reverse()
>>> t
[400, 4, 3, 1]
```
---
# Tipos de datos básicos: secuencias (cadenas)
```
>>> '' == str() == ""
True
>>> 'hola mundo'
'hola mundo'
>>> " ' "
" ' "
>>> ' " '
' " '
>>> '"' == "\""
True
>>> "'" == '\''
True
```
---
# Tipos de datos básicos: secuencias (cadenas)
```
>>> """
... Cadena con multiples lineas.
... Puede contener " y ' sin problemas.
... """
'\nCadena con multiples lineas.\nPuede contener " y \' sin problemas.\n'
>>> print _
Cadena con multiples lineas.
Puede contener " y ' sin problemas.
```
---
# Tipos de datos básicos: secuencias (cadenas con acentos)
```
>>> 'Cadena con acentos: 
áéíóúñ
'
'Cadena con acentos: \xc3\xa1\xc3\xa9\xc3\xad\xc3\xb3\xc3\xba\xc3\xb1'
>>> u'Cadena con acentos: 
áéíóúñ
'
u'Cadena con acentos: \xe1\xe9\xed\xf3\xfa\xf1'
```
---
# Tipos de datos básicos: secuencias (cadenas)
* Rebanadas e índices
```
>>> c = 'Hola Mundo'
>>> c[0]
'H'
>>> c[3]
'a'
>>> c[1:3]
'ol'
>>> c[­1]
'o'
>>> c[­3:­1]
'nd'
>>> c[2:]
'la Mundo'
>>> c[2:][­1]
'o'
```
---
# Tipos de datos básicos: secuencias (tuplas vs listas vs cadenas)
## Tuplas
* Secuencia
* Contiene cualquier tipo de valor
* Delimitado por paréntesis
* No es mutable.
* La posición es importante.
## Lista
* Secuencia
* Contiene cualquier tipo de valor.
* Delimitado por corchetes.
* Mutable
## Cadena
* Secuencia
* Contiene caracteres
* Delimitado por“y'
* Inmutable
* La posición es importante.
---
# Tipos de datos básicos: secuencias (diccionarios)
* Diccionario: Es una secuencia de valores indexados por una llave.
* Se delimita por {}
* Las llaves deben ser objetosinmutables
```
>>> {'foo': 'bar', 777: 'A sus ordenes jefe'}
{777: 'A sus ordenes jefe', 'foo': 'bar'}
```
---
# Tipos de datos básicos: secuencias (diccionarios)
 * Rebanadas (slicing) e índices
 ```
 >>> d = {'foo': 'bar', 777: 'A sus ordenes jefe'}
>>> d['foo']
'bar'
>>> d[777]
'A sus ordenes jefe'
>>> d['no existe']
Traceback (most recent call last):
  
File "<stdin>", line 1, in <module>
KeyError: 'no existe'
>>> d['ahora si'] = 3.1416
>>> d
{777: 'A sus ordenes jefe', 'foo': 'bar', 'ahora si': 3.1416}
```
---
# Tipos de datos básicos: secuencias (tuplas vs listas vs cadenas vs diccionarios)
## Tuplas
* Secuencia
* Contiene cualquier tipo de valor
* Delimitado por paréntesis
* No es mutable.
* La posición es
importante.
## Lista
* Secuencia
* Contiene cualquier tipo de valor.
* Delimitado por corchetes.
* Mutable
* La posición no importa mucho
## Cadena
* Secuencia
* Contiene caracteres
* Delimitado por “y'
* Inmutable
* La posición es importante.
## Diccionario
* Secuencia
* Contiene cualquiertipo de valor, perolas llaves deben ser inmutables.
* Delimitado por {}
* La posición nunca importa
---
# Taller intensivo de Python
## Operaciones y Operadores
---
# Operaciones: El cero
* None
* 0
* 0.0
* 0L
* 0x00
* 0b00
* 0o00
* ()
* “”
* ''
* “””“””
* ''''''
* []
* {}
---
# Operaciones: El cero
## Cualquier valor “cero” también se evalúa como False.
---
# Operadores booleanos
| Operador | Resultado                                                                    |
|----------|------------------------------------------------------------------------------|
| x or y   | Si X es falso, entonces el resultado equivale a Y. De lo contrario es X.     |
| x and y  | Si X es falso, entonces el resultado equivale a X. De lo contrario es Y.     |
| Not X    | SI X es falso, entonces el resultado equivale a X. De lo contrario es False. |
---
# Operadores booleanos
## Ejemplo de or
```
>>> a = 0
>>> b = 7
>>> a or b
7
>>> a = 1
>>> a or b
1
```
---
# Operadores booleanos
## Ejemplo de and
```
>>> a = 0
>>> b = 7
>>> a and b
0
>>> a = 1
>>> a and b
7
```
---
# Operadores booleanos
## Ejemplo de not
```
>>> a = 0
>>> not a
0
>>> b = []
>>> not b
True
>>> b.append(5)
>>> not b
False
```
---
# Operadores booleanos
## Son más útiles juntos
```
>>> canasta = []
>>> not canasta and 'La canasta esta vacia' or 'La canasta tiene algo'
'La canasta esta vacia'
>>> canasta.append('manzana')
>>> not canasta and 'La canasta esta vacia' or 'La canasta tiene algo'
'La canasta tiene algo'
```
---
