# URL/apresentante

Parâmetros

<table data-header-hidden><thead><tr><th width="182.33333333333331"></th><th width="462"></th><th></th></tr></thead><tbody><tr><td><strong>Campo</strong></td><td><strong>Descrição</strong></td><td><strong>Opcional</strong></td></tr><tr><td>dataInicial</td><td>Data inicial do período de apresentação dos títulos Preencher da seguinte forma: <strong>dmy</strong> Ex: 01012017</td><td></td></tr><tr><td>dataFinal</td><td>Data final do período de apresentação dos títulos Preencher da seguinte forma: <strong>dmy</strong> Ex: 01012017</td><td></td></tr><tr><td>idCartorio</td><td>Ao informar esse parâmetro, o serviço irá retornar somente os apresentante que possuam títulos no cartório informado</td><td>X</td></tr><tr><td>tipoApresentante</td><td><p>Informando este parâmetro, o serviço irá retornar apresentantes do tipo informado Preencher com 1,2,3,4 ou 5.</p><ul><li>1: Todos</li><li>2: Tipo banco</li><li>3: Tipo convênio</li><li>4: Somente convênios públicos</li><li>5: Somente convênios privados</li></ul></td><td>X</td></tr></tbody></table>

**Parâmetros passados via GET**

**Resposta**

```markup
    {
  "_links": {
    "self": {
      "href": "http://craUF.api.crabr.com.br/apresentante?dataInicial=03012017&amp;dataFinal=03012017"
    }
  },
  "_embedded": {
    "apresentante":
    [
      {
        "id": 91,
        "nome": "BANCO SA",
        "codigo": "777",
        "_links": {
          "self": {
            "href": "http://craUF.api.crabr.com.br/apresentante/91"
          }
        }
      },
      {
        "id": 1,
        "nome": "Banco INC",
        "codigo": "000",
        "_links": {
          "self": {
            "href": "http://craUF.api.crabr.com.br/apresentante/1"
          }
        }
      }
    ]
  },
  "total_items": 2
}
```
