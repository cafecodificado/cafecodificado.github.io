---
published: true
title: Emmet não é tecnlogia, é magia mesmo.
layout: post
---
<center>
<img src="http://upload.wikimedia.org/wikipedia/en/9/97/Doc_Brown.JPG" title="Ops não esse!" alt="Prof Emmett" width="80%">
</center>
***Descupe Dr. Emmett Brown, mas não é do senhor que vamos falar...***

<center>
<img src="http://www.n8d.at/blog/wp-content/uploads/2014/11/emmet.io_.jpg" width="100%" title="Emmet tools for developers" alt="Emmet tools for developers">
</center>

<hr>
Bora falar sobre o Emmet, uma ferramenta que é, indispensável, e utilizado por muitos desenvolvedores que já tenha boa experiência. 
<br>
Não é um pré-processador como o LESS, porém ele abrevia o modo como você escreve o HTML e CSS, pra que você se torne mais rápido ao codificar.
Escrito em Javascript puro (SIM JAVASCRIPT ```<3```) e podendo funcionar em diferentes plataformas, a ferramenta foi desenvolvida para os editores de códigos mais utilizados do mercado, como o **Sublime Text**, **Notepad++**, **Atom**, **Eclipse**, **Coda**, **Komodo Edit**, **NetBeans**, **Dreamweaver**(Por favor não use esse) e o meu xodó o [Brackets](http://brackets.io/), mais para frente farei um post sobre...

***Mas o que exatamente o Emmet faz?***

>Então chega de blá, blá, blá e vamos para o que interessa. 

O site do [Emmet.io](http://emmet.io/) diz;

>Abbreviations are the heart of the Emmet toolkit

ou seja <strike>cerveja</strike>

O que o Emmet faz de melhor é abreviar

Os *snippets* são totalmente dinâmicos. A medida que você escreve e aperta a tecla tab, a abreviação em Emmet é transformado na hora. Veja um exemplo bem simples:

Para um criar um documento HTML5 utilizando a abreviação Emmet, digite apenas ```html:5```, e tecle tab e a magica acontecerá! <strike>Não é magia é tecnologia!</strike> OPS clichê de propaganda não!

![html:5](https://blodrix.github.io/public/resources/images/code1.png  "html:5")
Para criar uma um menu com itens numerados, digite no editor ``` .menu>.item*5>a[href="#"]```. 

![](https://blodrix.github.io/public/resources/images/code2.png) 
Percebendo que é muito fácil entender como o emmet funciona e como ele escreve o HTML. 

Para nomear um elemento com classe, basta utilizar um ponto antes do nome, como no CSS. O mesmo vale para criar o elemento com ID, basta digitar o ```#``` antes do nome e teclar tab sempre.
O sinal de ```>```, serve para aninhar elementos, assim como o sinal de ```^``` serve para sair do aninhamento anterior. Exemplo: digite ```.menu>.item>a^.item2>h2```:
![](https://blodrix.github.io/public/resources/images/code3.png) 
O sinal de ```*``` serve para multiplicar a quantidade de um determinado elemento. O sinal de ```+``` serve para quebrar adicionar mais elementos e quebrar as linhas. Por exemplo, ao digitar ```#menu+.sidebar+.footer```:
![](https://blodrix.github.io/public/resources/images/code4.png) 
Parece complicado, mas com o passar do tempo e com prática, acaba ficando mais simples.

>CSS

No CSS, a ferramenta ajuda bastante na hora de escrever as propriedades. Pra quem já sabe decorado quase todas as propriedades do CSS, fica mais fácil até de deduzir qual abreviação utilizará para escrever o código. 

```#elemento {
     w200+h100+pos-a+t0+l0       //tecle tab depois de escrever isso
}```


Resultará nisso:


```#elemento {
     width: 200px;
     height: 100px;
     position: absolute;
     top: 0;
     left: 0;
}
```
<center>
<img src="http://media.tumblr.com/35b625bfac2c9521d57fa44a8d561f91/tumblr_inline_n851dfII0R1sr1i40.gif" width="100%" title="Isso é lindo" alt="Isso é lindo">
</center>


*São uma porrada de abreviações que o Emmet possui e ainda permite que você mesmo crie suas próprias abreviações. Na [Documentação](http://docs.emmet.io/abbreviations/) você pode ler todas as abreviações disponíveis.*

***Então vai lá e de uma olhada.***

