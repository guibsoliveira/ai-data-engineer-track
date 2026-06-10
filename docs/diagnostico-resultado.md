# Diagnóstico — resultado completo (2026-06-10)

Conduzido em 3 rounds interativos, 24 perguntas, sem consulta. Este é o ponto de
partida real da trilha — o que calibrou os ciclos.

## O padrão central

**Você executa acima do que consegue nomear.** Três vezes você descreveu
corretamente, com suas palavras, conceitos cujo nome de mercado não conhecia
(SCD, ELT, o que o dbt faz). A lacuna dominante não é capacidade — é
vocabulário + método. Consolidar é mais rápido que adquirir: por isso a trilha
começa dando nome e estrutura ao que você já faz, antes de expandir.

**O padrão a quebrar:** "a IA gera a solução e eu não fixo" (suas palavras, em
duas respostas). Daí a regra de ouro do repositório: você escreve, a IA revisa.

## Mapa por área

### Caixa A — domina (consolidar o vocabulário, não reaprender)
- SQL operacional em produção (views financeiras complexas na EDF)
- Fluxo ELT na prática (gennera_stg cru → views → export É ELT; faltava o nome)
- Integração LLM em produção (Claude API na Eurocoding e automações)
- Ritual Git/PR/CI/Conventional Commits (opera com rigor; sem nomear o que o CI faz)
- Conversação em inglês do dia a dia (B2; você ensina inglês)

### Caixa B — fez mas não consolidou (dar nome, método e prática deliberada)
- Window functions (usou via IA; não distingue GROUP BY de SUM OVER de cabeça)
- Histórico vs cadastral (descreveu a essência de SCD sem saber o nome)
- Intuição correta do que o dbt faz ("minhas views com templates")
- Lint/CI (sabe que verifica "organização do código"; esqueceu nome e o resto: pytest)
- Prompt engineering (usa em produção; otimiza a entrada sem medir a saída)
- MCP como consumidor (usa servidores prontos; nunca construiu)

### Caixa C — nunca tocou (aprender do zero, em ordem de prêmio)
- **Evals / LLM-as-Judge** (maior prêmio salarial; confundiu "medir saída" com "gerar prompt melhor")
- **RAG / chunking / embedding** (não sabia o que é)
- **Cloud em profundidade** (só console; não distingue providers; lacuna estrutural integral)
- **Warehouse cloud** (BigQuery/Snowflake: nunca) e **Terraform/IaC** (só de ouvir)
- **dbt como ferramenta** (nunca usou)
- **Testes/TDD** ("valido olhando o resultado, por falta de conhecimento")
- **Docker** (não explica imagem vs container; não dockerizaria sozinho)
- **Modelagem dimensional como método** (grão: confundiu com valor de campo; star/snowflake: não sabia)
- **Performance/EXPLAIN** (query lenta → workaround com LIMIT; nunca leu um plano de execução)
- **Idempotência** (confundiu com transação/rollback — vem do mundo app, não do mundo pipeline)

## Decisões tomadas com base no diagnóstico

1. **Bloco ML/MLOps: FORA do plano de 12 meses.** Justificativa: "um dia, se
   trabalhar com dados financeiros, talvez precise" é o raciocínio que cria
   roadmap infinito. Trabalhar com dados financeiros NÃO exige treinar modelos
   (engenheiros de dados de fintech raramente treinam); e o alvo AI/LLM usa
   modelos prontos. Revisitar no mês 12 — com a base dados+IA construída, o pulo
   para ML fica curto se algum dia fizer sentido.
2. **Portfólio público hoje = zero, e parte do que existe nunca poderá ser público.**
   A migração EDF não pode ir para o GitHub (CPFs, financeiro, menores —
   SECURITY.md do próprio projeto). RotaKids é privado e é evidência de app, não
   de dados+IA. Por isso o projeto-vitrine (ciclos 4-6) é a alavanca nº 1.
3. **Título atual ("Analista de Sistemas Sênior") não comunica no mercado-alvo.**
   Nenhum recrutador internacional busca por isso, e "systems analyst" lê como
   perfil não-engenharia. O reposicionamento de narrativa é missão do
   posicionamento (LinkedIn/GitHub como Data/AI Engineer com evidência).
4. **Inglês: B2 conversacional confirmado.** Gap específico: registro técnico,
   listening em velocidade nativa, discurso estruturado (STAR). Não é "aprender
   inglês" — é migrar de registro. Trilha diária própria.

## Sequência dos ciclos (por que esta ordem)

1. **SQL/Modelagem primeiro:** consolida a força, aplica AMANHÃ na EDF (a bancada
   está quente, com prazo), e destrava o vocabulário de entrevista da área core.
2. **dbt/Pipelines em seguida:** transforma as views EDF em projeto dbt — aprende
   a ferramenta nº 1 do modern data stack sobre trabalho que já existe.
3. **Fundamentos de produção:** testes e Docker — os hábitos que o mercado assume.
4. **Cloud/Warehouse:** a maior lacuna, atacada quando já há o que migrar para lá
   (e onde nasce o projeto-vitrine).
5. **Evals/RAG:** o maior prêmio, sobre a base de dados já consolidada.
6. **Agentes/MCP + vitrine pública:** a fronteira mais quente, fechando o ciclo
   com a evidência pública que falta.
