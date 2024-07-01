# Retorno único

A CRA disponibiliza aos cartórios dois tipos de arquivo de retorno: um arquivo individual para cada apresentante ou um único arquivo contendo todos os apresentantes, podendo ser enviado em TXT, ou XML.

Se o cartório optar pelo arquivo único, ele deve organizar os dados separando cada apresentante conforme os exemplos abaixo:

{% tabs %}
{% tab title="TXT" %}
Para o envio em TXT, o cartorio deve organizar os dados separando cada apresentante conforme o exemplo abaixo e obedecendo o [<mark style="color:green;">**`Layout FEBRABAN`**</mark>](../../../../apresentante/layout-febraban/):

{% code fullWidth="true" %}
```markup
0001APRESENTANTE 1 [Preencher os dados do header conforme o layout FEBRABAN prevê] 0001
1001   [Preencher os dados do retorno conforme o layout FEBRABAN prevê]            0002
9001APRESENTANTE 1 [Preencher os dados do trailer conforme o layout FEBRABAN prevê]0003

0002APRESENTANTE 2 [Preencher os dados do header conforme o layout FEBRABAN prevê] 0001
1002   [Preencher os dados do retorno conforme o layout FEBRABAN prevê]            0002
9002APRESENTANTE 2 [Preencher os dados do trailer conforme o layout FEBRABAN prevê]0003

0003APRESENTANTE 3[Preencher os dados do header conforme o layout FEBRABAN prevê]  0001
10030    [Preencher os dados do retorno conforme o layout FEBRABAN prevê]          0002
9003APRESENTANTE 3 [Preencher os dados do trailer conforme o layout FEBRABAN prevê]0003

0004APRESENTANTE 4 [Preencher os dados do header conforme o layout FEBRABAN prevê] 0001
1004   [Preencher os dados do retorno conforme o layout FEBRABAN prevê]            0002
1004   [Preencher os dados do retorno conforme o layout FEBRABAN prevê]            0003
9004APRESENTANTE 4 [Preencher os dados do trailer conforme o layout FEBRABAN prevê]0004
```
{% endcode %}
{% endtab %}

{% tab title="XML" %}
No envio XML o cartorio deve organizar os dados separando cada apresentante conforme o exemplo abaixo:

```markup
<retorno>
  <hd h01="0" h02="001" h03="APRESENTANTE 1" h04=[...] h17="0001" />
  <tr t01="1" t02="001" t03="..."  t04="" t05="" t06= [...] t52="0002" />
  <tl t01="9" t02="001" t03="APRESENTANTE 1" t04=[...] t08="0003" />

  <hd h01="0" h02="002" h03="APRESENTANTE 2" h04=[...] h17="0001" />
  <tr t01="1" t02="002" t03="..." t04="" t05="" t06= [...] t52="0002" />
  <tl t01="9" t02="002" t03="APRESENTANTE 2" t04=[...] t08="0003" />

  <hd h01="0" h02="003" h03="APRESENTANTE 3" h04=[...] h17="0001" />
  <tr t01="1" t02="003" t03="..."  t04="" t05="" t06= [...] t52="0002" />
  <tl t01="9" t02="003" t03="APRESENTANTE 3" t04=[...] t08="0003" />

  <hd h01="0" h02="004" h03="APRESENTANTE 4" h04=[...] h17="0001" />
  <tr t01="1" t02="004" t03="..." t04="" t05="" t06= [...] t52="0002" />
  <tl t01="9" t02="004" t03="APRESENTANTE 4" t04=[...] t08="0003" />
</retorno>
```
{% endtab %}
{% endtabs %}

**Nomenclatura do arquivo:** O arquivo de retorno único deve seguir a seguinte nomenclatura: **R000DDMM.AAS**

**Exemplo:** R0002512.241

**Descrição:**

* **R**: constante
* **000**: constante para identificar o envio de vários apresentantes no mesmo arquivo
* **DD**: dia do retorno
* **MM**: mês do retorno
* **.** : ponto
* **AA**: ano do retorno
* **S**: sequencial do arquivo

#### &#x20;

