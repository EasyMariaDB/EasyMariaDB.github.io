# Entender la arquitectura cliente servidor

Si desde Base conectamos con un servidor de base de datos MariaDB o MySQL, estamos empleando la arquitectura cliente servidor.

Sin querer ser muy ténico ni preciso en las explicaciones, la arquitectura cliente servidor consiste en dos partes, una parte, 
la parte servidora, proporciona unos servicios y otra parte, la parte cliente loc consume.

En nuestro caso, MaríaDB o MySQL actuan como la parte servidora y proporcionan unos servicios; el primero que vemos y más fácil de entender, 
es el acceso a los datos, pero proporciona otros muchos, como, por ejemplo, la gestión de usuarios y permiso de acceso a la base de datos.

Por otro lado, la parte cliente, en nuestro caso Base, consume los servicios proporcionados por el servidor. Base pide al la parte servidor los datos y
este se los porporciona, además, con el servicio de gestión de usuarios y permisos, puede que solo proporcione algunos datos o ninguno, o que permita modiricar
los datos o solo leerlos.
