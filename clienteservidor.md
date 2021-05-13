# Entender la arquitectura cliente servidor

## Servidor y cliente

Si desde Base conectamos con un servidor de base de datos MariaDB o MySQL, estamos empleando la arquitectura cliente servidor.

Sin querer ser muy técnico ni preciso en las explicaciones, la arquitectura cliente servidor consiste en dos partes, una parte, la parte servidora, proporciona unos servicios y otra parte, la parte cliente los consume.

En nuestro caso, MaríaDB o MySQL actúan como la parte servidora y proporcionan unos servicios; el primero que vemos más claramente y, por tanto, más fácil de entender, es el acceso a los datos, pero proporcionan otros servicios, como, por ejemplo, la gestión de usuarios o de los permisos de acceso a los datos.

Por otro lado, la parte cliente, en nuestro caso Base, consume los servicios proporcionados por el servidor. Base pide a la parte servidora los datos, esta se los proporciona y Base los muestra, bien sea en una tabla directamente o a través de consultas, formularios o informes. Además, con los servicios de gestión de usuarios y permisos, puede que el servidor solo proporcione algunos datos o ninguno, o que permita modificar los datos o solo leerlos.

Ser servidor o cliente no depende de que una parte esté instalada en un equipo configurado como servidor y la otra no, de hecho ambas partes pueden estar instaladas en el mismo equipo y este puede ser un ordenador de escritorio normal o un portátil. Como he dicho antes, la parte servidora es la que proporciona unos servicios y la cliente la que los consume, independientemente de donde esté instalada cada una de las partes.

## El lado servidor

En nuestro caso el servidor va a ser un servidor de base de datos MariaDB o un servidor MySQL. 

Como hemos visto antes, puede estar instalada en cualquier equipo. Si lo único que necesitamos es una base de datos fiable y que nos proporcione otros servicios como gestión de usuarios o permisos de acceso a los datos, podemos instalar MariaDB o MySQL en el mismo equipo en el que vamos a trabajar. El consumo de recursos de cualquiera de los dos servidores es bajo y no se necesita un equipo especialmente potente.

Si además necesitamos que nuestra base de datos sea multiusuario, la instalación del servidor de bases de datos elegido la tenemos que hacer en un equipo al que tengan acceso todos los usuarios que necesiten acceder a los datos. Como ya hemos visto no es necesario que sea un equipo especialmente potente (a no ser que sean cientos de usuarios los que se van a conectar). Por ejemplo en un pequeño negocio con cuatro o cinco ordenadores, se puede hacer la instalación en cualquiera de los ordenadores y el resto acceder a los datos. Lo único necesario es que, como es lógico, el equipo que ejecuta el servidor debe estar encendido para poder acceder a los datos.

## El lado cliente

Nuestro lado cliente serán uno o varios archivos .odb de Base configurados para conectarse con el servidor. 

Tenemos que entender que, mientras que los datos, es decir las tablas y su contenido (y también las vistas), residen en el servidor, el resto de los elementos (formularios, consultas e informes) se guardan en el archivo .odb de Base. Por tanto, si accidentalmente borramos o se corrompe el archivo .odb, perderemos los informes, las consultas y los formularios, pero no perderemos los datos: ¡los datos están a salvo en el servidor!, siempre que, claro está, el servidor esté íntegro. Esto da cierta seguridad.

También es importante saber que mientras que en los archivos de bases de datos HSQL o Firebird incorporadas, hay que guardar las tablas y también el archivo .odb para que los datos se guarden efectivamente en la base de datos (y si no los guardamos podemos perder los datos de toda una sesión), en el caso de conectarse a los servidores MariaDB o MySQL, los datos se guardan automáticamente después de la edición de cada registro, al movernos a otro registro, por lo que no es necesario guardar las tablas o el archivo .odb, solo es necesario guardar el último registro editado, con lo cual en caso de un fallo inesperado de cualquier tipo, la pérdida de trabajo (de datos) sería ínfima.

Anteriormente he dicho que en el lado cliente podemos tener uno o varios archivos .odb. En realidad, para ser más precisos, las posibilidades son que varios o todos los usuarios accedan a través de un mismo archivo .odb o que cada usuario tenga su propio archivo .odb. Veamos las diferencias entre uno y otro caso.

### Un solo archivo .odb de Base para varios usuarios

Si queremos que varios o todos los usuarios utilicen el mismo archivo, este debe estar en una ubicación de la red a la que puedan acceder los usuarios que lo necesiten.

En este caso, al compartir el mismo archivo, los usuarios compartirán los mismos formularios, informes y consultas, pero solamente el primer usuario que acceda el archivo podrá modificar dichos elementos. Esto no debería ser un problema, puesto que una vez creados los formularios, consultas e informes que se necesiten, normalmente no será necesario modificarlos. De hecho, mi recomendación en este caso es que, una vez creados todos los elementos necesarios, el archivo se configure como de solo lectura para todos los usuarios. 

El hecho de que el archivo sea de solo lectura, supone que el usuario no podrá modificar el archivo .odb, y por tanto no podrá modificar ni los informes, ni los formularios, ni las consultas, pero sí que podrá modificar los datos, ya que estos residen en el servidor y no en el archivo .odb.

### Cada usuario tiene su propio archivo .odb de Base

Si el usuario posee su propio archivo .odb, es libre de crear y modificar sus propios formularios, informes y consultas, que serán diferentes de los de otro usuario; pero los datos, que, como sabemos, residen en el servidor, serán los mismos para todos los usuarios. Esta forma de acceder a los datos es conveniente cuando cada usuario tiene unas necesidades diferentes, por ejemplo un usuario de la oficina de personal puede crear sus propios elementos para el acceso a las tablas de empleados, salarios y nóminas, etc, mientras que el encargado de contabilidad puede crear los suyos para acceso a facturación, cuentas bancarias, etc.

Este sistema proporciona más flexibilidad, pero también más trabajo para preparar formularios y demás elementos.

|[< Introducción](index.md#introducción) | [Índice](index.md#índice) | [Ayuda de EasyMariaDB >](ayuda.md) |
