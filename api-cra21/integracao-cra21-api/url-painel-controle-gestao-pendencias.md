# URL/painel-controle/gestao-pendencias

Parâmetros

| **Campo** | **Descrição**                                                                                               | **Opcional** |
| --------- | ----------------------------------------------------------------------------------------------------------- | ------------ |
| dias      | Dias para consulta                                                                                          | X            |
| novoPrazo | <p>Preencher com 0 ou 1.</p><ul><li>0: Não conziderar novo prazo</li><li>1: Considerar novo prazo</li></ul> | X            |

**Parâmetros passados via GET**

**Resposta**

```
   {
  "_links": {
    "self": {
      "href": "http://craUF.api.crabr.com.br/painel-controle/gestao-pendencias"
    }
  },
  "_embedded": {
    "gestao_pendencias": [
      {
        "id": 1,
        "protocolo": "0000000001",
        "dataProtocolo": {
          "date": "2017-01-05 00:00:00.000000",
          "timezone_type": 3,
          "timezone": "America/Sao_Paulo"
        },
        "nossoNumero": "100000000000000",
        "numeroTitulo": "1000000000",
        "especie": "DMI",
        "saldo": "100.00",
        "remessa": {
          "sequencial": "00001",
          "data": {
            "date": "2017-01-05 09:47:03.000000",
            "timezone_type": 3,
            "timezone": "America/Sao_Paulo"
          }
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
        "justificativas": [
          {
            "id": 1,
            "dataRegistro": {
              "date": "2017-06-20 00:00:00.000000",
              "timezone_type": 3,
              "timezone": "America/Sao_Paulo"
            },
            "novoPrazo": {
              "date": "2017-06-20 00:00:00.000000",
              "timezone_type": 3,
              "timezone": "America/Sao_Paulo"
            },
            "texto": "Justificativas",
            "usuario": {
              "id": 2,
              "tipo": "CRA",
              "usuario": "crapi",
              "perfil": {
                "id": 2,
                "nome": "Administrador CRA"
              },
              "cra": {
                "id": 1,
                "razaoSocial": "Instituto de Estudos de Protesto de Titulos do Brasil - Seção UF"
              }
            }
          }
        ],
        "_links": {
          "self": {
            "href": "http://craUF.api.crabr.com.br/painel-controle/gestao-pendencias"
          }
        }
      }
    ]
  },
  "total_items": 1
}
```

\
