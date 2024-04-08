# Desafio TW - RPE

## Introdução
Esta API oferece funcionalidades para autorizar acessos e gerenciar informações de portadores. Projetada para atender às necessidades de diversas plataformas e sistemas, essa API oferece uma gama de funcionalidades essenciais para garantir a segurança e a integridade dos dados dos portadores.

### Objetivo

O principal objetivo da API é facilitar o acesso e a gestão de informações de portadores, permitindo que empresas e organizações realizem operações como consulta de detalhes, atualização de dados, bloqueio e adição de telefones de forma eficaz e segura.

### Funcionalidades Principais
**Autenticação Segura:** A API oferece um endpoint dedicado para autenticação, garantindo que apenas clientes autorizados possam acessar os recursos protegidos.

**Gestão de Portadores:** Permite consultar detalhes completos de portadores, atualizar informações pessoais ou de contato, bloquear o acesso por motivos de segurança, e adicionar ou remover números de telefone associados aos portadores.

### Benefícios
**Segurança Aprimorada:** Com autenticação robusta e recursos de bloqueio, a API oferece uma camada adicional de segurança para os dados dos portadores.

**Eficiência Operacional:** Simplifica e agiliza processos de gerenciamento de portadores, reduzindo o tempo e os recursos necessários para realizar operações relacionadas.

**Integração Flexível:** Projetada para fácil integração com uma variedade de sistemas e plataformas, a API Desafio TW se adapta às necessidades específicas de cada aplicação.

## Principais Endpoints

#### [Emitir token de acesso](https://matthewsls.stoplight.io/docs/intro-docs-reference/api/desafio-tw/operations/create-a-oauth-2-token)
Este endpoint é usado para obter um token de acesso, necessário para autenticar outras solicitações à API.

- **Método**: POST
- **URL**: [https://horizon-api-sb.app.rpe.tech/oauth2/token](https://horizon-api-sb.app.rpe.tech/oauth2/token)


#### [Consultar detalhes de uma pessoa portadora](https://matthewsls.stoplight.io/docs/intro-docs-reference/api/desafio-tw/operations/get-a-2001)
Este endpoint é usado para retornar os detalhes de uma pessoa portadora específica.

- **Método**: GET
- **URL**: `{{gateway}}portadores/{idPortador}`

#### [Atualizar dados de uma pessoa portadora](https://matthewsls.stoplight.io/docs/intro-docs-reference/api/desafio-tw/operations/modify-a-2001)
Este endpoint atualiza os dados de uma pessoa portadora específica.

- **Método**: PATCH
- **URL**: `{{gateway}}portadores/{idPortador}`

#### [Bloquear pessoa portadora](https://matthewsls.stoplight.io/docs/intro-docs-reference/api/desafio-tw/operations/create-a-bloqueio)
Este endpoint bloqueia uma pessoa portadora específica.

- **Método**: POST
- **URL**: `{{gateway}}portadores/bloqueios`


#### [Deletar telefone da pessoa portadora](https://matthewsls.stoplight.io/docs/intro-docs-reference/api/desafio-tw/operations/delete-a-2001-telefone-1)
Este endpoint remove um número de telefone associado a uma pessoa portadora.
- **Método**: DELETE
- **URL**: `{{gateway}}portadores/{idPortador}/telefones/{idTelefone}`

#### [Registrar telefone da pessoa portadora](https://matthewsls.stoplight.io/docs/intro-docs-reference/api/desafio-tw/operations/create-a-2001-telefone)
Este endpoint adiciona um novo número de telefone de uma pessoa portadora.
- **Método**: POST
- **URL**: `{{gateway}}portadores/{idPortador}/telefones`

## Jornada do produto

### 1. Autenticação e autorização:
- **Objetivo**: Obter um token de acesso para autenticar as solicitações à API.
- **Passos**:
  1. O cliente faz uma solicitação de autenticação POST para o endpoint de autorização, fornecendo as credenciais necessárias.
  2. O servidor valida as credenciais.
  3. Se as credenciais forem válidas, o servidor retorna um token de acesso.
  4. O cliente armazena o token de acesso recebido para autenticar as solicitações subsequentes à API.

### 2. Gerenciamento de portadores:
- **Objetivo**: Realizar operações relacionadas aos portadores, como consultar detalhes, atualizar informações, bloquear, remover e adicionar telefones.
#### **Passo a passo**:

**1. Consultar detalhes de uma pessoa portadora:**

  - O cliente faz uma solicitação GET para o endpoint de detalhes do portador, fornecendo o ID da pessoa portadora desejado.
  - O servidor retorna os detalhes da pessoa portadora.

**2. Atualizar dados de uma pessoa portadora:**

  - O cliente faz uma solicitação PATCH para o endpoint de atualização de dados do portador, fornecendo o ID da pessoa portadora e os dados atualizados.
  - O servidor atualiza os dados da pessoa portadora conforme especificado.

**3. Bloquear pessoa portadora:**

  - O cliente faz uma solicitação POST para o endpoint de bloqueio de portador, fornecendo o ID da pessoa portadora e informações adicionais de bloqueio.
  - O servidor registra o bloqueio da pessoa portadora.

**4. Deletar telefone da pessoa portadora:**

  - O cliente faz uma solicitação DELETE para o endpoint de remoção de telefone do portador, fornecendo o ID da pessoa portadora e o ID do telefone a ser removido.
  - O servidor remove o número de telefone especificado da pessoa portadora.

**5. Registrar telefone da pessoa portadora:**

  - O cliente faz uma solicitação POST para o endpoint de adição de telefone ao portador, fornecendo o ID da pessoa portadora e os detalhes do novo telefone.
  - O servidor adiciona o novo número de telefone à lista de telefones da pessoa portadora.

## Casos de Uso

#### [**Emitir token de acesso:**](https://matthewsls.stoplight.io/docs/intro-docs-reference/api/desafio-tw/operations/create-a-oauth-2-token)
Um sistema de gestão de portadores que utiliza o endpoint da API para autenticar usuários antes de permitir o acesso às informações dos portadores. Isso garante que apenas usuários autorizados possam realizar operações de gerenciamento de portadores, protegendo assim os dados confidenciais.e acesso para autenticar solicitações subsequentes à API.

#### [**Consultar detalhes da pessoa portadora:**](https://matthewsls.stoplight.io/docs/intro-docs-reference/api/desafio-tw/operations/get-a-2001)
Um aplicativo de cliente utiliza a API para obter informações detalhadas sobre os portadores, como informações pessoais e histórico de transações. Isso permite que o aplicativo forneça aos usuários finais uma visão abrangente de suas contas e atividades, melhorando assim a experiência do usuário.

#### [**Atualizar dados da pessoa portadora:**](https://matthewsls.stoplight.io/docs/intro-docs-reference/api/desafio-tw/operations/modify-a-2001)
Um sistema de back-office usa a API para atualizar informações de contato dos portadores, como endereços e números de telefone. Isso garante que os dados dos portadores estejam sempre atualizados e precisos, facilitando a comunicação eficaz com os clientes e melhorando a qualidade do serviço.

#### [**Bloquear pessoa portadora:**](https://matthewsls.stoplight.io/docs/intro-docs-reference/api/desafio-tw/operations/create-a-bloqueio)
Um sistema de detecção de fraude utiliza a API para bloquear temporariamente as contas de portadores suspeitos de atividades fraudulentas. Isso ajuda a proteger contra transações fraudulentas e a manter a integridade do sistema, minimizando assim as perdas financeiras e protegendo a reputação da empresa.

#### [**Deletar telefone da pessoa portadora:**](https://matthewsls.stoplight.io/docs/intro-docs-reference/api/desafio-tw/operations/delete-a-2001-telefone-1)
Os clientes finais podem usar um aplicativo móvel para remover números de telefone associados às suas contas. Isso oferece aos usuários maior controle sobre suas informações pessoais e preferências de contato, aumentando assim a satisfação do cliente e a confiança na marca.

#### [**Registrar telefone da pessoa portadora:**](https://matthewsls.stoplight.io/docs/intro-docs-reference/api/desafio-tw/operations/create-a-2001-telefone)
Os clientes podem adicionar novos números de telefone às suas contas por meio de um portal de autoatendimento online. Isso oferece conveniência aos clientes e reduz a necessidade de interações diretas com a equipe de suporte, aumentando assim a eficiência operacional e a satisfação do cliente.


> #### Nota:
>Esta jornada do cliente e os casos de uso abrangem as principais funcionalidades da API de gerenciamento de portadores e autorização de acesso.
