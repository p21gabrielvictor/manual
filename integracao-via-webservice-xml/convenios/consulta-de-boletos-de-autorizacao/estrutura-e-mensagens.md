# Estrutura e mensagens

#### Estrutura da resposta do serviço

**Atributos**

<table data-header-hidden><thead><tr><th width="173.57142857142856"></th><th></th></tr></thead><tbody><tr><td><strong>Atributo</strong></td><td><strong>Descrição</strong></td></tr><tr><td>boleto</td><td>base64 do boleto</td></tr><tr><td>nomeMunicipio</td><td>Nome do município</td></tr><tr><td>nomeCartorio</td><td>Nome do cartório</td></tr><tr><td>valorTitulo</td><td>Valor do título</td></tr><tr><td>saldoTitulo</td><td>Saldo do título</td></tr><tr><td>nossoNumero</td><td>Nosso número</td></tr><tr><td>nomeDevedor</td><td>Nome do devedor</td></tr></tbody></table>

### Exemplos de requisição e resposta

**Exemplo de requisição do serviço**

```xml
<soapenv:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:urn="urn:localhost">
   <soapenv:Header/>
   <soapenv:Body>
      <urn:BoletoAutorizacao soapenv:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/">
         <numeroTitulo xsi:type="xsd:string">999999999</numeroTitulo>
         <documentoDevedor xsi:type="xsd:string">999999999</documentoDevedor>
      </urn:BoletoAutorizacao>
   </soapenv:Body>
</soapenv:Envelope>
```

**Exemplo de resposta do serviço**

```xml
<relatorio>
  <boleto>JVBERi0xLjMKMyAwIG9iago</boleto>
  <nomeMunicipio>Nome do Município</nomeMunicipio>
  <nomeCartorio>Nome do cartório do município</nomeCartorio>
  <valorTitulo>99999.99</valorTitulo>
  <saldoTitulo>99999.99</saldoTitulo>
  <nossoNumero>99999999</nossoNumero>
  <nomeDevedor>Nome do Devedor</nomeDevedor>
</relatorio>
```

| **CÓDIGO** | **DESCRIÇÃO**                                            |
| ---------- | -------------------------------------------------------- |
| 2298       | Informe pelo menos o número do título                    |
| 2299       | Foi encontrado mais de um boleto com os dados informados |
| 2300       | Não foi encontrado boleto com os parâmetros informados   |
| 10003      | Acesso negado. Contate o administrador.                  |
