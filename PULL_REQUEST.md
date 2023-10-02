# Corelab Notes - Back-end

Projeto realizado de acordo com as regras do desafio. Para fins de teste prático de diferentes conceitos do dia-dia, foi proposto a criação de uma aplicação web, tanto da API como do front-end. A seleção em questão faz parte do processo seletivo para vaga de <b>Desenvolvedor Full-stack Junior</b>, na empresa <b>Corelab</b>.

## O projeto

Consiste em um aplicativo de notas. O usuário é capaz de criar e gerenciar suas notas. 
Esse repositório é apenas referente ao <b>Back-end</b> da aplicação. O código responsável O código que irá consumir a API e renderizar a interface, estará contido em outro repositório.

### Requisitos Funcionais

- Os usuários devem ser capazes de criar, ler, atualizar e excluir tarefas usando a API.
- Os usuários devem ser capazes de marcar um item como favorito.
- Os usuários devem ser capazes de definir uma cor para cada item de tarefa.
- O frontend React deve exibir a lista de tarefas do usuário de maneira responsiva e visualmente atrativa, com a capacidade de filtrar por itens favoritos, título e texto do corpo.
- Os itens favoritos devem ser exibidos no topo da lista.

### Requisitos Não Funcionais

- A API deve ser construída no framework Adonis.js e usar um banco de dados de sua escolha (por exemplo, MongoDB, PostgreSQL, etc.).
- O frontend deve ser construído em React e utilizar ferramentas modernas de desenvolvimento web e as melhores práticas.
- A aplicação deve ser responsiva e visualmente atraente.

### Ferramentas utilizadas

- <b>Adonis.js ^5.9</b> 

- <b>NPM ^8.5.5</b>: como gerenciador de pacotes.

- <b>ESLint</b>: apenas para desenvolvimento, auxilia na padronização do código, a partir de regras pré-configuradas.

- Database:
    - <b>MySQL</b>: para desenvolvimento, banco de dados relacional, de simples implementação.
    - <b>Lucid ORM</b>: query builder, para auxiliar na criação de queries SQL e abstração do código.

- <b>Typescript ^~4.6</b> 

## Database

### Schema

O banco de dados possui o seguinte schema:
- Tabela "Note"
    - id: number
    - title: string
    - content: string
    - favorite: boolean
    - color: string

## Rotas 

- <b>/notes</b>
    - POST: inserir no banco de dados nova note com um title, e content 
    - GET: retorna todas as notes do banco de dados
    
- <b>/notes/:id</b>
    - GET: retorna uma note caso o id esteja presente no banco de dados
    - DELETE: deleta uma note a partir de um id
    - PUT: atualiza uma note, a partir de um id e um JSON

----
