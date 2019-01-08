Nombre del rol
==============
Descripcion breve del rol.

Procedimiento
=============

Procedimiento para agregar nuevos servidores al rol y procedimiento de uso del rol. 

Cambios en ansible
------------------

Cambios en inventario
---------------------

Cambios en monitoreo
--------------------

Cambios en runbook
------------------

Cambios en otras planillas
--------------------------

Requerimientos
--------------

Roles:
  velneo_server
  postfix_client (uses localhost tcp 25 for smtp)

Variables
---------

Variables necesarias para ejecutar el rol.

Tags
----

Breve descripcion de cada una de las tags del rol.

Dependencias
------------

Los roles de los que depende.

Ejemplo en Playbook
-------------------

Incluir un ejemplo de como agregar el rol a un playbook.

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

Afecta
------

Archivos de sistema o servicios que este rol afecte y que sea necesario aclarar para no interferir con otros roles.

Licencia
--------

Aclarar la licencia.

Informacion del autor
---------------------

Informacion opcional del autor.

Troubleshooting
---------------

```text
Fri 2017/07/28 15:57:39 gammu-smsd[2316]: SMS sent on device: "/dev/ttyS0" status=500, reference=-1
Fri 2017/07/28 15:57:39 gammu-smsd[2316]: Error getting send status of message: Unknown error. (UNKNOWN[27])
```

When you get status=500, is probably that you are getting some network denied to register to the GSM/3g/4g provider.
Test the chip with some other phone to get more details or try to activate logs for these messages: `Logformat = textall` on `[gammu]` device section. https://wammu.eu/docs/manual/config/index.html#fully-documented-example
