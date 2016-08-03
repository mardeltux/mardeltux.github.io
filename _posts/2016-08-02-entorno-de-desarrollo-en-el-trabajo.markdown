---
layout: post
title:  "Entorno de desarrollo en el trabajo"
date:   2016-08-02 15:35:00 -0300
categories: Software Libre
---

Logre generar mi entorno de desarrollo a duras penas en mi trabajo sobre un triste entorno llamado guindows.
En primer lugar utilizando virtualbox instale una maquina virtual con un Archlinux a la cual le accedo 
facilmente gracias a al cliente ssh que trae gitbash la cual me genera una hermosa consola con transparencia y cliente ssh.
Luego instale un programa llamado VBoxVmService que levanta la maquina virtual como si fuera un servicio 
y ademas por otro lado tambien instale otro programa WinSshFs que monta automaticamente el home del la maquina virtual en el windows!

Ademas de eso hoy tuve que instalar un proxy local CNTLM para poder usar git ya que no podia clonar por un error ssl.
