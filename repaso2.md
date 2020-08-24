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


