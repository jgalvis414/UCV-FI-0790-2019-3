# UCV-FI-0790-2019-3-06

Bienvenidos a la primera lectura de repaso de la cátedra de Programación (0790), en esta repasaremos los tópicos ya vistos durante clases y reforzaremos el conocimiento con algunos problemas resueltos.

# Repaso 1

## Lenguajes de Programación

Cuando construimos un algoritmo de computo, requerimos de alguna forma comunicarle a un computador los pasos y/o instrucciones de este algoritmo, para esto se implementa un lenguaje de programación el cual puede ser entendido por el computador, estos lenguajes análogos a los lenguajes hablados por los humanos, tienen una sintáctica que siguen algunas reglas para definir lo que queremos expresar mediante ese lenguaje.

Este repaso de programación cubrirá estas reglas básicas y generales para construir mediante un lenguaje de programación un algoritmo de computo típico encontrado en problemas de programación.

## Python

El lenguaje seleccionado para este repaso es el lenguaje de programación Python, creado por [Guido Van Rossum](https://gvanrossum.github.io/) en 1989. Siendo unos de los lenguajes mas populares y con mas aplicaciones en la industria, también es el lenguaje con mejor curva de aprendizaje. He seleccionado este lenguaje precisamente por esta característica, el mismo permitirá al aprendiz manejar de forma oportuna los conceptos fundamentales de programación.

### Instalación y Ejecución de Python

Python puede ser descargado de su pagina oficial [Python](https://www.python.org/), para cada sistema operativo respectivamente. Para su ejecución basta con ir al terminal del sistema operativo y ejecutar la siguiente instrucción

```
> python
Python 3.7.4 (tags/v3.7.4:e09359112e, Jul  8 2019, 20:34:20) [MSC v.1916 64 bit
(AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

Un programa de interfaz de linea de comandos se ejecuta, el cual nos permite realizar e introducir comandos e instrucciones de Python directamente, intentemos introducir algunos comandos:

```python
>>> 4 + 10
14
>>> 12 - 15
-3
>>> "hola" + " mundo"
'hola mundo'
>>> 101 > 100
True
>>>
```
## Variables y Tipos de Datos

El computador es una maquina que tiene como principio realizar dos cosas, almacenar información y realizar cálculos de una forma muy rápida, hoy en dia los computadores han evolucionado a tal punto de que podemos tener un sistema de computo del tamaño de un reloj, el cual esta programado para realizar interacción con las personas mediante muchas herramientas también programadas, no obstante, sigue siendo una maquina que almacena información y realiza cálculos de una forma muy rápida.

La forma en que un computador almacena la información es a través de la implementación física de *bit* y *byte*, donde un bit es la unidad de información mínima el cual solo representa dos estados, activado y desactivado, *1* o *0*, pero la agrupación de varios bits y sus posibles combinaciones nos permiten hacer otras representación, como números o letras. La agrupación por defecto utilizada en sistemas de computo es el byte, el cual es una agrupación de 8 bits. Entonces si tenemos 8 elementos los cuales cada uno puede representar dos valores distintos, cuantos valores distintos en total podemos representar en un byte?. Esto es un problema clásico de variaciones con repetición, la formula m^n nos permite determinar esto.

```python
>>> 2 ** 8
256
```

El operador ****, es el operador de potencia, eleva la base *2* a su *8*va potencia.

Como podemos observar, es posible representar 256 valores distintos en un byte, los sistemas de computo puede almacenar en un byte números enteros en 0 y 255, o entre -127 a 128, pero recordemos que un byte es solo una secuencia de 8 bits, combinaciones de unos o ceros a los cuales les hemos asignado un equivalente numérico, pero también podemos hacer lo mismo para el alfabeto, actualmente esta representación ya existe, cada carácter que puede ser introducido, almacenado y/o procesado en un sistema de computo sigue el standard [ASCII](https://es.wikipedia.org/wiki/ASCII).

Binario | Dec | Hex | Represetación
--------|-----|-----|--------------
0100 0000 |	64 | 40 | @
0100 0001 |	65 | 41 | A
0100 0010 |	66 | 42 | B
0100 0011 | 67 | 43 | C
0100 0100 |	68 | 44 | D
0100 0101 | 69 | 45 | E
0100 0110 | 70 | 46 | F
0100 0111 | 71 | 47 | G
0100 1000 | 72 | 48 | H
0100 1001 |	73 | 49 | I
0100 1010 | 74 | 4A | J
0100 1011 |	75 | 4B | K
0100 1100 |	76 | 4C | L
0100 1101 |	77 | 4D | M
0100 1110 |	78 | 4E | N
0100 1111 |	79 | 4F | O
0101 0000 |	80 | 50 | P
0101 0001 |	81 | 51 | Q
0101 0010 |	82 | 52 | R
0101 0011 |	83 | 53 | S
0101 0100 | 84 | 54 | T
0101 0101 |	85 | 55 | U
0101 0110 |	86 | 56 | V
0101 0111 |	87 | 57 | W
0101 1000 |	88 | 58 | X
0101 1001 |	89 | 59 | Y
0101 1010 |	90 | 5A | Z

En esta tabla, podemos ver algunos de los caracteres ASCII, el alfabeto en mayúscula, y como el mismo es representado mediante bytes, en la primera columna podemos observar las distintas combinaciones de bits para formar el carácter especificado, y también podemos ver su equivalente en representación decimal y hexadecimal, la conveniencia de esta ultima representación es que podemos usar dos caracteres para representar un byte.

Aunque hoy en dia no tratamos directamente con el sistema binario para programar un algoritmo de computo, es necesario entender como el computador almacena nuestra información, hoy en dia los lenguajes de programación nos permiten representar la información mediante tipos de datos y ser almacenados en un bloque de memoria al cual se le asigna un nombre que lo identifica, esto es lo que conocemos en programación como variable.

En la tabla ASCII podemos ver que podemos almacenar tres tipos de datos distintos, un carácter o serie de caracteres, a esto se le conoce como *string*, un numero, o un hexadecimal.

Los tipos de datos básicos que podemos representar en Python son los siguientes.

Tipo | Nombre
-----|-------
Entero | int
Flotante | float
Complejo | complex
Cadena de Caracteres | string
Lista | list
Tupla | tuple
Diccionario | dict

Veamos algunos ejemplos

```python
>>> 256
256
>>> 3.1416
3.1416
>>> 1 + 2j
(1+2j)
>>> "Hola Mundo"
'Hola Mundo'
>>> [4, 3, 2, 1]
[4, 3, 2, 1]
>>> (4, 3, 2, 1)
(4, 3, 2, 1)
>>> {1: "uno", 2: "dos", 3: "tres"}
{1: 'uno', 2: 'dos', 3: 'tres'}
```
Introducir un valor directamente implementado su tipo de dato en un lenguaje de programación, se le conoce como literal. El ejemplo anterior se muestran casos de literales correspondientes a la tabla anterior. 

Como nota adicional, en los literales para cadena de caracteres pueden usarse tanto comillas dobles como comillas simples.

## Operadores (Asignación)

## Operadores (Aritméticos y Lógicos)

## Estructuras (Estructura Condicional - If)