# Web Service – SoapUI

## SoapUI

SoapUI permite que você facilmente e rapidamente criar e executar testes funcionais, de regressão, de conformidade e de carga automatizados. Em um ambiente de teste individual, SoapUI oferece cobertura de teste completo e suporta todos os protocolos e tecnologias padrões.

Para realizar testes de conexão com o **Web Service** da CRA utilizando a ferramente Soap UI são necessários os seguintes passos.

#### 1.º Faça o download do SoapUI.

[<mark style="color:green;">https://www.soapui.org/downloads/soapui/</mark>](https://www.soapui.org/downloads/soapui/)

**2.º Após a instalação do produto crie um novo projeto SOAP clicando no ícone.**\
<img src="../../../.gitbook/assets/image (34).png" alt="" data-size="original">

**3.º Preencher os campos com o nome do projeto e o link para a conexão WSDL**

![](<../../../.gitbook/assets/image (7).png>)

**4.º Escolha o serviço que deseja utilizar, crie ou seleciona uma **<mark style="color:green;">**request**</mark>**.**\
![](<../../../.gitbook/assets/image (6).png>)

\*\*5.º Seleciona a aba Auth(Basic) preencha o <mark style="color:green;">**Username**</mark> e <mark style="color:green;">**Pasword**</mark> (esses dados devem ser cadastrados anteriormente pelo gestor da CRA) preencha também o <mark style="color:green;">**domain**</mark> do serviço, e selecione a opção \*\*<mark style="color:green;">**Authenticate pre-emptively.**</mark>\ <mark style="color:green;">\*\*\*\*</mark>

![](<../../../.gitbook/assets/image (33).png>)

**6.º Após isso clique no botão play na parte superior, o sistema irá mostra o resultado da sua requisição na parte lateral direita RAW/XML.**

{% hint style="info" %}
**Para enviar os dados do arquivo utilizar a tag abaixo:**\
\<!\[CDATA\[inserir aqui no formato XML o conteudo da remessa]]>
{% endhint %}
