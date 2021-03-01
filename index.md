# Introducción
Al poco tiempo de comenzar a utilizar LibreOffice Base, descubrí que la base de datos HSQLDB incorporada, con el tiempo, daba errores debido a la corrupción del archivo .odb. Para evitarlo, en varia páginas web recomendaban hacer una base de datos separada.

Desde LibreOffice, para solucionar los porblemas de corrupción de las bases de datos HSQLDB, comenzaron a incorporar la base de datos Firebird, pero, de momento, la integración de esta base de datos no es completa.

Con el tiempo, también descubrí que estas bases de datos incorporadas son monousuario, es decir, que la base de datos no puede ser abierta por dos (o más) usuarios simultáneamente.

No hay problema, me dije, LibreOffice Base tiene infinitas posibilidades de conexión a servidores de bases de datos fiables y altamente probados. No tuve muchos problemas para instalar diferentes servidores de bases de datos en mi equipo para probar cual me sería más útil. Enseguida me di cuenta de que, aunque la conexión a los servidores había sido relativamente fácil, si quería crear una base de datos necesitaba crearla desde un programa en la línea de comandos, en la que además tenía que escribir sentencias SQL, que en ese momento desconocía. Para rematar, además, las sentencias SQL no eran exactamenteUna vez que conseguí 

# ¿Qué es EasyMariaDB?

La herramienta EasyMariaDB, es una herramienta diseñada para facilitar la creación de bases de dato y de usuarios desde LibreOffice en un servidor MariaDB o MySQL
## ¿Dónde puedeo descargar EasyMariaDB?

La puedes descargar en [esta dirección](https://github.com/EasyMariaDB/Basic/blob/Extension/Extensiones/EasyDB/EasyDB.zip)

O en las páginas de [liberación](https://github.com/EasyMariaDB/Basic/releases)
