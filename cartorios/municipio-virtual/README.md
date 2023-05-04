# Município Virtual

O apresentante Banco do Brasil, não consegue enviar títulos para municípios que não tem agência. Pensando nisso desenvolvemos a solução do município virtual.\
\
Para explicar usarei os seguintes municípios como exemplo.

Município A com agência do Banco do Brasil e Código IBGE 3311111.

Município B não tem agência do Banco do Brasil Código IBGE 3322222.

&#x20;

A CRA cria o município virtual derivado do município “A”, pois ele tem agência do Banco do Brasil.

O código IBGE do município “A” é 3311111

Então o município virtual derivado dele terá o código 3911111 e o nome do município “A II”.

Após criar o município, a CRA cria dois cartórios virtuais:

Cartório virtual A II

Cartório virtual B II.

O Banco do Brasil fornece o código desses cartórios virtuais.

Cartório virtual A II - Código 99

Cartório virtual B II - Código 11



Como é o fluxo?\
Basicamente quando o apresentante envia arquivo, remessa, desistência e cancelamento

O cartório utiliza o conversor para trocar do município virtual para o dele. E quando o cartório for enviar o retorno, trocar no conversor para os códigos do município virtual.\
&#x20;\
O apresentante Banco do Brasil envia remessa para o município virtual, o cartório normal acessa o cartório virtual utilizando o login do cartório virtual, baixa a remessa, passa essa remessa no converso para trocar o código IBGE e do cartório virtual para o dele.

Confirma no sistema dele, após confirmado o cartório normal pega a confirmação, passa no conversor para trocar o código IBGE e cartório dele para os códigos IBGE e cartório da comarca virtual, esse processo é para remessa, desistência, cancelamento e retorno.

O cartório normal gera o retorno, passa o retorno no converso para trocar os códigos IBGE e do cartório dele para os códigos IBGE e cartório da comarca virtual.
