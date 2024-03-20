---
title: EasyMariaDB
---

| [ Español ](index.md) ![Jekyll](/img/spain.png) | [ English ](EN_index.md) ![Jekyll](/img/england.png)

|[< Introeduction](index.md#introduction) | [Index](EN_index.md) | [EasyMariaDB help>](En_ayuda.md) |

# Understanding client-server architecture

## Server and client

If from Base we connect to a MariaDB or MySQL database server, we are using the client server architecture.

Without wanting to be very technical or precise in the explanations, the client server architecture consists of two parts, one part, the server part, provides some services and another part, the client part, consumes them.

In our case, MariaDB or MySQL act as the server part and provide some services; the first one that we see more clearly and, therefore, easier to understand, is the access to the data, but they provide other services, as, for example, the management of users or of the permissions of access to the data.

On the other hand, the client side, in our case Base, consumes the services provided by the server. Base asks the server for the data, the server provides it and Base displays it, either in a table directly or through queries, forms or reports. In addition, with user and permissions management services, the server may only provide some data or none at all, or allow data to be modified or only read.

Being a server or a client does not depend on one part being installed on a computer configured as a server and the other not, in fact both parts can be installed on the same computer and this can be a normal desktop computer or a laptop. As I said before, the server part is the one that provides some services and the client part is the one that consumes them, independently of where each part is installed.

## The server side

In our case the server is going to be a MariaDB database server or a MySQL server. 

As we have seen before, it can be installed on any computer. If all we need is a reliable database that provides us with other services such as user management or data access permissions, we can install MariaDB or MySQL on the same computer where we are going to work. The resource consumption of either server is low and you do not need a particularly powerful computer.

If we also need our database to be multi-user, the installation of the chosen database server must be done on a computer to which all the users who need to access the data have access. As we have already seen, it does not need to be a particularly powerful computer (unless hundreds of users are going to connect). For example, in a small business with four or five computers, the installation can be done on any of the computers and the rest can access the data. The only thing necessary is that, of course, the computer running the server must be turned on in order to access the data.

## The client side

Our client side will be one or more Base .odb files configured to connect to the server. 

We have to understand that while the data, i.e. the tables and their contents (and also the views), reside on the server, the rest of the elements (forms, queries and reports) are stored in the Base .odb file. Therefore, if we accidentally delete or corrupt the .odb file, we will lose the reports, queries and forms, but we will not lose the data: the data is safe on the server, provided, of course, that the server is intact. This provides a certain degree of security.

It is also important to know that while in the built-in HSQL or Firebird database files, you have to save the tables and also the .odb file so that the data is effectively saved in the database (and if you do not save them you can lose the data of a whole session), in the case of connecting to MariaDB or MySQL servers, the data is automatically saved after the edition of each record, when you move to another record, so you do not need to save the tables or the . odb file, it is only necessary to save the last edited record, so in case of an unexpected failure of any kind, the loss of work (data) would be minimal.

Earlier I said that on the client side we can have one or several .odb files. Actually, to be more precise, the possibilities are that several or all users access through the same .odb file or that each user has its own .odb file. Let's look at the differences between the two cases.

### A single Base .odb file for multiple users

If the same file is to be used by several or all users, it must be in a location on the network that can be accessed by the users who need it.

In this case, by sharing the same file, users will share the same forms, reports and queries, but only the first user to access the file will be able to modify these items. This should not be a problem, since once you have created the forms, queries and reports you need, you will normally not need to modify them. In fact, my recommendation in this case is that, once all the necessary elements have been created, the file should be set to read-only for all users. 

The fact that the file is read-only means that the user will not be able to modify the .odb file, and therefore will not be able to modify the reports, forms or queries, but will be able to modify the data, since it resides on the server and not in the .odb file.

### Each user has his or her own Base .odb file

If the user has his own .odb file, he is free to create and modify his own forms, reports and queries, which will be different from those of another user; but the data, which, as we know, resides on the server, will be the same for all users. This way of accessing data is convenient when each user has different needs, for example a user in the personnel office can create his own elements for access to employee tables, salaries and payrolls, etc, while the accounting manager can create his own elements for access to invoicing, bank accounts, etc.

This system provides more flexibility, but also more work to prepare forms and other elements.

|[< Introduction](EN_index.md#introduction) | [Index](EN_index.md) | [Install the extension >](EN_instalarextension.md) |
