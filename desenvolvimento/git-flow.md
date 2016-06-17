# Git Flow

> Fluxo do versionamento dos projetos.

### Repositório principal

**Importante:** Os repositórios relacionados à clientes internos, devem ser **privados**, assim como os seus respectivos forks.

Todos os projetos devem ser atualizados via pull request. Assim, podemos fazer o Code Review de forma mais eficiente e de acordo com a especificação do mesmo.

O usuário que fizer o fork de um repositório, deve dar acesso de leitura do mesmo aos outros integrantes da equipe.

---

No repositório principal devemos ter o branch `master` e um ou mais [branches órfãos](https://git-scm.com/docs/git-checkout/1.7.3.1).

Um bom exemplo de um branch órfão, seria o branch `template`, onde o mesmo deve conter todo o front-end da aplicação.

**Branch master** - É o branch que contém código em nível de produção.

**Branch template** - É o branch órfão que contém todo o front-end da aplicação em nível de produção.

### Nomenclatura de branches para os forks.

Basicamente, em cada pull request, cada branch deve ser uma entrega. Por exemplo, uma pequena lista do que utilizar e do que não utilizar:

#### O que utilizar:

`fix-issue-6789`, `add-modulo-usuarios`, `add-feature-example`, `fix-login-stuff`, `fix4123`, `addSomeFeature` etc.

#### O que não utilizar:

`developer`, `template`, `master`, etc. Estes branches podem ser utilizados como base para o desenvolvedor, mas não para envio de pull requests.


### Padrão de commits

Este padrão foi baseado no padrão de commits do [repositório do angular.js](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md#commit).

---

A mensagem deve seguir o seguinte formato:

```
<tipo>(<escopo/modulo>): <assunto>

<corpo da mensagem>

<rodape>
```

Caso seja possível explicar o commit apenas com a primeira linha, pode-se desconsiderar o `corpo da mensagem`.

#### Tipo

Deve ser um destes:

- **feat**: Uma nova feature
- **fix**: Um bug fix
- **docs**: Alterações na documentação
- **style**: Alterações que não afetarão o signifcado/lógica do código (white-space, formatação, falta de ponto e vírgula - em algumas linguagens, etc)
- **refactor**: Refatoração do código, mas que não é um bug fix e nem adiciona uma nova feature
- **perf**: Mudança de código que traz uma melhoria de performance
- **test**: Adicionando/melhorando os testes

#### Escopo ou Módulo

Pode ser definido como qualquer área do site, módulo do sistema, sub-site, área de um aplicativo, etc.

#### Assunto

O assunto deve conter uma descrição sucinta sobre a alteração.

- Não começar com letra maiúscula
- Não utilizar ponto final (.) ao final.

#### Corpo

O corpo deve incluir a motiviação para aquela alteração ter ocorrido e a difereciação em relação ao comportamento anterior.

#### Rodape

O rodapé pode ser utilizado para fechar issues. Ex.:

- `Fix #10`
- `Fixed #130`
- `Closes #13, #2, #43`
