---
cover: ../.gitbook/assets/Design sem nome (2).png
coverY: -6
---

# Web Service – SoapUI

## SoapUI

O SoapUI é um aplicativo de teste de serviço da Web de código aberto para Protocolo de Acesso a Objeto Simples e transferências de estado representacional. Sua funcionalidade abrange inspeção de serviços da Web, invocação, desenvolvimento, simulação e situação, testes funcionais, testes de carga e conformidade.

Com ele será possível realizar testes de envio de arquivo com a CRA21&#x20;

Para realizar testes de conexão com o **Web Service** da CRA utilizando a ferramente Soap UI são necessários os seguintes passos.

#### 1.º Faça o download do SoapUI.

[<mark style="color:green;">https://www.soapui.org/downloads/soapui/</mark>](https://www.soapui.org/downloads/soapui/)

**2.º Após a instalação do produto crie um novo projeto SOAP clicando no ícone.**\


<figure><img src="../.gitbook/assets/image (34) (2).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

**3.º Preencher os campos com o nome do projeto e o link para a conexão WSDL**

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

**4.º Escolha o serviço que deseja utilizar, crie ou selecione uma **<mark style="color:green;">**request**</mark>**.**\


<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

5.º Seleciona a aba Auth(Basic) preencha o <mark style="color:green;">**Username**</mark> e <mark style="color:green;">**Pasword**</mark> (esses dados devem ser cadastrados anteriormente pelo gestor da CRA) e selecione a opção <mark style="color:green;">**`Authenticate pre-emptively.`**</mark>

{% hint style="info" %}
**Para enviar os dados do arquivo utilizar a tag abaixo:**\
\<!\[CDATA\[inserir aqui no formato XML o conteudo da remessa]]>
{% endhint %}

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

**6.º Após isso clique no botão play na parte superior, o sistema irá mostra o resultado da sua requisição na parte lateral direita RAW/XML.**

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>
