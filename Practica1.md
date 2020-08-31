
---

<center> <h1>PRACTICA 1 </h1> </center> 
<center> <h3>(Continuación semestre vía telemática)<h3> </center>

---

## INSTRUCCIONES:

- Una vez recibido esta copia digital de la práctica Ud. **Tiene 48hs a partir del momento en que este correo ha sido recibido**
- Coloque de forma clara y específica la respuesta de cada problema planteado en ***formato markdown*** justificando cada paso de su procedimiento: Análisis para resolverlo, resolución (explicación detallada y código) y análisis de resultados. Recuerde que el código deberá ser explicado ***línea por línea, o por fragmentos***(Esto para facilitar el proceso de entendimiento al lector del código), y los resultados deberán ser analizados y justificando porqué debió ser ese y no otro. 
- La resolución debe ser individual. Si dos o mas estudiantes presentan igual procedimiento y redacci ´ on en la resolución en al menos una pregunta de la práctica entonces todos los involucrados se le asignará a nota ***0 (cero)*** en la práctica. 
- Usted debe enviar su resolución vía correo electrónico, en cualquier momento antes de la fecha y hora límite. Para ello, envíe el archivo markdown nombrado de la siguiente manera: ***01.practica.Nombre.Apellido.Celuda de indentidad del estudiante***. Será enviado al correo: jgalvis414@gmail.com con el asunto del correo con el mismo nombre del archivo
- No se aceptará entregas fuera del tiempo establecido. De tener algún problema con los servicios que impidan la realización del trabajo deberán informar de inmediato al correo jgalvis414@gmail.com o al número +584242672280 explicando el problema para coordinar una posible entrega posterior.
- Todos los ejercicios deben ser ejecutados en el lenguaje de programación **Python**

---

### Ejercicio 1.

Los ***números cadena*** son creados al sumar continuamente el cuadrado de cada dígito de un número para formar otro. Por ejemplo, si se tiene el número 44, se procede a elevar cada uno de sus dígitos al cuadrado y la suma de ellos resulta en 32 <img src="https://latex.codecogs.com/gif.latex?()4^2&plus;4^2&space;=&space;16&space;&plus;&space;16&space;=&space;32)" title="()4^2+4^2 = 16 + 16 = 32)" />. Luego se hace lo mismo con el 32 <img src="https://latex.codecogs.com/gif.latex?(3^2&space;&plus;&space;2^2&space;=&space;13)" title="(3^2 + 2^2 = 13)" /> y así sucesivamente. Por ejemplo: 

<img src="https://latex.codecogs.com/gif.latex?44\rightarrow&space;32\rightarrow&space;13\rightarrow&space;10\rightarrow&space;\mathbf{1}\rightarrow&space;\mathbf{1}" title="44\rightarrow 32\rightarrow 13\rightarrow 10\rightarrow \mathbf{1}\rightarrow \mathbf{1}" />

<img src="https://latex.codecogs.com/gif.latex?85\rightarrow&space;\mathbf{89}\rightarrow&space;145\rightarrow&space;42\rightarrow&space;20\rightarrow&space;4\rightarrow&space;16\rightarrow&space;37\rightarrow&space;58\rightarrow&space;\mathbf{89}" title="85\rightarrow \mathbf{89}\rightarrow 145\rightarrow 42\rightarrow 20\rightarrow 4\rightarrow 16\rightarrow 37\rightarrow 58\rightarrow \mathbf{89}" />

Una vez que la cadena llegue a **1** u **89**, la cadena queda en un ciclo infinito como los mostrados en los ejemplos anteriores. Es interesante notar que al comenzar CUALQUIER número entero positivo, eventualmente llegará a 1 (llamado número ***feliz***) u 89 (llamado número ***infeliz***)

Diseñe un programa que permita conocer todos los números felices e infelices desde el 1 hasta un **N** (leído como dato). Pruebe con mínimo 2 ejemplos.

**(5ptos)**

---

### Ejercicio 2.

Un caracol cae en un pozo de **H** metros de profundidad. Este caracol durante el día
asciende una distancia **Ld** metros, pero durante la noche, al quedarse dormido,
resbala y desciende **Ln** metros. Diseñe un programa que simulando el movimiento
del animalito, determine en cuánto tiempo sale del pozo (si es que esto sucede). 


Muestre un ejemplo en la cual el caracol salga del pozo, y otro donde esto no suceda

**(3ptos)**

---

### Ejercicio 3.

Realice un programa que genere la suma dada por la siguiente serie:

<img src="https://latex.codecogs.com/gif.latex?S&space;=&space;(1-x)^{2}-\frac{(1-x)^{4}}{3!}&plus;\frac{(1-x)^{6}}{5!}-\frac{(1-x)^{8}}{7!}&plus;..." title="S = (1-x)^{2}-\frac{(1-x)^{4}}{3!}+\frac{(1-x)^{6}}{5!}-\frac{(1-x)^{8}}{7!}+..." />

Como condiciones debe verificar que se cumpla que el valor de **x** leída como dato sea **0<x<1**. Obligatoriamente debe generar el término **N-ésimo* a partir del termino anterior (en este caso como una unidad y no viéndolo como la generación del numerador y el denominador por serparado) y detenga el cálculo cuando el último término, en valor absoluto, sumado sea menor que una tolerancia dada.

**(7ptos)**

---

### Ejercicio 4.

La búsqueda (o método) de la **Sección dorada** es una técnica para hllar el extremo (mínimo o máximo) de una función unimodal, mediante reducciones sucesivas del rango de valores en el cual se conoce que se encuentra extremo. Diseñar un programa que contenga una función que calcule **máximo** de una función, Use: $f(x)= e^{x} + sen(x)$ por método de la **Sección dorada**, dado un intérvalo inicial de búsqueda (A,B).

Dicho método se basa en calcular dos puntos **L** y **M** interiores al intervalo (A,B) tales que: 

<img src="https://latex.codecogs.com/gif.latex?L&space;=&space;A&space;&plus;&space;0,382(B-A)$&space;y&space;$M&space;=&space;A&space;&plus;&space;0,618&space;(B&space;-A)" title="L = A + 0,382(B-A)$ y $M = A + 0,618 (B -A)" />

Si <img src="https://latex.codecogs.com/gif.latex?f(L)>f(M)" title="f(L)>f(M)" />entonces 
<img src="https://latex.codecogs.com/gif.latex?A&space;=&space;L;\;&space;\;&space;L&space;=&space;M&space;\;&space;\;&space;y&space;\;&space;\;&space;M&space;=&space;A&space;&plus;&space;0,618(B-A)" title="A = L;\; \; L = M \; \; y \; \; M = A + 0,618(B-A)" />


En caso contrario <img src="https://latex.codecogs.com/gif.latex?B&space;=&space;M;&space;\;&space;\;&space;M&space;=&space;L;&space;\;&space;\;&space;y&space;\;&space;\;&space;L&space;=A&plus;0,382(B-A)" title="B = M; \; \; M = L; \; \; y \; \; L =A+0,382(B-A)" />

El proceso se repite hasta que $(B-A) <$ ***Error***, donde ***Error*** es leído como dato. 

**(5ptos)**
