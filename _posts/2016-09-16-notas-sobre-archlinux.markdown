---
layout: post
title:  "Notas sobre git"
date:   2016-09-16 13:27:00 -0300
categories: Software libre
---

Scheme sobre particionado BIOS/GPT:
{% highlight ruby %}
parted /dev/sdx
(parted) mklabel gpt
(parted) mkpart non-fs 0% 2MiB
(parted) mkpart primary ext4 2MiB 20GiB
(parted) mkpart primary linux-swap 20GiB 24GiB
(parted) mkpart primary ext4 24GiB 100%

(parted) set 1 bios_grub on
(parted) set 2 boot on
(parted) quit
{% endhighlight %}

Formatear y activar la swap
{% highlight ruby %}
mkswap /dev/sdx3
swapon /dev/sdx3
{% endhighlight %}

Fuente:
https://wiki.archlinux.org/index.php/Swap
https://wiki.archlinux.org/index.php/GNU_Parted
https://wiki.archlinux.org/index.php/Installing_Arch_Linux_on_ZFS
