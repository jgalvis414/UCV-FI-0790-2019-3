# UCV-FI-0790-2019-3-06

Bienvenidos a la tercera lectura de repaso de la cátedra de Programación (0790), en esta repasaremos los tópicos ya vistos durante clases y reforzaremos el conocimiento con algunos problemas resueltos.

# Repaso 2

## Estructuras de Ciclos (*while*)

Durante la codificación de un algoritmo, a veces requerimos realizar tareas repetitivas mientras se mantenga una condición o no, un ejemplo de esto tipo de tareas las vemos muy a menudo en nuestras vidas, por ejemplo, si vamos caminando, caminamos mientras no hayan obstáculos en el camino, una vez conseguido un obstáculo nos detenemos, esto aunque parezca algo trivial para una computadora debe ser especifico.

La estructura de ciclo *while* nos permite definir un conjunto de sentencias o instrucciones *Python* de forma repetitiva, con el propósito de determinar la solución a un problema si esta solución existe, esto es importante ya que si un determinado programa no encuentra una soluciones dentro de un numero establecido de repeticiones debe dar como respuesta que ha fallado, asi evitaremos ejecuciones de ciclos infinitos en nuestro programa.

Veamos esta estructura en código *Python*:

```python
while (expresion):
    instruccion_1
    instruccion_2
    instruccion_3
```

Hay unos aspectos importantes que resaltar en esta estructura, el primero es que se usa la palabra reservada *while* del lenguaje de programación, el segundo es que debemos encapsular dentro de paréntesis (en caso de ser necesarios) una expresión de relación y/o lógica, en caso de que esta evaluación de como resultado *verdadero*, se procede a las instrucciones correspondientes. Estas instrucción realizan los cómputos que requiere el algoritmo, y se vuelven a repetir mientras aun la expresión siga dando como resultado verdadero. Esto indica que dentro de nuestra expresión, la cual también indirectamente es una condición de parada, debe contener una variable o juegos de variables, que sean actualizadas dentro de las instrucciones para que al ser evaluadas nuevamente dentro de nuestra expresión, den un resultado final de *falso*, y la ejecución del *while* se interrumpe, prosiguiendo el programa a las siguientes instrucciones.

<script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=default'></script>

$$ {J(\theta) =\frac{1}{2m} [\sum^m_{i=1}(h_\theta(x^{(i)}) - y^{(i)})2 + \lambda\sum^n_{j=1}\theta^2_j} $$



