# Ciclo 1 — SQL e Modelagem Dimensional

**Janela:** ~5 semanas (jun-jul 2026) · **Bancada:** migração EDF (views reais)
**Status:** EM FOCO · Unidade atual: 1.1

## Objetivo do ciclo

Sair de "escrevo SQL que funciona" para "modelo dados com método e explico por
quê". Ao final, você declara grão, desenha um star schema, justifica SCD, escreve
window functions à mão e diagnostica query lenta com EXPLAIN — o vocabulário e o
método que separam analista de engenheiro, aplicados nas suas views de produção.

## O que o mercado cobra aqui

SQL avançado é requisito em ~94% das vagas de dados; modelagem dimensional é o que
as vagas chamam de "sinal direto de senioridade e ownership do warehouse". É a
competência mais durável da área — ferramentas mudam, modelar bem não.

## Por que ele vem primeiro

É sua força (Caixa A operacional) com o método faltando (Caixa C conceitual) — a
consolidação de maior velocidade. E a bancada está quente: cada conceito se aplica
na migração EDF na manhã seguinte.

---

## Unidade 1.1 — O grão (semana 1)

A pergunta mais importante da modelagem: o que cada linha representa?

- [x] Teoria: grão, tabela-fato, dimensão, aditividade de métricas. Por que somar
      métrica não-aditiva infla número sem dar erro.
- [ ] Exercício (você escreve): declarar, em uma frase cada, o grão de 5 views da
      migração EDF (sbolsa, sservico, splanopgto e mais 2 à sua escolha).
- [ ] Exercício: para cada view, listar quais métricas são aditivas, semi-aditivas
      e não-aditivas — e onde um SUM ingênuo mentiria.
- [x] Checkpoint oral: explicar grão para um leigo em 1 minuto, sem consulta.

## Unidade 1.2 — Star schema e o método Kimball (semana 2)

- [ ] Teoria: os 4 passos de Kimball (processo de negócio → grão → dimensões →
      fatos); star vs snowflake; por que o analítico desnormaliza de propósito.
- [ ] Exercício (papel ou dbdiagram.io, você desenha): o star schema do financeiro
      EDF — fato_cobranca + dim_aluno, dim_responsavel, dim_plano, dim_tempo.
- [ ] Exercício: identificar nas suas views atuais onde nasceu uma "big flat
      table" e o que ela esconde.
- [ ] Checkpoint: defender o seu modelo — o professor ataca com perguntas de
      negócio ("e se a escola pedir X?") e o modelo tem que responder.

## Unidade 1.3 — Histórico: Slowly Changing Dimensions (semana 3)

Você já tem a intuição (diagnóstico, pergunta 3) — agora o método e o nome.

- [ ] Teoria: SCD tipos 1 e 2, surrogate key vs chave natural, vigência
      (valid_from/valid_to), snapshot no fato.
- [ ] Exercício (você escreve o DDL e o SQL): modelar o caso real — bolsa do aluno
      muda no meio do ano; o relatório precisa do valor vigente em cada cobrança.
- [ ] Checkpoint: dado um cenário novo de mudança cadastral, decidir tipo 1 ou
      tipo 2 e justificar em 3 frases.

## Unidade 1.4 — Window functions à mão (semana 4)

Zerar a dependência da IA aqui: 10 exercícios escritos por você, do zero.

- [ ] Teoria: PARTITION BY vs GROUP BY (colapsa vs mantém), ROW_NUMBER/RANK,
      LAG/LEAD, SUM OVER com frame (acumulado).
- [ ] Exercícios 1-5 (dados EDF): somatório por responsável SEM colapsar as
      parcelas; saldo acumulado; % da parcela no total do contrato.
- [ ] Exercícios 6-10: última cobrança de cada aluno (ROW_NUMBER), comparação com
      mês anterior (LAG), deduplicação com janela.
- [ ] Checkpoint: 3 exercícios novos, sem consulta, no tempo de um café.

## Unidade 1.5 — EXPLAIN: a query lenta de verdade (semana 5)

Aposentar o LIMIT como analgésico.

- [ ] Teoria: como ler EXPLAIN (ANALYZE) no PostgreSQL — Seq Scan vs Index Scan,
      nested loop, custo estimado vs real; quando índice resolve e quando não.
- [ ] Exercício de campo: pegar a SUA query lenta recorrente da EDF, rodar
      EXPLAIN ANALYZE, apontar o gargalo e propor a correção (você propõe, o
      professor revisa, você aplica).
- [ ] Checkpoint: dado um plano de execução impresso, narrar o que o banco fez e
      onde dói.

## Checkpoint final do ciclo

- [ ] Teste misto (oral + prático, ~60 min): grão, star schema, SCD, window
      functions e um plano de execução — tudo sem consulta.
- [ ] Aprovado → professor escreve o detalhamento do Ciclo 2 calibrado pelo
      resultado, e atualiza o `README.md`.
