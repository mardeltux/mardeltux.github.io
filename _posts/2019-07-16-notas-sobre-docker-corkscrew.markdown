---
layout: post
title:  "notas sobre docker and corkscrew"
date:   2019-07-16 09:05:00 -0300
categories: Software Libre
---

docker run --restart unless-stopped -p 127.0.0.1:3128:3128 --name cntlm -e CNTLM_USERNAME=jhon.doe -e CNTLM_DOMAIN=nirvana.com -e CNTLM_PROXY_URL=xx.xx.xx.xx:8080 -e CNTLM_PROXY_PORT=3128 -e CNTLM_PASSNTLMv2=B93elpasswordhasheadoWB8 -d jaschac/cntlm

ssh -v -TND 8080 jhondoe@xxx.xxx.xxx.xxx -o "ProxyCommand corkscrew 127.0.0.1 3128 xxx.xxx.xxx.xxx 443"

ssh -v -p 443 jhondoe@xxx.xxx.xxx.xxx -o "ProxyCommand corkscrew 127.0.0.1 3128 xxx.xxx.xxx.xxx 443"
