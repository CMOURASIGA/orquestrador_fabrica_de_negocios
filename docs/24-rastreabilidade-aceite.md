# Rastreabilidade e critérios de aceite | candidata v0.1
Doc/17 contém critério resumido para cada RF; docs/14 e 16 preservam CT01–25 e CA26–45. A matriz abaixo vincula grupos aos cenários, não inventa execução. Casos que cobrem vários RF exigem subcritérios antes do teste.
| RF | Casos candidatos | Jornada |
|---|---|---|
| 001–009 | CA27,28,29,34,38; CT11,19,24 | A/B/evolução |
| 010–014 | CT01,03–06,20,23; CA26,28,37 | A/B/C |
| 015–022 | CT02,10,11,13,15–17; CA27–29,44 | A/B/C |
| 023–025 | CT05,12,13; CA29,36 | A/B/C |
| 026–030 | CT14,20,23; CA30,31,36,37 | A |
| 031–033 | CT16,19; CA29 | B |
| 034–040 | CA31–33,40; CT20,23 | A |
| 041–047 | CT07–09,24,25; CA33,34 | Fundação/EVAL |
| 048–054 | CT14,21,24,25; CA34–36 | PoC |
| 055–057 | CT01,04,20,21,25; CA26,35,37,45 | A/B/C |
| 058–062 | CT10–13,19,22; CA38 | A/evolução |
| 063–066 | CA39,40; CT22 | Posterior |
| 067–069 | CT05,11–13; CA41 | A/B/C |
| 070–073 | CA42; CT11,19 | Encerramento |
| 074–076 | CA43; CT15 | C/gerencial |
## Template de evidência
ID caso; RF/subcritério; fase; pré-condição; versão do agente/modelo/critério; entradas autorizadas; passos; esperado; observado; PASS/FAIL/BLOQUEADO/NÃO EXECUTADO; evidência; custo e latência quando aplicáveis; responsável; data; decisão. Testes objetivos, JEV, aceite humano e homologação são independentes. Todos os 45 casos existentes estão NÃO EXECUTADOS. Cobertura por grupo não equivale a cobertura integral de subregras; completar casos atômicos e negativos na preparação da PoC e de cada incremento. RNF do doc/23 possuem gates próprios.
