## Iteração 4 de Mutação

### Comando
`npx stryker run`

### Resultado
- Projetos mutáveis encontrados: 1 de 9 arquivo(s)
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
- A alteração de `fatorial` já melhorou a detecção de mutantes, mas ainda há cobertura faltante em casos específicos de base.
- Os dois mutantes de `clamp` refletem mudança de igualdade de limite e podem exigir testes de `valor === min` e `valor === max` mais explícitos ou uma revisão de especificação.
- Existem 3 mutantes em timeout, indicando que alguns casos podem precisar de ajustes na execução do teste ou em configuração do Stryker para evitar hangs.

### Próximo passo sugerido
- Adicionar testes exclusivos para `fatorial(0)` e `fatorial(1)` com assertivas específicas.
- Garantir testes limites exatos para `clamp(min, min, max)` e `clamp(max, min, max)`.
- Revisar a causa dos 3 timeouts no relatório HTML de Stryker para identificar se são mutantes lentos ou problemas de ambiente.
