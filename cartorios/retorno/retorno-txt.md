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

[<mark style="color:green;">**`DOWNLOAD LAYOUT`**</mark>](https://drive.google.com/file/d/1-xofUSo-UFjdB72LltWqDKEuF4x0w\_nD/view?usp=sharing)

Exemplo de um arquivo de retorno.\
(Dados fictícios)

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

Feito isso, basta juntar os retornos de todos os apresentantes em um arquivo.

(Dados fictícios)

```
0237Bradesco                                06102023SDTBFORTP0000010002000200000002    280434304408                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 0001
1237455670782822938DR. ISAAC JONAS SOTO FILHO                   SRA. CYNTHIA REZENDE BURGOS                  7405049400015519301-522, AVENIDA GUILHERME, 439. FPORTO TAI86520596JENNIFER DO NORTE   RN235/6361-881478CCB695-195/06622082023060920230010000000054174100000000545446SANTA FRANCISCO     MA1SR. LUAN SALAS TAMOIO JR.                    00200043649631431           86533-121, AV. CONSTANCIA, 50822SAO NOELI    55232440TOLEDO DO NORTE     DF0121536264355061020230000000000 0610202301AV. LEO MEIRELES, 570000000000P     000000000000000000000000000000000           0000000000                   0002
1237149573180552707SR. SAULO FLORES GONCALVES JR.               DR. ALLAN VALENTIN CORREIA                   1048239000013735324-394, RUA DA CRUZ, 77027. FUNDOSPORTO NO47080508RAPHAEL DO LESTE    TO384/2695-019274CRH300-068/09222082023060920230010000000056607800000000570467VILA MAYARA         MA1DR. ALONSO REIS JR.                          00188681143000157           85462-079, AV. THEO, 8. BLOCO ALEIA DO SUL   56381361MIRELA DO LESTE     RJ0167208459172061020230000000000 0610202301AV. RENAN, 7685. APT0000000000P     000000000000000000000000000000000           0000000000                   0003
9237Bradesco                                0610202300002000000000001115913                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         0004
0341Itau                                    06102023SDTBFORTP00001300020002000000026780360434304408                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 0001
1341763479745538557SRA. THAIS DE AGUIAR FILHO                   RAPHAEL ZARAGOCA RICO FILHO                  3366239800018005160-912, AVENIDA BEZERRA, 61087. 160  ANDA 36441022GABRIELLE DO NORTE  SE239/2583-864'' DSI475-610/4''22082023060920230010000000008405100000000097923VILA IVANA D'OESTE  MA1EDUARDA CAMILA MASCARENHAS NETO              00118450315000104           92015-961, AV. APARECIDA, 36SANTA OLGA D'OEST96696386VILA HELOISE        AC0140196/77245061020230000000000 0610202301AV. AVILA, 23341. 8 0000000000P     000000000000000000000000000000000           0000000000                   0002
1341091388622516552SRA. ARIANE SEPULVEDA                        DAIANA EMANUELLY RIVERA JR.                  1461026700010535205-769, AVENIDA TELES, 82464. BLOCO CPATR 75950774SAO EMANUELLY       RR154/1250-700503NP 232-146/63722082023060920230010000000056025600000000573808ROSA DO NORTE       MA1SAULO SALAZAR SOBRINHO                       00200080745264107           45025-932, RUA JOAQUIN, 99766. BLOCO ATOLEDO 19915550DA CRUZ DO SUL      GO0134271/06789061020230000000000 0610202301LARGO AZEVEDO, 1. BC0000000000P     000000000000000000000000000000000           0000000000                   0003
9341Itau                                    0610202300002000000000000671731                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         0004
```



No arquivo acima existem retornos de dois apresentantes diferentes (237 - Bradesco e 341 - Itaú).&#x20;



