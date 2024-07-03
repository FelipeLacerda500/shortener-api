# SHORTENER API

Shortener API é um serviço para encurtar URLs, permitindo que os usuários criem links curtos que redirecionam para URLs longas. Ele oferece funcionalidades de autenticação, monitoramento de métricas e limitações baseadas no tipo de usuário (logado ou não logado).

## Requisitos Funcionais

- [ ] Deve ser possível se cadastrar.
- [ ] Deve ser possível se autenticar.
- [ ] Deve ser possível obter o perfil de um usuário logado.
- [ ] Deve ser possível que os usuários, logados ou não, encurtem um link.
- [ ] Deve ser possível obter o número de links encurtados pelo usuário logado.
- [ ] Deve ser possível que o usuário logado obtenha a métrica de quantas vezes um link encurtado foi clicado.
- [ ] Deve ser possível que o usuário logado obtenha uma listagem de seus links encurtados.

### Requisitos Funcionais Detalhados

- Cadastro: O usuário deve fornecer um e-mail e senha para se cadastrar.
- Autenticação: O usuário deve fornecer e-mail e senha para se autenticar.
- Perfil de Usuário: O usuário logado deve poder visualizar e atualizar seu perfil.
- Encurtamento de Links: Todos os usuários devem poder encurtar URLs fornecendo uma URL longa.
- Métricas de Links: O usuário logado deve poder visualizar quantas vezes cada um de seus links foi clicado.
- Listagem de Links: O usuário logado deve poder ver uma lista de todos os links que ele encurtou.

## Regras de Negócio

- [ ] O usuário não deve poder se cadastrar com um e-mail duplicado.
- [ ] A validade dos links encurtados de um usuário logado é de 10 dias.
- [ ] A validade dos links encurtados de um usuário não logado é de 2 dias.
- [ ] O usuário logado deve poder encurtar até 15 novos links e, após tal limite ser atingido, os links mais velhos devem perder a validade e serem sobrescritos, caso novos links sejam encurtados.
- [ ] O usuário não logado deve poder encurtar até 5 novos links e, após tal limite ser atingido, os links mais velhos devem perder a validade e serem sobrescritos, caso novos links sejam encurtados.

## Requisitos Não-funcionais

- [ ] A senha do usuário logado precisa estar criptografada.
- [ ] Os dados da aplicação precisam estar persistidos em um banco PostgreSQL.
- [ ] Todas as listas de dados precisam estar paginadas com 10 itens por página.
- [ ] O usuário logado deve ser identificado por um JWT (JSON Web Token).
- [ ] O usuário não logado deve ser identificado por meio do seu endereço IP.
