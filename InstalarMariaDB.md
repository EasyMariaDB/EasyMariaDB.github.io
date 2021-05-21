# Instalación de MaríaDB

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
sudo mysql_secure_instalation
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


