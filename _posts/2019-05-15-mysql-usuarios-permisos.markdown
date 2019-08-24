---
layout: post
title:  "Revisando permisos de usuarios en mysql"
date:   2019-05-15 6:05:00 -0300
categories: Dev
---

Listar usuarios
{% highlight ruby %}

{% endhighlight %}


Listar permisos de un usuario en particular
{% highlight ruby %}
SHOW GRANTS FOR 'algunusuario'@'%.example.com'
{% endhighlight %}


Revocar permisos
{% highlight ruby %}
REVOKE ALL ON *.* FROM 'algunusuario'@'%.example.com';
{% endhighlight %}


Otorgar permisos
{% highlight ruby %}
GRANT ALL ON algunadb.* TO 'algunusuario'@'algunlugar';
{% endhighlight %}
Se recomienda no usar ALL
{% highlight ruby %}
GRANT SELECT,INSERT,UPDATE,DELETE,CREATE,CREATE TEMPORARY TABLES,DROP,INDEX,ALTER ON algunadb.* TO 'algunusuario'@'algunlugar';
{% endhighlight %}

fuente: https://dev.mysql.com/doc/refman/5.7/en/creating-accounts.html

Crear base de datos
CREATE DATABASE databasename DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

GRANT SELECT, INSERT, UPDATE, DELETE, CREATE, DROP, INDEX, ALTER, CREATE TEMPORARY TABLES ON databasename.* TO 'username'@'localhost' IDENTIFIED BY 'password';

GRANT SELECT, INSERT, UPDATE, DELETE, CREATE, CREATE TEMPORARY TABLES, DROP, INDEX, ALTER ON databasename.* TO 'usuario'@'localhost' IDENTIFIED BY 'password';

CREATE DATABASE nomredelabase DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
GRANT SELECT, INSERT, UPDATE, DELETE, CREATE, DROP, INDEX, ALTER, CREATE TEMPORARY TABLES ON tribunal_disciplina.* TO 'nombredelabase'@'ip' IDENTIFIED BY 'clave';

Comprimir carpeta
tar -cvf archivo.tar /dir/a/comprimir/
Descomprimir carpeta
tar -xvf archivo.tar
Descargar con wget/curl archivo de gdrive
wget "https://drive.google.com/uc?export=download&id=ide_del_archivo"
