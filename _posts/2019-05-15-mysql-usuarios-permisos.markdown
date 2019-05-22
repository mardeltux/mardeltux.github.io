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
