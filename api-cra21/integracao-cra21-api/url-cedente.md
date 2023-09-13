# URL/cedente

Parâmetros

| **Campo**        | **Descrição**                                                    | **Opcional** |
| ---------------- | ---------------------------------------------------------------- | ------------ |
| nome             | Nome do cedente                                                  |              |
| tipoApresentante | Tipo do apresentante. Informar 1 para bancos e 2 para convênios. |              |
| codigoFebraban   | Código do apresentante                                           |              |

**Parâmetros passados via GET**

**Reposta**

```
{
    "_links": {
        "self": {
            "href": "http://craUF.api.crabr.com.br/cedente?nome=maria%20da%20guia&amp;tipoApresentante=2&amp;codigoFebraban=90L"
        }
    },
    "_embedded": {
        "cedente": [
            {
                "id": 11697,
                "codigo": "074",
                "nome": "MARIA DA GUIA",
                "documento": "09626431751",
                "cep": "23330193",
                "endereco": "RUA MONTE ALEGRE 26, 179 AP 104",
                "cidade": "CIDADE",
                "uf": "UF",
                "_links": {
                    "self": {
                        "href": "http://craUF.api.crabr.com.br/cedente/11697"
                    }
                }
            },
        ]
    },
    "total_items": 1
}
```
