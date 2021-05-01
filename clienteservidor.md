# Entender la arquitectura cliente servidor

## Servidor y cliente

Si desde Base conectamos con un servidor de base de datos MariaDB o MySQL, estamos empleando la arquitectura cliente servidor.

Sin querer ser muy ténico ni preciso en las explicaciones, la arquitectura cliente servidor consiste en dos partes, una parte, 
la parte servidora, proporciona unos servicios y otra parte, la parte cliente los consume.

En nuestro caso, MaríaDB o MySQL actuan como la parte servidora y proporcionan unos servicios; el primero que vemos más claramente y, por tanto, más fácil de entender, 
es el acceso a los datos, pero proporcionan otros muchos servicios, como, por ejemplo, la gestión de usuarios o de los permisos de acceso a los datos.

Por otro lado, la parte cliente, en nuestro caso Base, consume los servicios proporcionados por el servidor. Base pide a la parte servidora los datos y
esta se los porporciona, además, con el servicio de gestión de usuarios y permisos, puede que el servidor solo proporcione algunos datos o ninguno, o que permita 
modificar los datos o solo leerlos.

Ser servidor o cliente no depende de que una parte esté instalada en un servidor y la otra no, de hecho ambas partes pueden estar instaladas
en el mismo equipo. Como he dicho antes, la parte servidora es la que propociona unos servicios y la cliente la que los consume, independientemente de donde esté
instalada cada una de las partes.
