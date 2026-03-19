# Imagens da Remessa

{% hint style="warning" %}
Atenção: Este manual será desativado em breve e substituído por uma versão mais atualizada. Acesse a nossa nova documentação clicando aqui: [https://manual.p21website.com.br/ ](https://manual.p21website.com.br/%C2%A0)
{% endhint %}

[<mark style="color:green;">**`DOWNLOAD DO ARQUIVO EXEMPLO`**</mark>](https://github.com/p21sistemas/manual-cra-21/blob/main/EXEMPLO_ARQUIVO_IMAGENS_XML.zip?raw=true)

| **Descrição**                                                                                        | **Tamanho** | **Tipo**     | **Casas Decimais** | **Atributo**          |
| ---------------------------------------------------------------------------------------------------- | ----------- | ------------ | ------------------ | --------------------- |
| Tag de Remessas                                                                                      |             |              |                    | < remessas>           |
| Tag de Remessa                                                                                       |             |              |                    | < remessa>            |
| Número sequencial da remessa                                                                         | 006         | Numérico     | Nenhuma            | < sequencial>         |
| Código do Município da Praça de Pagamento                                                            | 007         | Alfanumérico |                    | < municipio>          |
| Tag de títulos da remessa                                                                            |             |              |                    | < titulos>            |
| Tag de título na remessa                                                                             |             |              |                    | < titulo>             |
| Documento do devedor                                                                                 | 014         | Numérico     | Nenhuma            | < documento\_devedor> |
| Nosso número                                                                                         | 015         | Alfanumérico |                    | < nosso\_numero>      |
| Número do Título                                                                                     | 011         | Alfanumérico |                    | < numero\_titulo>     |
| Saldo do Título                                                                                      | 011         | Numérico     | 2                  | < saldo>              |
| Imagem – arquivo compactado em formato .zip convertido em base 64. Extensões .pdf, .jpg, .png e .p7s |             |              |                    | < imagem>             |
