---
layout: post
title:  "Notas sobre git"
date:   2016-08-02 14:50:00 -0300
categories: Software libre
---

Para subir al repositorio:

{% highlight ruby %}
  git add .
  git commit
  git push origin master
{% endhighlight %}

Siemre antes de subir debemos traernos todo:
{% highlight ruby %}
  git pull --rebase origin master
{% endhighlight %}
