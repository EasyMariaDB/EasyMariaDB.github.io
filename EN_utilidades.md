---
title: EasyMariaDB
---

| [ Español ](index.md) ![Jekyll](/img/spain.png) | [ English ](EN_index.md) ![Jekyll](/img/england.png)

# Utilities provided by EasyMariaDB

**EasyMariaDB** provides the following utilities:

- [Create a database](#create-a-database)
- [Create a user](#create-a-user)
- [Delete a user](#delete-a-user)
- [Change a user's password (by an administrator)](#change-a-users-password-by-an-administrator)
- [Assign permissions to a user](#assign-permissions-to-a-user)
- [Change own password](#change-own-password)

To access all utilities, except *Change own password*, it is necessary to log in with the username and password of an administrator. See [Connection data](#connection-data)

### Connection data
When running any of the utilities, except *Change own password*, a dialog with two steps is displayed. The first step, common to all of them, is a dialog asking for the data for the connection to the MariaDB/MySQL server.

![Jekyll](/img/database1.png)

The data to be provided in this dialog are:
- **Server**: type the server name or IP address of the computer running the database server. If you are accessing from the same computer where the database server is installed, you can type *localhost*.
- **Port**: is the port through which the connection to the database server is made on the computer on which it is installed. The default port is *3306*.
- **User**: the name of a user who has MariaDB or MySQL administrator permissions.
- **Password**: the password of the previous user.

|[Subir ˄](#utilidades-proporcionadas-por-easymariadb)|

## Create a database

To create a database select the **Tools > EasyMariaDB > New database** menu, or click on the *New database* button on the *EasyMariaDB* toolbar or on the *Extension* tab, if you have configured the *Tabbed* user interface.

The *New database* dialog will appear. Fill in the connection data as explained under [Connection data](#connection-data).

Click on the *Next* button. The second step of the dialog appears. Fill in the *Database* text box with the name of the database to be created. 

Although you can enter any name, it is recommended that you do not use spaces, accents or other special characters (e.g. the letter *ñ*); it is also recommended that the name not be too long. 

It does not matter if you write the name in upper or lower case, it will always be saved in lower case on the server.

![Jekyll](/img/database2.png)

Once you have filled in the name, click *OK*. 

If all goes well, the database will be created and the following confirmation message will be displayed.

![Jekyll](/img/database3.png)

If the chosen name already exists on the server, an error message will be displayed.

![Jekyll](/img/database4.png)

[Subir ˄](#utilidades-proporcionadas-por-easymariadb)|


## Create a user

Para crear un usuario nuevo, seleccione el menú **Herramientas > EasyMariaDB > Nuevo usuario**, o haga  clic sobre el botón *Nuevo usuario* de la barra de herramientas *EasyMariaDB* o de la pestaña *Extensión*, si tiene configurada la interfaz de usuario *En pestañas*.

Aparecerá el diálogo *Nuevo usuario*. Rellene los datos de conexión como se explicó en [Datos de conexión](#datos-de-conexión).

Haga clic en *Siguiente* para mostrar el segundo paso del diálogo.

![Jekyll](/img/NuevoUsuario.png)

Rellene los datos del diálogo como sigue:
- **Usuario**: escriba el nombre del usuario que se va a crear.
- **Contraseña**: escriba una contraseña para el usuario.
- **Base de datos**: seleccione el nombre de la base de datos en la que tendrá permisos el usuario. Si va a crear un usuario administrador, no es necesario que seleccione ninguna base de datos.
- **Permisos**: seleccione los permisos que tendrá el usuario en la base de datos seleccionada anteriormente. En [Asignar permisos a un usuario](asigna-ermisos-a-un-usuario) se explican los privilegios de cada una de  las distintas posibilidades.

[Subir ˄](#utilidades-proporcionadas-por-easymariadb)|

## Delete a user

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

[Subir ˄](#utilidades-proporcionadas-por-easymariadb)|

## Change a user's password (by an administrator)

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

[Subir ˄](#utilidades-proporcionadas-por-easymariadb)|

## Assign permissions to a user

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

[Subir ˄](#utilidades-proporcionadas-por-easymariadb)|

## Change own password

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

[Subir ˄](#utilidades-proporcionadas-por-easymariadb)|


|[< Crear una base de datos y conectarse a ella](crearbd.md) | [Índice](index.md#índice) | [Índice de la ayuda](ayuda.md) |


