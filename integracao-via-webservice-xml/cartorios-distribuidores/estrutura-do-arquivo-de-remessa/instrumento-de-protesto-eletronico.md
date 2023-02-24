# Instrumento de Protesto eletrônico

Atualmente existe duas formas de realizar o envio do instrumento de protesto eletrônico.

**Envio no retorno**\
****O instrumento eletrônico deve ser compactado, e gerado o base64 do arquivo zip. A string gerada é adicionada no atributo t51 da tag de transação (tr);

**Envio de imagem**\
****O instrumento eletrônico deve ser compactado, e gerado o base64 do arquivo zip. A string gerada é adicionada na tag < base64 >

****

**NOMENCLATURA**

Protocolo, data do protocolo (sem pontuação) e sequencial (dois dígitos), separados por underline (\_). Como um título tem apenas um instrumento, o sequencial será sempre 01.

Exemplo:

**00256\_12032018\_01.pdf.p7s**

Arquivo pdf assinado em p7s referente ao título de protocolo 00256 de 12/03/2018.
