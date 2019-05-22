---
layout: post
title:  "youtube-dl"
date:   2019-03-15 12:16:00 -0300
categories: dev
---
# Gracias por existir youtube-dl!
Cortar extacto de video

````
youtube-dl --postprocessor-args "-ss 00:11:13.00 -t 00:4:2.00" https://www.youtube.com/watch?v=nI_owrxLoOQ&feature=youtu.be
````
````
youtube-dl --postprocessor-args "-ss 00:11:13.00 -t 00:4:2.00" -i --extract-audio --audio-format mp3 --audio-quality 0 https://www.youtube.com/watch?v=nI_owrxLoOQ&feature=youtu.be
````
