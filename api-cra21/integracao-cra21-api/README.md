# Integração – CRA21 API

### URL de Acesso

{% hint style="warning" %}
_<mark style="color:red;">**ATENÇÃO**</mark><mark style="color:red;">: Substituir</mark> <mark style="color:red;"></mark><mark style="color:red;">**UF**</mark> <mark style="color:red;"></mark><mark style="color:red;">pelo estado desejado.</mark>_

**Produção (ambiente de funcionamento do sistema):** \
[<mark style="color:green;">https://craUF.api.crabr.com.br/</mark>](https://crama.api.crabr.com.br/)\
**Exemplo:** [<mark style="color:green;">**https://crama.api.crabr.com.br/**</mark>](https://crama.api.crabr.com.br/)
{% endhint %}





**Produção (ambiente de funcionamento do sistema):** \
[https://craUF.api.crabr.com.br/](https://crama.api.crabr.com.br/)\
**Exemplo:** [<mark style="color:green;">**https://crama.api.crabr.com.br/**</mark>](https://crama.api.crabr.com.br/)

### Parâmetros de envio

* Autenticação básica: Usuário e senha do CRA21
* Headers:
  * Accept: application/json

### Serviços disponíveis

> _Nesta seção, os serviços são organizados conforme o tipo de cliente, facilitando a visualização do que está disponível para cada perfil._

#### Permissões CRA

| Serviço                        | Descrição                                                  | Método |
| ------------------------------ | ---------------------------------------------------------- | ------ |
| `/url/apresentante`            | Consulta de apresentantes com títulos no período informado | GET    |
| `/url/apresentantes`           | Consulta de apresentantes cadastrados                      | GET    |
| `/url/auth`                    | Autenticação                                               | GET    |
| `/url/cancelamento`            | Consulta de arquivo de cancelamento                        | GET    |
| `/url/cancelamento-titulo`     | Consulta as solicitações de cancelamentos de títulos       | GET    |
| `/url/cartorio`                | Consulta de cartório                                       | GET    |
| `/url/comprovantes-aberto`     | Consulta de comprovantes em aberto                         | GET    |
| `/url/desistencia`             | Consulta de desistência                                    | GET    |
| `/url/especie`                 | Consulta de espécie                                        | GET    |
| `/url/gestao-pendencias`       | Consultar os títulos pendentes de retorno                  | GET    |
| `/url/pagamento-retido`        | Consulta dos títulos retidos na plataforma de pagamento    | GET    |
| `/url/produtividade-geral`     | Quantidade de títulos por ocorrência 1º                    | GET    |
| `/url/protesto-cancelamento`   | Quantidade de protestos e cancelamentos                    | GET    |
| `/url/protesto-indevido`       | Consulta de protesto indevido                              | GET    |
| `/url/relatorio-remessa`       | Consulta de relatório de remessa                           | GET    |
| `/url/remessa`                 | Consulta de remessas                                       | GET    |
| `/url/titulo`                  | Consulta de título                                         | GET    |
| `/url/titulo-especie`          | Quantidade de títulos por espécie                          | GET    |
| `/url/titulo-ocorrencia`       | Quantidade de títulos por ocorrência 2º                    | GET    |
| `/apibasecedente/rest/cedente` | Consulta de cedentes                                       | GET    |



#### Permissões cartório



| Serviço                        | Descrição                                                  | Método |
| ------------------------------ | ---------------------------------------------------------- | ------ |
| `/url/apresentante`            | Consulta de apresentantes com títulos no período informado | GET    |
| `/url/apresentantes`           | Consulta de apresentantes cadastrados                      | GET    |
| `/url/auth`                    | Autenticação                                               | GET    |
| `/url/cancelamento`            | Consulta de arquivo de cancelamento                        | GET    |
| `/url/cancelamento-titulo`     | Consulta as solicitações de cancelamentos de títulos       | GET    |
| `/url/desistencia`             | Consulta de desistência                                    | GET    |
| `/url/especie`                 | Consulta de espécie                                        | GET    |
| `/url/produtividade-geral`     | Quantidade de títulos por ocorrência 1º                    | GET    |
| `/url/protesto-cancelamento`   | Quantidade de protestos e cancelamentos                    | GET    |
| `/url/protesto-indevido`       | Consulta de protesto indevido                              | GET    |
| `/url/remessa`                 | Serviço de consulta de remessas                            | GET    |
| `/url/titulo`                  | Consulta de título                                         | GET    |
| `/url/titulo-especie`          | Quantidade de títulos por espécie                          | GET    |
| `/url/titulo-ocorrencia`       | Quantidade de títulos por ocorrência 2º                    | GET    |
| `/url/pendencias-cartorio`     | Consulta de títulos pendentes de retorno                   | GET    |
| `/apibasecedente/rest/cedente` | Consulta de cedentes                                       | GET    |



Permissões distribuidor

| Serviço                      | Descrição                                                  | Método |
| ---------------------------- | ---------------------------------------------------------- | ------ |
| `/url/apresentante`          | Consulta de apresentantes com títulos no período informado | GET    |
| `/url/apresentantes`         | Consulta de apresentantes cadastrados                      | GET    |
| `/url/auth`                  | Autenticação                                               | GET    |
| `/url/cancelamento`          | Consulta de arquivo de cancelamento                        | GET    |
| `/url/cancelamento-titulo`   | Consulta as solicitações de cancelamentos de títulos       | GET    |
| `/url/desistencia`           | Consulta de desistência                                    | GET    |
| `/url/especie`               | Consulta de espécie                                        | GET    |
| `/url/produtividade-geral`   | Quantidade de títulos por ocorrência 1º                    | GET    |
| `/url/protesto-cancelamento` | Quantidade de protestos e cancelamentos                    | GET    |
| `/url/protesto-indevido`     | Consulta de protesto indevido                              | GET    |
| `/url/remessa`               | Serviço de consulta de remessas                            | GET    |
| `/url/titulo`                | Consulta de título                                         | GET    |
| `/url/titulo-especie`        | Quantidade de títulos por espécie                          | GET    |
| `/url/titulo-ocorrencia`     | Quantidade de títulos por ocorrência 2º                    | GET    |



Permissões convênio&#x20;

| Serviço                      | Descrição                               | Método |
| ---------------------------- | --------------------------------------- | ------ |
| `/url/auth`                  | Autenticação                            | GET    |
| `/url/cancelamento`          | Consulta de arquivo de cancelamento     | GET    |
| `/url/cartorio`              | Consulta de cartório                    | GET    |
| `/url/desistencia`           | Consulta de desistência                 | GET    |
| `/url/especie`               | Consulta de espécie                     | GET    |
| `/url/produtividade-geral`   | Quantidade de títulos por ocorrência 1º | GET    |
| `/url/protesto-cancelamento` | Quantidade de protestos e cancelamentos | GET    |
| `/url/remessa`               | Serviço de consulta de remessas         | GET    |
| `/url/titulo`                | Consulta de título                      | GET    |
| `/url/titulo-especie`        | Quantidade de títulos por espécie       | GET    |
| `/url/titulo-ocorrencia`     | Quantidade de títulos por ocorrência 2º | GET    |

Permissão apresentante

| Serviço                      | Descrição                               | Método |
| ---------------------------- | --------------------------------------- | ------ |
| `/url/auth`                  | Autenticação                            | GET    |
| `/url/cancelamento`          | Consulta de arquivo de cancelamento     | GET    |
| `/url/cartorio`              | Consulta de cartório                    | GET    |
| `/url/desistencia`           | Consulta de desistência                 | GET    |
| `/url/especie`               | Consulta de espécie                     | GET    |
| `/url/produtividade-geral`   | Quantidade de títulos por ocorrência 1º | GET    |
| `/url/protesto-cancelamento` | Quantidade de protestos e cancelamentos | GET    |
| `/url/remessa`               | Serviço de consulta de remessas         | GET    |
| `/url/titulo`                | Consulta de título                      | GET    |
| `/url/titulo-especie`        | Quantidade de títulos por espécie       | GET    |
| `/url/titulo-ocorrencia`     | Quantidade de títulos por ocorrência 2º | GET    |

