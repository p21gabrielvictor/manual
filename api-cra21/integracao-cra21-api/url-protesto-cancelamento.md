# URL/protesto-cancelamento

Parâmetros

<table data-header-hidden><thead><tr><th width="178.33333333333331"></th><th width="466"></th><th></th></tr></thead><tbody><tr><td><strong>Campo</strong></td><td><strong>Descrição</strong></td><td><strong>Opcional</strong></td></tr><tr><td>dataInicial</td><td>Data inicial do período de apresentação dos títulos Preencher da seguinte forma: <strong>dmy</strong> Ex: 01012017</td><td></td></tr><tr><td>dataFinal</td><td>Data final do período de apresentação dos títulos Preencher da seguinte forma: <strong>dmy</strong> Ex: 01012017</td><td></td></tr><tr><td>idCartorio</td><td>Recuperado após autenticação ou através do serviço <strong>URL/cartorio</strong> Ao informar esse parâmetro, o serviço irá retornar somente títulos do cartório informado</td><td>X</td></tr><tr><td>tipoApresentante</td><td><p>Informando este parâmetro, o serviço irá retornar apresentantes do tipo informado Preencher com 1,2,3,4 ou 5.</p><ul><li>1: Todos</li><li>2: Tipo banco</li><li>3: Tipo convênio</li><li>4: Somente convênios públicos</li><li>5: Somente convênios privados</li><li>0: Específico</li></ul></td><td>X</td></tr><tr><td>idApresentante</td><td>Recuperado após autenticação ou através do serviço <strong>URL/apresentante</strong> <strong>ATENÇÃO</strong> : Ao informar o <strong>idApresentante</strong> o campo <strong>tipoApresentante</strong> deve ser preenchido com <strong>0</strong></td><td>X</td></tr></tbody></table>

**Obs:** Quando não possuir com autorização cancelamento e com autorização desistência o relatório deve ser preenchido como 100% Não cancelado **Parâmetros passados via GET**

```
    {
  "_links": {
    "self": {
      "href": "http://craUF.api.crabr.com.br/protesto-cancelamento?dataInicial=03012017&amp;dataFinal=03012017"
    }
  },
  "_embedded": {
    "protesto_cancelamento": [
      {
        "ocorrencia": "Com autorização cancelamento",
        "totalOcorrencia": "1118",
        "valorOcorrencia": "1434296.64"
      },
      {
        "ocorrencia": "Com autorização desistência",
        "totalOcorrencia": "0",
        "valorOcorrencia": "0"
      },
      {
        "ocorrencia": "Sem autorização",
        "totalOcorrencia": "6771",
        "valorOcorrencia": "13743638.45"
      }
    ]
  },
  "total_items": 3
}
```
