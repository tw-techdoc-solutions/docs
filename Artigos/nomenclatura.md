# Nomenclatura

A nomenclatura de endpoints é muito importante para que o cliente tenha uma visão refinada do que se trata cada ponto da jornada do produto, para isso vamos mostrar nesse artigo uma padronização na construção inicial da documentação de um endpoint.

#### URI
É o caminho (endereço) de acesso de um endpoint. por exemplo produto/v1/transação

## Boas práticas

- Endpoints devem ser compostos unicamente por nomes;
- Utilize kebab-case para palavras compostas;
- Utilize letras minúsculas;
- Não termine seus endpoints com “/”;
- Use diferentes verbos HTTP para suas operações.
- O URI de um endpoint deve utilizar o nome no plural, sendo assim apesar da sua classe chamar-se Transação, a URI será:`produto/v1/transacoes`
- Caso seja um produto com palavras compostas como Produto Transação ficaria no formato kebab-case dessa forma: produto/v1/produtos-transacoes
> Observação: Note que dessa forma, não possui uma barra final e está tudo em letras minúsculas.

## Métodos
Sobre os diferentes tipos de verbo, para uma jornada completa para o cliente é necessário utilizar diferentes tipos como **GET**, **POST**, **PATCH**, **PUT** e **DELETE**.

#### GET
É utilizado quando o cliente deseja obter recursos do servidor.
Realizar uma requisição de um formulário.

#### POST
É utilizado quando o cliente deseja enviar dados para processamento ao servidor.
Quando o cliente cria um cadastro.

#### PATCH
É bastante utilizado para atualizar de forma parcial
Quando o cliente deseja atualizar um campo ou outro de um formulário ou cadastro.

#### PUT
É utilizado para atualizar de forma completa
Quando o cliente deseja alterar todo um documento será uma grande atualização de todos os dados.

#### DELETE
É utilizado para deletar.
Quando o cliente deseja excluir uma conta.

## Títulos padronizados
Para obter a melhor experiência, padronizar títulos de endpoints de acordo com seu método e URI é uma boa pratica, pois oferece uma excelente experiência para o cliente, com que ele entenda a jornada do produto.

Tendo isso em mente vamos trabalhar com alguns exemplos e dicas de como documentar o título do endpoint.

#### GET
Um endpoint com método **GET** irá listar ou consultar uma requisição, dessa forma é uma boa pratica utilizar
de forma consciente como os exemplos abaixo:

- **GET** `produto/v1/transacoes` - Listar transações
- **GET** `produto/v1/transacoes{id}` - Consultar transação

Note que nos dois exemplos possui uma grande diferença do que o endpoints pode oferecer para o cliente, no  Listar transações ele irá listar todas as transações feita naquela conta, quanto no Consultar transação ele irá consultar uma transação especifica na conta. Essa diferença de títulos e preocupação em analisar a URI é essencial para uma boa documentação de APIs.

#### POST
Um endpoint com método **POST** irá realizar uma ação, pode ser ao ativar um cartão ou até como criar uma conta, dessa forma é uma boa pratica dessa forma vou listar uns exemplos:

**POST** `produto/v1/contas` - Criar conta
**POST** `produto/v1/cartoes` - Ativar cartão

#### PUT e PATCH
Um endpoint com método **PUT** irá realizar uma ação de atualizar, poderá ser atualizar uma conta por completo ou em caso de **PATCH** atualizar de forma parcial, exemplo abaixo:

**PUT** `produto/v1/contas` - Atualizar conta
**PATCH** `produto/v1/contas` - Atualizar dados específicos de uma conta

#### DELETE
Um endpoint com método DELETE irá realizar uma ação de deletar ou desativar algo, exemplos abaixo:

DELETE produto/v1/contas - Excluir conta
DELETE produto/v1/cartoes - Desativar cartão
