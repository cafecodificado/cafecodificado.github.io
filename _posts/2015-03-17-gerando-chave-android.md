---
published: true
title: Gerando Chave Privada Para Android
layout: post
---

<center>
<img src="https://blodrix.github.io/public/resources/images/androidKEY.jpg" width="40%" title="Chave de android, bahh dumm dishhh" alt="Android 18">
</center>
<center>
<small><b>Meus poderes de montagens, são mais de 8 MILLLLL</b></small>
</center><br>


Olá Pessoal, vou mostrar como é fácil gerar uma chave privada para, as suas aplicações feitas para Android, você vai precisar de apenas que ter o [JAVA JDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html), meu sistema operacional que estou usando é o Linux Mint, mas o processo é bem similar nos outros sistemas operacionais.

O sistema Android requer que todas as aplicações instaladas sejam assinadas digitalmente com um certificado cuja chave privada é mantida pelo desenvolvedor. O Android usa o certificado como um meio de identificar o autor da aplicação e estabelecer uma relação de confiança entre as aplicações.

O certificado não controla que aplicações o usuário pode instalar. Ele não precisa ser assinado por uma autoridade certificadora: é perfeitamente permitido, e tipico, aplicações Android usarem certificados auto-assinados.

Nesse tutorial vamos apenas gerar a chave privada, em outro tutorial vamos publicar um aplicativo desenvolvido com Phonegap (Mas isso é outro tema que vamos abordar mais para frente), então...
<center>
<img src="http://4.bp.blogspot.com/-q00t4wvXxT0/U6C6H2onupI/AAAAAAAAEt8/LaeM9_qQ78w/s1600/e+la+vamos+nos+pica+pau.jpg" width="30%" alt="E lá vamos nós...">
</center>

### Atenção

***Depois de gerada a chave siga as recomendações abaixo para manter a longevidade de sua aplicação, que estará publicada***

* Esteja em sua posse
* Represente a entidade pessoal, corporativa ou organizacional que será identificada com sua aplicação
* Tenha um período de validade que exceda o tempo de vida esperado da aplicação. Um período de validade de 25 anos é recomendado. Se você planeja publicar sua aplicação no Google Play, observe que um período de validade que termine depois de 30/11/2034 é necessário; Você não poderá fazer upload de um apk se este estiver assinada com uma chave cuja validade expire antes dessa data.
* Guarde a senha que você gerou assim como o Alias da aplicação.

<small>Caso tenha mais alguma dúvida, leia o artigo [Securing Your Private Key](http://developer.android.com/guide/publishing/app-signing.html#secure-key) </small>


####Chega de blá, blá porque agora é mão na massa.

Para gerar a chave vamos usar o comando e ferramenta do JDK o Keytool.

Vamos abrir o terminal  se preferir use o `Ctrl+Alt+t`:

`keytool -genkey -v -keystore "nomeDaChave.keystore" -alias NomeChave -keyalg RSA -validity 10000`

Precione `Enter`, digite a senha para a chave.

<center>
<img src="https://blodrix.github.io/public/resources/images/tela1.png" alt="tela com o comando keytool -genkey -v -keystore nomeDaChave.keystore -alias NomeChave -keyalg RSA -validity 10000" width="80%">
</center>

Logo em seguida aparecera informações que você deve preencher.

<center>
<img src="https://blodrix.github.io/public/resources/images/tela2.png" alt="tela com os dados para preenchimento" width="80%">
</center>

Depois pedira para confirmar com `Sim` ou `Não` seus dados e escolha a opção adequada...

Tudo ocorrendo com planejado, aparecerá um dialogo pedindo que você digite outra senha para a chave gerada, ou se quiser usar a mesma senha que colocou no começo apenas digite `RETURN`.

<center>
<img src="https://blodrix.github.io/public/resources/images/tela3.png" alt="tela para digitar a ultima senha" width="80%">
</center>

Como não escolhemos um diretorio, por padrão o `keytool` vai gerar a chave na pasta `home`

<center>
<img src="https://blodrix.github.io/public/resources/images/tela4.png" alt="tela com o arquivo salvo na pasta home" width="80%">
</center>

*Simples assim*

#### Mas o que significa cada comando do Keytool?

`keytool -genkey -v -keystore "nomeDaChave.keystore" -alias NomeChave -keyalg RSA -validity 10000`

>Vamos por partes<br>
<small><cite>- Morgan, Dexter</cite></small>

* `-genkey`<br>

***Gera um par de chaves (pública e privada)***

* `-v` <br>

***Ativa o modo verbose***

* `-keystore` <br>

***Um nome para a keystore que conterá sua chave privada.***

* `-alias` <br>

***Um apelido para a chave. Apenas os 8 primeiros caracteres do apelido são usados.***

* `-keyalg` <br>

***Algoritmo de encriptação usado para geração da chave. Tanto o DSA quanto o RSA são suportados.***

* `-validity` <br>

***O periodo de validade da chave, em dias. Um valor de 10000 ou maior é recomendado.***

Outros comando uteis, mas não necessários

* `-keysize` <br>

***O tamanho de cada chave gerada (bits). Se não fornecida, Jeytool usa um tamanha padrão de 1024 bits. Em geral, é recomendado uma chave de 2048 bits ou  maior.***

* `-dname` <br>

***Um nome único que descreva quem criou a chave. O valor é usado nos campos issuer e subject nos certificados auto-assinados.
Observe que você não precisa especificar essa opção na linha de comando. Se não fornecida, o Jarsigned lhe pedirá para informar cada campo Nome Único (CN, OU, e assim em diante).***

* `-keypass` <br>

***A senha para essa senha.Como precaução de segurança, não inclua essa opção na linha de comando. Se não fornecida, o Keytool pedirá que você informe a senha. Desta maneira, sua senha não será armazenada no histórico do shell.***

* `-storepass` <br>

***Uma senha para a keystore.
Como precaução de segurança, não inclua essa opção na linha de comando. Se não fornecida, o Keytool pedirá que você informe a senha.***


*Isso é tudo pessoal!*

<center>
<img src="https://pbs.twimg.com/media/B6tJt_SIMAAQ7MZ.jpg:small" title="Ate mais e obrigado pelos peixes" alt="Ate mais e obrigado pelos peixes">
</center>

