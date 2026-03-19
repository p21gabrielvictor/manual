# Parâmetros de envio



{% hint style="warning" %}
Atenção: Este manual será desativado em breve e substituído por uma versão mais atualizada. Acesse a nossa nova documentação clicando aqui: [https://manual.p21website.com.br/ ](https://manual.p21website.com.br/%C2%A0)
{% endhint %}

**Os dados (parâmetros) devem ser enviados via protocolo SOAP**

**Ao consumir o WebService, em todos os serviços, a autenticação deverá ser realizada utilizando autenticação básica.**

* Deverão ser passados os parâmetros de _usuário_ e _senha_, fornecidos pela CRA.
* Após a autenticação serão validados os parâmetros de entrada e por último a crítica do arquivo

**Serviços disponíveis:**

* | **BoletoAutorizacao** | download de boletos de autorização |
  | --------------------- | ---------------------------------- |

**Parâmetros dos serviços disponíveis:**

*   Download<br>

    | **numeroTitulo**     | número do título     |
    | -------------------- | -------------------- |
    | **documentoDevedor** | documento do devedor |

**O encoding do XML deve estar de acordo com ISO-8859-1.**

**Assim como no HTML, o XML possui entidades, que devem ser substituídas conforme tabela abaixo:**

* | **De** | **Para** |
  | ------ | -------- |
  | <      | & lt;    |
  | >      | & gt;    |
  | &      | & amp;   |
  | ‘      | & apos;  |
  | “      | & quot;  |
