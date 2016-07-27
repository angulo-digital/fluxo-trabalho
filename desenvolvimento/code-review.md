# Code Review - Manual

Checklist para realização do code review manual no momento de análise dos [PRs](/desenvolvimento/git-flow.md#pull-request).

## Geral

- O código funciona? Ele desempenha o papel esperado? A lógica está correta?
- O código é facilmente entendido?
- O código respeita as convenções de boas práticas?
- Existe algum código redundante ou duplicado?
- O código é o mais modular possível?
- Algum código de log ou debug pode ser removido?
- Código comentado foi removido?

## Segurança

- Todos os inputs foram validados (tipo correto, tamanho, formato, valores válidos)?
- Os parâmetros inválidos foram tratados?

## Documentação

- Deve ser avisado na descrição do PR se for necessário executar algum comando para rodar as dependências para que o código funcione
- O código possui documentação? Nos principais métodos e lógicas complexas?
- Todas as variáveis foram definidas com nomes significativos, consistentes e claros?

## Performance

- Informações que podem ser armazenadas em cache estão sendo cacheadas?
- Processamentos redundantes ou lentos foram otimizados?
- Foi evitado o uso de construções IF-ELSE para diminuir a complexidade da execução?

## Testes

- Se a tarefa envolver apenas um módulo, executar os testes daquele módulo. Se envolver mais de um, rodar todos os testes do sistema.
- Os testes unitários devem ser rodados com todos os erros do PHP habilitados de modo à garantir que nenhum notice,warning,deprecated entre na base.
- Se for uma tarefa que crie ou altere uma API devem ser criados/alterados os testes de Api referentes a tarefa
- Os testes unitários devem cobrir tanto dos casos de sucesso quanto dos casos de erro
- Testar a interface cross browser:

    - Microsoft Internet Explorer
    - Chrome
    - Safari
    - Firefox version

- Testar a interface em multiplataformas
- Caso não consiga testar em todos os navegadores deve descrever na descrição do PR em quais navegadores realizou os testes




## Referências

[https://github.com/Coderockr/Standards/blob/master/Checklist.md](https://github.com/Coderockr/Standards/blob/master/Checklist.md)
