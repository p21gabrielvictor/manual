# Retorno TXT

O cartório deverá definir qual opção irá utilizar seguindo as orientações detalhadas de cada opção.

O envio do retorno segue o seguinte fluxo.

1.  O cartório envia o arquivo de retorno contendo os títulos com suas situações no cartório para a CRA.\


    * &#x20;Municípios que tem apenas um cartório de protesto, o arquivo de retorno é enviado pelo próprio cartório.
    * &#x20;Municípios que tem mais de um cartório de protesto, o arquivo de retorno pode ser enviado pelo cartório de distribuição contendo informações de todos os cartórios.


2. A CRA disponibiliza para o apresentante o arquivo de retorno de cada município ou um arquivo único contendo todos os municípios.

**NOME: RCCCDDMM.AAS**&#x20;

**R**             Constante - Identifica tratar-se de arquivo retorno gerado pelo Cartório. \
**CCC**      Código de Compensação do Banco/Portador. \
**DD**           Dia do envio do Arquivo Retorno ao Portador. \
**MM**        Mês do envio do Arquivo Retorno ao Portador. \
**AA**         Ano do envio do Arquivo Retorno ao Portador. \
**S**            Número Sequencial da Remessa - Identifica o número da remessa que está sendo enviada.

**EXEMPLO: R2370610.231**



A montagem do arquivo deve seguir o padrão do Layout FEBRABAN.&#x20;

(Link layout) \
Exemplo de um arquivo de retorno.

```
0341Itau                                    06102023SDTBFORTP0000010003000300000003 300380434115200                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 0001
1341589516448731555Sra. Manoela Molina Sobrinho                 Lidiane Toledo                               9100098200017785244-832, R. Emanuelly, 4. Apto 984Porto Hel15922654Regiane do Leste    PI544/5852-485497RA 207-393/81622082023060920230010000000025739100000000262405Sao Raissa do Norte MA1Srta. Irene Garcia Caldeira Jr.              00200091909501190           04473-751, Avenida Sarah Fontes, 19. FPorto S75409854Thomas do Norte     RR0134110/12842061020230000000000 0610202301Av. Serrano, 7555. F0000000000P00000000000000000000000000000000000000           0000000000                   0002
1341378794300136290Jorge Ferminiano Salazar                     Amelia Dias Carrara                          9182510500013596408-112, R. Regiane, 26. Bc. 80 Ap. 66Carmo48273733Sao Robson          DF876/5336-911004CCR553-525/08322082023060920230010000000002804700000000028653Wilson do Norte     MA1Dr. Inacio Juan Medina Filho                 00200027687187342           48490-761, Rua Daiana, 838. Apto 78Porto Isaa88373036Vila Gael           AL0140566421679061020230000000000 0610202301Avenida Pamela, 19170000000000P00000000000000000000000000000000000000           0000000000                   0003
1341764019262302498Sra. Lilian Eunice Bonilha                   Sra. Manuela Molina                          9198166600012385775-199, Largo Padilha, 602Santa Lilian - A61156320Marco do Sul        SP904/3853-568700CDA469-485/66122082023060920230010000000076539900000000768934Mares do Sul        MA1Bella das Neves Neto                         00200050512395365           39281-600, Rua Ornela, 48Nelson do Norte - AC68200519Livia d'Oeste       MA0173489/7930B061020230000000000 0610202301Largo Marisa Aguiar,0000000000P00000000000000000000000000000000000000           0000000000                   0004
9341Itau                                    0610202300003000000000001059992                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         0005

```



O cartório pode enviar também um arquivo único contendo os retornos de todos os apresentantes.&#x20;



**NOME: RCCCDDMM.AAS**&#x20;

**R**             Constante - Identifica tratar-se de arquivo retorno gerado pelo Cartório. \
**CCC**      Constante - Identifica tratar-se de arquivo retorno único gerado pelo Cartório.\
**DD**           Dia do envio do Arquivo Retorno ao Portador. \
**MM**        Mês do envio do Arquivo Retorno ao Portador. \
**AA**         Ano do envio do Arquivo Retorno ao Portador. \
**S**            Número Sequencial da Remessa - Identifica o número da remessa que está sendo enviada.

**EXEMPLO: R0000610.231**

Para a montagem desse arquivo cada apresentante deve ter seus registros compostos por Header (0), Transação (1) e Trailer (9).&#x20;

Feito isso, basta juntas os retornos de todos os apresentantes em um arquivo.

```
0E61Municipio de Tres Coroas                05102023SDTBFORTP00028000010001000000018389750434313409                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 0001
1E611010           PREFEITURA MUNICIPAL DE TRES COROAS          PREFEITURA MUNICIPAL DE TRES COROAS          88199971000153AV. JOAO CORREA, 380 CENTRO                  95660000TRES COROAS         RS202365         CDA202365     24052023240520230010000000019706100000000197061NOVO HAMBURGO         1ZELADORIA ENCOSTA DA SERRA LTDA - ME         00105374272000175           RUA RIO PELOTAS, 15                          93332330NOVO HAMBURGO       RS0111357/5090B061020230000000000I0610202301LIBERDADE           0000000000P     000000000000000000000000000000000           0000000000                   0002
9E61Municipio de Tres Coroas                0510202300001000000000000197061                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         0003
0F02MUNICIPIO DE XANGRI-LA                  06102023SDTBFORTP00057600030003000000037439920434313409                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 0001
1F022266/220903-9  MUNICIPIO DE XANGRI-LA                       MUNICIPIO DE XANGRI-LA                       94436474000124AV. ELMAR RICARDO WAGNER, 854                95588000XANGRI-LA           RS320886         CDA5212/2023  06102023999999990010000000141659400000001145545NOVO HAMBURGO         1DAIANA RIGHI TEN CATEN                       00200095303324087           R. JOAQUIM PEDRO SOARES, 175 604             93510320NOVO HAMBURGO       RS013129715671F061020230000000000I0610202301CENTRO              0000000000P     0000000000000000000000000000000000          0000000000                   0002
1F022266/220903-9  MUNICIPIO DE XANGRI-LA                       MUNICIPIO DE XANGRI-LA                       94436474000124AV. ELMAR RICARDO WAGNER, 854                95588000XANGRI-LA           RS320894         CDA5219/2023  06102023999999990010000000010710900000000075845NOVO HAMBURGO         1MATEUS CAPROSKI DE LIMA                      00200000656874007           RUA JOAO PEDRO SCHMITT, 105 APTO 06          95588000NOVO HAMBURGO       RS0199272/4292D061020230000000000I0610202301MAUA                0000000000P     0000000000000000000000000000000000          0000000000                   0003
1F022266/220903-9  MUNICIPIO DE XANGRI-LA                       MUNICIPIO DE XANGRI-LA                       94436474000124AV. ELMAR RICARDO WAGNER, 854                95588000XANGRI-LA           RS320905         CDA5228/2023  06102023999999990010000000030489700000000182712NOVO HAMBURGO         1OSVALDO CORREA DE ANDRADE                    00200013535986087           R. LIBIA, 20                                 91370210NOVO HAMBURGO       RS0191360/22435061020230000000000I0610202301PETROPOLIS          0000000000P     0000000000000000000000000000000000          0000000000                   0004
9F02MUNICIPIO DE XANGRI-LA                  0610202300003000000000001404102                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         0005

```

No arquivo acima existem retornos de dois apresentantes diferentes (E61 - Município de Tres Coroas e F02 - Município de Xanfri-LA).&#x20;



