# 2.3 Arreglos

## Definición formal

Los arreglos son estructuras muy sencillas pero útiles y ampliamente utilizadas. Para definirlos adoptaremos dos enfoques, uno formal y otro más práctico. Este último, asociado al uso conceptual de la memoria, nos permitirá comprender el costo computacional de sus operaciones usuales.  <br>
Formalmente un arreglo se puede definir como una función de la siguiente manera: 

<div align="center">
<img src="images/def1.jpg" alt="definición de arreglos" width="700">
</div>


En este sentido, un arreglo bidimensional *B* de enteros, de tamaño 7 x 5, sería una función *B: I -> Int* donde *I* es el producto cruz: 

<div align="center">
<img src="images/prodi1.jpg" alt="producto cruz I" width="250">
</div>

Y, por ejemplo, el elemento B[1][2], en realidad es la función B evaluada en el vector i =(1,2), es decir B(i) = B(1,2) = B[1][2]:

<div align="center">
<img src="images/arr1.jpg" alt="Arreglo bidimensional con la celda (1,2) resaltada" width="250">
</div>

El primer índice (en este caso el 1) nos indica un desplazamiento por la dimensión 1 que mide $n_1=7$, mientras que el segundo índice (en este caso 2) indica cuántas columnas desplazarse a la derecha, es decir, indica un desplazamiento por la dimensión 2, que mide $n_2=5$.  

## Memoria 
Fuera de la disposición física de la memoria en nuestra computadora, como programadores, estamos acostumbrados a imaginarla como un arreglo unidimensional de celdas con tamaño de 1 byte = 4 bits. Cada celda esta asociada a una dirección $m$ que pertenece a un espacio de direcciones predefinido $m \in [0,M)$. 

<div align="center">
<img src="images/memoria.jpg" alt="Arreglo bidimensional con la celda (1,2) resaltada" width="600"> 
</div>

## Definición práctica
Esta definición se dividirá en tres partes, asumiendo que *X* es algún tipo de dato cuyo tamaño sea *k* bytes:
 - **Celda de tipo X**: Es un espacio contiguo en memoria cuyo tamaño
 - **Arreglo unidimensional de tipo X**: Es una colección de $n$ celdas consecutivas de tipo X accesibles mediante un índice $i \in \{0, 1, \ldots, n\}$
 - **Arreglo multidimensional de tipo X y dimensión d**:
     - Si $d = 1$, se trata de un arreglo unidimensional de tipo X.
     - Si $d > 1$, es un arreglo de arreglos multidimensionales de dimensión $d - 1$.
   
## Polinomio de direccionamiento 

### De la posición de un arreglo hacia la posición efectiva en memoria
En lenguajes como Fortran o Pascal todo arreglo, multidimensional o no, se almacenaba en memoria como un arreglo unidimensional. En este contexto el compilador tenía que calcular la posición en memoria, también conocida como la **posición efectiva** de una celda en particular. 

Por ejemplo, si tuviéramos un arreglo unidimensional $C$ de tamaño $n = 9$ y tipo entero (Int). Considerando la celda $C[4]$, para calcular su posición efectiva $pC[4]$ de la celda, a sabiendas de que la dirección en memoria del arreglo $C$ es $dir(C)$:

<div align="center">
<img src="images/arr2.jpg" alt="arreglo unidimensional C" width="500">
</div>

simplemente tenemos que hacer las siguientes operaciones: 

$$
p(C[4]) = dir(C) + tamaño(Int) \cdot 4 = dir(C) + 4\cdot 4
$$

Recordemos que el tamaño de un dato de tipo Int es de cuatro bytes, por ello es que $tamaño(Int) = 4$. En general para calcular la posición efectiva de una celda C[i] de tipo $X$ es:

$$
p(C[i]) = dir(C) + tamaño(X) \cdot i
$$

Este es nuestro **polinomio de direccionamiento**, una transformación lineal que a partir del índice de una celda nos permite conocer su posición efectiva en memoria. 

### Desde un arreglo multi-dimensional hacia su posición efectiva en memoria
Ahora supongamos que nuestro arreglo $C$ es bidimensional, de tamaño $n = 7 \times 5$ y queremos conocer la posición efectiva de la celda $C[4][3]$ en memoria:

<div align="center">
<img src="images/arr3.jpg" alt="arreglo C bidimensional con celda E[4][3] resaltada" width="550">
 
</div>

Observemos que $i_1 = 4$ y que $i_2 = 3$. La primer entrada de nuestro vector de índices $i_1$ nos dice cuántos renglones bajar. Como cada renglón tiene $n_2 = 5$ celdas, entonces debemos multiplicar $i_1 \cdot n_2 = 4 \cdot 5 = 20$. Esto quiere decir que la dirección en memoria de  


Antes de abordar la versión generalizada del polinomio de direccionamiento veamos un último ejemplo. Esta vez pediremos que $C$  sea un arreglo tridimensional, de tamaño $n = 7 \cdot 5 \cdot 3$, y de tipo Int. Supongamos que, dada la celda $C[5][5][1]$: 

<div align="center">
<img src="images/arr4.jpg" alt="Arreglo tridimensional en su versión prisma" width="450">
 
</div>

que también podemos visualizar de la siguiente manera,

<div align="center">
<img src="images/arr5.jpg" alt="arreglo C tridimensional conceptualizado como arreglo de arreglos" width="500">
 
</div>

en un arreglo de arreglos de arreglos; y que queremos encontrar su posición efectiva en nuestra memoria, que, como habíamos dicho, puede conceptualizarse como un arreglo unidimensional. <br>
En este caso debemos multiplicar la primer entrada de nuestro vector de índices $i_1 = 5$ por el producto de los tamaños de las dimensiones siguiente $n_2 \times n_3$. Posteriormente debemos multiplicar 

### Polinomio generalizado
Retomando nuestros conceptos de la definición con la que comenzamos esta atención 

## Operaciones con arreglos 
Los arreglos son estructuras estáticas, esto quiere decir que una vez reservada la memoria y asignadas sus celdas a valores específicos, 
obtendremos una estructura que no cambiará en tiempo de ejecución. <br>

La principal desventaja es que tanto borrar un elemento como aumentar el tamaño de un arreglo dado tomará tiempo lineal $O(n)$ con $n$ el tamaño del arreglo. En el primer caso, supongamos que tenemos un arreglo $A$ de dimensión $d$, y tamaño $n$. <br> 
Para borrar el elemento de una celda, digamos $A[i]$, tendremos que reemplazarlo por el contenido de la celda $A[i+1]$. A su vez, el contenido de la celda $A[i+2]$ debe reemplazar al contenido de la celda $A[i + 1]$ y así sucesivamente hasta que reemplacemos el contenido de la celda $A[n-2]$ por el contenido de la celda $A[n-1]$. En total habremos hecho $(n-1) - (i + 1) + 1 = n - i - 1$. En caso de que  operaciones de copia  consideramos eliminar el contenido de la celda A[0] entonces haríamos $n - 1$ operaciones. <br>
Ahora bien, si queremos aumentar el tamaño del arreglo, $A$ de tipo $X$ y tamaño $n$, al tamaño $n + k$, tenemos que reservar nuevo espacio en la memoria y copiar los $n$ elementos almacenados, operación que tiene un orden lineal O(n).


## Arreglos escalonados
Al definir un arreglo multidimensional de dimensión $d$ en Java y otros lenguajes modernos, podemos posponer la inicialización de algunos de los subarrejlos de dimensión $d - k$ con $k \in \{1,\ldots,d-1\}$:

```
int [][][]

```


