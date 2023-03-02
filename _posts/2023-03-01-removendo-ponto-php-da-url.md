---
layout: post
title: Removendo a extensão .php das URLs com .htaccess
slug: 
categoria: php
---

Crie um arquivo e salve-o com o nome: **.htaccess** , ele deve ficar na raiz do site. Copie e cole o código abaixo:

    RewriteEngine on  
    RewriteCond %{REQUEST_FILENAME} !-d  
    RewriteCond %{REQUEST_FILENAME}\.php -f  
    RewriteRule ^(.*)$ $1.php

Obs.: Para que de certo o site *precisa estar* hospedado *em servidor apache.*

Agora, os links podem ser usados sem a extensão “.php”.
Exemplo com .php: https://gean.me/watch.php?v=ZhTcVe88koo
Exemplo sem .php: https://gean.me/watch?v=ZhTcVe88koo
