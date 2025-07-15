# API

## Integrantes

Alumno: Santiago Jimenez Abel

## Tecnologias Usadas

Angular 20
Material Design

## Explicacion del codigo

El codigo consiste de dos componentes, login y dashboard.

### login
Login es el componente donde nos logeamos y donde ocurre la logica de validacion del usuario cuando consulta la api de usuarios (https://68743fcedd06792b9c937143.mockapi.io/api/users)
#### Login HTML
El html consiste de etiquetas, inputs y botones estilizados con la libreria de material design. Al momento de oprimir el boton login es que enviamos desde el html el contenidos de los campos al archivo ts  y son guardados en variables para ser consultadas despues, sus unicos atributos que nos interesan son su email y su contraseña. 
#### Login ts
Aqui encontramos la logica de validacion.
Tenemos un arreglo de usuarios, que es donde almacenamos todos los usuarios de la api.Despues iniciamos los metodos que nos permiten capturar los  datos en el arreglo. 
Se elaboro un metodo de nombre login() que realiza 2 validaciones en la contraseña, para confirmar que la longitud sea de 8 o mas caracteres y para saber si tiene una mayuscula, una minuscula. Si se cumplen estas condiciones ahora verificamos si estos usuarios estan en la api de usuarios que elegimos, es aqui que consultamos el arreglo de todos los usuarios  y por medio de metodos como find() es que navegamos el arreglo para encontrar una coincidencia con el email y el password que se guardaron al principio del formulario.
De no encontrarlo, se enviara una alerta de que el las credenciales son incorrectas.
De otro modo, nos otorgara acceso y podemos acceder al segundo componente, el dashboard.

### dashboard
El dashboard es nuestro segundo componente y donde visualizamos los elementos de las apis que se consultaron.
#### dashboard html

En este archivo se configuro para representar dos tablas. Una de ellas mostrara los datos del usuario que inicio sesion en el componente anterior, datos como nombre, correo, numero de id, fotografia y contraseña.
En la segunda tabla, encontraremos los datos de la segunda api consultada, Bob's burgers characters, así como una opcion de botones e inputs para manipular los contenidos de la tabla, ya sea para eliminar o editar los campos que nos interesan.

#### dashboard ts

En este archivo definimos variables donde almacenaremos valores de interes:
1. email del usuario que se logeo
2. id que queramos manipular
3. atributo de nombre
4. atributo de genero
5. atributo de cabello
6. atributo de edad

En el componente anterior, el email guardado fue almacenado de manera global por lo que podemos acceder a el desde un componente distinto. 
En este metodo de nombre getUsuario, obtenemos todos los usuarios de la api y los almacenamos en un arreglo, luego filtramos 
## APIS elegidas

## Capturas de pantalla del proyecto
