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
- Eliminar un usuario
- Cambiar la contraseña de un usuario (por un administrador)
- Asignar permisos a un usuario
- Cambiar la contraseña propia

### Datos de conexión
Al ejecutar cualquiera de las utilidades, excepto *Cambiar la contraseña propia*, se muestra un diálogo con dos pasos. El primer paso, común a todos ellos, es un diálogo en el que se piden los datos para la conexión al servidor MariaDB/MySQL.

![Jekyll](/img/database1.png)

Los datos que se tienen que proporcionar en este diálogo son:
- **Servidor**: escriba el nombre del servidor o la dirección IP del equipo que ejecuta el servidor de bases de datos. Si está accediendo desde el mismo equipo en el que está instalado el servidor de bases de datos, puede escribir *localhost*
- **Puerto**: es el puerto a través del cual se realiza la conexión al servidor de bases de datos en el equipo en que está instalado. El puerto por defecto es *3306*
- **Usuario**: el nombre de un usuario que tenga permisos para acceder al servidor de bases de datos y que también tenga permisos para realizar la tarea a ejecutar, por ejemplo, si se va a crear una base de datos, el usuario deberá tener permisos de creación de bases de datos.
- **Contraseña**: la contraseña del usuario anterior.

### Nueva base de datos

Para crear una base de datos seleccione el menú **Herramientas > EasyMariaDB > Nueva base de datos**, o haga  clic sobre el botón *Nueva base de datos* de la barra de herramientas *EasyMariaDB* o de la pestaña *Extensión*, si tiene configurada la interfaz de usuario *En pestañas*.

Aparecerá el diálogo *Nueva base de datos*. Rellene los datos de conexión como se explicó en [Datos de conexión](#datos-de-conexión).

Haga clic en el botón *Siguiente*. Aparecerá el segundo paso del diálogo. Rellene el cuadro de texto *Base de datos* con el nombre de la base de datos que se creará. 

Aunque se puede poner cualquier nombre, se recomienda no emplear espacios, acentos ni otros signos especiales (como, por ejemplo, la letra *ñ*); también se recomienda que el nombre no sea muy largo. 

No importa si escribe el nombre en mayúsculas o minúsculas, en el servidor siempre se guardará en minúsculas.

![Jekyll](/img/database2.png)

Una vez haya rellenado el nombre, haga clic en *Aceptar*. 

Si todo va bien, se creará la base de datos y mostrará el siguiente mensaje de confirmación.

![Jekyll](/img/database3.png)

Si el nombre elegido ya existe en el servidor, se mostrará un mensaje de error.

![Jekyll](/img/database4.png)

### Nuevo usuario

Para crear un usuario nuevo, seleccione el menú **Herramientas > EasyMariaDB > Nuevo usuario**, o haga  clic sobre el botón *Nuevo usuario* de la barra de herramientas *EasyMariaDB* o de la pestaña *Extensión*, si tiene configurada la interfaz de usuario *En pestañas*.

Aparecerá el diálogo *Nuevo usuario*. Rellene los datos de conexión como se explicó en [Datos de conexión](#datos-de-conexión).

Haga clic en *Siguiente* para mostrar el segundo paso del diálogo.

![Jekyll](/img/NuevoUsuario.png)

Rellene los datos del diálogo como sigue:
- **Usuario**: escriba el nombre del usuario que se va a crear.
- **Contraseña**: escriba una contraseña para el usuario.
- **Base de datos**: seleccione el nombre de la base de datos en la que tendrá permisos el usuario. Si va a crear un usuario administrador, no seleccione ninguna base de datos.
- **Permisos**: seleccione los permisos que tendrá el usuario en la base de datos seleccionada anteriormente. En Gestión de permisos se explican los privilegios de cada una de  las distintas posibilidades.

### Eliminar usuario

Para eliminar un usuario nuevo, seleccione el menú **Herramientas > EasyMariaDB > Eliminar usuario**, o haga  clic sobre el botón *Eliminar usuario* de la barra de herramientas *EasyMariaDB* o de la pestaña *Extensión*, si tiene configurada la interfaz de usuario *En pestañas*.

Aparecerá el diálogo *Eliminar usuario*. Rellene los datos de conexión como se explicó en [Datos de conexión](#datos-de-conexión).

Haga clic en *Siguiente* para mostrar el segundo paso del diálogo.

![Jekyll](/img/EliminarUsuario.png)

En el campo *Usuario*, seleccione el nombre del usuario a eliminar en la lista desplegable.

Haga clic en *Aceptar*. Un nuevo diálogo pedirá confirmación.

![Jekyll](/img/EliminarUsuarioConfirmacion.png)

Haga clic en *Sí* en este nuevo diálogo para eliminar definitivamente al usuario. Se mostrará un mensaje confirmando la eliminación.

![Jekyll](/img/UsuarioEliminado.png)

Haga clic en *Aceptar* para cerrar el diálogo.

### Cambiar la contraseña de un usuario (por un administrador)

Seleccione el menú **Herramientas > EasyMariaDB > Cambiar contraseña a un usuario**, o haga  clic sobre el botón *Cambiar contraseña a un usuario* de la barra de herramientas *EasyMariaDB* o de la pestaña *Extensión*, si tiene configurada la interfaz de usuario *En pestañas*.

Aparecerá el diálogo *Cambiar contraseña*. Rellene los datos de conexión como se explicó en [Datos de conexión](#datos-de-conexión).

Haga clic en *Siguiente* para mostrar el segundo paso del diálogo.

![Jekyll](/img/pass2.png)

Rellene los datos del diálogo como sigue:
- **Usuario**: seleccione el nombre del usuario al que se va a modificar la contraseña.
- **Contraseña**: escriba una contraseña para el usuario.
- **Repita contraseña**: vuelva a escribir la contraseña para el usuario.

Se mostrara un mensaje confirmando el cambio de contraseña.

![Jekyll](/img/PassConfirmation.png)

Haga clic en *Aceptar* para cerrar el diálogo

### Asignar permisos a un usuario

|[< Entender la arquitectura cliente servidor](clienteservidor.md) | [Índice](index.md#índice) |


