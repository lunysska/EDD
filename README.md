## Curso de Estructuras de Datos con Java.
Este curso forma parte de los complementos a desarrollar para el curso de Estructuras de Datos para la carrera de Ciencias de la Computación, para la Facultad de Ciencias, UNAM.

[Tareas](capitulos/tareas.md)

1. Motivación
2. Introducción
3. TDA
   (El ejemplo de booleano)
4. [El tiempo de ejecución de un programa](capitulos/moduloTiempoEjecuciónPrograma.md)
5. Introducción a la complejidad de algoritmos
    1. Definición de O-grande
    2. Las reglas de la suma y el producto
6. Recursión
   1. Cálculo de complejidad para algoritmos recursivos
7. Estructuras de datos
   1. Definición
   2. Operaciones
   3. Clasificaciòn.    
8. Arreglos.
   1. Polinomio de direccionamiento
   2. Características
   3. De una dimensión
   4. De dos dimensiones
   5. Definicion formal general<br>
   *. **Tarea:** Tarea con puntos extras: Hacer un esquema del polinomio para dos dimensiones<br>
9. Estructuras de datos lineales.
   1. Listas ligadas
       1. Qué son
       2. Sus operaciones y el análisis del tiempo de ejecución
       3. Definición del TDA celda
       4. Definición del TDA ListaLigada
       5. Métodos de servicio: agregarEnCabeza, agregarEnCola, AgregarDespuésDeUnValor, eliminarDadoUnValor, actualizarUnObjetoDadoUnValor, obtenerUnObjetoDadoUnValor
       6. El método **size** con implementación lineal y constante.
            1. Ventajas y desventajas de cada implementación <br>
   *. **Tarea:** Tarea con puntos extras: Revisar y analizar la clase equivalente para Lista Ligada en el API de Java, examinarla a detalle<br>
   2. Listas doblemente ligadas
     1. TDAS: CeldaDoblementeLigada. ListaDoblementeLigada. La revisión se realiza en pseudocodigo-lenguaje natural.
     2. El análisis del tiempo de ejecución de cada método<br>
   *. **Tarea:** Tarea con puntos extras: Definir los dos TDA's de esta sección a un nivel que el pseudocódigo se parezca más a código de Java<br>
   *. **Tarea:** Tarea con puntos extras: Revisar el API de Collections de Java y verificar qué clase es la equivalente a Lista Doblemente Ligada y realizar un análisis minucioso <br>

   3. Pilas
      1. Sus operaciones. 
      2. Implementamos con un soporte con lista ligada en la parte privada.
      3. Analizamos el tiempo de ejecución de sus métodos.
      4. Vimos sus ventajas vs desventajas.
      5. Analizamos la implementaciión con un arreglo como soporte.
      6. Aplicaciones:
         1. El uso de pila para la JVM. De manera muy general.
         2. La identacion de paréntesis, solo usando paréntesis redondos
         3. Generalizamos para: [](){}<br>
   **Tarea:** TDA de Pila con soporte de arreglos<br>
   **Tarea:** Evaluación de expresiones aritméticas sencillas, usando dos pilas. Ejemplo: ((3+4)*(4+8))/2<br>        
