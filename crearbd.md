---
title: EasyMariaDB
---

| [ Español ](index.md) ![Jekyll](/img/spain.png) | [ English ](EN_index.md) ![Jekyll](/img/england.png)

# Crear una base de datos y conectarse a ella

Una vez cumplidos los requisitos previos, siga los siguientes pasos

1. Para poder acceder al menú de EasyMariaDB, debe abrir cualquiera de las aplicaciones de LibreOffice, excepto Math. Para poder acceder desde Base, además, debe abrir un archivo .odb de Base, pero este no será el archivo de conexión a la base de datos, sino que crearemos uno más adelante.
2. Despliegue el menú **Herramientas > EasyMariaDB**
3. Seleccione _Nueva base de datos_ para crear una [base de datos](utilidades.md#nueva-base-de-datos).
4. Una vez creada la base de datos, cree al menos un [usuario](utilidades.md#nuevo-usuario) de la base de datos con los necesarios. Para poder crear tablas, es necesario tener al menos permisos _Avanzados_.
5. Conecte con la nueva base de datos del siguiente modo:
  - Seleccione el menú **Archivo > Nuevo > Base de datos**. Aparece el _Asistente de bases de datos_.

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

| [< Requisitos previos](requisitos.md) | [Índice](index.md#índice) | [Ayuda de EasyMariaDB](ayuda.md) | [Utilidades de EasyMariaDB >](utilidades.md) |
