---
published: true
title: Aquele Sobre JSON
layout: post
---

<center>
<img src="http://cdn.marketplaceimages.windowsphone.com/v8/images/db5d3cf1-222f-4cb0-b438-b7aff22ca3d7?imageType=ws_icon_large" width="50%" title="Aquele sobre json" alt="logo json">
</center>

>JSON é um acrônimo para "JavaScript Object Notation", é um formato leve para intercâmbio de dados computacionais. JSON é um subconjunto da notação de objeto de JavaScript, mas seu uso não requer JavaScript exclusivamente.
<br>
<small><cite>a enciclopédia livre, Wikipédia</cite></small>

####Afinal, o que é JSON?

JSON é como diz a Wiki é basicamente um formato leve de troca de informações/dados entre sistemas. só podendo usar com JavaScript correto? Na verdade não e alguns ainda caem nesta armadilha.

O JSON além de ser um formato leve para troca de dados é também muito simples de ler. Mas quando dizemos que algo é simples, é interessante compará-lo com algo mais complexo para entendermos tal simplicidade não é? Neste caso podemos comparar o JSON com o formato XML.

#### XML

<script src="https://gist.github.com/godrix/59e84af85639d676dba0.js"></script>

---

#### JSON

```
{"id":1,"nome":"Joao da Silva", "endereco":"R. Dos Bobos"}
```

Muitas das suposições sobre o quão lento, dispendioso e "gordo" o XML é se comparado à leveza do JSON, não foram sustentadas pelo teste feito por David Lee, engenheiro líder na Marklogic, após a execução de um experimento "crowd sourcing" com 33 documentos diferentes e aproximadamente 1200 testes, em uma grande quantidade de navegadores e sistemas operacionais mais utilizados. David afirma ter descoberto que o desempenho total da experiência de usuário ‒ transferência, análise (parsing) e consulta (querying) de um documento ‒ é quase idêntico em ambos os formatos: XML e JSON.

Para o seu experimento David criou e divulgou publicamente um ambiente de teste que imita um caso de uso em que documentos XML e JSON são entregues por um servidor web, para serem analisados e consultados em um navegador web.

O servidor abastece o cliente com uma fonte de dados, e coleta os resultados provenientes do cliente. O cliente é uma aplicação JavaScript executada no navegador, codificada especificamente para medir performance, exceto a parte que faz as medições de desempenho do jQuery.

Além de usar sete documentos diferentes com tamanhos entre 100Kb e 1Mb, e cada documento apresentar duas variantes JSON e três variantes XML, David também tentou cobrir uma gama de dispositivos, navegadores, sistemas operacionais e redes em seu teste. Ele fez isso através de "crowd sourcing", ou seja, tornou pública a URL do ambiente de testes e divulgou em várias listas de e-mail e sites de mídia social. O resultado de aproximadamente 1200 testes distintos e bem sucedidos foram coletados até agora, abrangendo os navegadores e sistemas operacionais mais utilizados. Em seu artigo, David documentou todos os dados do teste, bem como os seus resultados.

**Algumas das conclusões obtidas após a experiência de David são:**

* A velocidade de análise (parsing) varia de acordo com a técnica usada. A análise com JavaScript puro é mais rápida para XML do que para o JSON, enquanto a consulta é normalmente mais rápida para o JSON. Ambos apresentando exceções, em que o contrário é verdadeiro.
* O uso da biblioteca JavaScript jQuery impõe uma penalidade exagerada para o JSON, e pior ainda para o XML.
* Documentos compactados em todos os formados, mesmo representações muito grandes em JSON ou XML apresentam tamanho idêntico após a compressão, o que indica que ambos possuem o mesmo conteúdo de informação.
* A transferência de documentos para uma grande variedade de dispositivos leva efetivamente o mesmo tempo em cada dispositivo, independentemente do formato adotado (XML ou JSON).

**Baseando-se em seu experimento, David inclui algumas sugestões para arquitetos e desenvolvedores:**

* Usar Compressão HTTP, na maioria das vezes, é o fator mais importante no desempenho total.
* Otimizar a marcação para transmissão e consulta.
* Não tentar otimizar, a menos que a transmissão de dados, a análise e a consulta sejam problemas significativos se comparados às outras questões.