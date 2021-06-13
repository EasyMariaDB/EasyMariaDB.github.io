# Índice
- [Introducción](https://#introducción)
- [¿Qué es EasyMariaDB](#qué-es-easymariadb)
- [Entender la arquitectura cliente servidor](clienteservidor.md)
- [Instalar la extensión](instalarextension.md)
- [Ayuda de EasyMariaDB](ayuda.md)
  - [Requisitos previos](requisitos.md)
  - [Crear una base de datos y conectarse a ella](crearbd.md)
  - [Utilidades proporcionadas por EasyMariaDB](utilidades.md)

# Introducción
Al poco tiempo de comenzar a utilizar LibreOffice Base, descubrí que la base de datos HSQLDB incorporada, con el uso, daba errores debido a la corrupción del archivo .odb. Para evitarlo, en varias páginas web recomendaban hacer una base de datos separada.

Para solucionar los problemas de corrupción de las bases de datos HSQLDB, en LibreOffice comenzaron a incorporar la base de datos Firebird, pero, de momento, la integración de esta base de datos no es completa y produce errores.

Más tarde, también descubrí que estas bases de datos incorporadas son monousuario, es decir, que la base de datos no puede ser abierta por dos (o más) usuarios simultáneamente.

¡No hay problema!, me dije, LibreOffice Base tiene infinitas posibilidades de conexión a servidores de bases de datos fiables y altamente probados. 

No tuve muchos problemas para instalar diferentes servidores de bases de datos en mi equipo para probar cuál me sería más útil. Enseguida me di cuenta de que, aunque la instalación y la conexión a los servidores había sido relativamente fácil, si quería crear una base de datos necesitaba crearla desde un programa de línea de comandos, en el que además tenía que escribir sentencias SQL, que en ese momento desconocía. Para rematar, además, las sentencias SQL no eran exactamente las mismas para unos servidores que para otros, unos con comillas dobles, otros con sencillas... Al final me desanimé y deje de utilizar Base.

Hace poco, en un canal de Telegram, volví a ver las preguntas de siempre ¿Base es fiable? ¿Es multiusuario? Y la respuesta (errónea) fue no a las dos preguntas. Digo que la respuesta es errónea porque la fiabilidad y la capacidad multiusuario no las proporciona Base, sino el servidor de bases de datos al que se conecte, bien sea un servidor incorporado o uno externo.

Así que tomé la decisión de intentar demostrar que Base puede ser fiable y multiusuario y mi reto es que, además, la puesta en marcha de un servidor de base de datos sea fácil y la pueda realizar cualquier usuario sin necesidad de tener conocimientos avanzados. Por esta razón creé **EasyMariaDB**.


# ¿Qué es EasyMariaDB?

La herramienta **EasyMariaDB**, es una extensión de LibreOffice diseñada para facilitar la creación de bases de datos y de usuarios en un servidor MariaDB o MySQL desde LibreOffice, sin utilizar otros programas ni la consola de comandos.

Ha sido diseñada para utilizarse con un servidor MariaDB o con un servidor MySQL. Ambos servidores son rápidos, fiables y seguros y tienen al menos una versión que es software libre y puede ser descargada e instalada libre y gratuitamente. Además LibreOffice Base tiene incorporado un conector nativo que facilita mucho la conexión a cualquiera de estos dos servidores.

Al utilizar cualquiera de estos servidores junto con LibreOffice Base obtendremos, como era nuestro objetivo, bases de datos fiables, seguras y multiusuario, y junto con la extensión **EsayMariaDB**, fácil de poner en funcionamiento.

Tras [instalar la extensión](instalarextension.md), se genera una nueva opción, EasyMariaDB, en el menú Herramientas de todas las aplicaciones de LibreOffice, excepto Math. Este submenú da acceso a las [utilidades](utilidades.md) proporcionadas por EasyMariaDB


|[< Introducción](index.md#introducción) | [Índice](index.md#índice) | [Entender la arquitectura cliente servidor >](clienteservidor.md) |
