---
layout: post
title:  "Notas sobre mi .bashrc"
date:   2016-08-02 15:05:00 -0300
categories: Software Libre
---

Para levantar mi mongo:
{% highlight ruby %}
  mongod --storageEngine=mmapv1 --dbpath /home/sublime/db/
{% endhighlight %}



Sobre mi sitio Jekyll:
{% highlight ruby %}
  # Para configurar el path donde se encuentran los binarios
  export PATH=$PATH:/home/sublime/.gem/ruby/2.3.0/bin
  #export GEM_HOME=$(ruby -e 'print Gem.user_dir')
  #export GEM_PATH=/home/sublime/.gem/ruby/2.3.0
  # Para levantarlo
  bundle exec jekyll serve --host=10.2.26.117
{% endhighlight %}

Para configurar la salida por mi proxy local:
{% highlight ruby %}
  # Configuro el proxy.
  export http_proxy=http://127.0.0.1:3128/
  export https_proxy=http://127.0.0.1:3128/
{% endhighlight %}


