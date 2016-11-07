---
published: true
title: Phonegap Removendo delay de toque
layout: post
---
<center>
<img src="https://build.phonegap.com/images/marketing/build-diagram.png" title="Phonegap é fod* pa baralho!" width="100%"/>
</center>

Desenvolver apps Híbridas sem a ajuda de um framework que tenham, todas as particularidades nas plataformas é um caso de dependência de várias técnicas, se você está nesse campo à um bom tempo, sabe que essa tarefa as vezes depende muito de bibliotecas e pequenos scripts em Javascript para fazer funcionar de uma forma nativa.

Um dos problemas enfrentados é o famoso Delay dos 300ms, esse problema afeta tanto apps híbridas como as feitas em Titanium, Cordova, etc, como os "site-apps" nos navegadores.

Quando eu começei a criar um aplicativo do `Guia dos mochileiro das galáxias`, apresentava esse problema, dando uma aparência de lentidão e quebrado, coisa que tirava toda a experiência de se criar algo ao estilo nativo. Na época eu resolvi com algumas técnicas relacionadas a CSS, melhorou, mais não tanto quanto depois usando o FastClick.

O [FastClick](https://github.com/ftlabs/fastclick) resolve esse problema, especialmente relacionado ao errinho do web-kit em dispositivos que tenham navegadores que usam ele como base, assim como o Webkit(WebView) do Apache Cordova.

>Antes de chamar qualquer biblioteca no Cordova, você deve esperar o evento “deviceReady”

Inclua o FastClick na dependência do seu projeto.<br/>

     ```javascript
        <script type='application/javascript' src='/path/to/fastclick.js'></script>
     ```



E em seguida inclua essa linha abaixo:

<table>
 <td border="2px">
     window.addEventListener('load', function() { <br/>
    FastClick.attach(document.body);<br/>
}, false);
 </td>
</table>

E como em um passe de mágica, sem precisar melhorar nada na performance, seu App já ganha de cara uns 10% até 20% de melhoria na responsividade do toque para a execução.
