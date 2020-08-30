# UCV-FI-0790-2019-3-06

Bienvenidos a la tercera lectura de repaso de la cátedra de Programación (0790), en esta repasaremos los tópicos ya vistos durante clases y reforzaremos el conocimiento con algunos problemas resueltos.

# Repaso 3

## Estructuras de Ciclos (*while*)

Durante la codificación de un algoritmo, a veces requerimos realizar tareas repetitivas mientras se mantenga una condición o no, un ejemplo de esto tipo de tareas las vemos muy a menudo en nuestras vidas, por ejemplo, si vamos caminando, caminamos mientras no haya obstáculos en el camino, una vez conseguido un obstáculo nos detenemos, esto aunque parezca algo trivial para una computadora debe ser especifico.

La estructura de ciclo *while* nos permite definir un conjunto de sentencias o instrucciones *Python* de forma repetitiva, con el propósito de determinar la solución a un problema si esta solución existe, esto es importante ya que si un determinado programa no encuentra una solución dentro de un numero establecido de repeticiones debe dar como respuesta que ha fallado, asi evitaremos ejecuciones de ciclos infinitos en nuestro programa.

Veamos esta estructura en código *Python*:

```python
while (expresion):
    instruccion_1
    instruccion_2
    instruccion_3
```

Hay unos aspectos importantes que resaltar en esta estructura, el primero es que se usa la palabra reservada *while* del lenguaje de programación, el segundo es que debemos encapsular dentro de paréntesis (en caso de ser necesarios) una expresión de relación y/o lógica, en caso de que esta evaluación de como resultado *verdadero*, se procede a las instrucciones correspondientes. Estas instrucciones realizan los cómputos que requiere el algoritmo, y se vuelven a repetir mientras aun la expresión siga dando como resultado verdadero. Esto indica que, dentro de nuestra expresión, la cual también indirectamente es una condición de parada, debe contener una variable o juegos de variables, que sean actualizadas dentro de las instrucciones para que, al ser evaluadas nuevamente dentro de nuestra expresión, den un resultado final de *falso*, y la ejecución del *while* se interrumpe, prosiguiendo el programa a las siguientes instrucciones.

Ahora resolvamos el siguiente problema:

La siguiente serie infinita permite determinar el número de Euler:

![numero euler](https://github.com/carrasquel/UCV-FI-0790-2019-3/raw/master/ecuaciones/euler.png "Numero euler")

Realice un programa en Python para determinar el resultado de esta serie y por consiguiente el numero de Euler.

Solución:

Algo que resaltar en esta serie es que no tiene fin, dado que el número de Euler es un numero irracional, mientras más términos usemos de la sumatoria más precisos seremos en el cálculo de este número.

Lo cual conlleva a establecer cuantos términos de esta sumatoria vamos a utilizar, pero dado que nuestra expresión va a servir de condición de parada para finalizar, establezcamos un criterio que es ampliamente usado en los cómputos científicos, y es el criterio de *tolerancia*.

Si observamos nuestra serie, cada resultado de la siguiente sumatoria da un numero más pequeño, supongamos que para los efectos de nuestros cálculos queremos tener una precisión de 6 decimales, entonces nuestra tolerancia será de 1.0e-7.

Veamos esta codificación en Python:

```python
# euler.py

tol = 1.0e-7

contador = 1
denominador = contador
termino = 1 / denominador
resultado = 1 + termino

while termino > tol:

    contador += 1
    denominador *= contador
    termino = 1 / denominador
    resultado += termino

print("Numero Euler:", resultado)
```

Sí ejecutamos este módulo veremos con resultado en pantalla lo siguiente:

```python
Numero Euler: 2.718281826198493
```

Algo que debemos resaltar de nuestro código, es que antes de ejecutar nuestra estructura *while* debemos establecer que variables tienen interacción dentro de la estructura, y si las mismas variables tienen valores iniciales o no, que deben ser asignados antes, esto se conoce como *inicialización*. Para nuestro código hemos establecido tres 4 variables.

Nombre | Propósito
-------|----------
contador | La idea de esta variable es incrementar en cada ciclo ya que en la definición de nuestra ecuación observamos que existe un valor que va incrementándose, el cual es el último término de la multiplicación en el denominador.
denominador | Como el denominador de nuestra ecuación siempre es un producto, observamos que los productos de los siguientes términos guardan una relación con el termino anterior, lo cual nos permite reusar esta variable para estos cómputos.
termino | En esta variable almacenaremos el valor de cada termino a medida que vamos calculando nuestra serie, esta variable es importante para detener el ciclo *while*, ya que al tener siempre valores cada vez más pequeños, eventualmente su valor va a ser menor al valor de la tolerancia, y se finalizara la ejecución del ciclo *while*.
resultado | finalmente tenemos esta variable que va a ir sumándose a ella, al igual que nuestra serie, el resultado de cada termino, y finalmente poder mostrar en pantalla el resultado de este computo.

Realicemos otro problema:

El Valor de PI (𝜋) puede ser calculado de diferentes formas, una de ellas es empleando la expresión abajo indicada:

![numero pi](https://github.com/carrasquel/UCV-FI-0790-2019-3/raw/master/ecuaciones/pi.png "Numero pi")

Vamos a usar un enfoque muy similar al problema anterior para resolver este problema:

```python
# pi.py

tol = 1.0e-7

contador = 1
denominador = (contador) ** 2 * (contador + 1) ** 2 * (contador + 2) ** 2
termino = 1 / denominador
resultado = termino

while termino > tol:

    contador += 1
    denominador = (contador) ** 2 * (contador + 1) ** 2 * (contador + 2) ** 2
    termino = 1 / denominador
    resultado += termino

resultado = ((resultado * 16 + 39) / 4) ** 0.5

print("Numero Pi:", resultado)
```

Sí ejecutamos este módulo veremos con resultado en pantalla lo siguiente:

```python
Numero Pi: 3.14159251116778
```

## Modulos Incorporados de Python

Python posee muchos módulos con funciones y variables que nos permiten reducir nuestro código a la hora de realizar ciertos cómputos. Si requerimos de computar el valor de Pi, con Python podemos obtenerlo a partir del módulo math.

Los módulos incorporados pueden ser usados en nuestro código usando la palabra reservada *import* del lenguaje de programación.

```python
>>> import math
>>> math.pi
3.141592653589793
>>> math.e
2.718281828459045
>>> math.sin(0.75)
0.6816387600233341
```

Algo que resaltar es que al importar un módulo, podemos usar todas las funcionalidades que están agrupadas dentro del módulo incorporado. Si por el contrario solo queremos utilizar algunas pocas podemos usar la forma de importación alternativa usando la palabra reservada *from* del lenguaje de programación.

```python
from math import sin, cos
>>> sin(0.75)
0.6816387600233341
>>> cos(0.75)
0.7316888688738209
```

A lo largo de este curso utilizaremos otras funcionalidades de los distintos módulos incorporados dentro de Python.


