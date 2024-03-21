---
title: EasyMariaDB
---

| [ Español ](index.md) ![Jekyll](/img/spain.png) | [ English ](EN_index.md) ![Jekyll](/img/england.png)

# Create a database and connect to it

Once you have fulfilled the prerequisites, follow these steps

1. In order to access the EasyMariaDB menu, you must open any of the LibreOffice applications, except Math. To be able to access from Base, you must also open a Base .odb file, but this will not be the database connection file, we will create one later.
2. Pull down the **Tools > EasyMariaDB** menu.
3. Select _New database_ [to create a database](EN_utilidades.md#create-a-database).
4. Once the database is created, [create one user](EN_utilidades.md#create-a-user) of the database with the required permissions to be able to create tables, it is necessary to have at least _Advanced_ permissions.
5. Connect to the new database as follows:
  - Select the **File > New > Database** menu. The _Database Wizard_ appears.

![Jekyll](/img/con1.png)

  - Select _Connect to an existing database_ and from the drop-down list, select _MySQL/MariaDB_. Click _Next_.

![Jekyll](/img/con2.png)

  - Select _Connect directly_ and click _Next_.

![Jekyll](/img/con3.png)

  - Type the _Database name_ created in the previous steps and the _Server_ and _Port_ data. The server name is usually the name of the computer on which the database server is installed; if accessing from the same computer, you can type _localhost_. The port, is the one you configured in the server installation.

![Jekyll](/img/con4.png)

  - Enter the _User name_ and check the _Password required_ box.

![Jekyll](/img/con5.png) 

  - Decide whether or not to register the database and what to do at the end of the wizard. Click _Finish_ and save the .odb file in a convenient location.

![Jekyll](/img/con6.png)

Open the newly created .odb file and start working with your new database.

| [< Prerequisites](EN_requisitos.md) | [Index](EN_index.md#index) | [EasyMariaDB help index](EN_ayuda.md) | [EasyMariaDB Utilities >](EN_utilidades.md) |
