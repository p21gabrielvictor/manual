# Informar emolumentos do título (XML)

{% tabs %}
{% tab title="Objetivo" %}
Descrever o serviço para informar custas dos títulos enviados entre Cartórios de Protesto e o CRA21.
{% endtab %}

{% tab title="URL" %}
* **Homologação (ambiente de testes):**

&#x20;     _**craUF**.cra21.com.br/**craUF**/xml/protestos\_cartorio.php?wsdl_

&#x20;    __     Ex: _https://cradf.cra21.com.br/cradf/xml/protestos\_cartorio.php?wsdl_

&#x20;  _     **  **<mark style="color:red;">**ATENÇÃO:**</mark>** no ambiente de homologação utilizar o protocolo HTTPS**_ \
_****_

* **Produção (ambiente de funcionamento do sistema):**\
  ****\
  ****_**craUF**.crabr.com.br/**craUF**/xml/protestos\_cartorio.php?wsdl_\
  __Ex: _https://cradf.crabr.com.br/cradf/xml/protestos\_cartorio.php?wsdl_\
  _<mark style="color:red;">**ATENÇÃO:**</mark>** ****no ambiente de produção utilizar o protocolo HTTPS**_
{% endtab %}

{% tab title="Parâmetros de Envio" %}
* **Os dados (parâmetros) devem ser enviados via protocolo SOAP.**
* **Ao consumir o WebService, em todos os serviços, a autenticação deverá ser realizada utilizando autenticação básica.**
  * Deverão ser passados os parâmetros de _usuário_ e _senha_, fornecidos pela CRA.
  * Após a autenticação serão validados os parâmetros de entrada e por último a crítica do arquivo
*   **Serviços disponíveis:**

    | **CustasTitulo** | Envio de emolumentos dos títulos |
    | ---------------- | -------------------------------- |
*   **Parâmetros dos serviços disponíveis:**

    * **Upload**

    | **userArq**   | Nome do arquivo no formato **ENNNDDMM.AAS.** |
    | ------------- | -------------------------------------------- |
    | **userDados** | Conteúdo do arquivo XML.                     |

    * **O encoding do XML deve estar de acordo com ISO-8859-1.**
    * **O conteúdo dos arquivos enviados para CRA devem seguir o padrão de codificação ASCII**

\

{% endtab %}

{% tab title="Nomenclatura de Arquivos" %}
**EMOLUMENTOS**&#x20;

* **ENNNDDMM.AAS, onde:**
  * **E:** constante que indica ser arquivo de Emolumentos;
  * **NNN:** constante 000;
  * **DD:** dia;
  * **MM:** mês;
  * **AA:** ano de referência;
  * **S:** sequencial do arquivo (mínimo 1, máximo 9).Ex: E0000404.221
{% endtab %}

{% tab title="Estrutura do Arquivo" %}
#### REGISTRO – ARQUIVO EMOLUMENTOS



<mark style="color:green;">**``**</mark>[<mark style="color:green;">**`DOWNLOAD ARQUIVO EXEMPLO`**</mark>](https://github.com/p21sistemas/manual-cra-21/blob/main/exemplos\_custas.zip?raw=true)

| _**Atributo**_         | _**Descrição**_                                   | _**Tam**_    | _**Tipo**_            | _**Casas Decimais**_ | _**Obrigatório**_ |
| ---------------------- | ------------------------------------------------- | ------------ | --------------------- | -------------------- | ----------------- |
| **codigo**             | **Código do apresentante**                        | **Variável** | **Alfanumérico**      | **Nenhuma**          | **Sim**           |
| **protocolo**          | **Protocolo do título**                           | **Variável** | **Alfanumérico**      | **Nenhuma**          | **Não**           |
| **documento\_devedor** | **Documento do devedor**                          | **Variável** | **Numérico**          | **Nenhuma**          | **Não**           |
| **data\_protocolo**    | **Data de protocolo**                             | **010**      | **Data (01/01/2024)** | **Nenhuma**          | **Não**           |
| **numero\_titulo**     | **Número do título**                              | **Variável** | **Numérico**          | **Nenhuma**          | **Não**           |
| **nosso\_numero**      | **Nosso número**                                  | **Variável** | **Numérico**          | **Nenhuma**          | **Não**           |
| **valor**              | **Documento do devedor**                          | **Variável** | **Decimal**           | **2**                | **Não**           |
| custas                 | Custas do cartório/distribuidor/demais despesas   | Variável     | Decimal               | 2                    | Não               |
| intimacao              | Custas de intimação                               | Variável     | Decimal               |  2                   | Não               |
| cancelamento           | Custas de cancelamento                            | Variável     | Decimal               |  2                   | Não               |
| edital                 | Custas de edital                                  | 003          | Decimal               |  2                   | Não               |
| **tipo**               | **Tipo de custas (1 – Retirada, 2 Cancelamento)** | **001**      | **Inteiro**           | **Nenhuma**          | **Não**           |
| **total**              | **Total das custas pré-calculadas**               | **Variável** | **Decimal**           | **2**                | **Não**           |
| vigencia               | Vigência das custas                               | 010          | Data (01/01/2024)     | Nenhuma              | N                 |

\


Observações:

* **O envio das custas simplificado prevê o preenchimento dos em destaque.**
* A vigência indica até quando essas custas podem ser consultadas pelo apresentante ou em rotinas públicas, o não preenchimento desse campo indica que as custas não têm uma data de validade.
{% endtab %}

{% tab title="Mensagens" %}


**Mensagens:**

* Custas do título atualizadas com sucesso.

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<mensagem>
    <codigo>2291</codigo>
    <descricao>Custas do título atualizadas com sucesso.</descricao>
</mensagem>
```



* Título não encontrado.



```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<mensagem>
    <codigo>2196</codigo>
    <descricao>Título não encontrado.</descricao>
</mensagem>
```

****\
****

| **CÓDIGO** | **DESCRIÇÃO**                             |
| ---------- | ----------------------------------------- |
| 2291       | Custas do título atualizadas com sucesso. |
| 2196       | Título não encontrado.                    |

\

{% endtab %}
{% endtabs %}





&#x20;
