---
published: true
title: Aquele sobre Crosswalk
layout: post
---
![Aquele sobre Crosswalk](https://crosswalk-project.org/assets/identity/crosswalkproject-logo-horizontal-dark.png)

<br><br>

### Mas que p☠rr@ é o Crosswalk?


O Crosswalk é um wrapper do projeto Chromium para Android, contando com as mesmas características do navegador, criando uma webview com mais compatibilidade com as aplicações, os dispositivos Android com versões 4X e inferior sao equipados com webview diferente do mantido pelo Google, muitas vezes não recebendo atualizações das fabricantes, e com pouco compatibilidade com os recursos atuais, diferente da versão 5X e superior, que tem o webview como um app, mantido pelo Google, recebendo atualizações diretamente da Google Play.

Apesar de se basear no Chromium para Android, o Crosswalk possui alguns diferenciais próprios:

* Não é mostrada a barra de endereços e abas, pois o projeto funciona em tela cheia, como se fosse um aplicativo nativo. Então, não é preciso usar a ação Request fullscreen do objeto Browser.
* No Chrome para Android, uma música só pode ser iniciada com um evento de toque. Já no Crosswalk a música pode ser tocada a qualquer momento.
* No Crosswalk é possível usar as condições On back button, On menu button e On search button do objeto Browser (funcionam apenas no projeto exportado). No navegador estas condições não funcionam.

Para instalar o Crosswalk na sua aplicacao é bem simples, apenas instale o plugin

```$ cordova plugin add cordova-plugin-crosswalk-webview
```

ou

```$ ionic browser add crosswalk
```

Você também pode adicionar o plugin de forma mais fácil ainda, se você estiver usando o intelXDK, basta dar um check no input.

![](https://ionickers.github.io/public/images/crosswalk.png)

> O Crosswalk garante compatibilidade para Android antigos, MASSS...

![](https://49.media.tumblr.com/tumblr_maqoftf6T31r2a5r0o1_500.gif)

Ao adicionar o Crosswalk em sua aplicação, sera adicionado um webview, o que ocasionará em mais ou menos 20 MB a mais em sua aplicação, então não esqueça de na hora de subir para os marketplace, faça a build de seus apps com o Crosswalk e sem, para os dispositivos que não necessitam do Crosswalk para deixar mais leve.



[Project Crosswalk](https://crosswalk-project.org)

[IntelXDK](https://software.intel.com/pt-br/intel-xdk)

[Multiple APK Support](http://developer.android.com/google/play/publishing/multiple-apks.html)