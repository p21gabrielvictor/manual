---
description: >-
  Descrição do serviço de atualização das custas de retirada/cancelamento dos
  títulos, que pode ser utilizado pelos cartórios.
---

# Emolumentos dos títulos

{% tabs %}
{% tab title="Parâmetros de Envio" %}
* **Os dados (parâmetros) devem ser enviados via protocolo SOAP.**
* **Ao consumir o WebService, em todos os serviços, a autenticação deverá ser realizada utilizando autenticação básica.**
  * Deverão ser passados os parâmetros de _usuário_ e _senha_, fornecidos pela CRA.
  * Após a autenticação serão validados os parâmetros de entrada e por último a crítica do arquivo
*   **Serviços disponíveis:**

    <table data-header-hidden><thead><tr><th width="234"></th><th></th></tr></thead><tbody><tr><td><strong>CustasTitulo</strong></td><td>Envio de emolumentos dos títulos</td></tr></tbody></table>
*   **Parâmetros dos serviços disponíveis:**

    * **Upload**

    <table data-header-hidden><thead><tr><th width="144"></th><th></th></tr></thead><tbody><tr><td><strong>userArq</strong></td><td>Nome do arquivo no formato <strong>ENNNDDMM.AAS.</strong></td></tr><tr><td><strong>userDados</strong></td><td>Conteúdo do arquivo XML.</td></tr></tbody></table>

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



[<mark style="color:green;">**`DOWNLOAD ARQUIVO EXEMPLO`**</mark>](https://github.com/p21sistemas/manual-cra-21/blob/main/EXEMPLO\_CUSTAS\_TITULO.zip?raw=true)

| _**Atributo**_         | _**Descrição**_                                                  | _**Obrigatório**_ | _**Tamanho**_ | _**Tipo**_            | _**Casas Decimais**_ |
| ---------------------- | ---------------------------------------------------------------- | ----------------- | ------------- | --------------------- | -------------------- |
| **codigo**             | **Código do apresentante**                                       | **Sim**           | **Variável**  | **Alfanumérico**      | **Nenhuma**          |
| **protocolo**          | **Protocolo do título**                                          | **Sim**           | **Variável**  | **Alfanumérico**      | **Nenhuma**          |
| **documento\_devedor** | **Documento do devedor**                                         | **Sim**           | **Variável**  | **Numérico**          | **Nenhuma**          |
| **data\_protocolo**    | **Data de protocolo**                                            | **Sim**           | **010**       | **Data (DD/MM/AAAA)** | **Nenhuma**          |
| **numero\_titulo**     | **Número do título**                                             | **Sim**           | **Variável**  | **Numérico**          | **Nenhuma**          |
| **nosso\_numero**      | **Nosso número**                                                 | **Sim**           | **Variável**  | **Numérico**          | **Nenhuma**          |
| **valor**              | **Valor do título**                                              | **Sim**           | **Variável**  | **Decimal**           | **2**                |
| **tipo**               | **Tipo de custas (1 – Retirada, 2 Cancelamento)**                | **Sim**           | **001**       | **Inteiro**           | **Nenhuma**          |
| **total**              | **Valor total das custas para retirada/cancelamento do título.** | **Sim**           | **Variável**  | **Decimal**           | **2**                |
| **vigência**           | **Vigência das custas**                                          | **Sim**           | **010**       | **Data (DD/MM/AAAA)** | **Nenhuma**          |

\


Observações:

* **O envio das custas prevê o preenchimento dos campos acima em destaque.**
* A vigência indica o prazo de validade das custas informadas. O não preenchimento da vigência indica que o prazo de validade das custas é indefinido.
{% endtab %}

{% tab title="Mensagens" %}


**Mensagens:**

* Exemplo de custas do título atualizadas com sucesso.

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<mensagem>
    <codigo>2291</codigo>
    <descricao>Custas do título atualizadas com sucesso.</descricao>
</mensagem>
```



* Exemplo de  título não encontrado.

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<mensagem>
    <codigo>2196</codigo>
    <descricao>Título não encontrado.</descricao>
</mensagem>
```

\


<table data-header-hidden><thead><tr><th width="183"></th><th></th></tr></thead><tbody><tr><td><strong>CÓDIGO</strong></td><td><strong>DESCRIÇÃO</strong></td></tr><tr><td>2291</td><td>Custas do título atualizadas com sucesso.</td></tr><tr><td>2196</td><td>Título não encontrado.</td></tr><tr><td>2292</td><td>Campos inválidos ou não informados (<strong>APRESENTANTES</strong>)<br>Campos inválidos ou não informados (<strong>APRESENTANTE</strong>)<br>Campos inválidos ou não informados (<strong>TITULOS</strong>)<br>Campos inválidos ou não informados (<strong>TITULO</strong>)<br>Campos inválidos ou não informados (<strong>EMOLUMENTOS</strong>)<br>Campos inválidos ou não informados (<strong>EMOLUMENTO</strong>)<br>Campos inválidos ou não informados (<strong>TOTAL</strong>)<br>Campos inválidos ou não informados (<strong>TIPO</strong>)<br>Campos inválidos ou não informados (<strong>documentoDevedor</strong>).</td></tr><tr><td>2137</td><td>Campo (<strong>TIPO DE EMOLUMENTO</strong>) inválido<br>Campo (<strong>VIGENCIA</strong>) inválido</td></tr></tbody></table>

\

{% endtab %}
{% endtabs %}





&#x20;
