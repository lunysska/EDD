# EDD
## Curso de Estructuras de Datos con Java.

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

### Tarea Examen

1. Suponga que T1 (n) y T2 (n) son el tiempo de ejecución para dos fragmentos
de algoritmos A1 y A2 , respectivamente, tales que T1 (n) = O(f (n)) y T2 (n) =
O(g(n)). Pruebe que T1 (n)T2 (n) es O(f (n)g(n)) .

2. Para cada uno de los siguientes fragmentos de programas, dé un análisis
del tiempo de ejecución (O(n)). Justifique con sumas (sumatorias) y muestre la solución paso a paso de dichas sumas.

  <pre><code>  
  sum = 0 ;
  f o r ( i =0; i <n ; i ++)
      sum++;

  sum = 0 ;
  f o r ( i =0; i <n ; i ++)
      f o r ( j =0; j <n ; j ++)
          sum++;

  sum = 0 ;
  f o r ( i =0; i <n ; i ++)
    f o r ( j =0; j <n∗n ; j ++)
      sum++;

  sum = 0 ;
  f o r ( i =0; i <n ; i ++)
    f o r ( j =0; j <i ; j ++)
      sum++;
  
  sum = 0 ;
  f o r ( i =0; i <n ; i ++)
    f o r ( j =0; j <i ∗ i ; j ++)
      f o r ( k=0; k<j ; k++)
        sum++;
   </code></pre>
