# MasterClass NotebookLM: Explorando RAG e Engenharia de Prompt na Prática

## 1. Contexto e Objetivos

Este projeto documenta um sistema prático de estudo com IA baseado em execução real, erros, correções e melhoria contínua.

O objetivo não é “usar IA”, mas construir um processo replicável que transforma informação em conhecimento.

Tema central:
**A evolução dos sistemas RAG (Retrieval-Augmented Generation) e a redução de alucinações em Modelos de Linguagem**

### Objetivos de Estudo

* Compreender como o NotebookLM aplica *grounding*
* Identificar limites e alucinações
* Criar prompts reutilizáveis orientados a extração e análise

---

## 2. Curadoria de Fontes

Critérios:

* Fonte confiável
* Conteúdo técnico
* Complementaridade

Fontes:

1. Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks (Meta AI)
2. Guia de Prompt Engineering (Google Cloud)
3. Sparks of Artificial General Intelligence (Microsoft Research)
4. Relatórios de mercado sobre IA generativa

---

## 3. Engenharia de Prompts e Cicatrizes

| Tipo        | Prompt                            | Problema                  | Correção                |
| ----------- | --------------------------------- | ------------------------- | ----------------------- |
| Superficial | "Resuma o paper"                  | Genérico, ignora detalhes | Pedir estrutura técnica |
| Enviesado   | "Por que RAG é a melhor solução?" | Viés de confirmação       | Tornar neutro           |
| Alucinação  | "Qual linguagem foi usada?"       | Informação inventada      | Forçar resposta estrita |

---

## 4. Estudo de Caso Real (Execução)

### Trecho da fonte

> "RAG combines parametric and non-parametric memory for language generation"

---

### ❌ Prompt ruim

```
Resuma o conceito de RAG
```

### Resposta da IA

```
RAG melhora respostas usando dados externos
```

### Problema

* Superficial
* Ignora arquitetura

---

### ✅ Prompt corrigido

```
Explique RAG com base no paper incluindo:
- memória paramétrica vs não paramétrica
- papel do retriever
- papel do generator
```

### Nova resposta

* Explica arquitetura
* Usa termos do paper
* Mais técnico

---

### Insight

Sem estrutura, a IA simplifica.
Com estrutura, ela respeita o nível técnico.

---

## 5. Falha Crítica Identificada

Durante testes, a IA afirmou que um exemplo usava Python.

Problema:
O documento não mencionava linguagem.

Conclusão:
Inferência baseada em padrão de mercado.

Correção:

```
Responda apenas com base no texto. Se não estiver explícito, diga "Não consta"
```

---

## 6. NotebookLM vs ChatGPT

| Critério        | NotebookLM        | ChatBot            |
| --------------- | ----------------- | ------------------ |
| Base            | Fontes fornecidas | Conhecimento geral |
| Alucinação      | Baixo             | Médio              |
| Rastreabilidade | Alta              | Baixa              |

---

## 7. Miniguia de Estudo

### O que é RAG

Combinação de geração de texto com busca em base externa.

### Benefício

Reduz alucinação ao usar fontes reais.

### Limitação

Depende da qualidade das fontes.

---

## 8. Glossário

RAG — geração com recuperação
Prompt — instrução
Grounding — ancoragem
Alucinação — erro plausível

---

## 9. Biblioteca de Prompts

**Comparação**

"Compare autores sobre [tema]"

**Extração**

"Extraia métricas e dados"

**Teste**

"Crie perguntas difíceis"

---

## 10. Como usar este repositório (execução prática)

1. Escolha um tema técnico
2. Selecione 3–5 fontes
3. Suba no NotebookLM

Use:

```
Crie um índice estruturado
```

Depois:

```
Explique o tópico com exemplos e limitações
```

Depois:

```
Crie perguntas difíceis sobre o conteúdo
```

Regra:
Se a resposta for genérica, o prompt está ruim.

---

## 11. Insights obtidos

* NotebookLM não elimina alucinação — limita o escopo
* Prompt não é pergunta — é instrução
* A IA sempre tenta responder
* Sem estrutura, ela simplifica demais

---

## 12. Conclusão

IA não melhora aprendizado.

Processo melhora.

Se o processo for ruim, a IA piora o resultado.
Se for bom, amplifica entendimento.

---

## 13. Próximos Passos

* Aplicar em React e APIs
* Criar templates
* Automatizar fluxo
