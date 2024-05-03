# Problema del empaquetamiento mínimo

Se desea empaquetar n objetos en contenedores de capacidad c. Podemos usar un árbol binario de búsqueda con duplicados y ejecutar el método en O(n log n).
En esta solución particular, el ABB contendrá un nodo por cada contenedor que se encuentre en uso y que tenga una capacidad "no usada" diferente de 0. Supongamos que cuando el objeto(i) de tamaño 4 unidades, esta por empaquetarse, existen en el árbol 10 contenedores en uso que tienen algún espacio disponible, sean estos espacios disponibles: A=1, B=3, C=12, D=6, E=8, F=1, G=20, H=6, K=5 y J=7 respectivamente, nota que pueden existir dos o más contenedores con el mismo espacio disponible. Estos contenedores se almacenarán en un ABB con la configuración como se muestra en la Figura A.
