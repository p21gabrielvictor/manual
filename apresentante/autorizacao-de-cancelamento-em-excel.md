# Autorização de cancelamento em Excel

#### [<mark style="color:green;">**`DOWNLOAD DO ARQUIVO EXEMPLO`**</mark>](https://github.com/p21sistemas/manual-cra-21/blob/main/Exemplo\_Autoriza%C3%A7%C3%A3o\_Cancelamento.xlsx?raw=true)

{% tabs %}
{% tab title="Instruções  Gerais" %}
| Tipo do arquivo | O arquivo deve ser do tipo xlsx.                                                                                                                                                                                                                                                                          |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Campo           | O nome das colunas deverão ser preenchidas em caixa alta, sem acentos, seguindo o padrão informado. Apenas a coluna CEDENTE não é obrigatória.                                                                                                                                                            |
| Tipo            | Tipo da célula.                                                                                                                                                                                                                                                                                           |
| Obrigatório     | Se o campo é obrigatório, o sistema não aceitará o registro com o campo em branco.                                                                                                                                                                                                                        |
| Nome do arquivo | <p>O nome do arquivo deve seguir o seguinte padrão de nomenclatura: XAANNNCCCCCCC.xlsx , onde:<br>X: Constante. Indica arquivo no formato Excel.<br>AC: AC para autorização de cancelamento.<br>NNN: Código do apresentante (3 ou 6 posições)<br>CCCCCCC: Conteúdo alfanumérico com tamanho variável.</p> |
| Delimitador     | O Delimitador para a contagem das linhas é a borda das colunas.                                                                                                                                                                                                                                           |
{% endtab %}

{% tab title="Preenchimento dos Campos" %}
| **Campo**   | **Obrigatório** | **Instruções**                                                       |
| ----------- | --------------- | -------------------------------------------------------------------- |
| CEDENTE     | NÃO             | Nome do Cedente do título.                                           |
| DEVEDOR     | NÃO             | Campo alfanumérico que deverá ser preenchido com o nome do devedor.  |
| DOCUMENTO   | NÃO             | Campo numérico que deverá ser preenchido com máscara ou sem máscara. |
| NUMERO      | NÃO             | Campo alfabético que deverá ser preenchido com o número do título.   |
| NOSSONUMERO | NÃO             | Campo alfanumérico que deverá ser preenchido com o nosso número.     |
| VALOR       | NÃO             | Campo do tipo valor que deverá ser preenchido com o valor do título. |
{% endtab %}
{% endtabs %}
