# Ciclo 5 — Evals e RAG — contrato

**Janela estimada:** out-dez 2026 · **Bancada:** Eurocoding (evals) + vitrine (RAG)
**Status:** aguardando (detalhamento no checkpoint do Ciclo 4)

## Objetivo

Fechar a lacuna de maior prêmio salarial do seu mapa: sair de "avalio a saída do
LLM no olho" para "tenho pipeline de avaliação que detecta regressão antes do
deploy" — e construir o seu primeiro RAG production-grade (as vagas pedem
literalmente "ao menos UM sistema RAG real construído").

## Escopo previsto

1. Eval set na Eurocoding: congelar entradas de teste reais, definir critérios,
   medir ANTES de mexer no prompt — o antes/depois com número, não impressão.
2. LLM-as-Judge: usar um modelo para pontuar saídas; armadilhas e calibração.
3. Prompt e context engineering sistematizado (dar método ao que você já faz).
4. RAG end-to-end na vitrine: chunking, embeddings, vector DB (pgvector — você já
   vive no Postgres), retrieval, reranking; respostas com citação verificável.
5. Evals DO RAG: recall@k, faithfulness — fechando o loop dos dois temas.

## Critério de entrada

Checkpoint do Ciclo 4 aprovado (o RAG nasce sobre o warehouse da vitrine).
