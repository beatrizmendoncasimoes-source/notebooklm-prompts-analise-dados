# notebooklm-prompts-analise-dados
Projeto de estudo sobre engenharia de prompts para análise de dados e tomada de decisão com IA
Engenharia de Prompts para Análise de Dados e Tomada de Decisão
Contexto e Objetivo

Este projeto tem como objetivo explorar como estruturar prompts eficazes para análise de dados e tomada de decisão utilizando Inteligência Artificial.

A proposta é construir uma "fonte única de verdade" com apoio do NotebookLM, integrando diferentes fontes de conhecimento e aplicando na prática conceitos de pensamento analítico, estruturação de problemas e validação de resultados.
Curadoria de Fontes

As seguintes fontes foram utilizadas para construção do conhecimento:
## 📚 Curadoria de Fontes

### Aplicação de IA em Finanças

1. [10 Formas Práticas de Utilizar IA na Rotina Financeira](./02.10-Formas-Praticas-de-Utilizar-IA-na-Rotina-Financeira.pdf)

2. [Como Criar Agentes de Inteligência Artificial para a Rotina Financeira](./03. Como-Criar-Agentes-de-Inteligencia-Artificial-para-a-Rotina-Financeira.pdf)

3. [Guia Completo: 100 Prompts de IA para Finanças](./04. Guia-Completo-100-Prompts-de-Inteligencia-Artificial-para-Financas.pdf)

   ---
   ### 1. Fundamentos de Prompt Engineering

4. [Claude Prompting Best Practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices)  
5. [OpenAI - Best Practices for Prompt Engineering](https://help.openai.com/en/articles/6654000-best-practices-for-prompt-engineering-with-the-openai-api)  

---

### 2. Aplicação de IA em Dados e Análise

6. [Microsoft - Instruções de IA no Power BI](https://learn.microsoft.com/pt-br/power-bi/create-reports/copilot-prepare-data-ai-instructions)  
7. [Databricks - AI for Data Analysis](https://www.databricks.com/blog/ai-for-data-analysis)  

---

### 3. Pensamento Analítico e Estruturação de Problemas

8. [Guia da McKinsey para Resolução de Problemas](https://www.fbm.org.br/post/o-guia-da-mckinsey-para-a-resolu%C3%A7%C3%A3o-de-problemas-maximiza%C3%A7%C3%A3o-do-uso-de-dados)  
9. [PwC - Controller & Tomada de Decisão](https://www.pwc.com/us/en/executive-leadership-hub/controller.html)  

---

### 4. Casos Práticos e Aplicações no Mercado

10. [Post LinkedIn - Aplicação prática 1](https://www.linkedin.com/feed/update/urn:li:activity:7436399244946624513/)  
11. [Post LinkedIn - Aplicação prática 2](https://www.linkedin.com/feed/update/urn:li:activity:7443006232744898562/)  
12. [Post LinkedIn - Aplicação prática 3](https://www.linkedin.com/feed/update/urn:li:activity:7432016174780968960/)  

---

### 5. Conteúdos em Vídeo (complementares)

13. [Vídeo 1 - IA e análise de dados](https://www.youtube.com/watch?v=xfRdSwqY0ts)  
14. [Vídeo 2 - IA aplicada](https://www.youtube.com/watch?v=tuyMOZGOSzw)  
15. [Vídeo 3 - Conceitos de IA](https://www.youtube.com/watch?v=VykwP8oX1EI)  
16. [Vídeo 4 - Estratégia com IA](https://www.youtube.com/watch?v=TTds9BZIez8)
17. [Vídeo 5 - Análise de Balanço Patrimonial](https://www.youtube.com/watch?v=TIIBgA-pxlU)

---

### 6. Limitações e Riscos da IA

18. [IBM - AI Hallucinations](https://www.ibm.com/think/topics/ai-hallucinations)

## Base de Dados Utilizada

Para os testes de engenharia de prompts, foi utilizada uma base de dados estruturada a partir de um modelo financeiro contendo:

- Fluxo de caixa operacional  
- Receitas e despesas por categoria  
- Estrutura de DRE  
- Dados de competência, vencimento e pagamento  

A base foi expandida a partir de dados reais (anonimizados) para múltiplos períodos, permitindo análises comparativas e identificação de tendências.

Arquivo: [base_financeira_expandida.csv](./base_financeira_expandida.csv)

Engenharia de Prompts e Testes
Prompt 1 — Exploração da base (genérico)
"Explique a estrutura da base de dados enviada, quais são as principais variáveis e quais análises financeiras podem ser feitas com ela."
Resumo da resposta:

A IA conseguiu identificar bem a estrutura da base
Classificou variáveis corretamente
Listou várias análises possíveis (DRE, fluxo de caixa, margem, etc.)

Aprendizado:

Mesmo com prompt simples, a IA funciona bem para entendimento estrutural
Porém, não direciona para decisão
Serve como primeiro passo (contexto)

Prompt 2 — Análise ampla (sum pouco mais estruturado)
"Analise o conjunto de dados enviado em formato .csv e identifique padrões, tendências e possíveis insights relevantes."
Resumo da resposta:

A IA trouxe análise em níveis: descritivo, diagnóstico, preditivo e prescritivo
Identificou padrões de receita, custos e dependência de canal
Já começou a sugerir ações estratégicas

Aprendizado:

Estrutura no prompt → resposta mais organizada
IA começa a sair do “descritivo” para o “estratégico”
Ainda depende de contexto mais claro para aprofundar

Prompt 3 — Estruturado (FP&A com direcionamento)
"Atue como analista financeiro. Analise os dados abaixo e responda:
Principais variações
Possíveis causas
Recomendações"
Resumo da resposta:

Identificou variações relevantes (insumos, aluguel, receita)
Explicou causas com lógica financeira
Trouxe recomendações práticas

Aprendizado:

Quando você define o papel (analista FP&A) → a qualidade sobe muito
A IA passa a responder com lógica de negócio
Já entrega valor real para decisão

Prompt 4 — Avançado (cenário + decisão)
"Você é um analista FP&A. Considere um cenário de planejamento financeiro. Analise os dados e gere:
Diagnóstico
Riscos
Ações recomendadas"
Resumo da resposta:

Trouxe diagnóstico completo da operação
Identificou riscos (liquidez, planejamento, custo fixo)
Sugeriu ações estratégicas (forecast, negociação, expansão)

Aprendizado:

Contexto + estrutura + objetivo → resposta nível estratégico
IA consegue atuar como “consultor”
Aqui está o nível ideal de uso

## Dificuldades Encontradas

- Prompts genéricos geraram respostas amplas e mais vagas, pouco direcionadas para decisão;
- Necessidade de contextualizar o papel da IA (ex: analista FP&A);  
- Diferença significativa entre respostas descritivas e estratégicas;  
- Necessidade de estruturar melhor o problema antes de perguntar;  
- Importância de validar os outputs gerados (principalmente em análises financeiras).

## Mini Guia de Estudo
### Principais aprendizados

- IA não substitui pensamento analítico, ela depende dele e atua como Copiloto;
- A qualidade da resposta está diretamente ligada à qualidade do prompt;  
- Prompts estruturados geram respostas mais estratégicas;  
- Definir o papel da IA melhora significativamente a saída;  
- Dados sem contexto geram análises superficiais;  
- IA é mais eficaz quando usada para apoiar decisão, não apenas descrever dados.

### Estrutura ideal de um bom prompt

1. Definir o papel (ex: "Atue como analista FP&A")  
2. Contextualizar o cenário (ex: planejamento financeiro)  
3. Definir claramente o objetivo  
4. Estruturar a resposta esperada  

## Glossário

- Prompt Engineering: Técnica de estruturar perguntas para obter melhores respostas da IA  
- LLM (Large Language Model): Modelo de linguagem treinado com grandes volumes de dados  
- FP&A: Financial Planning & Analysis (Planejamento e Análise Financeira)  
- DRE: Demonstração de Resultado do Exercício  
- Fluxo de Caixa: Controle das entradas e saídas financeiras  
- Forecast: Projeção futura com base em dados históricos  
- Margem de Contribuição: Receita menos custos variáveis  
- Break-even (Ponto de Equilíbrio): Nível mínimo de vendas para cobrir custos  
- Hallucination: Quando a IA gera informações incorretas ou não verificadas  

### Análise de dados
"Analise os dados abaixo e identifique padrões, tendências e insights relevantes."

### Análise estruturada
"Atue como analista financeiro e analise os dados abaixo considerando:
1. Principais variações  
2. Possíveis causas  
3. Recomendações"

### Análise estratégica
"Você é um analista FP&A. Considere um cenário de planejamento financeiro. Analise os dados e gere:
- Diagnóstico  
- Riscos  
- Ações recomendadas"

### Validação de dados
"Quais inconsistências ou riscos podem existir nesses dados?"

### Tomada de decisão
"Com base nesses dados, quais decisões práticas devem ser tomadas para melhorar o resultado financeiro?"

