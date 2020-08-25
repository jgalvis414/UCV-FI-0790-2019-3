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

Una vez que conocemos estos elementos esenciales podemos construir los primeros algoritmos de computo.

Problema propuesto: Desarrolle un algoritmo que determine la hipotenusa de un triangulo rectángulo dado la longitud de los catetos del angulo recto.

```python
>>> a = int(input("Introduzca cateto adyacente: "))
Introduzca cateto adyacente: 3
>>> b = int(input("Introduzca cateto opuesto: "))
Introduzca cateto opuesto: 4
>>> c = (a ** 2 + b ** 2) ** 0.5
>>> print("Longitud de la hipotenusa:", c)
Longitud de la hipotenusa: 5.0
```

Hasta ahora hemos recopilado los elementos básicos para hacer algoritmos de computo donde se evalúen expresiones algebraicas, pero muchos algoritmos requieren de procedimientos donde se realicen selecciones, tratamiento condicional y también que se repitan tareas u otros procedimientos un numero determinado de pasos o hasta que se cumpla una condición.

Para esto los lenguajes de programación propones estructuras cuya sintética permiten llevar a cabo este tipo de operaciones algorítmicas.

## Estructura Condicional (Sentencia *if*)

Muy a menudo requerimos llevar la ejecución de un algoritmo a través de una ruta o otra dependiendo de si una condición se cumple o no, en los lenguajes de programación estas condiciones se expresan con operaciones de relación, operaciones lógicas o una combinación de estas. Recordemos que el resultado de estas operaciones son valores booleanos que se interpretan como verdadero o falso, para una condición representa que la condición se cumple (*True*) o no se cumple (*False*).

Las operaciones que se realizan en base al valor bien sea verdadero o falso, se pueden separar y tratar mediante la sentencia *if*, la cual tiene la siguiente sintáctica.

```python
if (expresion):
    instruccion_1
    instruccion_2
    instruccion_3
```

Hay unos aspectos importantes que resaltar en esta estructura, el primero es que se usa la palabra reservada *if* del lenguaje de programación, el segundo es que debemos encapsular dentro de paréntesis (en caso de ser necesarios) una expresión de relación y/o lógica, en caso de que esta evaluación de como resultado verdadero, se procede a las instrucciones correspondientes. Un tercer aspecto es que este tipo de estructura tienen un código asociado que debe estar contenido dentro de un bloque de instrucciones, estos bloques se definen en un principio por el símbolo *:*, para indicar que inicia un bloque de instrucciones, de aquí en adelante todas las instrucciones asociadas a dicho bloque deben estar identadas (tabulaciones o espacios), con respecto al bloque anterior, se recomienda que para Python, cada identación sea de 4 espacios, una vez finalizado el bloque se regresa al bloque anterior reduciendo la identación. Veamos el siguiente ejemplo.

```python
print("***Inicio del programa***")

edad = int(input("Introduzca edad: "))

if (edad > 18):
    print("Es mayor de edad, puede entrar al establecimiento")

print("***Fin del programa***")
```

Si ejecutamos este programa, tendríamos los siguientes posibles resultados.

```python
***Inicio del programa***
Introduzca edad: 12
***Fin del programa***
```

```python
***Inicio del programa***
Introduzca edad: 21
Es mayor de edad, puede entrar al establecimiento
***Fin del programa***
```

Como podemos observar, dependiendo del valor que hayamos introducido, una linea extra se imprime en pantalla, debido a que se ejecuta una instrucción dentro del bloque de una sentencia *if*, cuyo resultado de la expresión de relación dio como verdadero.

También podemos ejecutar código cuando el resultado el falso usando el bloque de la palabra reservada *else*.

```python
print("***Inicio del programa***")

edad = int(input("Introduzca edad: "))

if (edad > 18):
    print("Es mayor de edad, puede entrar al establecimiento")
else:
    print("Es menor de edad, no puede entrar")

print("***Fin del programa***")
```

## Modulo de Python

Finalmente, debemos tener la posibilidad de poder ejecutar un programa cuantas veces sea necesario, para esto se definen los módulos de Python, los cuales son ficheros del sistema operativo donde podemos almacenar nuestro código, estos ficheros son escritos en formato de texto pero se guardan con extension *.py*. Podemos utilizar cualquier editor de texto para escribir nuestro código en Python y guardarlo bajo un nombre de archivo con extension Python, ejemplos *edad.py*.

Y la manera de ejecutar estos módulos es a través de la terminal del sistema operativo, navegando al mismo directorio donde reside el modulo ya guardado, y ejecutando el comando *python* seguido del nombre del fichero.

```
> python edad.py
```

Aunque podemos utilizar cualquier editor de texto, es recomendable usar uno que sea apropiado para el desarrollo, las ventajas principales es que estos editores hacen un resaltado de la sintáctica de Python, colocando colores especiales en las palabras reservadas como también en otros elementos del lenguaje para su fácil comprensión.

Los editores mas utilizados actualmente son Visual Studio Code, Sublime Text y Atom. El estudiante de este curso puede utilizar aquel editor con el cual se sienta mas comodo.
