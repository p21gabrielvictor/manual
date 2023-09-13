# URL/cancelamento

Parâmetros

<table data-header-hidden><thead><tr><th width="166.33333333333331"></th><th width="468"></th><th></th></tr></thead><tbody><tr><td><strong>Campo</strong></td><td><strong>Descrição</strong></td><td><strong>Opcional</strong></td></tr><tr><td>status</td><td><p>Preencher com 2.</p><ul><li>2: Não baixados</li></ul></td><td></td></tr><tr><td>idCartorio</td><td>Recuperado após autenticação ou através do serviço <strong>URL/cartorio</strong></td><td>X</td></tr><tr><td>idApresentante</td><td>Recuperado após autenticação ou através do serviço <strong>URL/apresentante</strong></td><td>X</td></tr></tbody></table>

**Parâmetros passados via GET**

**Resposta**

```
 {
  "_links": {
    "self": {
      "href": "http://craUF.api.crabr.com.br/cancelamento?status=2"
    }
  },
  "_embedded": {
    "cancelamento": [
      {
        "id": 1,
        "nomeArquivo": "CP0000906.161",
        "data": {
          "date": "2016-06-09 10:34:21.000000",
          "timezone_type": 3,
          "timezone": "America/Sao_Paulo"
        },
        "cartorio": {
          "id": 1,
          "nome": "Cartório 1° Ofício",
          "documento": "00000000000000",
          "uf": "UF",
          "tipo": "CARTORIO",
          "codigo": "01",
          "telefones": [
            "0000000000",
            "0000000000"
          ],
          "fax": [
            "0000000000"
          ],
          "emails": [
            {
              "id": 1,
              "nome": "CARTÓRIO",
              "email": "cartorio@cartorio.com"
            }
          ],
          "municipio": {
            "id": 1,
            "nome": "Município",
            "codigo": "0000000"
          }
        },
        "apresentante": {
          "id": 1,
          "nome": "BANCO SA",
          "codigo": "000"
        },
        "_links": {
          "self": {
            "href": "http://craUF.api.crabr.com.br/cancelamento/1"
          }
        }
      }
    ]
  },
  "total_items": 1
}
```
