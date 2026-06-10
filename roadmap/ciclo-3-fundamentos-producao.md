# Ciclo 3 — Fundamentos de Produção — contrato

**Janela estimada:** ago-set 2026 · **Bancada:** RotaKids + Eurocoding
**Status:** aguardando (detalhamento no checkpoint do Ciclo 2)

## Objetivo

Fechar as duas lacunas de hábito profissional que o diagnóstico expôs: testes
("valido olhando o resultado") e Docker (não explica imagem vs container). E dar
nome ao que o seu CI já faz.

## Escopo previsto

1. pytest de verdade: escrever testes para código existente do RotaKids; o teste
   como expectativa registrada; fixtures e mocking básico.
2. O hábito: teste junto com a feature (a água passando no encanamento que o seu
   CI já tem).
3. Anatomia do seu CI: o que Ruff/ESLint/pytest/sanity verificam e por quê.
4. Docker do zero ao uso: imagem vs container, Dockerfile, volumes;
   **exercício-âncora: dockerizar a automação da Eurocoding sozinho.**
5. Logging estruturado e tratamento de erro em pipeline (o que diferencia script
   de código de produção).

## Critério de entrada

Checkpoint do Ciclo 2 aprovado.
