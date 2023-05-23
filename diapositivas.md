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
# Operaciones: comparación
* Mayor que ... >
* Menor que ... <
* Mayor o igual ... >=
* Menor o igual ... <=
* Igual ... ==
* No igual ... !=
* El objeto es el mismo: is
* El objeto no es el mismo: is not
---
# Operaciones: comparación
```

>>> 2 > 1
True
>>> 1.1 > 2
False
>>> 1 +2j >= 1
... TypeError
```
---
# Operaciones: comparación
```
>>> a = []
>>> a == []
True
>>> a is []
False
>>> a = 100
>>> a == 100
True
>>> a is 100
True
>>> a == 100.0
True
>>> a is 100.0
False
```
---
# Operaciones básicas
* Suma ... +
* Resta ... -
* Multiplicación ... *
* División ... /
* División entera ... //
* Remanente ... %
* Potenciación ... **
---
# Operaciones básicas
```
>>> 1 + 1.1 + 0x01 + 0b0001 + 0o1 + 1L
6.1
>>> 0xFFFFFF – 255
16776960
>>> 0b01100110 – 10.78
91.22
>>> 'hola' + 'mundo'
'Holamundo'
>>> [1] + [3*7] + ['wtf'] *2
[1, 21, 'wtf', 'wtf']
```
---
# Operaciones básicas
```
>>> 1 / 1
0
>>> 1 / 2
0
>>> 1 / 2.0
0.5
>>> 1.0 / 2
0.5
>>> float(1/2)
0.0
>>> float(1)/2
0.5
```
---
# Operaciones básicas
```
>>> 10 / 3
3
>>> 10.0 // 3
3.0
>>> 10.0 % 3
1.0
>>> divmod(10,3)
(3,1)
>>> (10//3, 10%3)
(3,1)
```
---
# Operaciones booleanas a nivel de bit.
```
>>> #or
>>> hex(0x0f | 0xf0)
'0xff'
>>> #and
>>> hex(0x0f & 0xf0)
'0x0'
>>> #xor
>>> hex(0x0f ^ 0xf0)
'0xff'
>>> #Corrimiento
>>> hex(0x01 << 4), hex(0xF0 >> 4)
('0x10', '0xf')
>>> #inversion de bits
>>> hex(~0xF)
'­0x10'
```
---
# Otras operaciones matematicas
* Valor absoluto ... abs()
* Conversión a entero ... int()
* Conversión a long y float ... long(), float()
* División entera con residuo ... divmod()
---
# Taller intensivo de Python
## Todo es un objeto
---
# POO – Todo es un objeto
* Hay dos objetos principales
* object
* type
* Todo lo demás son descendientes de esto dos.
---
# POO – Introspección 101
* Sesión en terminal
* Aprender a usar dir() y help()
---
# POO – Todo es un objeto
* Hay dos objetos principales
* object
* type
* Todo lo demás deriva de ahí
---
# Taller intensivo de Python
## Estructuras de control
---
# Estructuras de control en python
* If ... elif .. else
* While ...
* For ...
* No hay switch o case.
---
# If – elif -else
```
>>> x = 1
>>> if x ==1:
...     print "Es uno"
... elif x>1:
...     print "Es mayor a uno"
... else:
...     print "Es 0 o menor a 1"
... 
Es uno
```
---
# while
```
>>> z = 10
>>> while z:
...     print z
...     z­=1
... 
10
9
8
7
6
5
4
3
2
1
```
---
# for
```
>>> range(5)
[0, 1, 2, 3, 4]
>>> for i in range(5):
...     print i
... 
0
1
2
3
4
```
---
# for
```
>>> platillos = {'pollito': 'papas', 'arroz': 'leche', 
... 'cafe':'galletas'}
>>> for k in platillos:
...     print k, 'con', platillos[k]
... 
pollito con papas
arroz con leche
cafe con galletas
```
---
# Taller intensivo de Python
## Clases métodos y funciones
---
# Funciones
```
def ladrar():
    
print "woof"
    
def maullar():
    
print "mrrmiau"
>>> ladrar()
Woof
>>> maullar()
mrrmiau
```
---
# Funciones
```
def correr(velocidad):
    
print "Corriendo a %i Km/h" % velocidad
>>> correr(10)
Corriendo a 10 Km/h
>>> correr
()
Traceback (most recent call last):
  
File "<stdin>", line 1, in <module>
TypeError: correr() takes exactly 1 argument (0 given)
>>
```
---
# Funciones
```
def correr(velocidad = 1):
    
print "Corriendo a %i Km/h" % velocidad
>>> correr(10)
Corriendo a 10 Km/h
>>> correr()
Corriendo a 1 Km/h
```
---
# Funciones
```
def comer(comida=None, gusta=False):
    
if comida and gusta:
        
        
print "Estoy comiendo %s y me gusta" % comida
    
elif comida and not gusta:
        
        
print "Estoy comiendo %s, pero no me gusta" % comida
    
else:
        
        
print "No tengo nada que comer."
>>> comer()
No tengo nada que comer.
```
---
# Funciones
```
def comer(comida=None, gusta=False):
    
if comida and gusta:
        
        
print "Estoy comiendo %s y me gusta" % comida
    
elif comida and not gusta:
        
        
print "Estoy comiendo %s, pero no me gusta" % comida
    
else:
        
        
print "No tengo nada que comer."
>>> comer('Pescado')
Estoy comiendo Pescado, pero no me gusta
```
---
# Funciones
```
def comer(comida=None, gusta=False):
    
if comida and gusta:
        
        
print "Estoy comiendo %s y me gusta" % comida
    
elif comida and not gusta:
        
        
print "Estoy comiendo %s, pero no me gusta" % comida
    
else:
        
        
print "No tengo nada que comer."
>>> comer('Pescado', True)
Estoy comiendo Pescado y me gusta
>>> comer('Quesadillas', gusta=True)
Estoy comiendo Quesadillas y me gusta
>>> comer(gusta=True, comida='Arroz con leche')
Estoy comiendo Arroz con leche y me gusta
```
---
# Objetos
```
class Comida(object):
    
platillos = []
    
costo = None
>>> desayuno = Comida()
>>> desayuno
<__main__.Comida object at 0xb774d9ec>
>>> desayuno.platillos.append('Fruta')
>>> desayuno.platillos.append('Huevos revueltos')
>>> desayuno.costo = 35
>>> desayuno.platillos
['Fruta', 'Huevos revueltos']
>>> desayuno.costo
35
```
---
# Objetos
```
class Comida(object):
    
platillos = []
    
costo = 0
    
    
def comer(self):
        
        
for nomnom in self.platillos: 
            
            
print u"
Ñ
om 
Ñ
om ­> ", nomnom
    
    
def pagar (self):
        
        
print "Soy %f pesos mas pobre :P" % self.costo
        
        
        
        
>>> desayuno = Comida()
>>> desayuno.comer()
>>> desayuno.pagar()
Soy 0.000000 pesos mas pobre :P
```
---
# Objetos
```
class Desayuno(Comida):
    
def __init__(self):
        
        
self.platillos = ['Jugo de naranja', 'Cafe negro', 
                          
                          
'Huevos estrellados']
        
        
self.costo = 35
                
                
>>> desayuno = Desayuno()
>>> desayuno.comer()
Ñ
om 
Ñ
om ­>  Jugo de naranja
Ñ
om 
Ñ
om ­>  Cafe negro
Ñ
om 
Ñ
om ­>  Huevos estrellados
>>> desayuno.pagar()
Soy 35.000000 pesos mas pobre :P
```
---
# Objetos
```
class TacosDeAsada(Comida):
    
def __init__(self, costo, presupuesto):
        
        
self.presupuesto = presupuesto
        
        
self.ntacos, self.sobrante = divmod(presupuesto, costo)
        
        
self.costo = presupuesto ­ self.sobrante
        
        
for i in range(self.ntacos):
            
            
self.platillos.append('taco')
        
        
    
def pagar(self):
        
        
super(TacosDeAsada, self).pagar()
        
        
print 'Y me sobraron %5.2f' % self.sobrante
```
---
# Objetos
```
>>> cena = TacosDeAsada(16, 87)
>>> cena.comer()
Ñ
om 
Ñ
om ­>  taco
Ñ
om 
Ñ
om ­>  taco
Ñ
om 
Ñ
om ­>  taco
Ñ
om 
Ñ
om ­>  taco
Ñ
om 
Ñ
om ­>  taco
>>> cena.pagar()
Soy 80.000000 pesos mas pobre :P
Y me sobraron  7.00
>>>
```
---
# Taller intensivo de Python
# Las baterías vienen incluidas
---
# built-ins
| abs()         | divmod()    | input()      | open()      | staticmethod() |
|---------------|-------------|--------------|-------------|----------------|
| all()         | enumerate() | int()        | ord()       | str()          |
| any()         | eval()      | isinstance() | pow()       | sum()          |
| basestring()  | execfile()  | issubclass() | print()     | super()        |
| bin()         | file()      | iter()       | property()  | tuple()        |
| bool()        | filter()    | len()        | range()     | type()         |
| bytearray()   | float()     | list()       | raw_input() | unichr()       |
| callable()    | format()    | locals()     | reduce()    | unicode()      |
| chr()         | frozenset() | long()       | reload()    | vars()         |
| classmethod() | gettattr()  | map()        | repr()      | xrange()       |
| cmp()         | globals()   | max()        | reversed()  | zip()          |
| compile()     | hasattr()   | memoryview() | round()     | __import__()   |
| complex()     | hash()      | min()        | set()       | apply()        |
| delattr()     | help()      | next()       | setattr()   | buffer()       |
| dict()        | hex()       | object()     | slice()     | coerce()       |
| dir()         | id()        | oct()        | sorted()    | intern()       |
---
# Actividad
| abs()         | divmod()    | input()      | open()      | staticmethod() |
|---------------|-------------|--------------|-------------|----------------|
| all()         | enumerate() | int()        | ord()       | str()          |
| any()         | eval()      | isinstance() | pow()       | sum()          |
| basestring()  | execfile()  | issubclass() | print()     | super()        |
| bin()         | file()      | iter()       | property()  | tuple()        |
| bool()        | filter()    | len()        | range()     | type()         |
| bytearray()   | float()     | list()       | raw_input() | unichr()       |
| callable()    | format()    | locals()     | reduce()    | unicode()      |
| chr()         | frozenset() | long()       | reload()    | vars()         |
| classmethod() | gettattr()  | map()        | repr()      | xrange()       |
| cmp()         | globals()   | max()        | reversed()  | zip()          |
| compile()     | hasattr()   | memoryview() | round()     | __import__()   |
| complex()     | hash()      | min()        | set()       | apply()        |
| delattr()     | help()      | next()       | setattr()   | buffer()       |
| dict()        | hex()       | object()     | slice()     | coerce()       |
| dir()         | id()        | oct()        | sorted()    | intern()       |
# Elijan 10 funciones y las probamos ;)
---
# Librería estándar de Python
* Cadenas
* Tipos de datos
* Funciones matemáicas
* Acceso a archivos, directorios y a algunas funciones del SO.
* Persistencia de datos
* Algoritmos de compresión y encriptado.
* Formatos de archivos(CSV, .ini, robots.txt)
---
# Librería estándar de Python
* Hilos, Colas y  multiprocesamiento.
* Email, JSON, mime, HTTP.
* XML
* FTP
* Internacionalización
* Depurado y pruebas de integración y unitarias.
---
# Cadenas
```
>>> '%s %i %2.3f' % ('Yeah', 100, 456.12345234523)
Yeah 100 456.123'
>>> '{0}, {1}, {2}'.format('a', 'b', 'c')
'a, b, c'
>>> # Los indices se pueden repetir
>>> '{0}{1}{0}'.format('abra', 'cad')
'abracadabra'
>>> 'Coordenadas: {latitud}, {longitud}'.format(
... latitud='37.24N', longitud='­115.81W')
'Coordenadas: 37.24N, ­115.81W'
```
---
# Cadenas
```
>>> coord = {'latitud': '37.24N', 'longitud': '­115.81W'}
>>> 'Coordenadas: {latitud}, {longitud}'.format(**coord)
'Coordinates: 37.24N, ­115.81W'
```
---
# Cadenas – Expresiones regulares
```
>>> import re
>>> ptrn = re.compile('^[a­z0­9\­_]+$')
>>> ptrn.match('#invalid')
>>> ptrn.match('tzicatl')
<_sre.SRE_Match object at 0x7f85cb50fe68>
>>> telefono = re.compile("0[­\d\s]{10,}")
>>> telefono.match('10')
>>> telefono.match('2224679801')
>>> telefono.match('02224679801')
<_sre.SRE_Match object at 0x7f85cb50fe68>
>>> telefono.match('01­2224679801')
<_sre.SRE_Match object at 0x7f85cb50f780>
>>
```
---
# Cadenas – StringIO
```
$ echo  "Hola mundo" > hola.txt
$ python
>>> fp = open('hola.txt')
>>> fp.read()
'Hola mundo\n'
>>> fp.close()
>>> fp = open('hola.txt', 'w')
>>> fp.write('Los caballeros de la mesa cuadrada\n')
>>> fp.write('Y ahora algo completamente diferente...\n')
>>> fp.close()
>>>
```
---
# Cadenas – StringIO
```
>>> import StringIO
>>> fp = StringIO.StringIO
('
Hola mundo\n')
>>> fp.read()
'Hola mundo\n'
>>> fp.close()
>>> fp = StringIO.StringIO
()
>>> fp.write('Los caballeros de la mesa cuadrada\n')
>>> fp.write('Y ahora algo completamente diferente...\n')
>>> print fp.getvalue()
Los caballeros de la mesa cuadrada
Y ahora algo completamente diferente...
>>> fp.close()
>>> print fp.getvalue() #TraceBack
```
---
# Tipos de datos - Fechas
```
>>> import datetime
>>> f = datetime.datetime.now()
>>> f.day, f.month, f.year 
(4, 9, 2012)
>>> f +  datetime.timedelta(days=11)
datetime.datetime(2012, 9, 15, 23, 3, 2, 797328)
```
---
# Tipos de datos – Queue - FIFO
```
import Queue
q = Queue.Queue()
for i in range(5):
    
q.put(i)
while not q.empty():
    
print q.get()
$ python Queue_fifo.py
0
1
2
3
4
```
---
# Tipos de datos – Queue - LIFO
```
import Queue
q = Queue.LifoQueue()
for i in range(5):
    
q.put(i)
while not q.empty():
    
print q.get()
$ python Queue_lifo.py
4
3
2
1
0
```
---
# Funciones matemáticas
```
>>> math.ceil(1.1)
2.0
>>> math.floor(1.99)
1.0
>>> from math import factorial as fact
>>> for i in range(5):
...     print fact(i)
... 
1
1
2
6
24
>>> fact(200)
788657867364790503552363213932185062295135977687173263294742533244359449963403342920304284011984623904177212138919638830257642790242637105061926624952829931113462857270763317237396988943922445621451664240254033291864131227428294853277524242407573903240321257405579568660226031904170324062351700858796178922222789623703897374720000000000000000000000000000000000000000000000000L
```
---
# Funciones matemáticas
```
>>> math.exp(1)
2.718281828459045     (Nota: Poner la notacion matematica)
>>> math.exp(0)
1.0
#Logaritmo natural base e
>>> for i in [1, 10, 100, 1000]:
...     print math.log(i)
... 
0.0
2.30258509299
4.60517018599
6.90775527898
```
----
# Funciones matemáticas
```
#Logaritmo base 2
>>> for i in [1, 2, 4, 8]:
...     print math.log(i, 2)
... 
0.0
1.0
2.0
3.0
#Logaritmo base 10
>>> for i in [1, 10, 100, 1000]:
...     print math.log(i,10), math.log10(i)
... 
0.0 0.0
1.0 1.0
2.0 2.0
3.0 3.0
```
---
# Funciones matemáticas y constantes
```
#Potencia y raiz cuadrada
>>> math.pow(2, 0.5)
1.4142135623730951
>>> math.sqrt(2)
1.4142135623730951
>>>
>>> math.e
2.718281828459045
>>> math.pi
3.141592653589793
```
---
# Acceso a archivos
```
>>> fp = open('/etc/passwd', 'ro')
>>> fp.read()
>>> fp = open('/etc/passwd', 'w')
Traceback (most recent call last):
  
File "<stdin>", line 1, in <module>
IOError: [Errno 13] Permission denied: '/etc/passwd'
>>> fp = open('/etc/shadow', 'r')
Traceback (most recent call last):
  
File "<stdin>", line 1, in <module>
IOError: [Errno 13] Permission denied: '/etc/shadow'
```
---
# Acceso a archivos
```
>>> fp = open('/etc/hosts', 'ro')
>>> for l in fp.readlines():
...     print l[:3]
... 
127
::1
#50
#12
#64
```
---
# Servicios del Sistema Operativo
```
>>> import os, sys
>>> os.name
'posix'
>>> os.uname()
('Linux', 'hormiga­gris', ..., 'x86_64')
>>> sys.platform
'linux2'
>>> 
>>> sys.version
'2.7.3 ...'
>>> sys.version_info
sys.version_info(major=2, minor=7, micro=3, ...
```
---
# Servicios del Sistema Operativo
```
>>> sys.byteorder
'little'
>>> sys.getdefaultencoding()
'ascii'
>>> sys.getfilesystemencoding()
'UTF­8'
>>> sys.maxint
9223372036854775807
>>> sys.maxsize
9223372036854775807
```
---
# Servicios del Sistema Operativo
```
Importante recordar sys.path
>>> sys.path
```
---
# Taller intensivo de Python
## La letra chiquita del contrato
---
# Algunas dificultades
* Errores y Tracebacks
* Unicode
* Hilos
---
# Errores y Excepciones
```
>>> 1/0
Traceback (most recent call last):
  
File "<stdin>", line 1, in <module>
ZeroDivisionError: integer division or modulo by zero
>>> try:
...     1/0
... except ZeroDivisionError:
...     print 'No dividas por cero. NO'
... 
No dividas por cero. NO
```
---
# Unicode
```
>>> print 'a
ñ
o 2012'
A
ñ
o 2012
>>> print u'%s 2012' %'a
ñ
o'
Traceback (most recent call last):
  
File "<stdin>", line 1, in <module>
UnicodeDecodeError: 'ascii' codec can't decode byte 0xc3 in 
position 1: ordinal not in range(128)
```
---
# Threads (GIL)
In CPython, the global interpreter lock, or
GIL, is a mutex that prevents multiple native
threads from executing Python bytecodes at
once. This lock is necessary mainly because
CPython's memory management is not
thread-safe. (However, since the GIL exists,
other features have grown to depend on the
guarantees that it enforces.)

---
# Módulos y el pythonpath
```
$ ls *.py
modulo.py
$ cat modulo.py 
simbolo = 1
def funcion():
    
print "hola"
$ python
>>> import modulo
```
---
# Módulos y el pythonpath
```
>>> import modulo
>>> modulo.simbolo
1
>>> modulo.funcion()
hola
>>> from modulo import funcion
>>> funcion()
hola
```
---
# Módulos
* Cualquier archivo .py
* Cualquier directorio con un archivo __init__.py
* Python busca módulos en el PYTHONPATH
* --> sys.path
---
# Taller intensivo de Python
## Módulos
---
# Taller intensivo de Python
## The cheeseshop: Pypi, eggs y Virtualenv
---
# PyPi
* PyPi = Python Package Index
* Miles de paquetes de software listos para ser
reusado.
---
# Setuptools vs RPM, deb, exe
* Funciona en todas las plataformas donde el paquete este soportado.
* Dependencias y versiones de paquetes.
* Reusable
---
# Eggs
* Python eggs ...
* Formato para redistribuir código fuente en python.
* Usa setuptools para definir nombre, versiones, dependencias, documentación, etc.
* Se instalan en el PYTHONPATH:
* ej. /usr/lib/python2.7/site-packages
---
# Virtualenv
* Por default, easy_install instala paquetes en /usr/lib/python2.7/site-packages (o equivalente).
* Algunos paquetes de software pueden dañar la instalación de python.
* Linux y OSX dependen de Python.
* Instalar un paquete a nivel de sistema puede dejar inoperable otros programas.
---
# Virtualenv
* Virtualenv crea un entorno aislado de Python.
* Ahi podemos instalar y probar todo tipo de librerías.
* Si el entorno virtual se daña, simplemente borramos el directorio.
* Virtualenv manipula el PYTHONPATH.
---
# Taller intensivo de Python
## ¿Dónde buscar ayuda?
---
# Documentación en línea
* http://docs.python.org/
* http://learnpythonthehardway.org/
* http://www.learnpython.org/
* http://www.greenteapress.com/thinkpython/
---
# Ayuda en español
* http://pythonmexico.org/
* http://mx.groups.yahoo.com/group/pythonmexico/
---
# Eso es todo por hoy.
Noe Nieto
nnieto@noenieto.com
http://noenieto.com
@tzicatl

---
Taller intensivo de Python
ha sido compilado
por Noe Misael Nieto Arroyo y se encuentra bajo
una Licencia
Creative Commons Atribución-
CompartirIgual
2.5 México.
