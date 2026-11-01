# Práctica 3: Matrices genéricas

**Tema:** Polinomios de direccionamiento.<br>
**Lenguaje:** Java.<br>
**Entrega:** Individual a través del almacén privado asignado por el laboratorista.<br>
**Fecha de entrega:** Domingo 8 de noviembre a las 11:59 AM.<br>
**Elaboró:** [Leonardo Gallo](https://github.com/lngallo)

## Descripción

Desarrollar una estructura de programación orientada a objetos en Java que permita representar y manipular matrices numéricas mediante el uso de clases abstractas, herencia y genéricos.

Como parte central de la práctica, se deberá implementar un mecanismo de almacenamiento de los elementos utilizando polinomios de direccionamiento, de manera que los datos de la matriz puedan almacenarse en un arreglo unidimensional en lugar de utilizar directamente una estructura bidimensional.

## Objetivos

Al finalizar la práctica, el estudiante será capaz de:

1. Diseñar e implementar clases abstractas y derivadas en Java, aplicando abstracción, herencia, polimorfismo y programación genérica.

2. Implementar polinomios de direccionamiento para representar matrices mediante arreglos unidimensionales.

3. Optimizar el almacenamiento de matrices simétricas aprovechando sus propiedades para evitar información redundante.

4. Implementar y validar operaciones matriciales, considerando las restricciones dimensionales y las características de cada representación.

## Problema

Desarrollar una estructura de clases en Java que permita representar y manipular matrices numéricas mediante arreglos unidimensionales, utilizando polinomios de direccionamiento para acceder a sus elementos. Se deberá implementar una matriz convencional y una matriz simétrica que optimice el almacenamiento al evitar datos redundantes, incorporando operaciones matriciales básicas y aplicando principios de programación orientada a objetos y genéricos.

Para cumplir lo anterior, se implementará una clase abstracta Matriz<T extends Number> que establezca las propiedades y operaciones fundamentales de una matriz, así como una clase derivada MatrizSimetrica<T extends Number> que especialice su comportamiento para representar matrices cuadradas que cumplan la propiedad de simetría.


