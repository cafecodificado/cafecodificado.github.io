---
published: true
title: Mudando a cor do Statusbar
layout: post
---
<center>
<img src="http://static.martinadamko.sk/files/28b2720ce5d0d2901c814f356f3c12e100bc91d9ad83a9888f449f29ce8d1970-1425x707.png" width="85%" title="Adcionando cor ao statusbar" alt="Cordova statusbar">
</center>

<br><br>

> Um tutorial simples, de como mudar a cor do statusbar


A partir das versões 5X do android, agora é possivel alterar a cor do Statusbar, como acontecia no IOS.

Primeiro vamos adicionar o plugin Statusbar:

```cordova plugin add cordova-plugin-statusbar```

ou

```cordova plugin add https://github.com/apache/cordova-plugin-statusbar.git```


Existe dois modos de alterar o Statusbar, uma bem simples, declarando a preference no arquivo config.xml. 

```<preference name="StatusBarBackgroundColor" value="#ff0000" />
```

No exemplo estou utilizando a cor RED em hexadeciamal, ficou assim: #ff0000.

A própria documentação, mostra que é possível utilizar palavras de cores reservadas, como RED, BLUE, YELLOW e etc, mas em alguns testes que eu realizei, em alguns dispositivos não funcionou, então fica a dica! USE SEMPRE HEXADECIMAL!

O outro modo é iniciar a function que altera a cor do Statusbar, eu normalmente coloco dentro do .run do app.js do ionic, pois essa função inicializa junto com todas as diretrizes do app

<script src="https://gist.github.com/godrix/f536d4653289e05b4960b5a9db34599b.js"></script>

Então é isso ai, bem simples não? 

by [@cgodrix](https://twitter.com/@cgodrix)

##### Links


[ngCordova](http://ngcordova.com/docs/plugins/statusbar/)

[Apache Cordova](https://cordova.apache.org/docs/en/3.1.0/config_ref/)





