# Instalación de MaríaDB

[Instalar MariaDB en Linux](#instalar-mariadb-en-linux)

[Instalar MariaDB en Windows](#instalar-mariadb-en-windows)

## Instalar MariaDB en Linux

Como no podemos abarcar la instalación en todas las distribuciones de Linux, en este documento explicaremos como instalar MariaDB en Ubuntu y sistemas derivados. Si usted tiene otra distribución de Linux diferente, puede que tenga que adaptar las órdenes a su sistema.

Para comenzar con la instalación de MariaDB abra un terminal, y en dicho terminal ejecute el siguiente comando:

```
sudo apt install mariadb-server
```
Comenzará la instalación de MariaDB

![Jekyll](/img/mariadb1.png)

Una vez que ha finalizado la instalación, para asegurar la instalación de MariaDB, ejecute el siguiente comando:
```
sudo mysql_secure_installation
```
Al ejecutar el comando aparecerá el siguiente mensaje.

![Jekyll](/img/mariadb2.png)

Tras el primer mensaje, se solicita la contraseña del usuario *root*. Se trata de la contraseña del usuario *root* de MariaDB, y no la del usuario *root* del sistema operativo. Como aún no hemos configurado una contraseña para este usuario, estará en blanco. Pulse *Intro* sin escribir nada para continuar.

Aparece un nuevo mensaje preguntando si deseamos configurar una contraseña para el usuario *root*. 

![Jekyll](/img/mariadb3.png)

Escriba *Y* o pulse *Intro* para configurar la contraseña. Escriba la contraseña dos veces. En realidad esta contraseña no tiene efecto porque, por defecto, MariaDB viene configurada para utilizar la identificación por *sockets*, que no usa contraseñas de usuario.

A continuación se muestran una serie de preguntas relacionadas con la seguridad de MariaDB. Lo mejor es que conteste *Y* a todo (o simplemente pulse *Intro*).

![Jekyll](/img/mariadb4.png)

Una vez finalizado el programa tendremos nuestra instalación de MaríaDB un poco más segura.

Aunque había prometido no tener que lidiar con comandos SQL, debido al sistema de identificación por *sockets*, para poder conectar al servidor MariaDB, necesitamos configurar un usuario con permisos de administrador. No se preocupe, esto tendremos que hacerlo solamente una vez.

En una pantalla de terminal, escriba:
```
sudo mariadb
```
Al pulsar *Intro*, tras un mensaje de bienvenida, aparece el indicador *MariaDB [(none)]>*, indicando que ahora nos encontramos en el terminal de MariaDB.

![Jekyll](/img/mariadb5.png)

Para poder conectar con MaríaDB desde lugares diferentes a este terminal, necesitamos crear un usuario y otorgarle los permisos necesarios.

Primero creamos el usuario y su contraseña. Escriba el siguiente comando y pulse *Intro*; puede sustituir el nombre de usuario *admin* por cualquier nombre elegido por usted, por supuesto debe cambiar la contraseña *password* por otra contraseña. Las comillas simples que rodean el nombre de usuario y la contraseña, forman parte del comando, por lo que debe escribirlas. Dese cuenta que el comando finaliza con punto y coma (;).
```
create user 'admin' identified by 'password';
```
Si todo es correcto, aparecerá el mensaje *Query OK* seguido del número de filas afectadas, en este caso 0.

![Jekyll](/img/mariadb6.png)

A continuación daremos todos los permisos en todas las bases de datos al usuario creado; es decir, vamos a crear un usuario administrador, con todos los permisos posibles. Escriba el siguiente comando, y a continuación pulse *Intro*.
```
grant all on *.* to 'admin' with grant option;
```
Nuevamente, si todo es correcto, aparecerá el mensaje *Query OK*.

![Jekyll](/img/mariadb7.png)

Para asegurarnos que los permisos son efectivos inmediatamente, escriba el siguiente comando, y a continuación pulse *Intro*.
```
flush privileges;
```

![Jekyll](/img/mariadb8.png)

Ya, para finalizar, escribimos el siguiente comando para salir del terminal de MariaDB, tras el comando pulse *Intro*.
```
exit;
```
Regresaremos al terminal de Linux.

![Jekyll](/img/mariadb9.png)

Queda así finalizada la instalación y configuración de MariaDB. Recuerde el nombre de usuario y la contraseña configurada en estos últimos pasos pues será necesaria para conectar con MariaDB desde LibreOffice.

## Instalar MariaDB en Windows

Descargue MariaDB de la página oficial de descargas https://mariadb.org/download/.

Una vez descargado el instalador ejecútelo. En primer lugar aparecerá una página de bienvenida.

![Jekyll](/img/mariadbwin1.png)

Haga clic en _Next_.

![Jekyll](/img/mariadbwin2.png)

A continuación se muestra la licencia, debe marcar la opción _I accept the termns in the License Agreement_ y haga clic en _Next_.

![Jekyll](/img/mariadbwin3.png)

Si lo desea, en _Third party tools_ puede marcar la opción _Entire feature will be unavailable_ para no instalar el programa HeidiSQL, no lo vamos a necesitar. Haga clic en _Next_.

![Jekyll](/img/mariadbwin4.png)

En la siguiente pantalla, deje marcado _Modify password for database user 'root'_ y escriba una contraseña, repita la contraseña en el siguiente cuadro de texto. Recuerde la contraseña, pues la necesitará más adelante. En este paso también debe marcar la opción _Use UTF8 as default server's character set_. Para mayor seguridad, deje sin marcar la opción _Enable access from remote machines for 'root' user_. Haga clic en _Next_.

![Jekyll](/img/mariadbwin5.png)

Si no tiene ninguna razón para ello, deje todo como está en la pantalla de configuración de la instancia. Haga clic en _Next_.

![Jekyll](/img/mariadbwin6.png)

Ya está todo listo para comenzar la instalación. Haga clic en _Install_, aparecera una ventana de confirmación de Windows, acepte para continuar con la instalación.

![Jekyll](/img/mariadbwin7.png)

Comenzará la instalación.

![Jekyll](/img/mariadbwin8.png)

Cuando la instalación haya finalizado, aparece una ventana informando de ello. Haga clic en _Finish_ par finalizar la instalación.

### Configurar MariaDB para que muestre los mensajes en español

Por defecto, todos los mensajes de MariaDB son en inglés, pero se puede configurar para que los mensajes sean en español. Para ello es necesario modificar, si existe, un archivo llamado _my.ini_; si el archivo no existe hay que crearlo.

El archivo _my.ini_ debe ser un archivo de texto plano, sin formato. Se puede crar o modificar con el *Bloc de notas*. Puede estar localizado en varios lugares, pero en nuestra experiencia, lo mejor es situarlo en la carpeta de datos de MariaDB, situada generalmente en "C:\Program Files\MariaDB XX.X\data\". Para configurar el archivo:
- Con el explorador de archivos naveguea hasta "C:\Archivos de programa\MariaDB XX.X\data\".
- Si no tiene visibles las extensiones de los archivos, en el menú del navegador de archivos seleccione *Vista* y marque la opción _Extensiones de nombre de archivo_.
- Si no existe el archivo _my.ini_, créelo:
  - Haga clic con el botón derecho del ratón en un lugar vacío de la carpeta.
  - En el menú emergente seleccione **Nuevo > Documento de texto**.
  - Cambie el nombre del archivo a _my.ini_ (escríba el nombre en minúsculas).
- Abra el archivo _my.ini_ haciendo doble clic sobre él.
- Si el archivo ya existia, busque la sección [mariadb]  y si no la encuentra o acaba de crear el archivo añada una línea con el texto (incluidos los corchetes):
```
[mariadb]
```
- En la sección [mariadb] añada la siguiente línea: 
```
lc_messages=es_ES
```
- Cierre el archivo y guarde los cambios.
- Reinicie el ordenador para que los cambios surtan efecto.

El archivo _my.ini_ deberá pareceerse a esta imagen:

![Jekyll](/img/mariadbwin9.png)
