# Confirmação Automática

**Objetivo da solução:**

Realizar as confirmações de forma automática para os apresentantes. Dessa forma, evitando atrasos e cumprindo a SLA esperada.&#x20;

* O sistema confirma as remessas para os apresentantes;
* &#x20;O sistema disponibiliza a remessa para os cartórios com o protocolo e a data do protocolo que devem ser apropriados no sistema dos cartórios.

**Para iniciar a solução no seu estado:**

* Necessário solicitar ao suporte da P21 que habilite a solução para o seu estado;
* Preencher o parâmetro 'Cartório Original' no cadastro do cartório virtual;
* Habilitar o parâmetro no cadastro do Cartório 'Confirmação automática'.
  * <mark style="color:red;">VERIFICAR SE TODOS OS TÍTULOS DO CARTÓRIO JÁ FORAM CONFIRMADOS ANTES DE MARCAR O PARÂMETRO.</mark>



&#x20;**Regras gerais:**&#x20;

* A regra não se aplica onde a distribuição é feita por um serviço de distribuição;\
  &#x20;     Exemplo: Distribuidores das capitais
* A regra se aplica onde a distribuição é feito pelo CRA21;\
  &#x20;     Exemplo: Distribuidores utilizados para remessas no Banco do Brasil.
* É uma solução para todos os apresentantes, se for marcado no cartório, todas as remessas enviadas ao CRA21 após a marcação do parâmetro serão confirmadas automaticamente;
* Os cartórios manuais visualizarão o protocolo e data de protocolo na ficha do título /materialização no menu de confirmar remessa;
* Para os cartórios que baixam arquivo, (XML e TXT), a CRA21 entregará a remessa com o protocolo e data do protocolo gerado pela CRA;
* Se as remessas estiverem aguardando para gerar a confirmação automática ficam com o status "Em análise";
* Os protocolos serão geridos pela CRA21, com uma regra própria. Ano corrente + sequencial incremental; \
  &#x20;     Exemplo: 2200000001;
* O protocolo é incrementado por cartório;
  * &#x20;O protocolo do cartório virtual e original podem ser o mesmo desde que o parâmetro 'Cartório Original' esteja preenchido no cadastro do cartório virtual;\
    Exemplo: Cartório ABC - protocolo 2200000001, Cartório ABC II - protocolo 2200000002;
* Todos os títulos serão protocolados na confirmação. A devolução deverá ser no retorno do cartório.&#x20;
