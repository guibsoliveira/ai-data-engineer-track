# Ciclo 4 — Cloud e Warehouse — contrato

**Janela estimada:** set-out 2026 · **Bancada:** projeto-vitrine (nasce aqui)
**Status:** aguardando (detalhamento no checkpoint do Ciclo 3)

## Objetivo

Atacar a sua maior lacuna estrutural (Caixa C integral no diagnóstico): um
provedor cloud em profundidade, um warehouse de verdade e infraestrutura como
código. É aqui que nasce o **projeto-vitrine** — o repositório público end-to-end
(ingestão → dbt → warehouse → IA) que será sua evidência de mercado.

## Escopo previsto

1. Conceitos que destravam tudo: compute vs storage, object storage, IAM,
   por que "console clicando" não é saber cloud.
2. BigQuery: carregar dados públicos, particionamento e clustering, o modelo de
   cobrança — por que uma query custa dólares e como custar centavos.
3. Terraform básico: provisionar e destruir o ambiente inteiro por código.
4. Airflow gerenciado (ou Dagster) orquestrando o primeiro pipeline na nuvem.
5. Projeto-vitrine v0: ingestão de uma fonte real (dados públicos de educação
   combinam com a sua narrativa) → dbt → BigQuery, com README documentando
   decisões.

## Decisão em aberto (tomar no detalhamento)

GCP/BigQuery vs AWS: BigQuery tem curva mais curta e gratuidade generosa; AWS
domina as vagas. Provável: BigQuery como warehouse + conceitos AWS por cima.

## Critério de entrada

Checkpoint do Ciclo 3 aprovado.
