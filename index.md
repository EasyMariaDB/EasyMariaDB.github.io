# Índice
- [Introducción](https://#introducción)
- [¿Qué es EasyMariaDB](#qué-es-easymariadb)
  - [¿Dóde puedo descargar EasyMariaDB](#dónde-puedo-descargar-easymariadb)
- [Ayuda de EasyMariaDB](#ayuda-de-easymariadb)
  - [Requisitios previos](#requisitos-previos)

# Introducción
Al poco tiempo de comenzar a utilizar LibreOffice Base, descubrí que la base de datos HSQLDB incorporada, con el tiempo, daba errores debido a la corrupción del archivo .odb. Para evitarlo, en varias páginas web recomendaban hacer una base de datos separada.

Para solucionar los problemas de corrupción de las bases de datos HSQLDB, en LibreOffice comenzaron a incorporar la base de datos Firebird, pero, de momento, la integración de esta base de datos no es completa y produce errores.

Más tarde, también descubrí que estas bases de datos incorporadas son monousuario, es decir, que la base de datos no puede ser abierta por dos (o más) usuarios simultáneamente.

¡No hay problema!, me dije, LibreOffice Base tiene infinitas posibilidades de conexión a servidores de bases de datos fiables y altamente probados. 

No tuve muchos problemas para instalar diferentes servidores de bases de datos en mi equipo para probar cuál me sería más útil. Enseguida me di cuenta de que, aunque la instalación y la conexión a los servidores había sido relativamente fácil, si quería crear una base de datos necesitaba crearla desde un programa de línea de comandos, en el que además tenía que escribir sentencias SQL, que en ese momento desconocía. Para rematar, además, las sentencias SQL no eran exactamente las mismas para unos servidores que para otros, unos con comillas dobles, otros sencillas... Al final me desanimé y deje de utilizar Base.

Hace poco, en un canal de Telegram, volvía a oír la pregunta de siempre ¿Base es fiable? ¿Es multiusuario? Y la respuesta (errónea) fue no a las dos preguntas. Digo que la respuesta es errónea porque la fiabilidad y la capacidad multiusuario no las proporciona Base, sino el servidor de bases de datos al que se conecte, bien sea un servidor incorporado o uno externo.

Así que tomé la decisión de intentar demostrar que Base puede ser fiable y multiusuario y mi reto es que, además, la puesta en marcha de un servidor de base de datos sea más o menos fácil y la pueda realizar cualquier usuario sin necesidad de tener conocimientos avanzados.

# ¿Qué es EasyMariaDB?

La herramienta EasyMariaDB, es una extensión de LibreOffice diseñada para facilitar la creación de bases de datos y de usuarios en un servidor MariaDB o MySQL, desde LibreOffice, sin utilizar otros programas ni la consola de comandos.

## ¿Dónde puedo descargar EasyMariaDB?

La puedes descargar en [esta dirección](https://github.com/jucasaca/Extension)

# Ayuda de EasyMariaDB

## Requisitos previos

Para poder utilizar EasyMariaDB, debe cumplir con los siguientes requisitos:

- Tener instalada una versión reciente de LibreOffice. [Descarga de LibreOffice](https://es.libreoffice.org/descarga/libreoffice/)
- Tener instalada la extensión EasyMariaDB.oxt.
- Tener instalado un servidor de bases de datos [MariaDB](InstalarMariaDB.md) o [MySQL](InstalarMySQL.md) y tener acceso al mismo.
- Conocer nombre de usuario y contraseña de un usuario administrador del servidor, es decir que tenga al menos permisos para la creación de bases de datos y de usuarios.
- Si los únicos datos de usuario administrador que conocemos son los del usuario root, en general, necesitamos tener acceso al mismo equipo en que está instalado el servidor (el usuario root no suele tener permiso de acceso remoto).

## Utilidades que proporciona EasyMariaDB

EasyMariaDB proporciona las siguientes utilidades:

- Crear una base de datos
- Crear un usuario
- Asignar o modificar la contraseña de un usuario
- Asignar permisos a un usuario
- Cambiar la contraseña propia
- 
