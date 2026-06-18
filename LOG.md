# LOG — registro de sessões

Uma linha por sessão. Preenchido pelo professor ao fim de cada sessão.

| Data | Min | Trilha | O que foi feito | Nota |
|---|---|---|---|---|
| 2026-06-10 | 30 | inglês | Shadowing no carro (trajeto para o trabalho) | primeira sessão registrada |
| 2026-06-10 | — | diagnóstico | Diagnóstico completo (3 rounds, 8 blocos) concluído no chat | mapa em docs/diagnostico-resultado.md |
| 2026-06-16 | 90 | c1.1 | Estudou o banco real EDF; teoria 1.1: grão (teste da unicidade), dimensão vs fato, carona, aditividade (3 sabores), SUM silencioso; grão à mão de saluno, sbolsaaluno + exercício sbolsa/sservico/splanopgto (3/5) | Entendimento 8/10, precisão/comunicação 6/10; checkpoint oral do grão passou. Carona precisou de 3 repetições (drillar). Pendente: 2/5 views (incluir 1 fato) + classificar medidas. Resumo HTML em resumos/ |
| 2026-06-17 | 60 | c1.1 | Fechou a 1.1: grão e classificação de medidas da sparcela (fato); corrigiu papel de VALOR/DESCONTO (medida aditiva no fato vs atributo na dimensão sservico); aprendeu por que view não-materializada é lenta (recompute) e o teste da unicidade em SQL (GROUP BY/HAVING) | Carona aplicada certo (removeu RA/CODPERLET do grão por dependência do contrato). Query de verificação correta. 1.1 CONCLUÍDA; próximo: 1.2 star schema/Kimball |
| 2026-06-17 | 120 | c1.2 | Star schema e Kimball: 4 passos, fato vs dimensão em estrela, origem (gennera_stg) vs modelo dimensional, como dim liga no fato (chave por dim; PK não liga; data=chave do tempo), dim_tempo (decidiu deixar fora). Montou o star da cobrança (fato invoice + dim contract/person/enrollment) e passou no checkpoint de 3 perguntas: faturado vs pago, responsável vs aluno, dever vs inadimplente, fan-out via ponte 1:N | Modelo aguentou os 3 ataques. Feedback dele: didática densa/direta demais (ajustado, ver memória feedback-study-teaching). Pendente 1.2: star vs snowflake/desnormalização + exercício big flat table. Resumo HTML em resumos/ |
