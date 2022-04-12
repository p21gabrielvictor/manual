# Preenchimento de pedido de desistência/cancelamento em Excel

{% tabs %}
{% tab title="Instruções gerais" %}


| Tipo do arquivo | O arquivo deve ser do tipo xlsx.                                                                                                                                                                                                                                                                                                                |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Campo           | O nome das colunas deverão ser preenchidas em caixa alta, sem acentos, seguindo o padrão informado.                                                                                                                                                                                                                                             |
| Tipo            | Tipo da célula.                                                                                                                                                                                                                                                                                                                                 |
| Obrigatório     | Se o campo é obrigatório, o sistema não aceitará o registro com o campo em branco.                                                                                                                                                                                                                                                              |
| Nome do arquivo | <p>O nome do arquivo deve seguir o seguinte padrão de nomenclatura: XAANNNCCCCCCC.xlsx , onde:<br>X: Constante. Indica arquivo no formato Excel.<br>AA: DP para solicitação de desistência ou CP para solicitação de cancelamento.<br>NNN: Código do apresentante (3 ou 6 posições)<br>CCCCCCC: Conteúdo alfanumérico com tamanho variável.</p> |
| Delimitador     | O Delimitador para a contagem das linhas é a borda das colunas.                                                                                                                                                                                                                                                                                 |
{% endtab %}

{% tab title="Preenchimento dos campos" %}


| **Campo**     | **Obrigatório** | **Instruções**                                                          |
| ------------- | --------------- | ----------------------------------------------------------------------- |
| MUNICIPIO     | SIM             | Código IBGE do município cadastrado no CRA21.                           |
| CARTORIO      | SIM             | Código do cartório cadastrado no CRA21.                                 |
| PROTOCOLO     | –               | Campo alfanumérico que deverá ser preenchido com o protocolo do título. |
| DATAPROTOCOLO | –               | Campo que deverá ser preenchido com a data do protocolo.                |
| NOSSONUMERO   | –               | Campo alfanumérico que deverá ser preenchido com o nosso número.        |
| NUMERO        | –               | Campo alfabético que deverá ser preenchido com o número do título.      |
| VALOR         | –               | Campo do tipo valor que deverá ser preenchido com o valor do título.    |
| DEVEDOR       | –               | Campo alfanumérico que deverá ser preenchido com o nome do devedor.     |
{% endtab %}
{% endtabs %}

#### ``[<mark style="color:green;">`DOWNLOAD DO ARQUIVO EXEMPLO`</mark>](https://github.com/p21sistemas/manual-cra-21/blob/main/EXEMPLO\_PEDIDO\_DESIST%C3%8ANCIA\_CANCELAMENTO\_APRESENTANTE.xlsx?raw=true)<mark style="color:green;">``</mark>
