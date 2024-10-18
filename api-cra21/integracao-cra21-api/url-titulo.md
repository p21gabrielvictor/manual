# URL/titulo



{% tabs %}
{% tab title="URL/titulo" %}
**Parâmetros passados via GET**

**Parâmetros**

<table><thead><tr><th width="199.90121796419186">Campo</th><th width="402">Descrição</th><th>Opcional</th></tr></thead><tbody><tr><td>idCartorio</td><td>Recuperado após autenticação ou através do serviço URL/cartorio</td><td>X</td></tr><tr><td>idApresentante</td><td>Recuperado após autenticação ou através do serviço URL/apresentante</td><td>X</td></tr><tr><td>identificador</td><td>Número identificador do título</td><td>X</td></tr><tr><td>numeroTitulo</td><td>Número do título</td><td>X</td></tr><tr><td>documentoDevedor</td><td>Documento do devedor do título</td><td>X</td></tr><tr><td>documentoCredor</td><td>CPF/CNPJ do credor do título</td><td>X</td></tr><tr><td>nomeCredor</td><td>Nome do credor do título</td><td>X</td></tr><tr><td>ocorrenciaRetorno</td><td>Ocorrência do título, parâmetros de busca: protesto, pagamento, cacelamento, sustação, devolução, desistência</td><td>X</td></tr><tr><td>dataRetorno</td><td>Data do retorno</td><td>X</td></tr></tbody></table>
{% endtab %}

{% tab title="Resposta" %}
**Resposta:**

```markup
  {
    "_links": {
        "self": {
            "href": "http://craUF.api.crabr.com.br/titulo?idCartorio=&amp;numeroTitulo=&amp;documentoDevedor=00000000000
             &amp;ocorrenciaRetorno=protesto"
        }
    },
    "_embedded": {
        "titulo": [
            {
                "id": 1,
                "numeroTitulo": "00000",
                "nossoNumero": "000-00000000-0",
                "protocolo": "0000000000",
                "dataProtocolo": {
                    "date": "2017-01-18 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America/Sao_Paulo"
                },
                "dataEmissao": {
                    "date": "2016-12-07 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America/Sao_Paulo"
                },
                "dataVencimento": "00/00/2017",
                "valor": "000.00",
                "saldo": "000.00",
                "especie": "DMI",
                "descricaoEspecie": "Especie do título",
                "endosso": "M",
                "situacao": "RETORNADO",
                "nomeSacador": "TESTE 123",
                "tipoDocumentoSacador": "CNPJ",
                "documentoSacador": "00000000000000",
                "nomeCedente": "TESTE 123",
                "devedores": [
                    {
                        "nome": "DEVEDOR DEVEDOR",
                        "tipoDocumento": "CNPJ",
                        "documento": "00000000000000"
                    }
                ],
                "apresentante": {
                    "id": 11,
                    "nome": "APRESENTANTE",
                    "codigo": "999",
                    "endereco":             {
                       "endereco": "Endereco de testes",
                       "bairro": "Centro",
                       "cep": "99999999",
                       "uf": "UF"
                    },
                    "telefones":             [
                       "6199999999",
                       "61999999999"
                    ],
                    "fax": ["61888888888"],
                    "emails":             [
                                      {
                          "id": 00,
                          "nome": "Email 1",
                          "email": "teste.@gmail.com"
                       },
                                      {
                          "id": 01,
                          "nome": "Email 2",
                          "email": "teste.@gmail.com"
                       }
                    ]
                },
                "cartorio": {
                    "id": 01,
                    "nome": "1º Ofício de testes",
                    "documento": "00000000000000",
                    "uf": "UF",
                    "tipo": "CARTORIO",
                    "codigo": "01",
                    "endereco": {
                       "endereco": "Avenida Francisco Raulino, 2061-A",
                       "bairro": "Centro",
                       "cep": "64290000",
                       "uf": "PI"
                     },
                    "telefones": [
                        "6100000000"
                    ],
                    "fax": [
                        "6100000000"
                    ],
                    "emails": [
                        {
                            "id": 1,
                            "nome": "NOME QUALQUER",
                            "email": "TESTE@TESTE.com.br"
                        }
                    ],
                    "municipio": {
                        "id": 1,
                        "nome": "TESTELANDIA",
                        "codigo": "1234567"
                    }
                },
                "retornos": [
                    {
                        "id": 1234567,
                        "dataApresentante": {
                            "date": "2017-01-30 12:38:19.000000",
                            "timezone_type": 3,
                            "timezone": "America/Sao_Paulo"
                        },
                        "dataCartorio": {
                            "date": "2017-01-30 12:38:19.000000",
                            "timezone_type": 3,
                            "timezone": "America/Sao_Paulo"
                        },
                        "ocorrencia": {
                            "codigo": "2",
                            "descricao": "Protestado",
                            "data": {
                                "date": "2017-01-27 00:00:00.000000",
                                "timezone_type": 3,
                                "timezone": "America/Sao_Paulo"
                            }
                        },
                        "valor": "000.00",
                        "saldo": "000.00",
                        "protocolo": "0000000000",
                        "dataProtocolo": {
                            "date": "2017-01-19 00:00:00.000000",
                            "timezone_type": 3,
                            "timezone": "America/Sao_Paulo"
                        },
                        "nossoNumero": "000-00000000-0",
                        "sequencial": "000001",
                        "status": "LIBERADO"
                    }
                ],
                "confirmacao": {
                    "id": 00000,
                    "dataConfirmacao": {
                        "date": "2017-01-18 11:41:35.000000",
                        "timezone_type": 3,
                        "timezone": "America/Sao_Paulo"
                    }
                }, 
                "remessa": {
                    "id": 00000,
                    "sequencial": "009999",
                    "nomeArquivo": "B9999999.181",
                    "data":             {
                       "date": "2018-04-17 08:29:27.000000",
                       "timezone_type": 3,
                       "timezone": "America/Sao_Paulo"
                    }
                }, 
                "custas":[
                  {
                    "tipo": "cancelamento",
                    "valor" : 10.34,
                    "vigencia":             {
                       "date": "2022-04-17 08:29:27.000000",
                       "timezone_type": 3,
                       "timezone": "America/Sao_Paulo"
                    }
                  },
                {
                    "tipo": "desistencia",
                    "valor" : 25.69,
                    "vigencia":             {
                       "date": "2022-04-17 08:29:27.000000",
                       "timezone_type": 3,
                       "timezone": "America/Sao_Paulo"
                    }
                  },
                ],
                "andamentos": [
                    {
                        "codigo": "AA",
                        "data": {
                            "date": "2024-10-08 19:05:45.000000",
                            "timezone_type": 3,
                            "timezone": "America/Sao_Paulo"
                        }
                    },
                    {
                        "codigo": "AB",
                        "data": {
                            "date": "2024-10-09 11:18:32.000000",
                            "timezone_type": 3,
                            "timezone": "America/Sao_Paulo"
                        }
                    },
                ],
                "_links": {
                    "self": {
                        "href": "http://craUF.api.crabr.com.br/titulo/0000000000"
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
