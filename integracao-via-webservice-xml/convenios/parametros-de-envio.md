# Parâmetros de envio

* **Os dados (parâmetros) devem ser enviados via protocolo SOAP**
* **Ao consumir o WebService, em todos os serviços, a autenticação deverá ser realizada utilizando autenticação básica.**
  * Deverão ser passados os parâmetros de _usuário_ e _senha_, fornecidos pela CRA.
  * Após a autenticação serão validados os parâmetros de entrada e por último a crítica do arquivo
*   **Serviços disponíveis:**

    * | **Remessa**                | upload do arquivo de remessa                                                                                                                                                      |
      | -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
      | **Confirmacao**            | download do arquivo de confirmação                                                                                                                                                |
      | **Retorno**                | download do arquivo de retorno                                                                                                                                                    |
      | **Desistencia**            | upload de desistência                                                                                                                                                             |
      | **Cancelamento**           | upload de cancelamento                                                                                                                                                            |
      | **Autoriza\_Cancelamento** | upload de autorização de cancelamento                                                                                                                                             |
      | **Autoriza\_Desistencia**  | upload de autorização de desistência                                                                                                                                              |
      | **BoletoAutorizacao**      | consulta de boletos de autorização. Os detalhes desse serviço podem ser conferidos nesse [link](https://manual.crabr.com.br/manual/boletos_autorizacao_webservice-apresentante/). |
      | **Homologadas**            | download de comarcas homologadas                                                                                                                                                  |
      | **Consulta**               | consulta de título                                                                                                                                                                |
      | **Consulta\_Slip**         | consulta de dados do slip                                                                                                                                                         |
      | **Instrumento**            | consulta dos instrumentos eletrônicos.                                                                                                                                            |
      | **Imagem**                 | upload de imagens do título após o envio da remessa.                                                                                                                              |
      | **Oficio\_Titulo**         | upload do arquivo de ofício                                                                                                                                                       |


* **Parâmetros dos serviços disponíveis:**
*   Upload\\

    | **user\_arq**   | nome do arquivo no formato **FEBRABAN** |
    | --------------- | --------------------------------------- |
    | **user\_dados** | conteúdo do arquivo XML                 |
*   Download\\

    | **user\_arq** | nome do arquivo no formato **FEBRABAN** |
    | ------------- | --------------------------------------- |
*   Homologadas\\

    | **codapres** | informar o código do apresentante                      |
    | ------------ | ------------------------------------------------------ |
    | cartorios    | informar '1' para obter dados dos cartórios (OPCIONAL) |
*   Consulta\\

    | **nosso\_numero**  | nosso número do título no CRA21 |
    | ------------------ | ------------------------------- |
    | **numero\_titulo** | número do título no CRA21       |
*   Consulta\_Slip\\

    | **cod\_municipio**  | nome do arquivo no formato **FEBRABAN** |
    | ------------------- | --------------------------------------- |
    | **cod\_cartorio**   | conteúdo do arquivo XML                 |
    | **protocolo**       | conteúdo do arquivo XML                 |
    | **data\_protocolo** | conteúdo do arquivo XML                 |
*   Instrumento\\

    | **userArq** | formato informado em **Download e Consulta** |
    | ----------- | -------------------------------------------- |
*   Imagem\\

    | **userArq**   | nome do arquivo no formato **FEBRABAN**         |
    | ------------- | ----------------------------------------------- |
    | **userDados** | conteúdo do arquivo XML em **Envio de Imagens** |
*   Oficio\_Titulo

    | userArq   | **nome do arquivo no formato definido**        |
    | --------- | ---------------------------------------------- |
    | userDados | conteúdo do arquivo XML em **Envio de ofício** |


* **O encoding do XML deve corresponder com ISO-8859-1.**
* **Assim como no HTML, o XML possui entidades, que devem ser substituídas conforme tabela abaixo:**
  * | **De** | **Para** |
    | ------ | -------- |
    | <      | & lt;    |
    | >      | & gt;    |
    | &      | & amp;   |
    | ‘      | & apos;  |
    | “      | & quot;  |
