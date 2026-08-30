# Práctica 1: Implementación de un sistema de autenticación

**Tema:** Tipos de Datos Abstractos (TDA) y Programación Orientada a Objetos (POO).
**Lenguaje:** Java.
**Entrega:** Individual a través del almacén privado asignado por el laboratorista.
**Fecha de entrega:** Martes 8 de septiembre a las 11:59 AM.
**Elaboró:** [Leonardo Gallo](https://github.com/lngallo)

## Descripción 

En esta práctica se integrarán conocimientos previamente adquiridos sobre Tipos de Datos Abstractos (TDA) y 
los cuatro pilares de la Programación Orientada a Objetos mediante la construcción de un sistema sencillo de autenticación.

El sistema permitirá validar las credenciales de un usuario utilizando un archivo de texto como fuente de datos y 
la consola como interfaz de interacción.

La práctica busca que el alumno pase de la identificación de conceptos de la POO a su aplicación dentro de una solución estructurada.

## Ojetivo

Al finalizar la práctica, el estudiante implementará en Java un sistema de autenticación funcional utilizando el patrón Modelo–Vista–Controlador (MVC),
 una clase que represente al usuario como TDA y un archivo de texto como fuente de datos, aplicando encapsulamiento, abstracción, herencia 
y polimorfismo cuando sean pertinentes a la solución, y demostrará su funcionamiento mediante casos de prueba de autenticación exitosa y fallida.


## Contexto

Una empresa de tecnología está desarrollando una aplicación y requiere que permita a sus usuarios autenticarse mediante un correo electrónico y una contraseña.

Debido a que la aplicación se encuentra en una etapa inicial de desarrollo, la información de los usuarios se almacenará temporalmente en un archivo de texto. La interacción con el sistema se realizará mediante la entrada y salida estándar.

El sistema deberá organizarse utilizando el patrón Modelo–Vista–Controlador (MVC).

## Flujo de ejecución

La aplicación deberá:

1. Solicitar un correo electrónico.
2. Solicitar una contraseña.
3. Consultar los usuarios registrados.
4. Validar las credenciales.
5. Informar si la autenticación fue exitosa o fallida.

## Organización

El proyecto contiene diversos componentes, de los cuales sólo trabajaras con algunos, y cada uno responde a las responsabilidades especificadas en la tabla:

| Componente | Responsabilidad |
|--|--|
| User | Representar al usuario activo en la aplicación |
|--|--|
| LoginView | Permitir la interacción con el usuario |
|--|--|
| LoginController | Coordinar el proceso de autenticación |
|--|--|
| UserDTO | Obtener los usuarios desde el archivo |
|--|--|
| Main | Iniciar la aplicación |
|--|--|

## Requerimientos

1. Leer los usuarios desde un archivo llamada __resources/users.txt__.
2. Solicitar las credenciales mediante la consola.
3. Comparar las credenciales proporcionadas con los usuarios registrados.
4. Mostrar un mensaje de autenticación.
    4.1 Crear un objeto User y mostrar su información en el mensaje cuando las credenciales sean correctas.
    4.2 Mostrar un mensaje de error cuando sean incorrectas.

## Extra

1. Valida el correo electrónico mediante una expresión regular. (1 punto)
2. Crea la clase InvalidEmailException para manejar formatos de correo no validos. (1 punto)
3. Crea la clase UserNotAllowedException para manejar la autenticación fallida. (1 punto)

## Criterios de evaluación

1. El programa compila y se ejecuta correctamente.
2. Los usuarios se obtienen desde users.txt.
3. La información del usuario se representa mediante objetos.
4. La interacción se realiza mediante consola.
5. Las credenciales correctas permiten iniciar sesión.
6. Las credenciales incorrectas son rechazadas.
7. Las clases están organizadas de acuerdo con MVC.
8. Los atributos de todas las clases están encapsulados.
9. El alumno puede explicar dónde se aplican los cuatro pilares de POO.
10. El alumno puede justificar la diferencia de un TDA y su implementación.
