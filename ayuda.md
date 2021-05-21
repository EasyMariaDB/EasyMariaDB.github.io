# Ayuda de EasyMariaDB

**EasyMariaDB** proporciona las siguientes utilidades:

- [Crear una base de datos](#nueva-base-de-datos)
- [Crear un usuario](#nuevo-usuario)
- [Eliminar un usuario](#eliminar-usuario)
- [Cambiar la contraseña de un usuario (por un administrador)](#cambiar-la-contrase%C3%B1a-de-un-usuario-por-un-administrador)
- [Asignar permisos a un usuario](#asignar-permisos-a-un-usuario)
- [Cambiar la contraseña propia](#cambiar-la-contrase%C3%B1a-propia)

Para acceder a todas las utilidades, excepto a *Cambiar la contraseña propia*, es necesario que se realice la conexión con el nombre de usuario y la contraseña de un administrador.

## Datos de conexión
Al ejecutar cualquiera de las utilidades, excepto *Cambiar la contraseña propia*, se muestra un diálogo con dos pasos. El primer paso, común a todos ellos, es un diálogo en el que se piden los datos para la conexión al servidor MariaDB/MySQL.

![Jekyll](/img/database1.png)

Los datos que se tienen que proporcionar en este diálogo son:
- **Servidor**: escriba el nombre del servidor o la dirección IP del equipo que ejecuta el servidor de bases de datos. Si está accediendo desde el mismo equipo en el que está instalado el servidor de bases de datos, puede escribir *localhost*.
- **Puerto**: es el puerto a través del cual se realiza la conexión al servidor de bases de datos en el equipo en que está instalado. El puerto por defecto es *3306*.
- **Usuario**: el nombre de un usuario que tenga permisos de administrador de MariaDB o MySQL.
- **Contraseña**: la contraseña del usuario anterior.

[Índice de la ayuda](#ayuda-de-easymariadb)


## Nueva base de datos

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

[Índice de la ayuda](#ayuda-de-easymariadb)


## Nuevo usuario

Para crear un usuario nuevo, seleccione el menú **Herramientas > EasyMariaDB > Nuevo usuario**, o haga  clic sobre el botón *Nuevo usuario* de la barra de herramientas *EasyMariaDB* o de la pestaña *Extensión*, si tiene configurada la interfaz de usuario *En pestañas*.

Aparecerá el diálogo *Nuevo usuario*. Rellene los datos de conexión como se explicó en [Datos de conexión](#datos-de-conexión).

Haga clic en *Siguiente* para mostrar el segundo paso del diálogo.

![Jekyll](/img/NuevoUsuario.png)

Rellene los datos del diálogo como sigue:
- **Usuario**: escriba el nombre del usuario que se va a crear.
- **Contraseña**: escriba una contraseña para el usuario.
- **Base de datos**: seleccione el nombre de la base de datos en la que tendrá permisos el usuario. Si va a crear un usuario administrador, no es necesario que seleccione ninguna base de datos.
- **Permisos**: seleccione los permisos que tendrá el usuario en la base de datos seleccionada anteriormente. En [Asignar permisos a un usuario](asigna-ermisos-a-un-usuario) se explican los privilegios de cada una de  las distintas posibilidades.

[Índice de la ayuda](#ayuda-de-easymariadb)


## Eliminar usuario

Para eliminar un usuario, seleccione el menú **Herramientas > EasyMariaDB > Eliminar usuario**, o haga  clic sobre el botón *Eliminar usuario* de la barra de herramientas *EasyMariaDB* o de la pestaña *Extensión*, si tiene configurada la interfaz de usuario *En pestañas*.

Aparecerá el diálogo *Eliminar usuario*. Rellene los datos de conexión como se explicó en [Datos de conexión](#datos-de-conexión).

Haga clic en *Siguiente* para mostrar el segundo paso del diálogo.

![Jekyll](/img/EliminarUsuario.png)

En el campo *Usuario*, seleccione el nombre del usuario a eliminar en la lista desplegable.

Haga clic en *Aceptar*. Un nuevo diálogo pedirá confirmación.

![Jekyll](/img/EliminarUsuarioConfirmacion.png)

Haga clic en *Sí* en este nuevo diálogo para eliminar definitivamente al usuario. Se mostrará un mensaje confirmando la eliminación.

![Jekyll](/img/UsuarioEliminado.png)

Haga clic en *Aceptar* para cerrar el diálogo.

[Índice de la ayuda](#ayuda-de-easymariadb)


## Cambiar la contraseña de un usuario (por un administrador)

Seleccione el menú **Herramientas > EasyMariaDB > Cambiar contraseña a un usuario**, o haga  clic sobre el botón *Cambiar contraseña a un usuario* de la barra de herramientas *EasyMariaDB* o de la pestaña *Extensión*, si tiene configurada la interfaz de usuario *En pestañas*.

Aparecerá el diálogo *Cambiar contraseña*. Rellene los datos de conexión como se explicó en [Datos de conexión](#datos-de-conexión).

Haga clic en *Siguiente* para mostrar el segundo paso del diálogo.

![Jekyll](/img/pass2.png)

Rellene los datos del diálogo como sigue:
- **Usuario**: seleccione el nombre del usuario al que se va a modificar la contraseña.
- **Contraseña**: escriba una contraseña para el usuario.
- **Repita contraseña**: vuelva a escribir la contraseña para el usuario.

Una vez rellenados los datos, haga clic en *Aceptar* para cambiar la contraseña.

Se mostrará un mensaje confirmando el cambio de contraseña.

![Jekyll](/img/PassConfirmation.png)

Haga clic en *Aceptar* para cerrar el diálogo

[Índice de la ayuda](#ayuda-de-easymariadb)


## Asignar permisos a un usuario

Seleccione el menú **Herramientas > EasyMariaDB > Permisos de usuario**, o haga  clic sobre el botón *Permisos de usuario* de la barra de herramientas *EasyMariaDB* o de la pestaña *Extensión*, si tiene configurada la interfaz de usuario *En pestañas*.

Aparecerá el diálogo *Permisos de usuario*. Rellene los datos de conexión como se explicó en [Datos de conexión](#datos-de-conexión).

Haga clic en *Siguiente* para mostrar el segundo paso del diálogo.

![Jekyll](/img/Privileges2.png)

Rellene los datos del diálogo como sigue:
- **Usuario**: seleccione el nombre del usuario al que se van a asignar o modificar los permisos.
- **Base de datos**: seleccione la base de datos para la que se otorgarán los permisos. Si los permisos que se van a asignar son de *Administrador*, no es necesario seleccionar ninguna base de datos
- **Permisos**: seleccione los permisos que se otorgarán al usuario.

Una vez rellenados los datos, haga clic en *Aceptar* para confirmar el cambio de permisos.

Se mostrará un nuevo mensaje confirmando el cambio de permisos.

![Jekyll](/img/Privileges2.png)

Haga clic en *Aceptar* para cerrar el mensaje.

Los permisos que se pueden asignar son los siguientes:
- **Ninguno (eliminar)**. Se eliminarán todos los permisos que tenga el usuario en la base de datos seleccionada.
- **Solo lectura**. El usuario podrá leer los datos de la base de datos, pero no podrá modificarlos.
- **Lectura y escritura**. El usuario podrá leer los datos de la base de datos y también modificarlos, pero no podrá crear ni eliminar tablas o vistas.
- **Avanzado**. El usuario tendrá todos los permisos en la base de datos seleccionada, además de leer y modificar los datos podrá crear tablas e índices y realizar otras tareas más avanzadas, como crear funciones, disparadores, etc.
- **Administrador**. Todos los permisos en todas las bases de datos y en el servidor. Son los mismos permisos que los del usuario root, añadiendo que puede iniciar sesión desde cualquier equipo de la red o incluso de iternet si la red tiene acceso externo. Estos permisos deberían asignarse con mucho cuidado y el usuario que los posea debe proteger cuidadosamente su contraseña. Si no se tienen problemas para acceder como usuario root desde el equipo local, es mejor no asignarlo.

[Índice de la ayuda](#ayuda-de-easymariadb)


## Cambiar la contraseña propia

Mientras que las demás opciones se puden ejecutar desde cualquier aplicación de LibreOffice, esta opción solo se puede ejecutar desde Base y además es requisito tener iniciada la sesión en la base de datos a la que pertenece el usuario.

También esta es la única opción en la que el diálogo no tienen la ventana de conexión.

Seleccione el menú **Herramientas > EasyMariaDB > Cambiar contraseña propia**, o haga  clic sobre el botón *Cambiar contraseña propia* de la barra de herramientas *EasyMariaDB* o de la pestaña *Extensión*, si tiene configurada la interfaz de usuario *En pestañas*.

Se mostrará la ventana de cambio de contraseña para el usuario actual.

![Jekyll](/img/PassPropia1.png)

Rellene los datos del diálogo como sigue:
- **Contraseña actual**: escriba la contraseña que tiene actualmente el usuario.
- **Nueva contraseña**: escriba la nueva contraseña.
- **Repita contraseña**: vuelva a escribir la nueva contraseña.

Una vez rellenados los datos haga clic en *Aceptar*.

Si todo es correcto se mostrará un mensaje de confirmación.

![Jekyll](/img/PassPropia2.png)

Haga clic en *Aceptar* para cerrar el mensaje.

Si hay algún error se mostrará un mensaje advirtiendo del error.

![Jekyll](/img/PassPropia3.png)

Haga clic en *Aceptar* para cerrar el mensaje. Corrija el error para poder continuar.

El cambio de contraseña no será efectivo hasta que no reinicie LibreOffice. Recomendamos reiniciarlo inmediatamente para evitar posibles errores.

[Índice de la ayuda](#ayuda-de-easymariadb)


|[< Entender la arquitectura cliente servidor](clienteservidor.md) | [Índice](index.md#índice) |


