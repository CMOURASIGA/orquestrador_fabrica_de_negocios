# Auditoria interna da especificação funcional | 25/11/2026
Status: parecer documental para revisão independente e decisão do idealizador. Não é baseline funcional oficial, homologação, autorização de desenvolvimento ou parecer de um JEV executado.
Base: Discovery v1.0 (24/11), README e docs/00 a 14, registro de decisões; docs/15, blob 9d514352859e87cef85b96ddf4fb0ccb542bd947, commit de atualização 379add78f9089a67c1e2024ff77d3a432d1101c1. Leitura e confronto documental; sem inspeção de código, entrevistas, chamadas faturáveis ou execução de testes. Os 76 IDs incluem nove agrupados, direções aprovadas e detalhamentos candidatos. Não confundir contagem com cobertura.

## Parecer
Visão coerente e diferenciada: inteligência consultiva, adaptativa, com artefatos reais, controle humano, memória e avaliação. A especificação é um registro cumulativo útil, mas ainda não é contrato funcional implementável. Recomenda-se consolidar após revisão independente, resolver decisões prioritárias e validar jornadas com usuários antes de arquitetura final. Não ampliar escopo por contagem de features.

## Achados e tratamento recomendado
Prioridade P0 = resolver regra/critério antes de fechar escopo ou arquitetura que dela dependa; P1 = detalhar antes de desenvolver a capacidade correspondente; P2 = melhoria documental/UX. Não são incidentes observados.
| ID | Prioridade | Evidência | Achado | Tratamento candidato |
|---|---|---|---|---|
| AF01 | P0 | docs/15 RF001–009 agrupados; docs/09 estados | Requisitos não atômicos, status heterogêneos | Individualizar IDs preservando rastreabilidade; matriz ID, origem, regra, aceite, prioridade, dependência, status |
| AF02 | P0 | RF012,026,035,063; docs/03 | Dois perfis não definem quais registros cada usuário acessa | Separar perfil, organização, autorização de contexto e concessão externa por versão; decidir se usuário vê todos os workspaces da sua organização ou só autorizados; negar acesso por padrão quando indefinido |
| AF03 | P0 | RF014,031,040,055–057,066 | Proatividade e automação podem gerar execução e custo sem intenção clara | Matriz de ações automáticas/delegadas/consultivas; gatilhos, teto, autorização revogável, deduplicação; comentário externo não dispara IA por padrão recomendado |
| AF04 | P0 | RF017,029,039,070–073; docs/04-05 | Estados de tarefa, artefato, qualidade, aceite e encerramento podem ser confundidos | Máquinas de estado independentes; aprovação por versão; exceção não vira conformidade; encerramento terminal com nova demanda vinculada |
| AF05 | P0 | RF048–054; docs/07 | Bootstrapping de modelos homologados, orçamento e custo real não demonstrados | Matriz inicial em sandbox com EVAL/JEV; comparar baseline; reserva atômica, limites por chamada, reconciliação; testar esgotamento e concorrência |
| AF06 | P0 | RF055,013,030; docs/04-05 | Execução persistente exige semântica de falha e retomada | Checkpoints, idempotência, reconciliação de efeitos externos, retries limitados, cancelamento cooperativo e recuperação de falhas; definir comportamento de autorização revogada |
| AF07 | P0 | docs/03, RF019–022,058–062,067–069 | Memória, documento e decisão podem divergir; fonte oficial por entidade indefinida | Matriz de autoridade, versões, escopo, proveniência, conflitos, retenção/exclusão, correção; impedir recuperação semântica não autorizada |
| AF08 | P0 | docs/11 vs RF034–076 | Expansão de visão sem atualização do recorte | Separar PoC, MVP e posteriores; não reduzir segurança/JEV para cumprir escopo |
| AF09 | P0 | docs/06,07,13 | Hipóteses de usuário e metas ainda sem evidência | Entrevistar 1–2 usuários representativos como previsto, observar trabalho real, medir baseline, critérios de sucesso acordados |
| AF10 | P1 | RF001–009,015,018,019,033 | Edição concorrente, conflito e formato não detalhados | Versão base, detecção de conflito, rascunho, original preservado; validar round-trip BPMN; matriz ler/editar/exportar por formato |
| AF11 | P1 | RF017,043–047; docs/04-05 | JEV e EVAL precisam contratos de avaliação e independência | Rubricas versionadas, dados de teste, severidades, critérios bloqueantes, evidência real, avaliação de avaliadores; duas rodadas mínimas não são suficiência estatística |
| AF12 | P1 | RF037–039,055,068 | Kanban, execução e pendência podem duplicar estado e registros | Uma fonte por entidade, vínculos e eventos; conclusão verificável; distinguir tarefa humana, dependência e execução técnica |
| AF13 | P1 | RF034,036,038 | Notificação lida não resolve ação; frequência e delegação não definidas | Identidade da pendência, destinatário autorizado, reaviso no retorno, adiamento e prazo; sem duplicação; link profundo com controle de acesso |
| AF14 | P1 | RF063–066 | Compartilhamento precisa segurança, identidade e validade | Link restrito por padrão proposto, expiração/revogação, limite de comentários, auditoria, isolamento de HTML ativo e download; comunicação exclusivamente humana |
| AF15 | P1 | RF041–047 | Configuração de agentes pode contornar controles | Núcleo protegido, ferramentas allowlist, sandbox, publicação administrativa, rollback e versões fixadas em missões ativas; não pressupor criação de novas ferramentas sem código |
| AF16 | P1 | RF070–073; docs/00 | Encerramento terminal de projeto não equivale a cancelar conversa ou oportunidade | Definir ciclo por tipo de workspace; manutenção de histórico; garantia pós-entrega em nova demanda sem reclassificar defeito técnico como comercial automaticamente |
| AF17 | P1 | RF074–076; docs/07 e docs/04-05 | Custo visível ao usuário está pendente embora baseline diga usuário vê custo/tempo/qualidade; aprovação inicial possui definições distintas | Decidir visibilidade; separar taxa JEV inicial de aceite humano inicial; definir fórmulas, período, custo de falhas e atribuição sem dupla contagem |
| AF18 | P1 | README, docs/10; RF058–066 | Repositório público e ampliação de dados/documentos externos | Não publicar segredos, dados reais ou prompts proprietários; decidir visibilidade antes de ativos sensíveis; segurança de conectores e conteúdo não confiável |
| AF19 | P2 | RF031–033 nota de proatividade ainda em discussão vs RF040 aprovado; RF051/054 vs consolidação financeira; docs/04-05 vs RF017 | Notas históricas superadas podem induzir interpretações | Manter histórico, adicionar remissões explícitas; JEV universal para finalização interna; distinguir parâmetros financeiros experimentais de despesa autorizada |
| AF20 | P2 | docs/12 e RF044–047 | Glossário não cobre EVAL e novos objetos | Atualizar glossário e índice na próxima baseline; EVAL é avaliação, não todo processo de evolução; não confundir com eval() |

## Mapa funcional (cobre todos os IDs; agrupamento não define módulos técnicos)
| Domínio | RF | Recorte recomendado |
|---|---|---|
| Artefatos, edição, importação, fontes e análise crítica | 001–009,015–022,031–033 | PoC: versões Storytelling/proposta e JEV; MVP: BPMN manual/chat/importação e fontes selecionadas; demais formatos posteriores |
| Workspace, continuidade, colaboração e dependências | 010–014,026–030 | PoC: contexto, autorização, espera; MVP: colaboração e timeline mínima |
| Inteligência crítica | 023–025 | PoC: questionamento e alternativas fundamentadas |
| Notificações, perfis, Kanban, proatividade | 034–040 | MVP básico, PoC apenas controles mínimos de isolamento e pendência |
| Administração e evolução | 041–047 | PoC: catálogo/configuração controlada e EVAL reproduzível; MVP: administração essencial; laboratório visual completo posterior |
| Modelos e custos | 048–054 | PoC: medir, limitar, comparar; MVP: catálogo e painel básico |
| Execuções e autorização | 055–057 | PoC: persistência, retomada e autorização; MVP: central de controle |
| Conhecimento e aprendizagem | 058–062 | PoC: referência organizacional selecionada; MVP: curadoria manual/versionada; sugestões avançadas posteriores |
| Colaboração externa | 063–066 | Posterior recomendado; exportação e registro interno de aceite no MVP |
| Decisões | 067–069 | PoC: registro mínimo; MVP: rotina estruturada e impactos |
| Encerramento | 070–073 | MVP: encerramento e vínculo básico; diagnóstico ampliado posterior |
| Gestão gerencial | 074–076 | MVP: indicadores convencionais essenciais; relatórios gerenciais avançados posteriores |

## Jornadas de referência, não pipelines obrigatórios
J1 Consultoria: conversa livre → transcrição autorizada → interpretação → Storytelling versionado → JEV → confirmação humana/cliente registrada → proposta com condições comerciais confirmadas → JEV → exportação. Alternativas: falta de dados, reprovação, oportunidade recusada; não criar projeto automático.
J2 BPMN isolado: solicitar ou criar/importar → edição humana/chat → comparar com contexto → validar XML e renderização → JEV → exportar BPMN/PDF → testar Bizagi. Pode existir sem projeto formal.
J3 Continuidade: colaborador autorizado entra → consulta histórico, decisões e pendências → responde lacuna → análise de suficiência → retoma somente dependentes → resultado e notificação.
J4 Evolução: humano ou orquestrador propõe referência → comparar capacidade vigente → versão experimental → EVAL em duas ou mais rodadas e regressão → JEV → autorização administrativa → publicar/descartar/rollback. Sem alterar produção durante teste.
J5 Revisão externa (posterior): compartilhar versão → comentário externo sem chat IA → notificação → consultor solicita análise agrupada → decide esclarecimento/revisão → nova versão/JEV → compartilhar autorizado.
J6 Encerramento: diagnóstico proporcional → resolver pendências reais → confirmação humana → histórico consultável → demanda futura autorizada com novo contexto vinculado.
J7 Gestão: dashboard convencional → solicitação humana de análise → dados atuais com período/fonte → relatório versionado/JEV aplicável → compartilhamento autorizado.

## Requisitos não funcionais candidatos (não aprovados em detalhe)
| ID | Dimensão | Critério de aceite candidato |
|---|---|---|
| RNF01 | Isolamento/autorização | Testes negativos em API, busca semântica, arquivos, links e ferramentas; nenhuma divulgação não autorizada nos casos testados |
| RNF02 | Identidade e segredos | Credenciais fora de prompts/logs/repo; revogação e privilégio mínimo; testes de autorização em servidor |
| RNF03 | Segurança de conteúdo | Documento/comentário externo não concede autoridade; bloquear chamadas fora de escopo; renderização HTML isolada |
| RNF04 | Privacidade e retenção | Inventário de dados, finalidade, retenção/exclusão, exportação e recuperação; avaliar obrigações legais e contratuais antes de dados reais |
| RNF05 | Confiabilidade | Reiniciar worker durante missão; recuperar estado sem repetir efeito externo confirmado; conciliar efeitos incertos |
| RNF06 | Consumo | Reserva concorrente não excede saldo autorizado no teste; registrar desvios de cobrança e impedir novas chamadas quando esgotado; não prometer teto exato de fornecedor |
| RNF07 | Performance | Medir tempo de primeira resposta, latência por atividade, espera e p50/p95; definir metas após baseline |
| RNF08 | Disponibilidade/recuperação | Definir RPO/RTO e SLO antes de produção; demonstrar backup/restauração em ambiente isolado |
| RNF09 | Auditoria | Eventos com autor, tempo, escopo, versão e autorização; integridade e acesso protegido, sem armazenar segredos |
| RNF10 | Usabilidade/acessibilidade | Testar jornadas com usuários, navegação por teclado, responsividade, foco, estados de erro, ajuda e clareza de conclusão |
| RNF11 | Portabilidade | Exportar artefato e conhecimento autorizado com versões/metadados; teste BPMN de intercâmbio |
| RNF12 | Observabilidade | Correlacionar missão, execução, modelo, tokens, ferramenta, custo, falha e resultado; distinguir estimado de medido |

## Priorização proposta e gates
PoC: jornada J1 real com dados autorizados ou fictícios, duas alternativas de roteamento comparadas, aprovação humana, espera/retomada, artefatos reais HTML/PDF, JEV e correção, controles mínimos de acesso e orçamento. Testar também uma tarefa isolada pequena para refutar pipeline fixo. US$30 é referência experimental não autorização. Gate: demonstrar evidências de funcionamento, custo/qualidade, isolamento e recuperação; se insuficiente, revisar arquitetura antes de ampliar.
MVP candidato: J1 + J2 + Status Report com fonte autorizada (não depender do Commander), workspace colaborativo, versões, decisões, Kanban/notificações internas, central de execuções, conhecimento/padrões básicos, administração essencial, indicadores convencionais, encerramento básico. Não exigir todos os formatos, integração automática, laboratório visual completo ou publicação externa. Gate: jornadas representativas aceitas por usuários, testes negativos e critérios de qualidade, operação recuperável, limites financeiros e documentação/ajuda.
Posterior: colaboração externa completa, executor local e publicação de aplicações, agentes temporários avançados, múltiplos fornecedores em runtime, sincronização externa, integrações amplas, dashboards/análises avançadas, expansão 7C. Não exclui da visão.
Não há cronograma, custo mensal comprovado ou stack definitiva.

## Casos adicionais candidatos (complementam CT01–25, não executados)
| ID | Cenário e resultado esperado | RF |
|---|---|---|
| CA26 | Conversa livre não cria projeto ou missão faturável de produção | 014,056 |
| CA27 | Editar versão aprovada mantém original e invalida selo da nova versão até avaliação | 001–009,017 |
| CA28 | Dois usuários editam mesma versão; conflito sinalizado, nenhuma perda silenciosa | 012,019 |
| CA29 | Importação BPMN omite regra; recomenda melhoria sem alterar AS-IS | 018,031–033 |
| CA30 | Resposta parcial não fecha pendência; atividade independente continua | 028–030 |
| CA31 | Notificação lida reaparece sem duplicação; link respeita acesso | 034 |
| CA32 | Salvamentos repetidos não duplicam card; DONE exige condição verificável | 037–039 |
| CA33 | ADMIN configura agentes; usuário operacional não altera configuração; contexto alheio inacessível | 035,041 |
| CA34 | Candidato melhor em uma métrica mas com regressão bloqueante não é publicado | 044–047 |
| CA35 | Duas chamadas concorrentes disputam saldo; reserva impede nova chamada não autorizada | 051–054 |
| CA36 | Falta de dado comercial gera pergunta, não modelo mais caro nem valor inventado | 049,056 |
| CA37 | Fechar navegador e reiniciar executor preservam progresso e autorização | 055–057 |
| CA38 | Conhecimento confidencial de cliente não é promovido à organização | 058–062 |
| CA39 | Convidado tenta acessar outra versão ou enviar instrução maliciosa; acesso/execução negados | 063–066 |
| CA40 | Comentários externos são registrados sem consumo LLM obrigatório; consultor decide análise | 066 |
| CA41 | Decisão substituída permanece consultável; nova versão orienta trabalho futuro | 067–069 |
| CA42 | Encerramento com pendência real é questionado; melhoria posterior cria novo contexto | 070–073 |
| CA43 | Dashboard atualiza sem LLM; relatório registra período e fonte | 074–076 |
| CA44 | JEV não acessa artefato real; estado bloqueado, não aprovado | 017 |
| CA45 | Efeito externo incerto após falha não é repetido cegamente | 055–057 |

## Decisões para o próximo ciclo
1. Acesso a workspaces dentro da organização e autoridade de aprovação (AF02).
2. Visibilidade financeira do usuário operacional (AF17).
3. Comentários externos: análise consolidada sob demanda como padrão (AF03/14).
4. Aprovar recorte PoC/MVP e critérios de gate (AF08).
5. Confirmar estados independentes, políticas de automação e autoridade de fontes (AF03/04/07).
6. Definir política de retenção, segurança e metas não funcionais proporcionais ao recorte.
Não pedir ao idealizador decisões de stack prematuramente. D28 permanece não bloqueante.

## Roteiro de revisão independente
Ler README, docs/13, docs/15 e este parecer; consultar docs/00–14 para confrontar achados. Avaliar se o propósito original foi preservado, se há lacunas, ambiguidades, redundâncias, contradições, excesso de escopo, riscos de segurança/consumo, requisitos não testáveis e alternativas mais simples. Separar problema funcional de hipótese técnica. Para cada achado indicar ID/RF, evidência, severidade, consequência e recomendação. Identificar também discordâncias com este parecer. Não assumir que a segunda revisão equivale a validação com usuários ou homologação.
Formato sugerido: ID | documento/RF | achado | prioridade | impacto | recomendação | decisão do idealizador (em branco). Parecer final: apto para consolidação funcional, apto com ressalvas, ou requer revisão; justificar. Não solicitar dados reais de clientes nem credenciais em repositório público.

## Próximo marco
Incorporar parecer independente, discutir divergências e decisões pendentes, produzir matriz atômica de requisitos/aceite e baseline funcional oficial mediante autorização. Depois arquitetura técnica e backlog da PoC. Nenhum requisito novo deste parecer é automaticamente aprovado.


## Segunda revisão externa recebida (25/11/2026)
Parecer fornecido pelo idealizador em conversa. Revisor relata leitura dos documentos 00–15 e comparação com versão anterior; não menciona doc/16, portanto não se presume que tenha avaliado a auditoria interna. Identidade, método e independência institucional não verificados. Síntese, não transcrição integral.

| Achado externo | Correspondência interna | Tratamento recomendado |
|---|---|---|
| Expansão de escopo e ausência de corte por RF | AF01, AF08 | Matriz por RF com entregas PoC/MVP/posterior, dependências e critérios; congelar novos RF durante consolidação, ideias em backlog separado |
| Documento cronológico em vez de especificação | AF01, AF04, AF07, AF12 | Preservar doc/15 histórico; criar versão organizada por domínio, modelo conceitual de entidades e relacionamentos, matriz de permissões, estados independentes |
| Estados de aprovação heterogêneos | AF01, AF19 | Separar aprovação da direção, detalhamento proposto, prioridade de entrega e evidência de validação |
| Acesso externo vs não-objetivo MVP | AF08, AF14 | Convidado não é perfil operacional; recomendar colaboração externa posterior ao MVP, exportação e aceite registrado internamente primeiro |
| Dois perfis vs autorização por workspace | AF02 | Manter ADMIN/USUARIO; decidir alcance de dados por organização/workspace e autoridade de aprovação sem criar perfis adicionais |
| JEV e significado de finalizado | AF04, AF11 | Distinguir rascunho, candidato à finalização, avaliação, aprovação interna, aceite e publicação; associar evidências à versão |
| Excesso de atrito e custo por inteligência crítica | AF03, AF13 | Política de relevância, agrupar observações não impeditivas, deduplicar; configurar intensidade e orçamento de análises. Não suprimir bloqueios críticos por limite arbitrário de interrupções |
| Falta de validação com usuários | AF09 | Entrevistar 1–2 usuários representativos e observar jornadas A/B/C; revisão documental não equivale a pesquisa ou homologação |
| Sobreposição com arquitetura técnica | AF05, AF06 | Especificar resultados verificáveis (retomada, não duplicação, limite financeiro); mecanismos de implementação permanecem candidatos |
| LGPD e dados pessoais | RNF04, AF18 | Explicitar LGPD na governança: inventário, finalidade, base legal aplicável, papéis de tratamento, retenção, direitos, segurança e fornecedores; validar requisitos legais antes de dados reais |
| Jornadas completas A/B/C | J1/J2 e lacuna de detalhamento de Status Report | Desenvolver passos humano/sistema, alternativas, falhas, autorizações e critérios de aceite antes do desenho definitivo |

Ressalvas: RF-066 ainda é proposta, não decisão de análise automática ou sob demanda; os 76 IDs não estão todos individualmente aprovados. Proatividade configurável não deve eliminar alertas críticos, e limite por sessão é hipótese de UX. A colaboração externa é visão aprovada, não escopo MVP aprovado. A linha de corte deve preservar a capacidade adaptativa e controles mínimos de qualidade, autorização e custo.

Recomendação de sequência: congelar levantamento expansivo; elaborar matriz e corte candidato, três jornadas completas, modelo de entidades, estados e permissões; discutir decisões pendentes; realizar entrevistas; consolidar baseline mediante autorização. Não alterar decisões anteriores nem iniciar desenvolvimento nesta revisão. Parecer externo registrado, recomendações ainda sujeitas ao idealizador.
