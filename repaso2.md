# UCV-FI-0790-2019-3-06

Bienvenidos a la segunda lectura de repaso de la cátedra de Programación (0790), en esta repasaremos los tópicos ya vistos durante clases y reforzaremos el conocimiento con algunos problemas resueltos.

# Repaso 2

## Operadores (Relación y Lógicos)

En el repaso anterior estuvimos trabajando con operadores aritméticos, para este repaso trabajaremos con mas operadores, en especifico con los operadores de relación y los operadores lógicos.

## Operadores de Relación

Ademas de poder realizar operaciones aritméticas entre variables y sus tipos de datos, podemos también realizar operaciones donde se relacionan los valores de las variables o de los literales.

Los operadores relacionales disponibles en el lenguaje de programación Python son los siguientes:

Operador | Nombre | Ejemplo
---------|--------|--------
== | Igualdad | i == j
!= | Desigualdad | i != j
> | Mayor que | i > j
< | Menor que | i < j
>= | Mayor o igual que | i >= j
<= | Menor o igual que | i <= j

Estos operadores al ser evaluados arrojan como resultado una expresión de tipo booleana (Verdadero o False), *True* ó *False*, que es utilizada para ser almacenada en una variable, o como la expresión de evaluación de una estructura *if* ó *while*, entre algunas de sus aplicaciones.

Hagamos algunos ejemplos:

```python
>>> 4 > 5
False
>>> 4.0 == 4
True
>>> a = 12
>>> b = 13
>>> a <= b
True
>>> b <= 5.67
False
```

Los resultados de estas relaciones pueden ser almacenadas en una variable para su posterior uso.

```python
>>> c = a == b
>>> c
False
```

## Operadores de Lógicos

Adicionalmente podemos hacer composiciones de relaciones, es decir, aquellas operaciones donde tenemos que relacionar mas de dos variables, al igual que las operaciones aritméticas, estas se componen usando los paréntesis *()* para asi agrupar relaciones, y entre agrupaciones podemos aplicar los siguientes operadores lógicos.

Operador | Nombre | Ejemplo
---------|--------|--------
and | Inclusión | (i > j) and (k == z)
or | Or | (i > j) and (k == z)
! | Negación | !(i > j)

Ademas de agrupaciones podemos aplicar los operadores lógicos entre variables booleanas, o una combinación de relaciones con variables booleanas.

## Entrada y Salida

El computador nos permite a través del Lenguaje de Programación, realizar el computo de un algoritmo para resolver un determinado problema, por lo general los algoritmos requieren una información conocida como datos de entrada, y el computo determina una información que requieren ser mostrados en pantalla, conocida como datos de salida.

La entrada de información se puede realizar en pantalla durante la ejecución de un programa, a través del comando *input*, donde el programa se interrumpe a la esperada de la entrada de información por el usuario.

```python
>>> edad = input("Edad? ")
Edad? 31
>>> edad
'31'
```

El comando o función incorporada *input*, permite suministrar un mensaje al usuario, este mensaje por lo general corto, da una idea al usuario de la información que requiere el programa para realizar los cómputos, otros usos de este comando es imprimir en pantalla información adicional como ayuda o una marquesina del programa.

En el ejemplo anterior, al mostrar la representación de la variable edad, vemos que el valor es *'31*', el mismo que hemos suministrado pero entre comillas simples, queriendo decir que la entrada fue interpretada como una cadena de caracteres.

Si requerimos para nuestro computo, realizar operaciones algebraicas sobre este dato de entrada, debemos transformar de cadena de caracteres a entero como tipo de dato.

Python nos ofrece una serie de funciones incorporadas para transformar entre tipo de datos.

Función | Acción | Ejemplo
--------|--------|--------
int | Transforma una variable o literal a entero | int(i)
float | Transforma una variable o literal a flotante | float(i)
str | Transforma una variable o literal a *str* o cadena de caracteres | str(i)

Adicionalmente podemos encapsular una función incorporada dentro de otra, para asi ahorrar algo de código, Python realizara las evaluaciones desde la mas interna hasta la mas externa.

```python
>>> edad_str = int(input("Edad? "))
Edad? 31
>>> edad
31
```

La salida de información se puede realizar en pantalla durante la ejecución de un programa, a través del comando *print*, donde el programa imprimirá en consola la información que proveamos como argumento de la función *print*.

```python
>>> print("Hola mundo")
Hola mundo
```

En la función *print*, podemos agregar tanta información como queramos separando con el separador de argumentos *,*.

```python
>>> faltante = 40 - edad
>>> print("Te falta", faltante, "años para cumplir 40")
Te falta 9 años para cumplir 40
```

Al usar de esta forma la función *print*, Python se encargara de convertir cada tipo de dato en su equivalente en cadena de caracteres, y finalmente concatenara separando con espacios.

## Nuestro primer algoritmo de computo

Una vez que conocemos estos elementos esenciales 
