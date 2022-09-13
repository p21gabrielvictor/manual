# Utilizando PHP

Para utilização dos serviços utilizando a linguagem PHP, você deverá utilizar a classe SoapClient.\
Caso você deseje mais detalhes sobre a classe, poderá acessar a documentação nesse link: \
[<mark style="color:green;">PHP: SoapCliente – Manual</mark>](http://php.net/manual/pt\_BR/class.soapclient.php)<mark style="color:green;"></mark>

### Exemplo de conexão

```php
<!--?php 
 
// Define o usuário e senha
$login = 'login';
$senha = 'senha';
 
// Opções de configurações do cliente WSDL
$options = array(
    'soap_version' => SOAP_1_1,
    'login'        => $login,
    'password'     => $senha
);
 
// Cria o objeto SOAP com a URL do serviço
$client = new SoapClient("http://cradf.cra21.com.br/cradf/xml/protestos.php?wsdl", $options);
```

### Executando um método

Com o serviço instanciado, podemos executar suas funções utilizando a sintaxe

`$cliente->Metodo(parametros);`

Onde Método será o nome do serviço, passando os parâmetros na função.\
Segue abaixo um exemplo de chamada para recepção de confirmação:

```php
// Exemplo de chamada do método para recepção de confirmação
$retornoXml = $client->Confirmacao('C0013110.141');
```

A variável _$retornoXml_ irá conter a resposta do serviço.

### Métodos disponíveis

```php
/**
 * Serviço de envio de remessa
 * 
 * @param string $userArq
 * @param string $userDados
 * @return Xml
 */
$client->Remessa($userArq, $userDados);
 
/**
 * Serviço de recepção de confirmação
 *
 * @param string $userArq
 * @return Xml
 */
$client->Confirmacao($userArq);
 
/**
 * Serviço de recepção de retorno
 *
 * @param string $userArq
 * @return Xml
 */
$client->Retorno($userArq);
 
/**
 * Serviço de envio de desistencia
 *
 * @param string $userArq
 * @param string $userDados
 * @return Xml
 */
$client->Desistencia($userArq, $userDados);
 
/**
 * Serviço de envio de cancelamento
 *
 * @param string $userArq
 * @param string $userDados
 * @return Xml
 */
$client->Cancelamento($userArq, $userDados);
 
/**
 * Serviço de envio de autorização de cancelamento
 *
 * @param string $userArq
 * @param string $userDados
 * @return Xml
 */
$client->Autoriza_Cancelamento($userArq, $userDados);
 
/**
 * Serviço de recepção das comarcas homologadas
 *
 * @param string $codapres
 * @return Xml
 */
$client->Homologadas($codapres);
```

Para fazer download do arquivo de exemplo, acesse o link: \
\
[<mark style="color:green;">**`DOWNLOAD DO ARQUIVO EXEMPLO`**</mark>](https://github.com/p21sistemas/manual-cra-21/blob/main/WebServiceCRA.zip?raw=true)<mark style="color:green;">**``**</mark>
