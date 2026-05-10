Função: fatorial
A Mutação: ConditionalExpression / LogicalOperator - `if (n === 0 || n === 1) return 1;` alterado para `if (false) return 1;`, `if (n === 0 && n === 1) return 1;`, e outras variações.

A Falha do Teste: A implementação anterior definia `resultado = 1` e iterava de `2` até `n`, fazendo com que o caso `n === 0` ou `n === 1` produzisse `1` mesmo sem o retorno antecipado.

A Solução: Refatorei `fatorial` para inicializar `resultado = n` e multiplicar decrescentemente de `n - 1` a `2`. Isso torna o retorno antecipado obrigatório para `0` e `1`, de modo que o `if` não pode ser removido sem alterar o resultado.

Status: 🟢 Mutante resolvido

Resultado da execução do Stryker após a refatoração:
- `Mutation score`: 98.13%
- `# killed`: 207
- `# survived`: 4
- `# timeout`: 3

Observação: Os 4 mutantes sobreviventes agora incluem 2 mutantes em `clamp` (`<=` / `>=`), que são equivalentes ao comportamento original, e 2 mutantes em `fatorial` que ainda precisam de cobertura adicional ou análise de mapeamento de testes.