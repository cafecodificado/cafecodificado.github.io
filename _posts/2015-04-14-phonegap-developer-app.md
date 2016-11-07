---
published: true
title: Aquele sobre PhoneGap Developer App
layout: post
---

<center>
<img src="https://blodrix.github.io/public/resources/images/phonegap-developer-app-hero.png" width="100%" title="" alt="">
</center>

Eu nunca pensei que iria usar tantas coisas da Adobe, aquela empresa dona do cara rápido da DC, mas ultimamente com o brackets e o que estão fazendo com o PhoneGap, estou gostando dela mas ainda não sou um bitch da Adobe.

Vou apresentar um recurso indispensável para quem pretende tirar o máximo de proveito do PhoneGap o [PhoneGap Developer App](https://github.com/phonegap/phonegap-app-developer).

PhoneGap Developer App é um aplicativo para [Android](https://play.google.com/store/apps/details?id=com.adobe.phonegap.app), [iOS](https://itunes.apple.com/us/app/phonegap-developer/id843536693?mt=8) e [Windows Phone](http://www.windowsphone.com/en-us/store/app/phonegap-developer/5c6a2d1e-4fad-4bf8-aaf7-71380cc84fe3) capaz de rodar aplicações que estão sendo desenvolvidas através deste framework.

É possível rodar um servidor em rede local que poderá ser acessado pelo PGDA e com isso testar e utilizar o aplicativo em tempo real, direto no smartphone ou tablet. Isso tudo sem downloads e uploads do App. Todo o processo é feito via rede wireless.

O único requisito é o computador que esta sendo utilizado no desenvolvimento estar na mesma rede do dispositivo mobile. No site oficial do PGDA você encontrará toda a documentação necessária para utilizar o recurso. Não fique preocupado, tudo é muito simples.


<center>
<img src="https://blodrix.github.io/public/resources/images/PhoneGap_Developer_App_Mobile.jpg" width="100%" title="" alt="">
</center>

É só entrar na pasta onde foi criado o projeto em PhoneGap e executar um comando: phonegap serve (serve mesmo, não server)
```
$ phonegap serve
```

No terminal sera gerado um endereço de ip, onde sera colocado no aplicativo, muito simples, todas as alterações feitas no projeto são automaticamente alterada no app.

Para cancelar aperte ```control + c``` no terminal de comando

Viu? muito simples, melhor do que esperar um ano para o emulador do Android ser aberto. =)

@carlosgodri
