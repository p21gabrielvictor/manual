# URL

**Homologação (ambiente de testes):** \
_cra**UF**.cra21.com.br/cra**UF**/xml/protestos.php?wsdl_\
**Exemplo:** _https://cra**df**.cra21.com.br/cra**df**/xml/protestos.php?wsdl_

{% hint style="warning" %}
_<mark style="color:red;background-color:yellow;">**ATENÇÃO**</mark><mark style="color:red;background-color:yellow;">: no ambiente de homologação utilizar o protocolo</mark>_ _<mark style="color:red;background-color:yellow;">**HTTPS**</mark>_
{% endhint %}

**Produção (ambiente de funcionamento do sistema):** _cra**UF**.crabr.com.br/cra**UF**/xml/protestos.php?wsdl_\
**Exemplo:** _https://cra**df**.crabr.com.br/cra**df**/xml/protestos.php?wsdl_

{% hint style="warning" %}
_<mark style="color:red;"><mark style="background-color:yellow;">**ATENÇÃO**<mark style="background-color:yellow;"></mark><mark style="color:red;"><mark style="background-color:yellow;">: no ambiente de produção utilizar o protocolo<mark style="background-color:yellow;"></mark> <mark style="color:red;"><mark style="background-color:yellow;"> </mark><mark style="color:red;background-color:yellow;"><mark style="color:red;"><mark style="background-color:yellow;">**HTTPS**<mark style="background-color:yellow;"><mark style="color:red;"></mark>_
{% endhint %}

**Observação:**

As configurações do servidor, para transações, estão definidas como:

* 100 MB – média tamanho de arquivos;
* 30 Min – tempo de espera do upload.

Caso retorne timeout antes desse tempo, verifique as configurações de espera da resposta pela sua aplicação.
