# Trello
> Controle de atividades

Os projetos devem ser classificados em um dos seguintes tipos:

- Site
- Sistema
- App
- Protótipo
- Manutenção

Para maiores detalhes da aplicação na prática do que será discutido neste documento, está disponível um [modelo](https://trello.com/b/Ngdm8HDe/0-modelo-prototipo) público de board com todas as regras deste documento.

## Boards

A nomenclatura de cada Board deverá seguir o seguinte padrão:

```
#<id> - <nome>(<tipo>)
```

- **id**: Número inteiro aleatório sequencial
- **nome**: Nome do projeto no formato **slug**
- **tipo**: Tipo do projeto no formato **slug**

## Listas

Deverá ser utilizado as seguintes Listas em todos os tipos de projetos:

- **Material**: Documentos do cliente e materiais de apoio
- **Ideas**: Possíveis novas features e discussões sobre o projeto
- **Backlog**: Todas as atividades do projeto
- **Sprint**: Tarefas selecionadas para um determinado sprint
- **In Progress**: Tarefas que estão sendo executadas
- **Review**: Code Review manual realizado pela equipe e automático realizado pelo Codacy
- **Test**: Testes manuais realizados pela equipe e automático realizado pelo Buildkite
- **Done**: Tarefas finalizadas e prontas para ir pra produção

## Cards

Na criação de um Card deverá ser obrigatório a escolha do membro responsável pela solicitação, a seleção das devidas etiquetas, definição da data de entrega da tarefa, definição de uma descrição da solicitação e a nomenclatura do Card deverá seguir o seguinte padrão:

```
#<id> [estimativa] - <descricao>
```

- **id**: Identificador do sprint
- **estimativa**: estimativa de finalização da tarefas **em horas**
- **descricao**: Descrição da tarefa

Exemplos de utilização:

- `#5 3h - Integrar página de eventos`
- `#8 1h - Alterar links do rodapé`

**Observação:** As regras acima não precisam ser seguidas em listas como *Material* e *Ideas*.

### Issues

Para controle das Issues (incidências após a conclusão do projeto) de um projeto será utilizado o Bitbucket, porém, para que o gerenciamento dos projetos e das    atividades não sofra inconsistência, deverá ser criado cards seguindo o padrão mencionado acima com a inclusão de um checklist onde os itens serão as issues selecionadas para aquele card.

Exemplos de nomenclatura para os itens do checklist:

- `#14: Corrigir retorno do tipo de dado da paginação`
- `#22: Correção da grid do blog`


## Etiquetas

Cada etiqueta deverá ter um significado, e caso o pojeto não se encaixe em nenhum tipo estabelecido, definir juntamente com a equipe do projeto e adotar um padrão para as etiquetas.

- **verde**: Aprovado
- **rosa**: Design
- **verde(claro)**:
- **preto**: Revisão
- **azul**: Pendente
- **amarelo**: Bloqueado
- **azul(claro)**: Bitbucket
- **laranja**: Front End
- **roxo**: Back End
- **vermelho**: Bug

## Extra

Deverá ser utilizado em todos os projetos as seguintes ferramentas extras:

- Calendário
- Envelhecimento de cartões