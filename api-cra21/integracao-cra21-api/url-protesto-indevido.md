# URL/protesto-indevido



{% tabs %}
{% tab title="URL/protesto-indevido" %}
Parâmetros

<table data-header-hidden><thead><tr><th width="130.66666666666666"></th><th width="456"></th><th></th></tr></thead><tbody><tr><td><strong>Campo</strong></td><td><strong>Descrição</strong></td><td><strong>Opcional</strong></td></tr><tr><td>idCartorio</td><td>Recuperado após autenticação ou através do serviço <strong>URL/cartorio</strong></td><td>X</td></tr></tbody></table>
{% endtab %}

{% tab title="Resposta" %}
```
 {
  "_links": {
    "self": {
      "href": "http://craUF.api.crabr.com.br/protesto-indevido?idCartorio=68"
    }
  },
  "_embedded": {
    "protesto_indevido": [
      {
        "id": 1,
        "numeroTitulo": "1000",
        "nossoNumero": "000000000000001",
        "protocolo": "1000000000",
        "dataProtocolo": {
          "date": "2017-02-03 00:00:00.000000",
          "timezone_type": 3,
          "timezone": "America/Sao_Paulo"
        },
        "dataEmissao": {
          "date": "2016-11-24 00:00:00.000000",
          "timezone_type": 3,
          "timezone": "America/Sao_Paulo"
        },
        "dataVencimento": "23/01/2017",
        "valor": "1000.00",
        "saldo": "1000.00",
        "sigla": "DMI",
        "endosso": "M",
        "devedores": [
          {
            "nome": "FULANO DE TAL",
            "documento": "00000000000000"
          }
        ],
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
            "href": "http://craUF.api.crabr.com.br/titulo/1"
          }
        }
      }
    ]
  },
  "total_items": 1
}
```
{% endtab %}
{% endtabs %}
