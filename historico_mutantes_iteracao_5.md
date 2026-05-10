## Iteração 5 de Mutação

### Comando
`npx stryker run`

### Resultado
- Projetos mutáveis encontrados: 1 de 10 arquivo(s)
- Mutantes instrumentados: 214
- Testes iniciais executados: 94
- Mutantes testados: 214/214
- Mutantes mortos: 207
- Mutantes sobreviventes: 4
- Mutantes em timeout: 3
- Mutation score: 98.13%

### Mutantes sobreviventes identificados
1. `src/operacoes.js:21:23`
   - Operação original: `for (let i = n - 1; i > 1; i--) { resultado *= i; }`
   - Mutante: `for (let i = n - 1; i >= 1; i--) { resultado *= i; }`
   - Contexto: sobrecarga de repetição em `fatorial`.

2. `src/operacoes.js:19:18`
   - Operação original: `if (n === 0 || n === 1) return 1;`
   - Mutante: `if (n === 0 || false) return 1;`
   - Contexto: cobertura insuficiente do caso `n === 0` isolado.

3. `src/operacoes.js:88:7`
   - Operação original: `if (valor <= min) return min;`
   - Mutante: `if (valor < min) return min;`
   - Contexto: igualdade de limite em `clamp`.

4. `src/operacoes.js:89:7`
   - Operação original: `if (valor >= max) return max;`
   - Mutante: `if (valor > max) return max;`
   - Contexto: igualdade de limite em `clamp`.

### Observações
- Resultado idêntico à iteração anterior, indicando que as mudanças não afetaram o score de mutação.
- Os mesmos 4 mutantes sobreviventes persistem, sugerindo que são equivalentes ou requerem testes mais específicos.
- Os 3 timeouts continuam, possivelmente indicando mutantes que causam loops infinitos ou execuções muito lentas.

### Próximo passo sugerido
- Investigar os mutantes sobreviventes no relatório HTML para entender melhor o contexto de execução.
- Considerar adicionar testes específicos para casos de borda que possam diferenciar os mutantes equivalentes.
- Revisar se os timeouts são evitáveis ajustando configurações de timeout no Stryker.