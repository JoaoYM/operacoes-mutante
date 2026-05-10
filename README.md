# Laboratório: Análise de Eficácia de Testes com StrykerJS

Este laboratório tem como objetivo exercitar o uso de ferramentas de teste de mutação para avaliar a eficácia de uma suíte de testes unitários, garantindo que a cobertura de código se traduza em segurança real contra falhas lógicas.

## 📌 Contexto do Projeto
O projeto consiste em uma biblioteca JavaScript (`src/operacoes.js`) que contém diversas operações matemáticas e lógicas. Existe uma suíte de testes inicial em `test/operacoes.test.js` utilizando o framework **Jest**.

## 🎯 Objetivos do Trabalho
- Configurar e executar o framework de teste de mutação **StrykerJS**.
- Analisar o relatório de mutação inicial e identificar mutantes sobreviventes.
- Aprimorar a suíte de testes para mitigar mutantes e elevar significativamente o Mutation Score.
- Elaborar um relatório técnico detalhando o processo de análise e melhoria.

## 🛠 Metodologia de Execução
Para atingir o objetivo proposto, o trabalho foi dividido em um pipeline iterativo de refatoração, com as etapas documentadas individualmente. O processo seguiu o ciclo: análise de mutantes sobreviventes -> diagnóstico de fragilidade do teste -> implementação de novos cenários -> validação de eficácia.

As iterações focaram em:
1. **Validações Estritas:** Substituição de asserções genéricas por verificações de mensagens de erro exatas e literais.
2. **Análise de Valores Limite (BVA):** Inclusão de testes de fronteira para operadores relacionais (`>`, `<`, `>=`, `<=`).
3. **Massa de Dados Dinâmica:** Uso de arrays desordenados e valores de borda para evitar o mascaramento de lógica em funções de ordenação e mediana.

## 📊 Resultados Obtidos
Abaixo, a comparação consolidada extraída do relatório técnico da disciplina:

| Métrica | Estado Inicial | Resultado Final |
| :--- | :--- | :--- |
| **Cobertura de Código (Jest)** | 98.44% | Mantida / Elevada |
| **Mutantes Gerados** | 213 | 213 |
| **Mutantes Sobreviventes** | 44 | 4 |
| **Mutation Score (Stryker)** | **73.71%** | **98.13%** |

## 📂 Organização dos Artefatos
- `src/operacoes.js`: Biblioteca com 50 operações matemáticas.
- `test/operacoes.test.js`: Suíte de testes unitários refatorada e blindada.
- `historico_mutantes_iteracao_*.md`: Logs detalhados de cada rodada de refatoração.
- `reports/`: Relatório visual HTML comprovando a mitigação dos mutantes.

## 🚀 Como Executar
1. Instale as dependências: `npm install`
2. Execute os testes com cobertura: `npm test --coverage`
3. Execute o teste de mutação: `npx stryker run`

---
**Autor:** João Pedro Aguiar  
**Disciplina:** Testes de Software - PUC Minas
