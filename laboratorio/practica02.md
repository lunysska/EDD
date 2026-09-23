# Práctica 2: Evaluando la eficiencia de un programa

**Tema:** Tiempo de ejecución.<br>
**Lenguaje:** Java.<br>
**Entrega:** Individual a través del almacén privado asignado por el laboratorista.<br>
**Fecha de entrega:** Domingo 27 de septiembre a las 11:59 AM.<br>
**Elaboró:** [Leonardo Gallo](https://github.com/lngallo)

## Descripción 

En esta práctica se abordará el concepto de tiempo de ejecución de un programa para poder determinar cómo afecta en el desmpeño de su ejecución e identificar los factores que afectan su eficiencia.

## Objetivo

Al finalizar la práctica, el alumno aplicará mecanismos para determinar cuánto tiempo tardan en ejecutarse diferentes algoritmos para arrojar una solución, además, experimentará con su propio equipo y podrá determinar que fatores influyen en los tiempos finales obtenidos.


## Contexto

Se busca comparar la funcionalidad y la complejidad de cuatro algoritmo, cada uno de los cuales resuelve el problema de subsecuencia de suma máxima.

## Definición de subsecuencia de suma máxima

Sea _Q_ =  a1, a2, ..., an una subsecuencia de n enteros (posiblemente negativos), el objetivo es encontrar naturales i, j (con 1 <= i <= j <= n), representando una subsecuencia contigua ai,..., aj en _Q_, tales que ai + a(i+1) + ... + a(j-i) + aj sea la mayor para cualesquiera i,j. Si para todo a en _Q_, a < 0, entonces la suma máxima es 0.

## Ejercicios

Usando el código que se te proporciona [aquí](https://github.com/CCLaboratorio/LeonardoGallo/tree/main/edd/src/java/util), en la clase _SequenceOfIntegers_, resuelve y responde lo siguiente:

1. Tomar el tiempo de ejecución para cada algoritmo usando secuencas de enteros muy grandos (100, 200, 300, 400, 500 elementos). El tiempo de ejecución se puede calcular con el reloj de java (revisa el método _System.currentTimeMillis()_).
2. Responder las siguientes preguntas:
   1. ¿Siempre se obtienen los mismos resultados de tiempo al usar las mismas secuencias de enteros?
   2. ¿Qué factores alteran los tiempos de ejecución?
   3. ¿Qué puede minimizar estos factores?
   4. ¿Cuál implementación esperas que tenga mejor tiempo de ejecución? ¿Por qué?
3. Graficar y comparar los resultados obtenidos en los puntos 1 y 2.
4. Elabora un análisis, no necesariamente formal, de lo que tarda cada algoritmo en ejecutarse respecto a una entrada de n elementos, basándose sólo en el algoritmo y no en los factores de su implementación.

Sugerencia: Para crear las secuencias de enteros para probar los ejercicios 1 y 2, puedes obtener números aleatorios con los métodos random disponibles en la bibliotecas de java y generar arreglos de enteros.

## Requerimientos

1. Incluir las imagenes de las gráficas en la carpeta _img/_.
2. En la carpeta _docs/_ incluir el archivo _reporteP02.md_ con las respuestas a las preguntas de la sección de ejercicios.

## Criterios de evaluación por ejercicio

1. [2.5 puntos]
2. [2.5 puntos]
3. [2.5 puntos]
4. [2.5 puntos]
