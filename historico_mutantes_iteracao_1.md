**Função:** divisao  
**A Mutação:** StringLiteral - mensagem de erro alterada para string vazia  
**A Falha do Teste:** Teste original verifica apenas se erro é lançado, não a mensagem exata  
**A Solução:** Novo teste verifica mensagem específica do erro  
**Status:** 🟢 Teste Implementado  

**Função:** raizQuadrada  
**A Mutação:** ConditionalExpression - condição if (n < 0) alterada para if (false)  
**A Falha do Teste:** Teste original só testa valores positivos  
**A Solução:** Novo teste cobre entrada negativa, forçando execução da condição  
**Status:** 🟢 Teste Implementado  

**Função:** raizQuadrada  
**A Mutação:** EqualityOperator - n < 0 alterado para n <= 0  
**A Falha do Teste:** Teste original não cobre limite zero  
**A Solução:** Novo teste verifica raiz quadrada de zero  
**Status:** 🟢 Teste Implementado  

**Função:** fatorial  
**A Mutação:** ConditionalExpression - condição if (n < 0) alterada para if (false)  
**A Falha do Teste:** Teste original só testa valores positivos  
**A Solução:** Novo teste cobre entrada negativa  
**Status:** 🟢 Teste Implementado  

**Função:** fatorial  
**A Mutação:** EqualityOperator - n < 0 alterado para n <= 0  
**A Falha do Teste:** Teste original não cobre limite zero explicitamente  
**A Solução:** Novo teste verifica fatorial de zero  
**Status:** 🟢 Teste Implementado  

**Função:** fatorial  
**A Mutação:** ConditionalExpression - condição if (n === 0 || n === 1) alterada para if (false)  
**A Falha do Teste:** Teste original testa fatorial(4), mas não isola casos base  
**A Solução:** Novo teste cobre fatorial de 1  
**Status:** 🟢 Teste Implementado  

**Função:** fatorial  
**A Mutação:** LogicalOperator - || alterado para &&  
**A Falha do Teste:** Teste original não cobre cenários onde && falharia  
**A Solução:** Novo teste verifica cálculo para n=3  
**Status:** 🟢 Teste Implementado  

**Função:** fatorial  
**A Mutação:** ConditionalExpression - condição if (n === 0 || n === 1) alterada para if (false || n === 1)  
**A Falha do Teste:** Teste original não isola caso n===1  
**A Solução:** Novo teste cobre fatorial de 1 isoladamente  
**Status:** 🟢 Teste Implementado  

**Função:** fatorial  
**A Mutação:** ConditionalExpression - condição if (n === 0 || n === 1) alterada para if (n === 0 || false)  
**A Falha do Teste:** Teste original não isola caso n===0  
**A Solução:** Novo teste cobre fatorial de 0 isoladamente  
**Status:** 🟢 Teste Implementado  

**Função:** mediaArray  
**A Mutação:** ConditionalExpression - condição if (numeros.length === 0) alterada para if (false)  
**A Falha do Teste:** Teste original só testa arrays não vazios  
**A Solução:** Novo teste cobre array vazio  
**Status:** 🟢 Teste Implementado  

**Função:** maximoArray  
**A Mutação:** ConditionalExpression - condição if (numeros.length === 0) alterada para if (false)  
**A Falha do Teste:** Teste original só testa arrays não vazios  
**A Solução:** Novo teste cobre array vazio  
**Status:** 🟢 Teste Implementado  

**Função:** minimoArray  
**A Mutação:** ConditionalExpression - condição if (numeros.length === 0) alterada para if (false)  
**A Falha do Teste:** Teste original só testa arrays não vazios  
**A Solução:** Novo teste cobre array vazio  
**Status:** 🟢 Teste Implementado  

**Função:** isPar  
**A Mutação:** ConditionalExpression - return n % 2 === 0 alterado para return true  
**A Falha do Teste:** Teste original só verifica true para par, não false para ímpar  
**A Solução:** Novo teste verifica false para ímpar  
**Status:** 🟢 Teste Implementado  

**Função:** isImpar  
**A Mutação:** ConditionalExpression - return n % 2 !== 0 alterado para return true  
**A Falha do Teste:** Teste original só verifica true para ímpar, não false para par  
**A Solução:** Novo teste verifica false para par  
**Status:** 🟢 Teste Implementado  

**Função:** isImpar  
**A Mutação:** ArithmeticOperator - n % 2 !== 0 alterado para n * 2 !== 0  
**A Falha do Teste:** Teste original não cobre cálculo incorreto  
**A Solução:** Novo teste verifica true para 3  
**Status:** 🟢 Teste Implementado  

**Função:** isPrimo  
**A Mutação:** EqualityOperator - n <= 1 alterado para n < 1  
**A Falha do Teste:** Teste original não cobre limite 1  
**A Solução:** Novo teste verifica false para 1  
**Status:** 🟢 Teste Implementado  

**Função:** isPrimo  
**A Mutação:** ConditionalExpression - condição if (n <= 1) alterada para if (false)  
**A Falha do Teste:** Teste original não cobre 0  
**A Solução:** Novo teste verifica false para 0  
**Status:** 🟢 Teste Implementado  

**Função:** isPrimo  
**A Mutação:** ConditionalExpression - for (let i = 2; i < n; i++) alterado para for (let i = 2; false; i++)  
**A Falha do Teste:** Teste original testa primo, mas não força execução do loop  
**A Solução:** Novo teste verifica true para 5  
**Status:** 🟢 Teste Implementado  

**Função:** isPrimo  
**A Mutação:** EqualityOperator - i < n alterado para i >= n  
**A Falha do Teste:** Teste original não cobre loop correto para não primos  
**A Solução:** Novo teste verifica false para 4  
**Status:** 🟢 Teste Implementado  

**Função:** isPrimo  
**A Mutação:** ConditionalExpression - if (n % i === 0) alterada para if (false)  
**A Falha do Teste:** Teste original testa primo, mas não força detecção de não primo  
**A Solução:** Novo teste verifica false para 9  
**Status:** 🟢 Teste Implementado  

**Função:** isPrimo  
**A Mutação:** BlockStatement - bloco do for removido  
**A Falha do Teste:** Teste original não cobre execução completa do loop  
**A Solução:** Novo teste verifica false para 6  
**Status:** 🟢 Teste Implementado  

**Função:** isPrimo  
**A Mutação:** ArithmeticOperator - n % i === 0 alterado para n * i === 0  
**A Falha do Teste:** Teste original não cobre cálculo de divisibilidade  
**A Solução:** Novo teste verifica false para 8  
**Status:** 🟢 Teste Implementado  

**Função:** produtoArray  
**A Mutação:** ConditionalExpression - condição if (numeros.length === 0) alterada para if (false)  
**A Falha do Teste:** Teste original só testa arrays não vazios  
**A Solução:** Novo teste cobre array vazio  
**Status:** 🟢 Teste Implementado  

**Função:** clamp  
**A Mutação:** ConditionalExpression - if (valor < min) alterada para if (false)  
**A Falha do Teste:** Teste original testa dentro do intervalo, não abaixo  
**A Solução:** Novo teste cobre valor abaixo do min  
**Status:** 🟢 Teste Implementado  

**Função:** clamp  
**A Mutação:** EqualityOperator - valor < min alterado para valor <= min  
**A Falha do Teste:** Teste original não cobre igualdade no min  
**A Solução:** Novo teste verifica valor igual a min  
**Status:** 🟢 Teste Implementado  

**Função:** clamp  
**A Mutação:** EqualityOperator - valor > max alterado para valor >= max  
**A Falha do Teste:** Teste original não cobre igualdade no max  
**A Solução:** Novo teste verifica valor igual a max  
**Status:** 🟢 Teste Implementado  

**Função:** clamp  
**A Mutação:** ConditionalExpression - if (valor > max) alterada para if (false)  
**A Falha do Teste:** Teste original testa dentro do intervalo, não acima  
**A Solução:** Novo teste cobre valor acima do max  
**Status:** 🟢 Teste Implementado  

**Função:** isDivisivel  
**A Mutação:** ConditionalExpression - return dividendo % divisor === 0 alterado para return true  
**A Falha do Teste:** Teste original só verifica true, não false  
**A Solução:** Novo teste verifica false para não divisível  
**Status:** 🟢 Teste Implementado  

**Função:** celsiusParaFahrenheit  
**A Mutação:** ArithmeticOperator - 9/5 alterado para 9*5  
**A Falha do Teste:** Teste original usa 0, que mascara erro de multiplicação  
**A Solução:** Novo teste usa 100 para detectar multiplicação incorreta  
**Status:** 🟢 Teste Implementado  

**Função:** celsiusParaFahrenheit  
**A Mutação:** ArithmeticOperator - 9/5 alterado para /9/5  
**A Falha do Teste:** Teste original usa 0, que mascara erro de divisão  
**A Solução:** Novo teste usa 20 para detectar divisão incorreta  
**Status:** 🟢 Teste Implementado  

**Função:** fahrenheitParaCelsius  
**A Mutação:** ArithmeticOperator - 5/9 alterado para 5*9  
**A Falha do Teste:** Teste original usa 32, que mascara erro  
**A Solução:** Novo teste usa 212 para detectar multiplicação  
**Status:** 🟢 Teste Implementado  

**Função:** fahrenheitParaCelsius  
**A Mutação:** ArithmeticOperator - 5/9 alterado para /5/9  
**A Falha do Teste:** Teste original usa 32, que mascara erro  
**A Solução:** Novo teste usa 68 para detectar divisão  
**Status:** 🟢 Teste Implementado  

**Função:** inverso  
**A Mutação:** ConditionalExpression - if (n === 0) alterada para if (false)  
**A Falha do Teste:** Teste original só testa valores não zero  
**A Solução:** Novo teste cobre zero  
**Status:** 🟢 Teste Implementado  

**Função:** isMaiorQue  
**A Mutação:** ConditionalExpression - return a > b alterado para return true  
**A Falha do Teste:** Teste original só verifica true, não false  
**A Solução:** Novo teste verifica false para menor  
**Status:** 🟢 Teste Implementado  

**Função:** isMaiorQue  
**A Mutação:** EqualityOperator - a > b alterado para a >= b  
**A Falha do Teste:** Teste original não cobre igualdade  
**A Solução:** Novo teste verifica false para igual  
**Status:** 🟢 Teste Implementado  

**Função:** isMenorQue  
**A Mutação:** ConditionalExpression - return a < b alterado para return true  
**A Falha do Teste:** Teste original só verifica true, não false  
**A Solução:** Novo teste verifica false para maior  
**Status:** 🟢 Teste Implementado  

**Função:** isMenorQue  
**A Mutação:** EqualityOperator - a < b alterado para a <= b  
**A Falha do Teste:** Teste original não cobre igualdade  
**A Solução:** Novo teste verifica false para igual  
**Status:** 🟢 Teste Implementado  

**Função:** isEqual  
**A Mutação:** ConditionalExpression - return a === b alterado para return true  
**A Falha do Teste:** Teste original só verifica true, não false  
**A Solução:** Novo teste verifica false para diferente  
**Status:** 🟢 Teste Implementado  

**Função:** medianaArray  
**A Mutação:** ConditionalExpression - if (numeros.length === 0) alterada para if (false)  
**A Falha do Teste:** Teste original só testa arrays não vazios  
**A Solução:** Novo teste cobre array vazio  
**Status:** 🟢 Teste Implementado  

**Função:** medianaArray  
**A Mutação:** MethodExpression - .sort((a, b) => a - b) alterado para sem sort  
**A Falha do Teste:** Teste original usa array ordenado  
**A Solução:** Novo teste usa array não ordenado  
**Status:** 🟢 Teste Implementado  

**Função:** medianaArray  
**A Mutação:** ArrowFunction - (a, b) => a - b alterada para () => undefined  
**A Falha do Teste:** Teste original não cobre função de comparação  
**A Solução:** Novo teste usa array decrescente  
**Status:** 🟢 Teste Implementado  

**Função:** medianaArray  
**A Mutação:** ArithmeticOperator - a - b alterado para a + b  
**A Falha do Teste:** Teste original não cobre operação incorreta na comparação  
**A Solução:** Novo teste usa array com duplicatas  
**Status:** 🟢 Teste Implementado  

**Função:** medianaArray  
**A Mutação:** ConditionalExpression - if (sorted.length % 2 === 0) alterada para if (false)  
**A Falha do Teste:** Teste original usa ímpar, não força par  
**A Solução:** Novo teste usa array par  
**Status:** 🟢 Teste Implementado  

**Função:** medianaArray  
**A Mutação:** ArithmeticOperator - sorted.length % 2 === 0 alterado para sorted.length * 2 === 0  
**A Falha do Teste:** Teste original não cobre cálculo incorreto do módulo  
**A Solução:** Novo teste usa array ímpar maior  
**Status:** 🟢 Teste Implementado