# Download do andamento em XML

Para efetuar o download do arquivo via XML é necessário utilizar a [<mark style="color:green;">**URL do WEBSERVICE**</mark> ](../../integracao-via-webservice-xml/convenios/url.md)  e utilizar o endpoint **Andamento**. \
Exemplo abaixo utilizando a aplicação SoapUI:&#x20;

<figure><img src="../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

Na TAG <mark style="color:green;">**\<userArq>**</mark> informar o nome do arquivo que deseja efetuar o download. A nomenclatura do arquivo deve obedecer ao nome estabelecido no Layout.

{% hint style="success" %}
**MCCCDDMM.AAS:**

* **M:** Constante – Identifica tratar-se do arquivo de andamento.&#x20;
* **CCC:** Código do Apresentante/Portador ou **constante 000**
* **DD:** Dia do envio do arquivo de andamento
* **MM:** Mês do envio do arquivo de andamento
* **AA:** Ano do envio do arquivo de andamento&#x20;
* **S:** Número Sequencial do arquivo de andamento (mínimo 1, máximo 9)
{% endhint %}

No download irá trazer as informações da data informada no arquivo e as pendentes de download.&#x20;



**Exemplo de requisição (Utilizando o SoapUI):**

```markup
<soapenv:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:urn="urn:cradf.crateste.com.br">
   <soapenv:Header/>
   <soapenv:Body>
      <urn:Andamento soapenv:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/">
         <userArq xsi:type="xsd:string">M0002308.231</userArq>
      </urn:Andamento>
   </soapenv:Body>
</soapenv:Envelope>
```

**Exemplo de resposta (Utilizando o SoapUI):** \
_Os dados apresentados na resposta, são dados fictícios._

<pre class="language-markup"><code class="lang-markup">&#x3C;SOAP-ENV:Envelope SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/"
   xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/"
   xmlns:xsd="http://www.w3.org/2001/XMLSchema"
   xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
   xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/">
   &#x3C;SOAP-ENV:Body>
      &#x3C;ns1:AndamentoResponse xmlns:ns1="urn:cradf.crateste.com.br">
         &#x3C;return xsi:type="xsd:string">
         &#x3C;![CDATA[&#x3C;?xml version="1.0" encoding="ISO-8859-1" standalone="no"?>
<strong>            &#x3C;relatorio>
</strong>            &#x3C;nome_arquivo>M0002308.231&#x3C;/nome_arquivo>
            &#x3C;comarca CodMun="5300108">
                 &#x3C;hd h01="0" h02="000" h03="APRESENTANTE" h04="23082023" h05="SDT" h06="BFO" h07="AND" h08="000001" h09="0024" h10="0000" h11="0000" h12="0000" h13="" h14="043" h15="5300108" h16="" h17="0001" />
                 &#x3C;tr t01="1" t02="000" t03="221832325837281" t04="ANDRESSA LIRA LOZANO" t05="DR. JULIO SANDOVAL FIDALGO" t06="05280532000143" t07="38109-330, AV. DENIS GUERRA, 25194DIOGO DO LE" t08="63720372" t09="SANTA AUGUSTO" t10="MT" t11="092/0159-840419" t12="DR" t13="685-361/969" t14="09072023" t15="24072023" t16="001" t17="7889.42" t18="7959.74" t19="ESTELA DO LESTE" t20="M" t21="A" t22="1" t23="CRISTIAN RICHARD DIAS" t24="002" t25="00003338759908" t26="00000000000" t27="42100-067, TRAVESSA JAMES VELASQUES, 467FRANC" t28="04092842" t29="JOYCE DO LESTE" t30="RN" t31="59" t32="64553/3335" t33="0" t34="23082023" t35="0" t36="" t37="23082023" t38="AB" t39="LARGO MARILIA, 45" t40="0" t41="000000" t42="0" t43="00000" t44="000000000000000" t45="000" t46="" t47="" t48="" t49="" t50="0" t51="23082023 210000" t52="0025" />
                 &#x3C;tl t01="9" t02="000" t03="APRESENTANTE" t04="23082023" t05="00024" t06="205153.59" t07="" t08="0026"/>
            &#x3C;/relatorio>]]>
         &#x3C;/return>
      &#x3C;/ns1:AndamentoResponse>
   &#x3C;/SOAP-ENV:Body>
&#x3C;/SOAP-ENV:Envelope>
</code></pre>

