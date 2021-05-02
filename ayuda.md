# Ayuda de EasyMariaDB

## Requisitos previos

Para poder utilizar **EasyMariaDB**, debe cumplir con los siguientes requisitos:

- Tener instalada una versión reciente de LibreOffice. [[Descarga de LibreOffice]](https://es.libreoffice.org/descarga/libreoffice/)
- Tener instalada la extensión **EasyMariaDB**. [[Descarga la extensión EasyMariaDB.oxt]](https://github.com/jucasaca/Extension/releases)
- Tener instalado un servidor de bases de datos MaiaDB o MySQL y tener acceso al mismo. [[Instalar MariaDB]](InstalarMariaDB.md) o [[Instalar MySQL]](InstalarMySQL.md)
- Conocer el nombre de usuario y la contraseña de un usuario administrador del servidor, es decir que tenga al menos permisos para la creación de bases de datos y de usuarios.
- Si los únicos datos de usuario administrador que conocemos son los del usuario *root*, en general, necesitamos tener acceso al mismo equipo en que está instalado el servidor (el usuario *root* no suele tener permiso de acceso remoto).

## Utilidades que proporciona EasyMariaDB

**EasyMariaDB** proporciona las siguientes utilidades:

- Crear una base de datos
- Crear un usuario
- Asignar o modificar la contraseña de un usuario
- Asignar permisos a un usuario
- Cambiar la contraseña propia

### Crear una base de datos

Para crear una base de datos seleccione el menú Herramientas > EasyMariaDB > Nueva base de datos, aparecerá un diálogo.

En el primer paso del diálogo, nos piden los datos de conexión al servidor de base de datos. En *Servidor* escriba el nombre del servidor o la dirección IP del equipo que ejecuta el servidor de bases de datos; si se está conectando desde el mismo en que está instalada el servidor de base de datos, puede dejar *localhost*. A continuación escriba el *Puerto* de conexión a la base de datos. Si no lo sabe escriba *3306* que es el puerto por defecto. En *Usuario* debe escribir el nombre de un usuario administrador (con permisos para crear bases de datos). En *Contraseña* escriba la contrseña del usuario administrador. Una vez rellenados todos los datos, pulse *Siguiente*.

![Jekyll](/img/database1.png)

En el segundo paso

![Jekyll](/img/database2.png)

![Jekyll](/img/database3.png)

![Jekyll](/img/database4.png)

|[< Entender la arquitectura cliente servidor](clienteservidor.md) | [Índice](index.md#índice) |
