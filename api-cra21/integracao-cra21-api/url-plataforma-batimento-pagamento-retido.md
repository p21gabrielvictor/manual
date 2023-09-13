# URL/plataforma-batimento/pagamento-retido

Parâmetros

<table data-header-hidden><thead><tr><th width="158.33333333333331"></th><th width="484"></th><th></th></tr></thead><tbody><tr><td><strong>Campo</strong></td><td><strong>Descrição</strong></td><td><strong>Opcional</strong></td></tr><tr><td>idCartorio</td><td>Solicitado através do serviço <strong>URL/cartorio</strong></td><td>X</td></tr><tr><td>idApresentante</td><td>Solicitado através do serviço <strong>URL/apresentante</strong></td><td>X</td></tr></tbody></table>

**Parâmetros passados via GET**

**Resposta**

```
   {
  "_links": {
    "self": {
      "href": "http://craUF.api.crabr.com.br/plataforma-batimento/pagamento-retido"
    }
  },
  "_embedded": {
    "pagamento_retido": [
      {
        "id": 25214,
        "data": {
          "date": "2017-02-07 00:00:00.000000",
          "timezone_type": 3,
          "timezone": "America/Sao_Paulo"
        },
        "valor": {
          "retorno": "968.87",
          "comprovado": "0.00",
          "liberado": "0.00"
        },
        "comprovantes": [],
        "apresentante": {
          "id": 8,
          "nome": "BANCO SA",
          "codigo": "000"
        },
        "cartorio": {
          "id": 64,
          "nome": "Cartorio 1º Oficio",
          "documento": "0000000000",
          "uf": "UF",
          "codigo": "00",
          "telefones": [],
          "fax": [],
          "emails": [
            {
              "id": 26,
              "nome": "Usuário",
              "email": "email@email.com.br"
            }
          ],
          "municipio": {
            "id": 155,
            "nome": "Município",
            "codigo": "0000000"
          }
        },
        "retornos": [
          {
            "id": 31109,
            "data": {
              "date": "2017-02-08 00:00:00.000000",
              "timezone_type": 3,
              "timezone": "America/Sao_Paulo"
            },
            "sequencial": "000160",
            "status": "RETIDO",
            "repasse": 968.87,
            "titulos": [
              {
                "id": 419194,
                "data": {
                  "date": "2017-02-08 00:00:00.000000",
                  "timezone_type": 3,
                  "timezone": "America/Sao_Paulo"
                },
                "ocorrencia": {
                  "codigo": "1",
                  "descricao": "Pago",
                  "data": {
                    "date": "2017-01-27 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America/Sao_Paulo"
                  }
                },
                "valor": "968.87",
                "saldo": "968.87",
                "protocolo": "0000009966",
                "dataProtocolo": {
                  "date": "2017-01-23 00:00:00.000000",
                  "timezone_type": 3,
                  "timezone": "America/Sao_Paulo"
                },
                "nossoNumero": "946730000347494",
                "sequencial": "000160",
                "status": "RETIDO"
              }
            ]
          }
        ],
        "_links": {
          "self": {
            "href": "http://craUF.api.crabr.com.br/plataforma-batimento/pagamento-retido"
          }
        }
      }
    ]
  },
  "total_items": 1
}
```
