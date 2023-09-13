# URL/instrumento

Parâmetros

<table data-header-hidden><thead><tr><th width="205.33333333333331"></th><th width="409"></th><th></th></tr></thead><tbody><tr><td><strong>Campo</strong></td><td><strong>Descrição</strong></td><td><strong>Opcional</strong></td></tr><tr><td>codigoAutenticacao</td><td>Código de autenticação gerado no upload do instrumento de protesto</td><td></td></tr><tr><td>imagem</td><td><strong>1</strong> – Com imagem instrumento<br><strong>0</strong> – Sem imagem instrumento</td><td></td></tr></tbody></table>

**Parâmetros passados via GET**

**Reposta**

```
 {
    "_links": {
        "self": {
            "href": "http://uf.teste.craapi.com.br/instrumento?codigoAutenticacao=XXX-XXX-XXX&amp;imagem=1"
        }
    },
    "_embedded": {
        "instrumento": [
            {
                "id": 479777,
                "devedores": [
                    {
                        "nome": "DEVEDOR TESTE",
                        "tipoDocumento": "CPF",
                        "documento": "00000000000"
                    }
                ],
                "cartorio": {
                    "nome": "1º Tabelionato de Protesto de Títulos "
                },
                "protocolo": "0000000000",
                "dataProtesto": {
                    "date": "2018-07-17 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America/Sao_Paulo"
                },
                "numeroTitulo": "124511",
                "saldoTitulo": "264.97",
                "imagem": "JVBERi0xLjbmRzdHJlYW0KZW5kb2JqCjUg"
                    "self": {
                        "href": "http://uf.teste.craapi.com.br/instrumento/558844"
                    }
                }
            }
        ]
    },
    "total_items": 1
}
```
