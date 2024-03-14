# Dados complementares do devedor

Rotina criada para possibilitar ao apresentante informar o e-mail e o telefone do devedor.

Os apresentantes poderão enviar as informações na remessa (XML), pelo Digita e Excel. Os dados serão exibidos na consulta do título e também poderão ser baixados pelos cartórios por meio do webservice de remessa (XML).

### FORMAS DE UPLOAD&#x20;

#### UPLOAD POR XML

Para enviar por XML, o apresentante deverá preencher os dados nas tags: <mark style="color:green;">**t53 = Telefone**</mark>, <mark style="color:green;">**t54= E-mail**</mark>.&#x20;

<mark style="color:green;">**Exemplo:**</mark>&#x20;

```markup
<remessa>
<hd ... h17="0001"/>
<tr ... t51="" t52="0002" t53="99999999999" t54="Emaildevedor@email.com.br"/>
<tr ... t51="" t52="0003" t53="99999999999" t54="Emaildevedor@email.com.br"/>
<tl ... t08="0004"/>
</remessa>
```

#### ENVIO PELA APLICAÇÃO CRA21&#x20;

Para informar os dados pela aplicação CRA21, o apresentante irá acessar o menu Remessa -> Gerar remessa -> informar os dados nos campos telefone e e-mail.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

#### ENVIO POR EXCEL  APLICAÇÃO CRA21&#x20;

Para efetuar o upload por Excel pela aplicação o apresentante irá acessar o menu Remessa -> Upload remessa Excel -> informar os dados nos campos telefone e e-mail na planilha (Conforme na imagem).

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Visualização pela aplicação CRA21

O e-mail e telefone do devedor pode ser verificado pela aplicação CRA21, acessando o menu Consulta -> Consulta titulo.&#x20;

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

### Download pelo cartório/distribuidor

{% hint style="success" %}
Para que o cartório tenha acesso a essas informações é necessário que no cadastro do cartório/distribuidor esteja habilitado o parâmetro **Receber campos complementares no XML.**&#x20;
{% endhint %}

O download via XML será disponibilizado ao cartório nessas mesmas tags <mark style="color:green;">**(t53 e t54).**</mark>

```markup
<remessa>
<hd ... h17="0001"/>
<tr ... t51="" t52="0002" t53="99999999999" t54="Emaildevedor@email.com.br"/>
<tr ... t51="" t52="0003" t53="99999999999" t54="Emaildevedor@email.com.br"/>
<tl ... t08="0004"/>
</remessa>
```

#### CONSULTA DOS DADOS COMPLEMENTARES DO TÍTULO VIA API&#x20;

Para consultar os dados complementares do título via é necessário utilizar a URL descrita abaixo e informar o serviço[ <mark style="color:green;">**/titulo**</mark>](../api-cra21/integracao-cra21-api/url-titulo.md).&#x20;

<mark style="color:green;">**Exemplo de resposta:**</mark>&#x20;

```markup
"devedores": [
                    {
                        "nome": "DEVEDOR DEVEDOR",
                        "tipoDocumento": "CNPJ",
                        "documento": "00000000000000"
                        "telefone": "0000000000",
                        "email": "email@email.com.br",
                    }
                ]
```

Para demais dúvidas sobre a API, [<mark style="color:green;">**clique aqui**</mark>](../api-cra21/integracao-cra21-api/).
