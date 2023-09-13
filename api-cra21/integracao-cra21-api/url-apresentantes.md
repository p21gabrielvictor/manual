# URL/apresentantes

Parâmetros de URL. Exemplo: **http://craUF.api.crabr.com.br/apresentantes/001**

| **Campo**                                   | **Descrição**                                                  | **Opcional** |
| ------------------------------------------- | -------------------------------------------------------------- | ------------ |
| /apresentantes                              | Recupera dados dos apresentantes.                              |              |
| /apresentantes/**código apresentante**      | Recupera dados do apresentante informado.                      | X            |
| /apresentantes/**?categoria=nomecategoria** | Recupera dados do apresentante conforme a categoria informada. | X            |

**Parâmetros passados via GET**

**Resposta**

```
{
    "id": 1048,
    "nome": "13ª Vara do Trabalho do Rio de Janeiro",
    "codigo": "G48",
    "documento": "12345678912345",
    "endereco": {
        "endereco": "Rua ",
        "bairro": "Centro",
        "cep": "99999999",
        "uf": "RJ",
        "cidade": "Rio de Janeiro"
    },
    "telefones": [
        "9999999999"
    ],
    "fax": [],
    "emails": "",
    "tipo": "CONVENIO",
    "tipoConvenio": "PUBLICO",
    "momentoCobranca": "CANCELAMENTO",
    "situacao": "ATIVO",
    "intimacao": "NAO",
    "categoria": {
        "id": 2,
        "nome": "Categoria 1"
    },
    "_links": {
        "self": {
            "href": "http://rj.teste.craapi.com.br/apresentante/1042"
        }
    }
}
```
