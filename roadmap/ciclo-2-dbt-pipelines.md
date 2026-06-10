# Ciclo 2 — dbt e Pipelines (ELT) — contrato

**Janela estimada:** jul-ago 2026 · **Bancada:** migração EDF
**Status:** aguardando (detalhamento será escrito no checkpoint do Ciclo 1)

## Objetivo

Transformar o seu fluxo de views EDF num projeto dbt de verdade — camadas
staging/intermediate/marts, testes de dados, documentação e lineage — e dominar os
conceitos de pipeline que o diagnóstico marcou: ETL vs ELT, idempotência, carga
incremental, backfill.

## Escopo previsto (unidades serão detalhadas no momento certo)

1. ETL vs ELT e a anatomia do seu fluxo atual (dar nome ao que você já opera).
2. dbt na prática: instalar, modelar as views EDF como models com ref(), camadas.
3. Testes de dados (unique, not_null, relationships) e docs/lineage gerados.
4. Idempotência e carga incremental (o conceito que faltou na pergunta 8 do
   diagnóstico — delete+insert, merge/upsert, full refresh).
5. Orquestração introdutória: o que o Airflow resolve (DAG, retries, backfill) —
   conceito agora, prática no Ciclo 4 com cloud.

## Critério de entrada

Checkpoint do Ciclo 1 aprovado.
