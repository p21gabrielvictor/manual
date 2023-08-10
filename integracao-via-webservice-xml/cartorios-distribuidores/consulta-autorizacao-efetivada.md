# Consulta autorização efetivada

{% tabs %}
{% tab title="Parâmetros de Envio" %}
Serviço criado para possibilitar que o cartório realize consultas das autorizações efetivadas por data ou período.

{% hint style="info" %}
**URL**&#x20;

**Altere UF pela sigla do estado.**

**Ambiente de Homologação:**\
_https://cra**uf**.cra21.com.br/cra**uf**/xml/protestos\_cartorio.php?wsdl_



**Produção (ambiente de funcionamento do sistema):**\
_https://cra**uf**.crabr.com.br/cra**uf**/xml/protestos\_cartorio.php?wsdl_
{% endhint %}



* **Os dados (parâmetros) devem ser enviados via protocolo SOAP.**
* **Ao consumir o WebService, em todos os serviços, a autenticação deverá ser realizada utilizando autenticação básica.**
  * Deverão ser passados os parâmetros de _usuário_ e _senha_, fornecidos pela CRA.
  * Após a autenticação serão validados os parâmetros de entrada e por último a crítica do arquivo
* **Serviços disponíveis:**

<table data-header-hidden><thead><tr><th width="229"></th><th></th></tr></thead><tbody><tr><td>AutorizacoesEfetivadas</td><td>A consulta das autorizações efetivadas poderá ser feita por um período máximo de 30 dias.</td></tr></tbody></table>

*   **Parâmetros dos serviços disponíveis:**



    <table data-header-hidden><thead><tr><th width="185"></th><th></th></tr></thead><tbody><tr><td><strong>userDados</strong></td><td>Conteúdo do arquivo XML.</td></tr></tbody></table>

    * **O encoding do XML deve estar de acordo com ISO-8859-1.**
    * **O conteúdo dos arquivos enviados para CRA devem seguir o padrão de codificação ASCII**
{% endtab %}

{% tab title="Estrutura do arquivo" %}
**ARQUIVO EXEMPLO:**&#x20;

```markup
<filtros>
  <dataInicial>dd/mm/AAAA</dataInicial>
  <dataFinal>dd/mm/AAAA</dataFinal>
</filtros>
```

**Por período:**&#x20;

```markup
<filtros>
  <dataInicial>01/01/1111</dataInicial>
  <dataFinal>30/01/1111</dataFinal>
</filtros>
```

**Somente um dia:**&#x20;

```markup
<filtros>
  <dataInicial>01/01/1111</dataInicial>
  <dataFinal>01/01/1111</dataFinal>
</filtros>
```
{% endtab %}

{% tab title="Mensagem" %}
**Exemplo de mensagem de sucesso:**

```markup
<autorizacoes>
    <autorizacao>
        <dataAutorizacao>07/08/2023 17:27:28</dataAutorizacao>
        <dataSituacao>07/08/2023 17:28:25</dataSituacao>
        <protocolo>7371513523</protocolo>
        <dataProtocolo>07/08/2023</dataProtocolo>
        <numeroTitulo>387-513/771</numeroTitulo>
        <valor>12.639,86</valor>
        <saldo>12.764,91</saldo>
        <situacao>EFETIVADO COM RETORNO</situacao>
        <devedores>
            <devedor>
                <nome>PAOLA URIAS JR.</nome>
                <documento>49.679.848/0001-88</documento>
            </devedor>
              <devedor>
                <nome>CRISTIANO CARMONA</nome>
                <documento>813.492.460-34</documento>
            </devedor>          
        </devedores>
    </autorizacao>
</autorizacoes>
```

\
A resposta será composta pelos seguintes campos:

* Data da autorização
* Data efetivação (Situação)
* Protocolo
* Data protocolo
* Numero do título
* Valor
* Saldo
* Nome devedor
* Documento devedor

Mensagens de recusa:

<table data-header-hidden><thead><tr><th width="153"></th><th></th></tr></thead><tbody><tr><td><strong>CÓDIGO</strong></td><td><strong>DESCRIÇÃO</strong></td></tr><tr><td>2327</td><td>Data inicial do período inválida.</td></tr><tr><td>2328</td><td>Data final do período inválida.</td></tr><tr><td>2137</td><td>Campo (filtros) inválido.</td></tr><tr><td>2329</td><td>Data inicial não pode ser maior que a data final</td></tr><tr><td>2330</td><td>Período informado não pode ser maior que 31 dias.</td></tr></tbody></table>
{% endtab %}
{% endtabs %}
