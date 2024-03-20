---
title: EasyMariaDB
---

| [ Español ](index.md) ![Jekyll](/img/spain.png) | [ English ](EN_index.md) ![Jekyll](/img/england.png)

# Create a database and connect to it

Once you have fulfilled the prerequisites, follow these steps

1. In order to access the EasyMariaDB menu, you must open any of the LibreOffice applications, except Math. To be able to access from Base, you must also open a Base .odb file, but this will not be the database connection file, we will create one later.
2. Pull down the **Tools > EasyMariaDB** menu.
3. Select _New database_ to create a [database](#new-database).
4. Once the database is created, create at least one [user](#new-user) of the database with the required ones. To be able to create tables, it is necessary to have at least _Advanced_ permissions.
5. Connect to the new database as follows:
  - Select the **File > New > Database** menu. The _Database Wizard_ appears.

Translated with www.DeepL.com/Translator (free version)

![Jekyll](/img/con1.png)

  - Seleccione _Conectar con una base de datos existente_ y en la lista desplegable, seleccione _MySQL_. Haga clic en _Siguiente_.

![Jekyll](/img/con2.png)

  - Seleccione _Conectar directamente_ y haga clic en _Siguiente_.

![Jekyll](/img/con3.png)

  - Escriba el _Nombre de base de datos_ creada en los pasos anteriores y los datos del _Servidor_ y _Puerto_. El nombre del servidor es generalmente el nombre del equipo en el que está instalado el servidor de base de datos; si accede desde el mismo equipo, puede escribir _localhost_. El puerto, es el que configuró en la instalación del servidor.

![Jekyll](/img/con4.png)

  - Escriba el _Nombre de usuario_ y marque la casilla _Contraseña obligatoria_.

![Jekyll](/img/con5.png) 

  - Decida si registrar o no la base de datos y qué hacer al finalizar el asistente. Haga clic en _Finalizar_ y guarde el archivo .odb en un lugar conveniente.

![Jekyll](/img/con6.png)

Abra el archivo .odb recién creado y comience a trabajar con su nueva base de datos.

| [< Prerequisites](EN_requisitos.md) | [Indedx](EN_index.md#index) | [Help index](EN_ayuda.md) | [EasyMariaDB Utilities >](EN_utilidades.md) |
