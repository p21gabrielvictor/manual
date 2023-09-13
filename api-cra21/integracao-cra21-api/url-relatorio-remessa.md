# URL/relatorio-remessa

Parâmetros

<table data-header-hidden><thead><tr><th width="183.33333333333331"></th><th width="460"></th><th></th></tr></thead><tbody><tr><td><strong>Campo</strong></td><td><strong>Descrição</strong></td><td><strong>Opcional</strong></td></tr><tr><td>visao</td><td>Modelo do relatório “Analítico detalhado". Preencher com: <strong>“3"</strong></td><td></td></tr><tr><td>dataInicial</td><td>Data inicial do relatório. Preencher da seguinte forma: <strong>dmy</strong> Ex: 10102017</td><td></td></tr><tr><td>dataFinal</td><td>Data final do relatório. Preencher da seguinte forma: <strong>dmy</strong> Ex: 25102018</td><td></td></tr><tr><td>tipoApresentante</td><td><p>Informando este parâmetro, o serviço retornará apresentantes do tipo informado. Preencher com 1, 2, 3, 4, 5 ou 0.</p><ul><li>1: Todos</li><li>2: Tipo banco</li><li>3: Tipo convênio</li><li>4: Somente convênios públicos</li><li>5: Somente convênios privados</li><li>0: Específico</li></ul></td><td>X</td></tr><tr><td>idApresentante</td><td>Recuperado através do serviço <strong>URL/apresentante</strong><br><strong>ATENÇÃO</strong> : Ao informar o <strong>idApresentante</strong> o campo <strong>tipoApresentante</strong> deve ser preenchido com <strong>0</strong>.</td><td>X</td></tr></tbody></table>

**Parâmetros passados via GET**

**Reposta**

```
{
    "_links": {
        "self": {
            "href": "http://df.teste.craapi.com.br/relatorio-remessa?visao=3&amp;dataInicial=10102017&amp;
dataFinal=24102017&amp;idApresentante=11&amp;tipoApresentante=0"
        }
    },
    "_embedded": {
        "relatorio_remessa": [
            {
                "id": 1779552,
                "devedores": [
                    {
                        "nome": "DEVEDOR XXXXXXXXXX",
                        "tipoDocumento": "CNPJ",
                        "documento": "00000000000000"
                    }
                ],
                "retornos": [
                    {
                        "id": 0000000,
                        "dataApresentante": {
                            "date": "2018-06-05 12:15:25.000000",
                            "timezone_type": 3,
                            "timezone": "America/Sao_Paulo"
                        },
                        "dataCartorio": {
                            "date": "2017-10-16 16:22:40.000000",
                            "timezone_type": 3,
                            "timezone": "America/Sao_Paulo"
                        },
                        "ocorrencia": {
                            "codigo": "1",
                            "descricao": "Pago",
                            "data": {
                                "date": "2017-10-16 00:00:00.000000",
                                "timezone_type": 3,
                                "timezone": "America/Sao_Paulo"
                            }
                        },
                        "valor": "175.11",
                        "saldo": "175.11",
                        "protocolo": "8005774633",
                        "dataProtocolo": {
                            "date": "2017-10-16 00:00:00.000000",
                            "timezone_type": 3,
                            "timezone": "America/Sao_Paulo"
                        },
                        "nossoNumero": "109-00401605-2",
                        "sequencial": "004893",
                        "status": "LIBERADO"
                    }
                ],
                "cartorio": {
                    "id": 10,
                    "nome": "1º Ofício de Protesto de Títulos da P21",
                    "documento": "04364134000142",
                    "uf": "DF",
                    "tipo": "CARTORIO",
                    "codigo": "67",
                    "telefones": [
                        "6100000000",
                        "6100000000"
                    ],
                    "fax": [
                        "6100000000"
                    ],
                    "emails": [
                        {
                            "id": 14,
                            "nome": "fake",
                            "email": "fake@p21sistemas.com.br"
                        }
                    ],
                    "municipio": {
                        "id": 1,
                        "nome": "Brasília",
                        "codigo": "5300108"
                    }
                },
                "apresentante": {
                    "id": 11,
                    "nome": "Itaú",
                    "codigo": "341"
                },
                "protocolo": "8005774633",
                "dataProtocolo": {
                    "date": "2017-10-16 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America/Sao_Paulo"
                },
                "dataRemessa": {
                    "date": "2017-10-16 15:44:48.000000",
                    "timezone_type": 3,
                    "timezone": "America/Sao_Paulo"
                },
                "dataConfirmacao": {
                    "date": "2017-10-16 15:49:20.000000",
                    "timezone_type": 3,
                    "timezone": "America/Sao_Paulo"
                },
                "dataVencimento": "05/10/2017",
                "valor": "175.11",
                "saldo": "175.11",
                "situacao": "RETORNADO",
                "numeroTitulo": "997462",
                "dataOcorrencia": null,
                "valorCra": "10.00",
                "_links": {
                    "self": {
                        "href": "http://df.teste.craapi.com.br/relatorio-remessa/1779552"
                    }
                }
            }
        ]
    }
    "total_items": 1
}
```
