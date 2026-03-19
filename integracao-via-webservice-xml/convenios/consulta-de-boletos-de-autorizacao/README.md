# Consulta de boletos de autorização

{% hint style="warning" %}
Atenção: Este manual será desativado em breve e substituído por uma versão mais atualizada. Acesse a nossa nova documentação clicando aqui: [https://manual.p21website.com.br/ ](https://manual.p21website.com.br/%C2%A0)
{% endhint %}

**Homologação (ambiente de testes):**\
&#xNAN;_&#x63;ra**UF**.cra21.com.br/cra**UF**/xml/protestos.php?wsdl_\
Ex: _https://cra**df**.cra21.com.br/cra**df**/xml/protestos.php?wsdl_

{% hint style="warning" %}
_<mark style="color:red;background-color:yellow;">**ATENÇÃO**</mark><mark style="color:red;background-color:yellow;">: no ambiente de produção utilizar o protocolo</mark> <mark style="color:red;background-color:yellow;"></mark><mark style="color:red;background-color:yellow;">**HTTPS**</mark>_
{% endhint %}

**Produção (ambiente de funcionamento do sistema):**\
&#xNAN;_**craUF**.crabr.com.br/**craUF**/xml/protestos.php?wsdl_\
Ex: _https://cra**df**.crabr.com.br/cra**df**/xml/protestos.php?wsdl_

{% hint style="warning" %}
_<mark style="color:red;background-color:yellow;">**ATENÇÃO**</mark><mark style="color:red;background-color:yellow;">: no ambiente de produção utilizar o protocolo</mark> <mark style="color:red;background-color:yellow;"></mark><mark style="color:red;background-color:yellow;">**HTTPS**</mark>_
{% endhint %}

**Observação:**

Caso retorne timeout antes desse tempo, verifique as configurações de espera da resposta pela sua aplicação.
