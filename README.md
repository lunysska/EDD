# EDD
## Curso de Estructuras de Datos con Java.

1. Motivación
2. Introducción
3. TDA
   (El ejemplo de booleano)
5. El tiempo de ejecución de un programa
   5.1 Un ejemplo de varios algoritmos resolviendo el mismo problema
   El tiempo de ejecucion de un programa. Tomando los tiempos del reloj de la compu.
   Como se grafican para comparar los tiempos de k programas diferentes
   Consideramos los supuestos bajo los cuales ese metodo funciona. E hicimos conclusiones pertinentes
   El tiempo de ejecucion de algoritmos secuenciales, condicionales y ciclos
   La importancia de resolver las series en lugar de reducir a una polinomica
7. Introducción a la complejidad de algoritmos
   defincion de o-grande
   las reglas de la suma y el producto
8. Recursión
   Cálculo de complejidad para algoritmos recursivos
9. Estructuras de datos
   Definicion. operaciones y su clasificaciòn.    
10. Arreglos  




Este curso forma parte de los complementos a desarrollar para el curso de Estructuras de Datos para la carrera de Ciencias de la Computación, para la Facultad de Ciencias, UNAM.

### Complejidad, TDA, Arreglos y Recursión

### Fechas
Fecha de inicio:  1 de Marzo de 2023
Fecha de fin: 15 de Marzo de 2023

### Lineamientos
1. Debe ser entregada a mano, con letra legible, con formato LEGIBLE (no escribir
en las orillas de las hojas, ni usar lápiz), y mucha limpieza, aunque sea a mano, no
quiere decir que no sea formal.
2. La elaboración es individual.
3. Sólo se reciben las tareas hasta el último día marcado, antes de las 11:59 pm

### Formato de Entrega
1. Genere un directorio principal con nombre "suNombreSuApellido", ejemplo: "VirginiaTeodosio"
2. Dentro del directorio principal, cree otro directorio con nombre "TareaExamen"
3. Cree un documento pdf con todas sus respuestas, incluido en la parte superior, su nombre completo, con nombre tareaExamenSuNombreSuApellido.pdf (reemplaze lo respectivo con sus datos personales, ejemplo: tareaExamenVirginiaTeodosio.pdf)
4. agregue el archivo pdf al subdirectorio TareaExamen.
5. Comprima el directorio principal, con el compresor que desee, y envielo a la dirección virginia@ciencias.unam.mx, con el subject:[EDD-tareaExamen]

### Tarea Examen 

1. Suponga que T1 (n) y T2 (n) son el tiempo de ejecución para dos fragmentos
de algoritmos A1 y A2 , respectivamente, tales que T1 (n) = O(f (n)) y T2 (n) =
O(g(n)). Pruebe que T1 (n)T2 (n) es O(f (n)g(n)) .

2. Para cada uno de los siguientes fragmentos de programas, dé un análisis
del tiempo de ejecución (O(n)). Justifique con sumas (sumatorias) y muestre la solución paso a paso de dichas sumas.

(a)
```{r}
  sum = 0 ;
  f o r ( i =0; i <n ; i ++)
      sum++;
```
  
(b)
```{r}
  sum = 0 ;
  f o r ( i =0; i <n ; i ++)
      f o r ( j =0; j <n ; j ++)
          sum++;
```

(c)
```{r}
  sum = 0 ;
  f o r ( i =0; i <n ; i ++)
    f o r ( j =0; j <n∗n ; j ++)
      sum++;
```

(d)
```{r}
  sum = 0 ;
  f o r ( i =0; i <n ; i ++)
    f o r ( j =0; j <i ; j ++)
      sum++;
```

(e)
```{r}
  sum = 0 ;
  f o r ( i =0; i <n ; i ++)
    f o r ( j =0; j <i ∗ i ; j ++)
      f o r ( k=0; k<j ; k++)
        sum++;
```

3. Defina un TDA para una Lista Ligada.
4. Suponga que se desea almacenar eficientemente una matriz triangular inferior (incluyendo la diagonal) en la que, además, todas las entradas de los
renglones de ı́ndice impar son cero. Obtenga el polinomio de direccionamiento para almacenar esta matriz en un arreglo unidimensional (Tip: la suma de los primeros k números naturales impares es k 2 ).
5. Calcular la complejidad del siguiente método, (Tip: Identifique casos para T(n) y luego vaya igualando en términos de T(n − 1), etc, hasta llegar al caso base):
```{r}
  int metodo ( i n t n ) {
    int x , i ;
    if( n <= 1 ) {
      return 1;
    }
    else{
      for( i =1; i<=n ; i++ ) {
        x = 1;
        while ( x < n ){
          x = x∗2;
        }
      }
      r e t u r n ( metodo ( n/2)+ metodo ( n / 2 ) ) ;
    }
  }
```
6. Diseñar un método recursivo borrar(L : ListaLigada, X : Dato) de forma recursiva. Este método eliminará de la lista el elemento tantas veces como este
aparezca.

7. Dé los polinomios de direccionamiento para:

a) encontrar el elemento i-ésimo en:

f l o a t [ ] m i s F l o t a n t e s = new f l o a t [ 8 9 ] ;

b) encontrar el elemento (i, j) en:

int [ ] [ ] m i s E n t e r o s = new i n t [ 1 0 ] [ 5 ] ;

## Tarea Examen - Ordenamientos y Búsquedas

##### Lineamientos de entrega 
Son los mismos, que en la tarea-examen pasada sólo modifican los valores, de la sección **Formato de entrega** en los puntos 4 y 5.

Quedando así:

4. agregue el archivo pdf al subdirectorio TareaExamen-OrdBusq
5. Comprima el directorio principal, con el compresor que desee, y envielo a la dirección virginia@ciencias.unam.mx, (con copia a Alain), con el subject:[tareaExamen-Ord-Busq]

Instrucciones
1. Muestra los pasos COMPLETOS para ordenar el arreglo [5, 12, 22, 3, 55, 8, 3, 10] usando MergeSort [2.5 ptos].
2. Muestra los pasos COMPLETOS para ordenar el arreglo [5, 12, 22, 3, 55] usando HeapSort
[2.5 ptos].
3. ¿Cuales son los tiempos de ejecución de ordenamiento por selección para el mejor caso, el
caso promedio y el peor de los casos?. Menciona cómo es el mejor caso [2.5 ptos].
4. Escribe el seudocódigo del algoritmo de QuickSort y dá el análisis de complejidad para el
peor de los casos y para el caso promedio [2.5 ptos]
5. Escribe el seudocódigo del algoritmo BFS. Calcula y justifica el peor
de los casos [2.5 ptos].
