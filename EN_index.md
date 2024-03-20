---
title: EasyMariaDB
---

| [ Español ](index.md) ![Jekyll](/img/spain.png) | [ English ](EN_index.md) ![Jekyll](/img/england.png)

# Index
- [Introduction](https://#introduction)
- [What is EasyMariaDB](#what-is-easymariadb)
- [Understanding client-server architecture](EN_clienteservidor.md)
- [Install the extension](EN_instalarextension.md)
- [EasyMariaDB Help](EN_ayuda.md)
  - [Prerequisites](EN_requisitos.md)
  - [Create a database and connect to it](EN_crearbd.md)
  - [Utilities provided by EasyMariaDB](En_utilidades.md)

# Introduction
Soon after I started using LibreOffice Base, I discovered that the built-in HSQLDB database, with use, was giving errors due to corruption of the .odb file. To avoid this, several web sites recommended making a separate database.

To solve the HSQLDB database corruption problems, LibreOffice started to incorporate the Firebird database, but, at the moment, the integration of this database is not complete and is in experimental mode.

Later, I also discovered that these built-in databases are single-user, that is, the database cannot be opened by two (or more) users simultaneously.

No problem, I said to myself, LibreOffice Base has infinite possibilities to connect to reliable and highly tested database servers. 

I had little trouble installing different database servers on my computer to test which one would be most useful to me. I soon realized that, although the installation and connection to the servers had been relatively easy, if I wanted to create a database I needed to create it from a command line program, in which I also had to write SQL statements, which at that time I did not know. To top it off, the SQL statements were not exactly the same for some servers than for others, some with double quotes, others with single ones... In the end I got discouraged and stopped using Base.

Recently, in a Telegram channel, I saw again the usual questions: Is Base reliable? Is it multi-user? And the (wrong) answer was no to both questions. I say the answer is wrong because reliability and multi-user capability is not provided by Base, but by the database server you connect to, either a built-in server or an external one.

So I made the decision to try to prove that Base can be reliable and multi-user and my challenge is that, in addition, setting up a database server is easy and can be done by any user without advanced knowledge. For this reason I created **EasyMariaDB**.


# What is EasyMariaDB?

The **EasyMariaDB** tool is a LibreOffice extension designed to facilitate the creation of databases and users on a MariaDB or MySQL server from LibreOffice, without using other programs or the command console.

It is designed to be used with either a MariaDB server or a MySQL server. Both servers are fast, reliable and secure and have at least one version that is free software and can be downloaded and installed free of charge. In addition LibreOffice Base has a built-in native connector that makes it very easy to connect to either of these two servers.

By using either of these servers together with LibreOffice Base we will get, as was our goal, reliable, secure and multi-user databases, and together with the **EsayMariaDB** extension, easy to get up and running.

After [installing the extension](EN_instalarextension.md), a new option, EasyMariaDB, is generated in the Tools menu of all LibreOffice applications except Math. This submenu gives access to the [utilities](EN_utilidades.md) provided by EasyMariaDB

|[< Introduction](EN_index.md#introduction) | [Index](EN_index.md#index) | [Understanding client-server architecture >](EN_clienteservidor.md) |
