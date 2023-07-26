# Remessa

#### REGISTRO HEADER – ARQUIVO REMESSA (Tag hd)

<table data-header-hidden><thead><tr><th width="117"></th><th></th><th></th><th></th><th></th></tr></thead><tbody><tr><td><em><strong>Atributo</strong></em></td><td><em><strong>Descrição</strong></em></td><td><em><strong>Tamanho</strong></em></td><td><em><strong>Tipo</strong></em></td><td><em><strong>Casas Decimais</strong></em></td></tr><tr><td>h01</td><td>Identifica o registro header no arquivo – Constante 0</td><td>001</td><td>Numérico</td><td>Nenhuma</td></tr><tr><td>h02</td><td>Código do apresentante (informar “999” se tiver mais de 3 dígitos)</td><td>003</td><td>Numérico</td><td>Nenhuma</td></tr><tr><td>h03</td><td>Nome do apresentante</td><td>040</td><td>Alfabético</td><td></td></tr><tr><td>h04</td><td>Data do envio do arquivo de remessa</td><td>008</td><td>Numérico</td><td>Nenhuma</td></tr><tr><td>h05</td><td>Identificação de Transação – Remetente</td><td>003</td><td>Alfanumérico</td><td></td></tr><tr><td>h06</td><td>Identificação de Transação – Destinatário</td><td>003</td><td>Alfanumérico</td><td></td></tr><tr><td>h07</td><td>Identificação de Transação – Tipo</td><td>003</td><td>Alfanumérico</td><td></td></tr><tr><td>h08</td><td>Sequencial da remessa</td><td>006</td><td>Numérico</td><td>Nenhuma</td></tr><tr><td>h09</td><td>Quantidade de registros na transação</td><td>004</td><td>Numérico</td><td>Nenhuma</td></tr><tr><td>h10</td><td>Quantidade de títulos na remessa</td><td>004</td><td>Numérico</td><td>Nenhuma</td></tr><tr><td>h11</td><td>Quantidade de indicações (tipo: DMI, DRI e CBI)</td><td>004</td><td>Numérico</td><td>Nenhuma</td></tr><tr><td>h12</td><td>Quantidade de títulos originais na remessa</td><td>004</td><td>Numérico</td><td>Nenhuma</td></tr><tr><td>h13</td><td>Número de identificação do apresentante (opcional)</td><td>006</td><td>Alfanumérico</td><td></td></tr><tr><td>h14</td><td>Versão do Layout</td><td>003</td><td>Numérico</td><td>Nenhuma</td></tr><tr><td>h15</td><td>Código do município</td><td>007</td><td>Alfanumérico</td><td></td></tr><tr><td>h16</td><td>Preencher em caso de código do apresentante com mais de 3 dígitos</td><td>497</td><td>Alfanumérico</td><td></td></tr><tr><td>h17</td><td>Sequencial do registro</td><td>004</td><td>Numérico</td><td>Nenhuma</td></tr></tbody></table>

**REGISTRO DE TRANSAÇÃO – ARQUIVO REMESSA (Tag tr)**

***

| **Atributo** | _**Descrição**_                                                                                                          | _**Tam**_**anho** | _**Tipo**_   | _**Casas Decimais**_ |
| ------------ | ------------------------------------------------------------------------------------------------------------------------ | ----------------- | ------------ | -------------------- |
| t01          | Identifica o registro transação no arquivo – Constante 1                                                                 | 001               | Numérico     | Nenhuma              |
| t02          | Código do apresentante                                                                                                   | 003               | Numérico     | Nenhuma              |
| t03          | Código do cedente do título                                                                                              | 015               | Alfanumérico |                      |
| t04          | Nome do Cedente/Favorecido                                                                                               | 045               | Alfanumérico |                      |
| t05          | Nome do Sacador                                                                                                          | 045               | Alfanumérico |                      |
| t06          | Número do CNPJ do Sacador                                                                                                | 014               | Alfanumérico |                      |
| t07          | Endereço do Sacador                                                                                                      | 045               | Alfanumérico |                      |
| t08          | CEP do Sacador                                                                                                           | 008               | Numérico     | Nenhuma              |
| t09          | Cidade do Sacador                                                                                                        | 020               | Alfanumérico |                      |
| t10          | UF do Sacador                                                                                                            | 002               | Alfabético   |                      |
| t11          | Nosso número                                                                                                             | 015               | Alfanumérico |                      |
| t12          | Espécie do título                                                                                                        | 003               | Alfabético   |                      |
| t13          | Número do título                                                                                                         | 011               | Alfanumérico |                      |
| t14          | Data da emissão do título                                                                                                | 008               | Numérico     | Nenhuma              |
| t15          | Data de vencimento do título                                                                                             | 008               | Numérico     | Nenhuma              |
| t16          | Tipo de moeda                                                                                                            | 003               | Numérico     | Nenhuma              |
| t17          | Valor do título                                                                                                          | 014               | Numérico     | 2                    |
| t18          | Saldo do título (valor a protestar)                                                                                      | 014               | Numérico     | 2                    |
| t19          | Praça de Pagamento                                                                                                       | 020               | Alfanumérico |                      |
| t20          | Tipo de endosso – Fixo Branco                                                                                            | 001               | Alfabético   |                      |
| t21          | Informação sobre aceite – Preencher com N                                                                                | 001               | Alfabético   |                      |
| t22          | Número de controle de devedores (sequencial dos devedores do título)                                                     | 001               | Numérico     | Nenhuma              |
| t23          | Nome do devedor                                                                                                          | 045               | Alfanumérico |                      |
| t24          | Tipo de documento do devedor: 001=CNPJ ou 002= CPF                                                                       | 003               | Numérico     | Nenhuma              |
| t25          | Número do documento do devedor (para CPF informar zero à esquerda)                                                       | 014               | Numérico     | Nenhuma              |
| t26          | R.G. (não informar)                                                                                                      | 011               | Alfanumérico |                      |
| t27          | Endereço do devedor                                                                                                      | 045               | Alfanumérico |                      |
| t28          | CEP do devedor                                                                                                           | 008               | Numérico     | Nenhuma              |
| t29          | Cidade do devedor                                                                                                        | 020               | Alfanumérico |                      |
| t30          | UF do devedor                                                                                                            | 002               | Alfabético   |                      |
| t31          | Uso restrito do Serviço de Distribuição – Preencher com Zero                                                             | 002               |              |                      |
| t32          | Uso restrito do Serviço de Distribuição – Preencher com Zero                                                             | 010               |              |                      |
| t33          | Uso restrito do Serviço de Distribuição – Preencher com Branco                                                           | 001               |              |                      |
| t34          | Uso restrito do Serviço de Distribuição – Preencher com Zero                                                             | 008               |              |                      |
| t35          | Uso restrito do Serviço de Distribuição – Preencher com Zero                                                             | 010               |              |                      |
| t36          | Fixo I – Imagem                                                                                                          | 001               |              |                      |
| t37          | Uso restrito do Serviço de Distribuição – Preencher com Zero                                                             | 008               |              |                      |
| t38          | Uso restrito do Serviço de Distribuição – Preencher com Branco                                                           | 002               |              |                      |
| t39          | Bairro do devedor                                                                                                        | 020               |              |                      |
| t40          | Uso restrito do Serviço de Distribuição – Preencher com Zero                                                             | 010               |              |                      |
| t41          | Uso restrito do Serviço de Distribuição – Preencher com Zero                                                             | 006               |              |                      |
| t42          | Uso restrito da Centralizadora (CRA) – Preencher com Zero                                                                | 010               |              |                      |
| t43          | Fixo – 0                                                                                                                 | 005               |              |                      |
| t44          | Fixo – 0                                                                                                                 | 015               |              |                      |
| t45          | Fixo – 0                                                                                                                 | 003               |              |                      |
| t46          | Fixo – 0                                                                                                                 | 001               |              |                      |
| t47          | Uso restrito do Serviço de Distribuição – Preencher com Branco                                                           | 008               |              |                      |
| t48          | Fixo – Branco                                                                                                            | 001               |              |                      |
| t49          | Fixo – Branco                                                                                                            | 001               |              |                      |
| t50          | Uso restrito dos cartórios – preencher com zeros                                                                         | 010               |              |                      |
| t51          | Imagens dos documentos zipados e convertidos em base64 (<mark style="color:red;">**Não inserir em co-devedores**</mark>) |                   |              |                      |
| t52          | Sequencial do registro                                                                                                   | 004               |              | Numérico             |

**REGISTRO DE TRAILLER – ARQUIVO REMESSA (Tag tl)**

***

| **Atributo** | _**Descrição**_                                                                     | _**Tam**_**anho** | _**Tipo**_   | _**Casas Decimais**_ |
| ------------ | ----------------------------------------------------------------------------------- | ----------------- | ------------ | -------------------- |
| t01          | Identifica o registro trailler no arquivo – Constante 9                             | 001               | Numérico     | Nenhuma              |
| t02          | Código do apresentante                                                              | 003               | Numérico     | Nenhuma              |
| t03          | Nome do apresentante                                                                | 040               | Alfabético   |                      |
| t04          | Data do envio do arquivo de remessa                                                 | 008               | Numérico     | Nenhuma              |
| t05          | <p>Somatório de Segurança<br>(somar as tags h09+h10+h11+h12 do registro HEADER)</p> | 005               | Numérico     | Nenhuma              |
| t06          | Somatório do campo t18 do registro de transação                                     | 018               | Numérico     | 2                    |
| t07          | Fixo – Branco                                                                       | 521               | Alfanumérico |                      |
| t08          | Sequencial do registro                                                              | 004               | Numérico     | Nenhuma              |
