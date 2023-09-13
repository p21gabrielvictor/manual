# URL/remessa

Parâmetros

<table data-header-hidden><thead><tr><th width="167.33333333333331"></th><th width="467"></th><th></th></tr></thead><tbody><tr><td><strong>Campo</strong></td><td><strong>Descrição</strong></td><td><strong>Opcional</strong></td></tr><tr><td>status</td><td><p>Preencher com 1.</p><ul><li>1: Remessas enviadas não confirmadas</li></ul></td><td></td></tr><tr><td>titulos</td><td>Ao informar esse parâmetro com 1, o serviço irá retornar os títulos da remessa</td><td>X</td></tr><tr><td>idCartorio</td><td>Recuperado após autenticação ou através do serviço <strong>URL/cartorio</strong></td><td>X</td></tr><tr><td>idApresentante</td><td>Recuperado após autenticação ou através do serviço <strong>URL/apresentante</strong></td><td>X</td></tr></tbody></table>

**Parâmetros passados via GET**

**Resposta**

```markup
   {
    "_links": {
        "self": {
            "href": "http://craUF.api.crabr.com.br/remessa?status=1&amp;titulos=1"
        }
    },
    "_embedded": {
        "remessa": [
            {
                "id": 1,
                "sequencial": "000001",
                "nomeArquivo": "B90C2203.172",
                "data": {
                    "date": "2017-03-22 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America/Sao_Paulo"
                },
                "titulos": [
                    {
                        "id": 5,
                        "numeroTitulo": "00000000000",
                        "nossoNumero": "000000000000",
                        "protocolo": null,
                        "dataProtocolo": null,
                        "dataEmissao": {
                            "date": "2017-03-14 00:00:00.000000",
                            "timezone_type": 3,
                            "timezone": "America/Sao_Paulo"
                        },
                        "dataVencimento": "A VISTA",
                        "valor": "00.00"
                        "saldo": "00.00",
                        "especie": "CDA",
                        "endosso": null,
                        "situacao": "ENVIADO",
                        "nomeSacador": "BANCO FICTICIO",
                        "tipoDocumentoSacador": "CNPJ",
                        "documentoSacador": "00000000000000",
                        "nomeCedente": "BANCO FICTICIO",
                        "devedores": [
                            {
                                "nome": "DEVEDOR",
                                "tipoDocumento": "CNPJ",
                                "documento": "00000000000000"
                            }
                        ],
                        "apresentante": {
                            "id": 1,
                            "nome": "Banco Ficticio",
                            "codigo": "00A"
                        },
                        "cartorio": null,
                        "retornos": [],
                        "confirmacao": null
                    }
                ],
                "cartorio": {
                    "id": 2,
                    "nome": "Cartório de Protesto",
                    "documento": "00000000000000",
                    "uf": "GO",
                    "tipo": "CARTORIO",
                    "codigo": "01",
                    "telefones": [
                        "000000000"
                    ],
                    "fax": [],
                    "emails": [
                        {
                            "id": 1,
                            "nome": "Cartório de Protesto",
                            "email": "cartorio@cartorio.com.br"
                        }
                    ],
                    "municipio": {
                        "id": 2,
                        "nome": "Município",
                        "codigo": "0000000"
                    }
                },
                "apresentante": {
                    "id": 1,
                    "nome": "Banco Ficticio",
                    "codigo": "00A"
                },
                "_links": {
                    "self": {
                        "href": "http://craUF.api.crabr.com.br/remessa/1"
                    }
                }
            }
        ]
    },
    "total_items": 1
}
```
