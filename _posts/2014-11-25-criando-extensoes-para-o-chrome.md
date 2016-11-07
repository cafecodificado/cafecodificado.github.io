---
published: true
title: Criando extensões para o Google Chrome
layout: post
---
![Extensões para o Google Chrome](https://build.phonegap.com/images/marketing/build-diagram.png)
Extensões são pequenos programas que permitem a você adicionar funcionalidades para o navegador, no nosso caso, o Google Chrome, usando tecnologias WEB, tais como: JavaScript, HTML e CSS.

A partir de um arquivo de manifesto, você diz ao navegador quais recursos você vai utilizar, e através de um arquivo JavaScript, você executa as tarefas desejadas.

Um recurso super legal em extensões, é que você consegue otimizar muitas tarefas. Um exemplo: Eu uso o One Click Note para me ajudar no controle diário das minhas tarefas. Uso também uma extensão que eu desenvolvi que abri um popup com os meus aplicativos. Resumindo, ao abrir o navegador,  a extensão carrega uma lista de todos os meus apps no chrome, sem  precisar ir para a pagina dos apps. Também faço o mesmo com meus e-mails e notificações do Github. Enfim, elas são muito úteis.

Hoje nós vamos criar uma extensão para o Google Chrome que abre um popup com uma calculadora. Algo bem simples. 
A idéia deste artigo é explicar como criar uma extensão, depois você pode criar extensões mais funcionais.

##### Preparações:
Para organizar os arquivos da nossa extensão, vamos criar uma pasta chamada: calculadora, e copiar os arquivos que esta no [github](https://github.com/godrix/Calculadora-Chrome-extension) e faça download.

##### agora vou esplicar um arquivo muito importante...

**O Manifesto:**
Qualquer extensão deve conter em seu diretório raiz um arquivo chamado manifest.json, que é responsável por declarar algumas informações referentes a extensão. Um manifesto declara: o nome da extensão, a versão, as permissões que ela precisa, dentre outras configurações.  Um arquivo de manifesto nada mais é do que um arquivo no formato JSON com algumas propriedades pré-definidas. 
Você pode encontrar todas as propriedades aceitáveis pelo arquivo manifest.json, no site do Google Chrome Developer.
Nosso arquivo manifest.json ficará assim:

```javascript
{
  "name": "Calculadora",
  "description": "Calculadora exemplo para chrome",
  "version": "0.0.1",
  "permissions": ["management"],
  "browser_action": {
    "default_icon": "browser_action_icon.png",
    "default_title": "Calculadora",
    "default_popup": "popup.html"
  },
  "icons": {
    "48": "icon.png"
  },
  "manifest_version": 2
}
```

***Explicando:***

`name:` Define o nome da extensão. Esse nome será utilizado para apresentar a extensão.

`description:` Uma breve descrição sobre o que faz a extensão. Seja simples e direto, pois, uma descrição não pode conter mais que 128 caracteres.

`version:` Qual é a versão da sua extensão? Quando falamos em versonamento, devemos seguir uma convensão. Mas isso é assunto para um outro artigo.

`manifest_version:` Informa qual é a versão do manifesto que estamos usando. Nós usaremos a version 2 do manifesto, pois, a versão 1 está defazada.

###### Testando nossa extensão:

Para testar nossa extensão, acesse a URL: `chrome://extensions/`, marque a opção: modo desenvolvedor; clique em: Carregar extensão expandida e, selecione a pasta calculadora.
Após fazer isso, você verá que a sua extensão foi carregada e instalada, sendo assim, você pode acessar o plugin que aparecera no lado da barra de url. 
Pronto Uma Calculadora aparecera em forma de popup
![Meme](http://geradormemes.com/media/created/euziag.png)