# Git Flow

> Fluxo do versionamento dos projetos.

### Repositório principal

**Importante:** Os repositórios relacionados à clientes internos, devem ser **privados**, assim como os seus respectivos forks.

No repositório principal devemos ter o branch `master` e um ou mais [branches órfãos](https://git-scm.com/docs/git-checkout/1.7.3.1).

Um bom exemplo de um branch órfão seria o branch `template`, onde o mesmo deve conter todo o Front end da aplicação.

**Branch master** - É o branch que contém código em nível de produção.

**Branch template** - É o branch órfão que contém todo o Front end da aplicação em nível de produção.

#### Pull Request

Todos os projetos devem ser atualizados via pull request seguindo todos os padrões descritos abaixo. Dessa forma, podemos fazer o Code Review de forma mais eficiente e de acordo com as especificações do mesmo.

Cada pull request deve ter no mínimo 2 revisadores e a opção de deletar o branch após o merge deve ser sempre marcada.

O dia de análise dos revisadores nos PRs é na terça e a aprovação dos mesmos na quinta, onde tanto a análise quanto a aprovação deve ser no horário da manhã.

**Importante:** É de extrema importância que se utilize com frequência a área de comentários dos PRs para que se gere discussão e tenhamos guardado todo o registro.

#### Projetos forkados

Caso seja necessário trabalhar em um fork de um projeto, o responsável continuará seguindo todos os padrões mencionados neste documento e deve dar acesso de leitura do mesmo aos outros integrantes do projeto.

#### Ambiente local

##### config

- `git config user.name "{nome}"`
- `git config user.email "{email}"`
- `git config core.fileMode false` (linux)

##### pull
Sempre que puxar alguma atualização do servidor remoto, deve-se puxar **sempre** do branch master e  utilizar o opção [rebase](http://www.arruda.blog.br/programacao/dicas-de-git-rebase-vs-merge/)

`git pull --rebase origin master`

### Nomenclatura de branches

Para cada pull request deve ser criado um branch, ou seja, branch para cada entrega.

#### O que utilizar:

`fix-issue-6789`, `add-modulo-usuarios`, `add-feature-example`, `fix-login-stuff`, `fix4123` etc.

#### O que não utilizar:

`developer`, `template`, `master`, `module`, `feature`, etc. Estes branches podem ser utilizados em ambiente local pelo desenvolvedor, mas não para push e criação de pull requests.

### Padrão de commits

> Este padrão foi baseado no padrão de commits do [repositório do angular.js](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md#commit).

Commits com mensagens extensas devem utilizar o comando `git commit` e seguir o formato abaixo para compor a mensagem:

```
<tipo>(<escopo/modulo>): <assunto>

<corpo da mensagem>

<rodape>
```

Caso seja possível explicar o commit apenas com a primeira linha, pode-se desconsiderar o `corpo da mensagem` e `rodape` e utilizar o comando `git commit -m "<tipo>(<escopo/modulo>): <assunto>"`.

#### \<tipo\>

- **feat**: Uma nova feature
- **fix**: Um bug fix
- **docs**: Alterações na documentação
- **syntax**: Alterações que não afetarão o signifcado/lógica do código (white-space, formatação, falta de ponto e vírgula - em algumas linguagens, etc)
- **refactor**: Refatoração do código, mas que não é um bug fix e nem adiciona uma nova feature
- **perf**: Mudança de código que traz uma melhoria de performance
- **test**: Adicionando/melhorando os testes

#### \<escopo/modulo\>

Deve indicar um escopo ou módulo do sistema, área do site, sub-site, área de um aplicativo, etc.

O escopo ou módulo deve ser escrito no **singular** e o padrão para nomenclatura de um módulo ou escopo específico deve ser **seguido por todo o projeto** para, futuramente, facilitar buscas, análises e automações.

Exemplos:
- `fix(usuario): remove incompatibilidade com IE 10` :white_check_mark:
- `feat(evento): add visualização através de lista e calendário` :white_check_mark:
- `docs(widget): segue o padrão estabelecido no primeiro commit` :white_check_mark:
- `feat(users): sai do padrão estabelecido para o módulo de usuários` :x:

#### \<assunto\>

O assunto deve conter uma descrição sucinta sobre a alteração.

- Mensagem por completa em minúsculo
- Não utilizar ponto final (.) no final da mensagem

#### \<corpo da mensagem\>

O corpo deve incluir os detalhes daquela implementação/alteração.

#### \<rodape\>

O rodapé deve ser utilizado somente fechar issues caso o corpo da mensagem seja necessário, caso contrário, o fechamento de issue deve ser realizado no assunto do commit. Ex.:

- `Fix #10`
- `Fixed #130`
- `Closes #13, #2, #43`

### Dicas

- https://www.gitignore.io/
- http://rogerdudler.github.io/git-guide/index.pt_BR.html
