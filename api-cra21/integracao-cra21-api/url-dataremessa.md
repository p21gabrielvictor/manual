---
hidden: true
---

# url/dataRemessa

Parâmetros de URL. Exemplo: **http://craUF.api.crabr.com.br/titulo?dataRemessa=02122024**

| **Campo**         | **Descrição**                                                     | **Opcional** |
| ----------------- | ----------------------------------------------------------------- | ------------ |
| /**dataRemessa=** | Retorna apenas os títulos referentes à data de remessa informada. |              |

**Parâmetros passados via GET**

http://am.craapi.com.br/titulo?dataRemessa=02122024\&apenasTitulosDadosComplementares=0

**Resposta**

```
{
                "id": 6722859,
                "numeroTitulo": "00000/000",
                "nossoNumero": "00000/000000",
                "protocolo": "0000000000",
                "dataProtocolo": {
                    "date": "2024-01-01 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America/Sao_Paulo"
                },
                "dataEmissao": {
                    "date": "2024-01-01 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America/Sao_Paulo"
                },
                "dataVencimento": "01/01/2024",
                "valor": "13.43",
                "saldo": "23.79",
                "especie": "NCR",
                "descricaoEspecie": "Nota de Crédito Rural",
                "endosso": "M",
                "situacao": "DEVOLVIDO",
                "nomeSacador": "ABGAIL ZAMBRANO",
                "tipoDocumentoSacador": "CNPJ",
                "documentoSacador": "82294992000171",
                "nomeCedente": "ARIANE TELES",
                "devedores": [
                    {
                        "nome": "STEPHANIE SARAIVA CARMONA",
                        "tipoDocumento": "CNPJ",
                        "documento": "93248793000143",
                        "telefone": [
                            "8230677355"
                        ],
                        "email": [
                            "simon43@hotmail.com"
                        ]
                    }
                ],
                "apresentante": {
                    "id": 106,
                    "nome": "BANCO SANTANDER SA",
                    "codigo": "033",
                    "documento": "90400888000142",
                    "endereco": {
                        "endereco": "Rua Amador Bueno",
                        "bairro": "Santo Amaro",
                        "cep": "04752005",
                        "uf": "SP",
                        "cidade": "São Paulo"
                    },
                    "telefones": [
                        "9236424142"
                    ],
                    "fax": [],
                    "emails": [],
                    "tipo": "BANCO",
                    "tipoConvenio": null,
                    "momentoCobranca": "CANCELAMENTO",
                    "situacao": "ATIVO",
                    "intimacao": "NAO",
                    "categoria": ""
                },
                "cartorio": {
                    "id": 49,
                    "nome": "CARTORIO 1º OFICIO",
                    "documento": "00000000000000",
                    "uf": "uf",
                    "tipo": "CARTORIO",
                    "codigo": "01",
                    "endereco": {
                        "endereco": "RUA 31 DE MARÇO",
                        "bairro": "CENTRO",
                        "cep": "0000000",
                        "uf": "uf"
                    },
                    "telefones": [
                        "9733521177"
                    ],
                    "fax": [],
                    "emails": [
                        {
                            "id": 346,
                            "nome": "cartorio",
                            "email": "alessandra_betina_caldeira@solutionimoveis.com.br"
                        }
                    ],
                    "municipio": {
                        "id": 857,
                        "nome": "municipio",
                        "codigo": "0000102"
                    }
                },
                "retornos": [],
                "confirmacao": {
                    "id": 619922,
                    "dataConfirmacao": {
                        "date": "2024-01-01 00:00:00.000000",
                        "timezone_type": 3,
                        "timezone": "America/Sao_Paulo"
                    }
                },
                "remessa": {
                    "id": 644589,
                    "sequencial": "000043",
                    "nomeArquivo": "B0330212.241",
                    "data": {
                        "date": "2024-01-01 00:00:00.000000",
                        "timezone_type": 3,
                        "timezone": "America/Sao_Paulo"
                    }
                },
                "custas": [],
                "andamentos": [],
                "_links": {
                    "self": {
                        "href": "http://uf.teste.craapi.com.br/titulo/6722859"
                    }
                }
            },
```
