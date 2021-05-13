# Ayuda de EasyMariaDB

## Requisitos previos

Para poder utilizar **EasyMariaDB**, debe cumplir con los siguientes requisitos:

- Tener instalada una versión reciente de LibreOffice. [[Descarga de LibreOffice]](https://es.libreoffice.org/descarga/libreoffice/)
- Tener instalada la extensión **EasyMariaDB**. [[Descarga la extensión EasyMariaDB.oxt]](https://github.com/jucasaca/Extension/releases)
- Tener instalado un servidor de bases de datos MariaDB o MySQL y tener acceso al mismo. [[Instalar MariaDB]](InstalarMariaDB.md) o [[Instalar MySQL]](InstalarMySQL.md)
- Conocer el nombre de usuario y la contraseña de un usuario administrador del servidor, es decir que tenga al menos permisos para la creación de bases de datos y de usuarios.
- Si los únicos datos de usuario administrador que conocemos son los del usuario *root*, en general, necesitamos tener acceso al mismo equipo en que está instalado el servidor (el usuario *root* no suele tener permiso de acceso remoto).

## Utilidades que proporciona EasyMariaDB

**EasyMariaDB** proporciona las siguientes utilidades:

- Crear una base de datos
- Crear un usuario
- Asignar o modificar la contraseña de un usuario
- Asignar permisos a un usuario
- Cambiar la contraseña propia

### Diálogo Datos de conexión
Al ejecutar cualquiera de las utilidades, excepto *Cambiar la contraseña propia*, se muestra un diálogo con dos pasos. El primer paso, común a todos ellos, es un diálogo en el que se piden los datos para la conexión a MariaDB/MySQL.

![Jekyll](/img/database1.png)

Los datos que tenemos que proporcionar en este diálogo son:
- **Servidor**: escriba el nombre del servidor o la dirección IP del equipo que ejecuta el servidor de bases de datos. Si está accediendo desde el mismo equipo en el que está instalado el servidor de bases de datos, puede escribir *localhost*
- **Puerto**: es el puerto a través del cual se realiza la conexión al servidor de bases de datos en el equipo en que está instalado. El puerto por defecto es *3306*
- **Usuario**: el nombre de un usuario que tenga permisos para acceder al servidor de bases de datos y que también tenga permisos para realizar la tarea a ejecutar, por ejemplo, si se va a crear una base de datos, el usuario deberá tener permisos de creación de bases de datos.
- **Contraseña**: la contraseña del usuario anterior.

### Crear una base de datos

Para crear una base de datos seleccione el menú **Herramientas > EasyMariaDB > Nueva base de datos**, o haga  clic sobre el botón *Nueva base de datos* de la barra de herramientas *EasyMariaDB* o de la pestaña *Extensión*, si tiene configurada la interfaz de usuario *En pestañas*.

Aparecerá el diálogo *Nueva base de datos*. Rellene los datos de conexión como se explicó en el punto anterior.

Haga clic en el botón *Siguiente*. Aparecerá el segundo paso del diálogo. Rellene el cuadro de texto *Base de datos* con el nombre de la base de datos que se creará. 

Aunque se puede poner cualquier nombre, se recomienda no emplear espacios, acentos ni otros signos especiales (como, por ejemplo, la letra *ñ*); también se recomienda que el nombre no sea muy largo. 

No importa si escribe el nombre en mayúsculas o minúsculas, en el servidor siempre se guardará en minúsculas.

![Jekyll](/img/database2.png)

Una vez haya rellenado el nombre, haga clic en *Aceptar*. 

Si todo va bien, se creará la base de datos y mostrará el siguiente mensaje de confirmación.

![Jekyll](/img/database3.png)

Si el nombre elegido ya existe en el servidor, se mostrará el siguiente mensaje de error.

![Jekyll](/img/database4.png)



|[< Entender la arquitectura cliente servidor](clienteservidor.md) | [Índice](index.md#índice) |
