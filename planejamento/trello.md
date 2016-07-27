# Trello

> Controle de atividades

Os projetos devem ser classificados em um dos seguintes tipos:

- Site (site)
- Sistema (sistema)
- App (app)
- Protótipo (prototipo)
- Manutenção (manutencao)

Para maiores detalhes da aplicação na prática do que será discutido neste documento, está disponível um [modelo](https://trello.com/b/Ngdm8HDe/0-modelo-prototipo) público de board com todas as regras deste documento.

## Boards

A nomenclatura de cada Board deverá seguir o seguinte padrão:

```
#<id> - <nome>(<tipo>)
```

- **id**: Número inteiro aleatório sequencial
- **nome**: Nome do projeto no formato
- **tipo**: Tipo do projeto no formato **slug**

## Listas

Deverá ser utilizado as seguintes Listas em todos os tipos de projetos:

- **Backlog**: Todas as atividades do projeto
- **In Progress**: Tarefas que estão sendo executadas
- **Review**: Code Review manual realizado pela equipe e automático realizado pelo Codacy
- **Test**: Testes manuais realizados pela equipe e automático realizado pelo Buildkite
- **Done**: Tarefas finalizadas e prontas para ir pra produção

## Cards

Deverá ser obrigatório na criação de um card:

- Escolha do membro responsável pela solicitação
- Seleção das devidas etiquetas
- Definição da data de entrega da tarefa
- Definição de uma descrição da solicitação

A Nomenclatura do Card deverá seguir o seguinte padrão:

```
[estimativa] - <descricao>
```

- **estimativa**: estimativa de finalização da tarefa **em horas**
- **descricao**: Descrição da tarefa

Exemplos de utilização:

- `3h - Integrar página de eventos`
- `1h - Alterar links do rodapé`

**Importante:** A discussão dentro dos cards é de total importância para o bom andamento do projeto, então, ative as notificações para ficar por dentro e responder em tempo ágil.

### Issues

Para controle das issues de um projeto será utilizado o Bitbucket, porém, para que o gerenciamento dos projetos e das atividades não sofram inconsistências, deverá ser criado cards seguindo o padrão mencionado acima com a inclusão de um checklist onde os itens serão as issues selecionadas para aquele card.

Exemplos de nomenclatura para os itens do checklist:

- `#14: Corrigir retorno do tipo de dado da paginação`
- `#22: Correção da grid do blog`


## Etiquetas

- **verde**:
- **rosa**:
- **verde(claro)**:
- **preto**: Material
- **azul**: Pendente
- **amarelo**: Lembrete
- **azul(claro)**: Bitbucket
- **laranja**: Front End
- **roxo**: Back End
- **vermelho**: Design

**Importante:** Caso o pojeto não se encaixe em nenhum tipo estabelecido, definir juntamente com a equipe do projeto e adotar um padrão para as etiquetas.

## Ferramentas Extras

Deverá ser utilizado em todos os projetos as seguintes ferramentas extras:

- Calendário
- Envelhecimento de cartões