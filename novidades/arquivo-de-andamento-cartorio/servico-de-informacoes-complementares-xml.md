# Andamento em XML

O objetivo desse serviço é viabilizar que informações complementares dos títulos sejam enviadas para a CRA. \
Alguns cartórios já enviam para a CRA21 as informações de custas/emolumentos para consultas de eventuais retiradas e cancelamentos por parte dos apresentantes. Visando não criar uma nova rotina para o cartório, criarmos esse novo serviço acrescentando a informação do andamento do título. \
Nesse primeiro momento, o serviço receberá os dados do andamento do título no cartório e informações de emolumentos/custas cartorárias para eventuais consultas para retirada ou cancelamento. Esse serviço poderá ser usado por todos os cartórios interessados, mesmo os que não usavam a [<mark style="color:green;">rotina de custas disponibilizado anteriormente</mark>](../../integracao-via-webservice-xml/cartorios-distribuidores/estrutura-do-arquivo-de-remessa/emolumentos-dos-titulos.md)<mark style="color:green;">.</mark>

{% hint style="success" %}
O serviço de emolumentos continuará funcionando normalmente caso queira continuar usando ele apenas para envio dos emolumentos.
{% endhint %}

O serviço permitirá o recebimento das duas informações (andamento e custas) ou apenas uma delas.

{% tabs %}
{% tab title="Parâmetros de Envio" %}
* **Os dados (parâmetros) devem ser enviados via protocolo SOAP.**
* **Ao consumir o WebService, em todos os serviços, a autenticação deverá ser realizada utilizando autenticação básica.**
  * Deverão ser passados os parâmetros de _usuário_ e _senha_, fornecidos pela CRA.
  * Após a autenticação serão validados os parâmetros de entrada e por último a crítica do arquivo
* **Serviços disponíveis:**

<table data-header-hidden><thead><tr><th width="200"></th><th></th></tr></thead><tbody><tr><td>TituloComplemento</td><td>Envio do status do andamento no cartório e emolumentos/custas cartorárias para eventuais consultas para retirada ou cancelamento.</td></tr></tbody></table>

*   **Parâmetros dos serviços disponíveis:**

    * **Upload**

    <table data-header-hidden><thead><tr><th width="185"></th><th></th></tr></thead><tbody><tr><td><strong>userArq</strong></td><td>Nome do arquivo no formato MAAADDMM.AAS</td></tr><tr><td><strong>userDados</strong></td><td>Conteúdo do arquivo XML.</td></tr></tbody></table>

    * **O encoding do XML deve estar de acordo com ISO-8859-1.**
    * **O conteúdo dos arquivos enviados para CRA devem seguir o padrão de codificação ASCII**
{% endtab %}

{% tab title="Nomenclatura do arquivo" %}
* **MCCCDDMM.AAS:**
  * **M:** Constante – Identifica tratar-se do arquivo de andamento.&#x20;
  * **CCC:** Código do Apresentante/Portador ou **constante 000**
  * **DD:** Dia do envio do arquivo de andamento
  * **MM:** Mês do envio do arquivo de andamento
  * **AA:** Ano do envio do arquivo de andamento&#x20;
  * **S:** Número Sequencial do arquivo de andamento (mínimo 1, máximo 9)
{% endtab %}

{% tab title="Estrutura do Arquivo" %}
* **DADOS DO TÍTULO:**

{% code fullWidth="true" %}
```
     ATRIBUTO     |         DESCRIÇÃO                | OBRIGATÓRIO | TAMANHO  |    TIPO      
 CODIGO           | CÓDIGO DO APRESENTANTE           |    SIM      | Variável | ALFANUMÉRICO
 PROTOCOLO        | PROTOCOLO  DO CARTÓRIO           |    SIM      | Variável | ALFANUMÉRICO
 DOCUMENTO_DEVEDOR| DOCUMENTO DO DEVEDOR             |    SIM      | Variável |   NUMÉRICO
 DATA_PROTOCOLO   | DATA DO PROTOCOLO                |    SIM      |   010    |    DATA
 NUMERO_TITULO    | NÚMERO DO TÍTULO                 |    SIM      | Variável |   NUMÉRICO
 NOSSO_NUMERO     | NOSSO NÚMERO INFORMADO NO TITULO |    SIM      | Variável |   NUMÉRICO
 VALOR            | VALOR DO TÍTULO                  |    SIM      | Variável |   DECIMAL
 SALDO            | SALDO DO TÍTULO                  |    SIM      | Variável |   DECIMAL
```
{% endcode %}

* **EMOLUMENTOS:**

```
     ATRIBUTO    |            DESCRIÇÃO             | OBRIGATÓRIO | TAMANHO  |   TIPO      
TIPO             | TIPO DAS CUSTAS                  |     SIM     |   001    |  INTEIRO
                 |   1 - RETIRADA                   |             |          |                   
                 |   2 - CANCELAMENTO               |             |          |           
TOTAL            | TOTAL DAS CUSTAS PRÉ-CALCULADAS  |     SIM     | Variável |  DECIMAL
VIGENCIA         | VIGÊNCIA DAS CUSTAS              |     SIM     |   010    |   DATA

```



* **ANDAMENTO:**

{% code fullWidth="false" %}
```
    ATRIBUTO     |        DESCRIÇÃO                  | OBRIGATÓRIO | TAMANHO  |    TIPO       
  CODIGO         | Ocorrência                        |    SIM      |   002    | ALFABÉTICO      
                 | AA Apontado                       |             |          |                                  
                 | AB Em intimação - Pessoal         |             |          |         
                 | AC Em intimação - Eletrônica      |             |          |       
                 | AD Em intimação – AR / Correios   |             |          | 
                 | AE Publicacao por Edital          |             |          |                       
                 | AF Em intimação – Aguardando AR   |             |          |                   
                 | AG Intimado – Aguardando tríduo   |             |          |                 
                 | AI Pedido de Retirada - Aguardando|             |          |                     
                 | tríduo                            |             |          |                   
                 | AJ Protesto do banco cancelado    |             |          |                 
                 | (Exclusivamente para título de    |             |          |                         
                 |  apresentante Banco)              |             |          | 
                 | AK Pagamento por Boleto -         |             |          |            
                 | Aguardando compensação            |             |          |                
                 |                                   |             |          |                
  DATA           | DATA DO ANDAMENTO                 |    SIM      | Variável | ALFANUMÉRICO  
                 | (FORMATO d/m/Y H:I:S)             |             |          |                        
```
{% endcode %}

* **ARQUIVO EXEMPLO:**&#x20;

```xml
<complementos>
    <apresentantes>
        <apresentante>
            <codigo>111</codigo>
            <titulos>
                <titulo>
                    <protocolo>0000000000</protocolo>
                    <documento_devedor>99999999999</documento_devedor>
                    <data_protocolo>09/12/2016</data_protocolo>
                    <numero_titulo>987987</numero_titulo>
                    <nosso_numero>987987987987987</nosso_numero>
                    <valor>166.31</valor>
                    <emolumentos>
                        <emolumento>
                            <tipo>1</tipo>
                            <vigencia>11/04/2022</vigencia>
                            <total>30.4</total>
                        </emolumento>
                    </emolumentos>
                    <andamentos>
                        <andamento>
                            <codigo>AA</codigo>
                            <data>01/01/2023 20:10:10</data>
                        </andamento>
                        <andamento>
                            <codigo>AB</codigo>
                            <data>01/01/2023 20:10:10</data>
                        </andamento>
                    </andamentos>
                </titulo>
            </titulos>
        </apresentante>
        <apresentante>
            <codigo>222</codigo>
            <titulos>
                <titulo>
                    <protocolo>0000000001</protocolo>
                    <documento_devedor>99999999991</documento_devedor>
                    <data_protocolo>09/12/2016</data_protocolo>
                    <numero_titulo>1239875</numero_titulo>
                    <nosso_numero>987987987847987</nosso_numero>
                    <valor>166.31</valor>
                    <emolumentos>
                        <emolumento>
                            <tipo>1</tipo>
                            <vigencia>11/04/2022</vigencia>
                            <total>12.4</total>
                        </emolumento>
                    </emolumentos>
                    <andamentos>
                        <andamento>
                            <codigo>AI</codigo>
                            <data>01/01/2023 20:10:10</data>
                        </andamento>
                    </andamentos>
                </titulo>
            </titulos>
        </apresentante>
    </apresentantes>
</complementos>
```
{% endtab %}

{% tab title="Mensagens " %}
**Mensagens:**

**Exemplo de mensagem com recusa completa:**&#x20;

```xml
<relatorio>
  <nome_arquivo>M0002507.231</nome_arquivo>
  <codigo>2292</codigo>
  <ocorrencia>CAMPOS INVÁLIDOS OU NÃO INFORMADOS (APRESENTANTES).</ocorrencia>
</relatorio>

```

**Exemplo de mensagem de sucesso:**

Enviando somente andamento

```xml
<complementos>
    <apresentantes>
        <apresentante>
            <codigo>111</codigo>
            <titulos>
                <titulo>
                    <protocolo>0000000000</protocolo>
                    <documento_devedor>99999999999</documento_devedor>
                    <mensagens>
                        <andamento>
                            <codigo>2322</codigo>
                            <descricao>Andamento inserido.</descricao>
                        </andamento>
                    </mensagens>
                </titulo>
            </titulos>
        </apresentante>
    </apresentantes>
</complementos>
```

&#x20;Enviando somente emolumentos

```xml
<complementos>
    <apresentantes>
        <apresentante>
            <codigo>111</codigo>
            <titulos>
                <titulo>
                    <protocolo>0000000000</protocolo>
                    <documento_devedor>99999999999</documento_devedor>
                    <mensagens>
                        <emolumento>
                            <codigo>2318</codigo>
                            <descricao>Custas atualizadas.</descricao>
                        </emolumento>
                    </mensagens>
                </titulo>
            </titulos>
        </apresentante>
    </apresentantes>
</complementos>

```

Enviando andamento e emolumento

```xml
<complementos>
    <apresentantes>
        <apresentante>
            <codigo>111</codigo>
            <titulos>
                <titulo>
                    <protocolo>0000000000</protocolo>
                    <documento_devedor>99999999999</documento_devedor>
                    <mensagens>
                        <emolumento>
                            <codigo>2318</codigo>
                            <descricao>Custas atualizadas.</descricao>
                        </emolumento>
                        <andamento>
                            <codigo>2322</codigo>
                            <descricao>Andamento inserido.</descricao>
                        </andamento>
                    </mensagens>
                </titulo>
            </titulos>
        </apresentante>
    </apresentantes>
</complementos>
```

<table data-header-hidden><thead><tr><th width="200"></th><th></th></tr></thead><tbody><tr><td><strong>CÓDIGO</strong></td><td><strong>DESCRIÇÃO</strong></td></tr><tr><td>2292</td><td>CAMPOS INVÁLIDOS OU NÃO INFORMADOS (ATRIBUTO)</td></tr><tr><td>2304</td><td>FOI ENCONTRADO MAIS DE UM TÍTULO COM OS DADOS INFORMADOS</td></tr><tr><td>2137</td><td>CAMPO (ATRIBUTO) INVÁLIDO.</td></tr><tr><td>2318</td><td>CUSTAS ATUALIZADAS</td></tr><tr><td>2196</td><td>TÍTULO NÃO ENCONTRADO</td></tr><tr><td>2322</td><td>ANDAMENTO INSERIDO </td></tr><tr><td>2334</td><td>O ARQUIVO POSSUI REGISTROS EM DUPLICIDADE. CONSULTE O LOG NO SISTEMA PARA MAIS INFORMAÇÕES. </td></tr><tr><td>2335</td><td>REGISTRO EM DUPLICIDADE</td></tr></tbody></table>
{% endtab %}

{% tab title="Diferença dos serviços" %}
Caso o seu sistema já esteja integrado e enviando os emolumentos, as mudanças para o novo layout são:

<mark style="color:green;">**CustasTitulo ⇒ TituloComplemento**</mark>

Para quem já usa o serviço de envio de custas, aqui estão algumas mudanças que precisam ser realizadas para reaproveitar o mesmo serviço já existente:

O Endpoint do serviço deverá ser alterado de CustasTitulo para TituloComplemento

A TAG raiz do XML foi alterado

De Titulos:

```html
<custas_titulo>
  <apresentantes>
    <apresentante>
      <codigo>...</codigo>
      ...
    
</custas_titulo>
```

Para Complementos:&#x20;

```markup
  <complementos>
    <apresentantes>
      <apresentante>
        <codigo>111</codigo>
        ...
  </complementos>
```

Agora é possível inserir informações adicionais no XML, além da tag de Emolumentos. É viável incluir ao conteúdo do título os dados referentes aos andamentos. Assim como para os emolumentos, também é permitido informar múltiplos andamentos de uma só vez, utilizando a seguinte estrutura:

```markup
...
<andamentos> 
    <andamento>
      <codigo>AA</codigo>
      <data>13/07/2023 13:50:25</data>
    </andamento>
    <andamento>
      <codigo>AA</codigo>
      <data>13/07/2023 13:50:25</data>
    </andamento>
</andamentos>
...
```

A resposta do webservice passou por alterações. No serviço de custas, era previsto o retorno de apenas um tipo de mensagem. No serviço de complementos, que possibilita informar outros dados do título, está habilitado para receber mais de um tipo de mensagem. A estrutura de resposta foi adaptada da seguinte maneira:

```markup
<mensagens>
    <emolumento>
        <codigo>2318</codigo>
        <descricao>Custas atualizadas.</descricao>
    </emolumento>
    <andamento>
        <codigo>2322</codigo>
        <descricao>Andamento inserido.</descricao>
    </andamento>
</mensagens>

OU 

<mensagens>
    <andamento>
        <codigo>2322</codigo>
        <descricao>Andamento inserido.</descricao>
    </andamento>
</mensagens>

OU

<mensagens>
    <emolumento>
        <codigo>2318</codigo>
        <descricao>Custas atualizadas.</descricao>
    </emolumento>
</mensagens>
```

É fundamental lembrar que se trata de um serviço capaz de receber ou enviar mais de uma informação, é importante prever, no momento da captura da resposta, a possibilidade da existência ou ausência de algum grupo de mensagens.

Com essa precaução, o sistema poderá lidar de forma adequada com diferentes cenários, garantindo que não ocorram erros inesperados durante o processamento das informações recebidas do serviço.

As mensagens de resposta são organizadas por título, não por informações enviadas. Portanto, caso haja alguma informação incorreta, o sistema irá gravar todas as demais informações corretas e, em seguida, notificar sobre a existência de algum erro específico.

Essa abordagem de gravação seletiva permite que as informações corretas sejam armazenadas adequadamente, mesmo em situações em que alguma parte dos dados não esteja correta. Ao mesmo tempo, a identificação dos erros possibilita que sejam tratados e corrigidos posteriormente.
{% endtab %}
{% endtabs %}



{% hint style="success" %}
O sistema agrupará todos os andamentos informados pelo cartório até o horário limite e disponibilizará para o apresentante no arquivo com formato alinhado nacionalmente.
{% endhint %}
