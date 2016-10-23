---
layout: post
title:  "Notas sobre archlinux"
date:   2016-09-16 13:27:00 -0300
categories: Software libre
---

Scheme sobre particionado BIOS/GPT:

````
parted /dev/sdx
(parted) mklabel gpt
(parted) mkpart non-fs 0% 2MiB
(parted) mkpart primary ext4 2MiB 20GiB
(parted) mkpart primary linux-swap 20GiB 24GiB
(parted) mkpart primary ext4 24GiB 100%

(parted) set 1 bios_grub on
(parted) set 2 boot on
(parted) quit
````

Formatear y activar la swap

````
mkswap /dev/sdx3
swapon /dev/sdx3
````

Fuente:
[Sobre swap](https://wiki.archlinux.org/index.php/Swap)
[Sobre GNU_Parted](https://wiki.archlinux.org/index.php/GNU_Parted)
[Leendo template de ejemplo](https://wiki.archlinux.org/index.php/Installing_Arch_Linux_on_ZFS)
