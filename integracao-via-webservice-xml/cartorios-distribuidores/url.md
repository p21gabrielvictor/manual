# URL

**Homologação (ambiente de testes):**\
_cra**UF**.cra21.com.br/cra**UF**/xml/protestos\_cartorio.php?wsdl_\
**Exemplo:** _https://cra**df**.cra21.com.br/cra**df**/xml/protestos\_cartorio.php?wsdl_

{% hint style="warning" %}
_<mark style="color:red;"><mark style="color:red;background-color:yellow;">**ATENÇÃO**<mark style="color:red;background-color:yellow;"></mark><mark style="color:red;"><mark style="color:red;background-color:yellow;">: no ambiente de homologação utilizar o protocolo<mark style="color:red;background-color:yellow;"></mark> <mark style="color:red;"><mark style="color:red;background-color:yellow;"> </mark><mark style="color:red;"><mark style="color:red;background-color:yellow;">**HTTPS**<mark style="color:red;background-color:yellow;"></mark>_&#x20;
{% endhint %}

**Produção (ambiente de funcionamento do sistema):**\
cra**UF**.crabr.com.br/cra**UF**/xml/protestos\_cartorio.php?wsdl\_\
Exemplo: _https://cradf.crabr.com.br/cradf/xml/protestos\_cartorio.php?wsdl_

{% hint style="warning" %}
_<mark style="color:red;background-color:yellow;">**ATENÇÃO**</mark><mark style="color:red;background-color:yellow;">: no ambiente de produção utilizar o protocolo</mark>_ _<mark style="color:red;background-color:yellow;">**HTTPS**</mark>_
{% endhint %}

**Observação:**

As configurações do servidor, para transações, estão definidas como:

* 100 MB – média tamanho de arquivos;
* 30 Min – tempo de espera do upload.

Caso retorne timeout antes desse tempo, verifique as configurações de espera da resposta pela sua aplicação.
