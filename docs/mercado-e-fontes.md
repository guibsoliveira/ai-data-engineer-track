# Mercado 2026 — o que as vagas exigem (consolidado e verificado)

Pesquisa de 5 frentes (Data Engineer internacional, AI/GenAI internacional, premium
BR, taxonomia de blocos, inglês técnico) + verificação adversarial das faixas
salariais. Números são **faixas, não pontos** — onde a verificação trimou um valor
otimista, está corrigido aqui.

## Comparação fria de salários (pleno; verificada)

| Trilha | BR CLT/mês | BR PJ/mês | Remoto USD/ano | Observação |
|---|---|---|---|---|
| Backend puro (piso de referência) | R$ 12-20k | R$ 17-28k | US$ 35-55k | Sem prêmio de dados/IA |
| Data / Analytics Engineer | R$ 18-28k (top-tier) | R$ 25-40k | US$ 54-84k (mid) | Prêmio 15-25% sobre dev genérico |
| AI / GenAI Engineer | R$ 20-32k | R$ 28-45k | US$ 70-130k (mid LATAM) | Prêmio GenAI ~10-15% sobre ML |
| **Híbrido AI/Data (alvo)** | R$ 20-32k | R$ 28-45k | **US$ 70-120k (mid)** | Captura o prêmio da interseção |

Notas de honestidade (da verificação):
- Faixas BR CLT de pleno só batem o topo em top-tier/SP. A média nacional de
  Engenheiro de Dados CLT é ~R$ 14,4k/mês (salario.com.br, base CAGED 2026).
- Nubank (levels.fyi): mediana ~R$ 245-249k/ano (~R$ 20k/mês) ≈ IC4/IC5, **não**
  IC3 (IC3 ~R$ 120k/ano ~R$ 10k/mês). Os pacotes altos (até R$ 1,2 mi/ano) vêm de
  stock/bônus, não do mensal.
- Remoto USD: os números US "cheios" são bem maiores (mid AI base US$ 140-210k);
  contratado LATAM via Deel roda ~30-50% disso. Bandas geográficas estão
  **parcialmente comprimidas, não eliminadas** (Anthropic/OpenAI ainda pesam SF).
- Forward Deployed Engineer (FDE) é o teto do segmento em 2026 (mid total
  ~US$ 250-510k), mas exige perfil customer-facing e o total é dominado por equity
  ilíquido.

**Alvo realista seu, 12 meses:** sair do nível atual para pleno e fechar contrato
remoto na faixa **US$ 60-90k/ano**, com a interseção dados+IA empurrando para
US$ 100k+ conforme você amadurece. É 2,5-4x um CLT brasileiro típico.

## Must-haves consolidados (aparecem nos dois alvos)

1. SQL avançado: window functions, CTEs, otimização (planos de execução = diferencial senior).
2. Python production-grade: modular, com error handling e testes — não "scripts".
3. Modelagem de dados: star schema (Kimball), SCD, declarar o grão antes do SQL.
4. Orquestração com Airflow (padrão; Dagster/Astronomer/MWAA como variações).
5. Cloud em profundidade: ao menos um provedor (AWS predominante).
6. Cloud data warehouse: Snowflake e/ou BigQuery.
7. dbt para transformação ELT (camadas staging/intermediate/marts, testes, lineage).
8. Git + CI/CD para pipelines (PR/review, GitHub Actions, deploy reproduzível).
9. Spark/PySpark: nice-to-have no internacional puro, **must-have no BR premium**.

## Onde o alvo internacional difere do BR premium

- **Inglês:** internacional é filtro eliminatório (nearshore aprova ~2%); BR
  premium é diferencial, raramente eliminatório.
- **Portfólio público:** internacional pesa portfólio no GitHub (substitui o nome
  de empregador desconhecido); BR premium pesa referral + nome de empresa no CV.
- **Stack de IA:** internacional cobra RAG/evals/agents/MCP como núcleo; BR premium
  ainda trata GenAI como diferencial emergente (forte no iFood), com núcleo em
  Spark+Airflow+cloud+modelagem.
- **Linguagem:** internacional assume Python/PySpark; parte do BR premium (Nubank)
  roda o core em Scala/Clojure — PySpark vira substituível ali.
- **Contratação:** internacional é PJ/contractor USD via marketplace nearshore
  (Revelo/Near/Howdy) ou Deel; BR premium é majoritariamente CLT nas top-tier.
- **Comunicação:** internacional exige operar low-context (explícito, pushback
  direto, ownership assíncrono) para um time em outro fuso confiar em você.

## Inglês — o veredito (além do B2)

B2 forte é o piso que passa em muitos processos de IC; **C1 é o alvo prático**
para conforto e trilha senior/client-facing. No B2 o gargalo deixa de ser
gramática e passa a ser: latência de produção (montar a frase rápido para entrar
na daily antes do tópico mudar), listening em velocidade nativa com sotaques
variados (inclusive indiano), idioms de negócio ("circle back", "take it
offline"), tom na escrita assíncrona (hedging em PR/Slack), narrativa STAR com
ownership ("I designed/I led", com números) e comportamento intercultural
low-context. Treino de maior retorno: shadowing diário + output ativo + 6 mock
interviews gravadas + comprehensible input do seu domínio + drills de escrita
assíncrona. Detalhe no bloco 08.

## Canais de acesso

- **Internacional (USD):** Revelo, Near (hirewithnear), Howdy, Mismo (nearshore);
  Wellfound, Himalayas, RemoteOK, RemoteRocketship, Jobgether (remote-first);
  Trampar de Casa (curadoria BR); LinkedIn; Deel/Wise para receber.
- **BR premium:** carreiras oficiais (Nubank, iFood/Greenhouse, Mercado Livre,
  Gupy nas fintechs); LinkedIn; referral interno (peso alto); comunidades de dados.

## Fontes principais

Salários e mercado:
- https://www.hirewithnear.com/blog/data-engineer-salary
- https://www.hirewithnear.com/blog/ai-engineer-salary
- https://www.hireinsouth.com/post/latam-salary-benchmark
- https://www.howdy.com/blog/2025-latin-america-software-developer-salaries
- https://www.kore1.com/ai-engineer-salary-guide/
- https://getperspective.ai/blog/2026-forward-deployed-engineering-compensation-report-1200-fdes
- https://www.levels.fyi/companies/nubank/salaries/software-engineer
- https://www.salario.com.br/profissao/engenheiro-de-dados-cbo-212205/
- https://www.deel.com/global-hiring-report-2026/
- https://mismo.team/latam-engineering-rates-costs-by-role-and-country/

Skills, taxonomia e roadmaps:
- https://github.com/DataTalksClub/data-engineering-zoomcamp
- https://github.com/chiphuyen/aie-book (AI Engineering, Chip Huyen)
- https://roadmap.sh/ai-engineer · https://roadmap.sh/data-engineer
- https://www.getdbt.com/blog/guide-to-dimensional-modeling
- https://www.getdbt.com/blog/what-is-analytics-engineering
- https://www.dataquest.io/blog/data-engineering-skills/
- https://montecarlo.ai/blog-what-is-an-ai-data-engineer/

Vagas reais (amostra):
- https://international.nubank.com.br/pt-br/careers/
- https://carreiras.ifood.com.br/gen-ai/
- https://wellfound.com/role/r/ai-engineer
- https://www.remoterocketship.com/country/latin-america/jobs/data-engineer/

Inglês técnico:
- https://speaktechenglish.com/star-method-answers-for-software-engineers-non-native-english-2026/
- https://practiceme.app/for/english-for-tech-workers
- https://www.testgorilla.com/blog/b2-language-proficiency/
- https://trykaiwa.com/blog/english-shadowing-technique-fluency-2026
