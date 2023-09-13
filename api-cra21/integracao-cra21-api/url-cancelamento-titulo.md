# URL/cancelamento-titulo

Parâmetros

<table data-header-hidden><thead><tr><th width="144.33333333333331"></th><th width="500"></th><th></th></tr></thead><tbody><tr><td><strong>Campo</strong></td><td><strong>Descrição</strong></td><td><strong>Opcional</strong></td></tr><tr><td>status</td><td><p>Preencher com 2.</p><ul><li>2: Não baixados</li></ul></td><td></td></tr><tr><td>idCartorio</td><td>Recuperado após autenticação ou através do serviço <strong>URL/cartorio</strong></td><td>X</td></tr></tbody></table>

**Parâmetros passados via GET**

**Resposta**

```markup
    {
  "_links": {
    "self": {
      "href": "http://craUF.api.crabr.com.br/cancelamento-titulo?status=2"
    }
  },
  "_embedded": {
    "cancelamento_titulo": [
      {
        "id": 1,
        "dataCancelamento": {
          "date": "2017-04-06 13:48:43.000000",
          "timezone_type": 3,
          "timezone": "America/Sao_Paulo"
        },
        "protocolo": "0000949709",
        "dataProtocolo": {
          "date": "2013-09-12 00:00:00.000000",
          "timezone_type": 3,
          "timezone": "America/Sao_Paulo"
        },
        "devedor": "FULANO DE TAL",
        "numero": "1234567",
        "valor": "100.00",
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
        "_links": {
          "self": {
            "href": "http://craUF.api.crabr.com.br/cancelamento-titulo/1"
          }
        }
      }
    ]
  },
  "total_items": 1
}
```
