# Introducción
Al poco tiempo de comenzar a utilizar LibreOffice Base, descubrí que la base de datos HSQLDB incorporada, con el tiempo, daba errores debido a la corrupción del archivo .odb. Para evitarlo, en varia páginas web recomendaban hacer una base de datos separada.

Para solucionar los problemas de corrupción de las bases de datos HSQLDB, en LibreOffice comenzaron a incorporar la base de datos Firebird, pero, de momento, la integración de esta base de datos no es completa y produce errores.

Con el tiempo, también descubrí que estas bases de datos incorporadas son monousuario, es decir, que la base de datos no puede ser abierta por dos (o más) usuarios simultáneamente.

¡No hay problema!, me dije, LibreOffice Base tiene infinitas posibilidades de conexión a servidores de bases de datos fiables y altamente probados. 

No tuve muchos problemas para instalar diferentes servidores de bases de datos en mi equipo, para probar cual me sería más útil. Enseguida me di cuenta de que, aunque la instalación y la conexión a los servidores había sido relativamente fácil, si quería crear una base de datos necesitaba crearla desde un programa de línea de comandos, en el que además tenía que escribir sentencias SQL, que en ese momento desconocía. Para rematar, además, las sentencias SQL no eran exactamente las mismas para unos servidores que para otros, unos con comillas dobles, otros sencillas... Al final me desanimé y deje de utilizar Base.

Hace poco, en un canal de Telegram, volvía a oir la pregunata de siempre ¿Base es fiable? ¿Es multiusuario? y la respuesta (errónea) fué no a las dos preguntas. Digo que la respuesta es errónea porque la fiabilidad y la capacidad multiusuario no las proporciona da Base, sino el servidor de bases de datos al que se conecte, bien sea un servidor incorporado o uno externo.

Así que tomé la decisión de intentar demostrar que Base puede ser fiable y multiusuario y mi reto es que, además, la puesta en marcha de un servidor de base de datos sea más o menos fácil y la pueda realizar cuaquier usuario sin necesidad de tener conocimientos avanzados.

# ¿Qué es EasyMariaDB?

La herramienta EasyMariaDB, es una extensión de LibreOffice diseñada para facilitar la creación de bases de datos y de usuarios en un servidor MariaDB o MySQL, desde LibreOffice, sin utilizar otros programas ni la consola de comandos.

## ¿Dónde puedeo descargar EasyMariaDB?

La puedes descargar en [esta dirección](https://github.com/EasyMariaDB/Basic/releases)

# Ayuda de EasyMariaDB

## Requisitos previos

Para poder utilizar EasyMariaDB, debe cumplir con los siguientes requisitos:

- Tener instalada una versión reciente de LibreOffice
- Tener instalada la extensión EasyMariaDB.oxt
- Tener instalado un servidor de bases de datos MariaDB o MySQL y tener acceso al mismo
- Conocer nombre de usuario y contraseña de un usuario adminstrador del servidor, es decir que tenga al menso permisos para la creación de bases de datos y de usuarios
- Si los únicos datos de usuario administrador que conocemos son los del usuario root, en general, necesitamos tener acceso al mismo equipo en que está instalado el servidor (el usuario root no suele tener permiso de acceso remoto)
