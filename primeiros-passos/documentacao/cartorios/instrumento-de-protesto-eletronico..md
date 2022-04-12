# Instrumento de Protesto eletrônico.

{% tabs %}
{% tab title="Envio" %}


**NOMENCLATURA**

Protocolo, data do protocolo (sem pontuação) e sequencial (dois dígitos), separados por underline (\_). Como um título tem apenas um instrumento, o sequencial será sempre 01.

Exemplo:

**00256\_12032018\_01.pdf.p7s**

Arquivo pdf assinado em p7s referente ao título de protocolo 00256 de 12/03/2018.

**FORMAS DE ENVIO**

**Upload no sistema (Menu retorno/Upload instrumento)**

* Envio de arquivos em formato .p7s ou pdf assinado;
* Os arquivos .p7s podem ser enviados individualmente ou compactados em formato .zip, quando houver mais de um;
* Caso o arquivo não esteja assinado, é possível assiná-lo no momento do upload;
* Arquivos em PDF assinado devem ser enviados zipados

![](<../../../.gitbook/assets/image (31).png>)

**Envio no retorno por web service (XML)**

* Utilizado por cartórios com sistema integrado ao da CRA e que enviam o retorno diretamente para a CRA;
* O instrumento eletrônico deve ser compactado, e gerado o base64 do arquivo zip. A string gerada é adicionada no atributo t51 da tag de transação (tr);
* Para mais informações sobre integração, acesse a [ documentação de web service para cartórios .](../../integracao-via-webservice-xml/)

**Envio de imagem por web service (XML)**

* Utilizado por cartórios com sistema integrado ao da CRA e que o distribuidor envia o retorno para a CRA.  O instrumento deve ser enviado após recepção do retorno pela CRA;
* O instrumento eletrônico deve ser compactado, e gerado o base64 do arquivo zip. A string gerada é adicionada na tag < base64 >.
* Para mais informações sobre integração, acesse a [ documentação de web service para cartórios .](../../integracao-via-webservice-xml/cartorios-distribuidores/envio-de-imagens.md)
{% endtab %}

{% tab title="Recepção / Consulta" %}
Para apresentantes, CRA e cartórios, é possível verificar o instrumento na tela de cadastro de imagem em “**Consulta título**" ou “**Consulta retorno**“.

Além dessas opções, existem outras específicas para CRA e Apresentante.

#### Apresentante

Download das imagens com ou sem assinatura na tela Retorno/Download retorno.

![](<../../../.gitbook/assets/image (36).png>)

#### CRA

A CRA pode fazer a impressão dos instrumentos através do menu Impressão/Impressão instrumento. É possível baixar as imagens separadamente ou todas em um arquivo .ZIP. Como essa tela é voltada para impressão, os instrumentos são baixados sem assinatura.

![](<../../../.gitbook/assets/image (17).png>)
{% endtab %}

{% tab title="Validação / Autenticidade" %}
A validação do instrumento eletrônico pode ser feita de dois modos:

* Selo eletrônico do tribunal;
* Código de autenticação do CRA 21.

{% hint style="info" %}
O código de autenticação é ativado sob demanda, basta abrir um chamado em nosso [portal de atendimento](http://atendimento.p21sistemas.com.br).
{% endhint %}

É inserido na lateral do PDF no momento do upload e pode ser verificado através da API disponibilizada aos institutos de protesto.

Cada instituto pode colocar um módulo de verificação de instrumentos em seu site e **consumir a API** para as verificações.
{% endtab %}
{% endtabs %}
