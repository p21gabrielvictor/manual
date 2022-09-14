# Integração – CRA21 API

### URL de Acesso

{% hint style="warning" %}
_<mark style="color:red;"><mark style="background-color:yellow;">**ATENÇÃO**<mark style="background-color:yellow;"></mark><mark style="color:red;"><mark style="background-color:yellow;">: Substituir<mark style="background-color:yellow;"></mark> <mark style="color:red;"><mark style="background-color:yellow;"> </mark><mark style="color:red;"><mark style="background-color:yellow;">**UF**<mark style="background-color:yellow;"></mark> <mark style="color:red;"><mark style="background-color:yellow;"> </mark><mark style="color:red;"><mark style="background-color:yellow;">pelo estado desejado.<mark style="background-color:yellow;"></mark>_
{% endhint %}

**Homologação (ambiente de testes):** \
http://UF.hm.craapi.com.br\
__**Exemplo:** http://**df**.hm.craapi.com.br

**Produção (ambiente de funcionamento do sistema):** \
http://cra**UF**.api.crabr.com.br\
**Exemplo:**http://cra**df**.api.crabr.com.br

### Parâmetros de envio

* Autenticação básica: Usuário e senha do CRA21
* Headers:
  * Accept: application/json

### Serviços disponíveis

| Serviço                                      | Descrição                                                                  | Envio |
| -------------------------------------------- | -------------------------------------------------------------------------- | ----- |
| url/titulo                                   | Consulta de título                                                         | GET   |
| url/especie                                  | Consulta de espécie                                                        | GET   |
| url/cartorio                                 | Consulta de cartório                                                       | GET   |
| url/protesto-indevido                        | Consulta de protesto indevido                                              | GET   |
| url/remessa                                  | Serviço de consulta de remessas                                            | GET   |
| url/cancelamento                             | Consulta de arquivo de cancelamento                                        | GET   |
| url/cancelamento-titulo                      | Consulta as solicitações de cancelamentos de títulos                       | GET   |
| url/desistencia                              | Consulta de desistência                                                    | GET   |
| url/apresentante                             | Consulta de apresentantes com títulos no período informado.                | GET   |
| url/titulo-ocorrencia                        | Quantidade de títulos por ocorrência 2º                                    | GET   |
| url/produtividade-geral                      | Quantidade de títulos por ocorrência 1º                                    | GET   |
| url/protesto-cancelamento                    | Quantidade de protestos e cancelamentos                                    | GET   |
| url/titulo-especie                           | Quantidade de títulos por espécie                                          | GET   |
| url/painel-controle/gestao-pendencias        | Consultar os títulos pendentes de retorno                                  | GET   |
| url/plataforma-batimento/pagamento-retido    | Consulta todos títulos retidos na plataforma de batimento                  | GET   |
| url/plataforma-batimento/comprovantes-aberto | Consulta os comprovantes em abertos cadastrados na plataforma de batimento | GET   |
| url/pendencias/cartorio                      | Consulta as pendências do cartório                                         | GET   |
| url/instrumento                              | Consulta e download dos instrumentos de protesto                           | GET   |
| url/cedente                                  | Consulta de dados do cedente                                               | GET   |
| url/relatorio-remessa                        | Consulta aos dados do relatório de remessa analítico detalhado             | GET   |
| url/apresentantes                            | Consulta informações dos apresentantes.                                    | GET   |