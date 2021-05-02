# Entender la arquitectura cliente servidor

## Servidor y cliente

Si desde Base conectamos con un servidor de base de datos MariaDB o MySQL, estamos empleando la arquitectura cliente servidor.

Sin querer ser muy ténico ni preciso en las explicaciones, la arquitectura cliente servidor consiste en dos partes, una parte, la parte servidora, proporciona unos servicios y otra parte, la parte cliente los consume.

En nuestro caso, MaríaDB o MySQL actuan como la parte servidora y proporcionan unos servicios; el primero que vemos más claramente y, por tanto, más fácil de entender, es el acceso a los datos, pero proporcionan otros servicios, como, por ejemplo, la gestión de usuarios o de los permisos de acceso a los datos.

Por otro lado, la parte cliente, en nuestro caso Base, consume los servicios proporcionados por el servidor. Base pide a la parte servidora los datos, esta se los porporciona y Base los muestra. Además, con el servicio de gestión de usuarios y permisos, puede que el servidor solo proporcione algunos datos o ninguno, o que permita modificar los datos o solo leerlos.

Ser servidor o cliente no depende de que una parte esté instalada en un equipo configurado como servidor y la otra no, de hecho ambas partes pueden estar instaladas en el mismo equipo y este puede ser un ordenador de escritorio normal o un portátil. Como he dicho antes, la parte servidora es la que propociona unos servicios y la cliente la que los consume, independientemente de donde esté instalada cada una de las partes.

## El lado servidor

En nuestro caso el servidor va a ser un servidor de base de datos MariaDB o un servidor MySQL. 

Como hemos visto antes, puede estar instalada en cualquier equipo. Si lo único que necesitamos es una base de datos fiable y que nos porporcione otros servicios como gestión de usuarios o permisos de acceso a los datos, podemos instalar MariaDB o MySQL en el mismo equipo en el que vamos a trabajar. El consumo de recursos de cualquiera de los dos servidores es bajo y no se necesita un equipo especialmente potente.

Si además necesitamos que nuestra base de datos sea multiusuario, la instalación del servidor de bases de datos elegido la tenemos que hacer en un equipo al que tengan acceso todos los usuarios que necesiten acceder a los datos. Como ya hemos visto no es necesario que sea un equipo especialmente potente (a no ser que sean cientos de usuarios los que se van a conectar). Por ejemplo en un pequeño negocio con cuatro o cinco ordenadores, se puede hacer la instalación en cualquiera de los ordenadores y el resto acceder a los datos. Lo único necesario es que, como es lógico, el equipo que actua de servidor debe estar encendido para poder acceder a los datos.

## El lado cliente

Nuestro lado cliente será uno o varios archivos .odb de Base configurados para conectarse con el servidor. 

Tenemos que entender que, mientras que los datos, es decir las tablas y su contenido (y también las vistas), residen en el servidor, el resto de los elementos (formularios, consultas e informes se guardan en el archivo .odb de Base. Por tanto, si accidentalmente borramos o se corrompe el archivo .odb, perderemos los informes, las consultas y los formularios, pero no perderemos los datos: ¡los datos están a salvo en el servidor!, siempre que, claro está, el servidor esté integro. Esto da cierta seguridad.

También es importante saber que mientras que en los archivos de bases de datos HSQL o Firebird incorporadas, hay que guardar las tablas y también el archivo .odb para que los datos se guarden efectivamente en la base de datos (y si no los guardamos podemos perder los datos de toda una sesión), en el caso de conectarse a los servidores MariaDB o MySQL, los datos se guardan automáticamente registro a registro, por lo que no es necesario guardar las tablas o el archivo .odb, con lo cual en caso de un fallo inesperado de cualquier tipo, la pérdida de trabajo (de datos) seria infima.

Veamos las diferencias entre uno y otro caso.

### Un solo archivo .odb de Base

Si queremos que todos los usuarios utilicen el mismo archivo, este debe estar en una ubicación de la red a la que puedan acceder los usuarios que lo necesiten.

En este caso, al compartir el mismo archivo, todos los usuarios compartiran los mismos formularios, informes y consultas, pero solamente el primer usuario que abra el archivo podrá modificar alguno de dichos elementos. Esto no debería ser un problema, porque una vez creados los formularios, consulta e informes que se necesiten, normalmente, no será necesario modificarlos. De hecho, mi recomendación en este caso es que el archivo se configure como de 
