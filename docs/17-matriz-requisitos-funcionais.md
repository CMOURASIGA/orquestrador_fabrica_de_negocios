# Matriz consolidada de requisitos | candidata v0.1 | 25/11/2026
Base: doc/15 blob 9d514352859e87cef85b96ddf4fb0ccb542bd947; auditoria doc/16 e segunda revisão externa. Preservar doc/15 como histórico. Congelamento de novas funcionalidades durante consolidação autorizado pelo idealizador nesta conversa. Não constitui baseline final nem validação técnica. RF001–009 são desdobramento candidato na ordem do bloco original, não IDs individualmente aprovados. Status conservador: aprovado refere-se à direção explícita, não aos detalhes; proposto inclui alinhamentos sem aprovação individual explícita. P=PoC (capacidade mínima experimental), M=MVP (incremental), F=pós-MVP. A prioridade é candidata, não aprovação de escopo. Dependências indicam relações funcionais, não ordem de implementação; ciclos são co-requisitos. 0=controle fundacional. Critérios resumidos complementam, não substituem regras integrais do doc/15. Todo requisito mantém condições e limites da fonte.

## Artefatos e fontes
| RF | Regra resumida | Status | Fase | Dependências RF | Aceite candidato |
|---|---|---|---|---|---|
| RF-001 | Editar manualmente versão sem perder original | Proposto (desdobramento) | M | 19 | Edição salva em nova revisão |
| RF-002 | Comparar versões | Proposto (desdobramento) | M | 1,19 | Diferenças identificadas |
| RF-003 | Interpretar diferenças relevantes | Proposto (desdobramento) | M | 2,21 | Interpretação separada do original |
| RF-004 | Solicitar justificativa seletiva | Proposto (desdobramento) | M | 3,24 | Mudança ambígua material gera pergunta |
| RF-005 | Avaliar impacto | Proposto (desdobramento) | M | 3,67 | Relacionados sinalizados sem sobrescrita |
| RF-006 | Registrar autoria e histórico | Proposto (desdobramento) | P | 19 | Autor e versão recuperáveis |
| RF-007 | Revalidar após alterações | Proposto (desdobramento) | P | 17,19 | Nova versão não herda parecer |
| RF-008 | Curar memória de alterações | Proposto (desdobramento) | M | 21,60 | Hipótese não vira regra |
| RF-009 | Propor evolução de agentes/avaliadores | Proposto (desdobramento) | F | 44,46 | Candidato não altera produção |
| RF-015 | Criar manualmente entregável não previsto | Aprovado: direção | M | 17,19 | BPMN sem projeto obrigatório |
| RF-016 | Importar trabalho existente | Aprovado: direção | M | 18,19 | Original associado sem sobrescrever |
| RF-017 | JEV universal para validação interna; autoria humana da própria especialidade dispensa autoaprovação redundante | Aprovado: direção | P | 19 | Rascunho livre; versão final avaliada; autor especialista não precisa aprovar formalmente a própria entrega após JEV favorável; preservar exigências específicas |
| RF-018 | Importar/exportar formatos selecionados | Proposto: detalhe/alinhamento | M | 19 | Round-trip BPMN com perdas sinalizadas |
| RF-019 | Fonte oficial e versões | Proposto: detalhe/alinhamento | P | 6 | Versão aprovada recuperável |
| RF-020 | Consultar fontes autorizadas | Proposto: detalhe/alinhamento | M | 35,57 | Fonte/data registradas ou lacuna explícita |
| RF-021 | Preservar orientação literal | Proposto: detalhe/alinhamento | P | 19 | Síntese não substitui fonte |
| RF-022 | Comunicar mudança externa | Proposto: detalhe/alinhamento | M | 19,21 | Impactos sem sincronização silenciosa |
| RF-031 | Confrontar artefato com contexto | Aprovado: direção | M | 19,21 | Omissão relevante sinalizada |
| RF-032 | Recomendar alteração fundamentada | Proposto: detalhe/alinhamento | M | 31,24 | AS-IS não vira TO-BE silenciosamente |
| RF-033 | Debater e revisar sob autorização | Proposto: detalhe/alinhamento | M | 17,31 | Rejeição preservada |

## Workspace e colaboração
| RF | Regra resumida | Status | Fase | Dependências RF | Aceite candidato |
|---|---|---|---|---|---|
| RF-010 | Retomar contexto real | Proposto: detalhe/alinhamento | P | 19,21 | Síntese com fontes e versões |
| RF-011 | Timeline de eventos | Proposto: detalhe/alinhamento | M | 10,55 | Eventos distinguem propostas |
| RF-012 | Colaboração autorizada | Proposto: detalhe/alinhamento | M | 35 | Segundo usuário acessa somente contexto permitido |
| RF-013 | Intervir em execução | Proposto: detalhe/alinhamento | P | 55,57 | Pausa/cancelamento preserva resultados válidos |
| RF-014 | Autonomia dentro de missão | Aprovado: direção | P | 56,57 | Pedido explícito executa sem aprovar cada passo |
| RF-026 | Direcionar pendências | Aprovado: direção | M | 12,35 | Responsável autorizado identificado |
| RF-027 | Contextualizar colaborador | Proposto: detalhe/alinhamento | M | 10,12 | Resumo respeita acesso |
| RF-028 | Identificar lacunas | Proposto: detalhe/alinhamento | P | 14 | Condição de desbloqueio explícita |
| RF-029 | Continuar atividades independentes | Proposto: detalhe/alinhamento | P | 28,55 | Dependência bloqueia só afetados |
| RF-030 | Verificar resposta e retomar | Proposto: detalhe/alinhamento | P | 28,57 | Resposta insuficiente mantém espera |

## Inteligência crítica
| RF | Regra resumida | Status | Fase | Dependências RF | Aceite candidato |
|---|---|---|---|---|---|
| RF-023 | Questionar incoerência material | Aprovado: direção | P | 21 | Contradição relevante sinalizada |
| RF-024 | Fundamentar questionamento | Proposto: detalhe/alinhamento | P | 23 | Referência e alternativa sem inventar |
| RF-025 | Respeitar autoridade humana; responsável do projeto resolve divergências | Aprovado: direção de resolução de divergências | P | 57 | Orquestrador analisa argumentos e impactos, consulta especialista se útil, registra decisão do responsável; confirmação não contorna segurança ou JEV |

## Kanban e acesso
| RF | Regra resumida | Status | Fase | Dependências RF | Aceite candidato |
|---|---|---|---|---|---|
| RF-034 | Notificações internas clicáveis | Aprovado: direção | M | 26,35 | Leitura não encerra pendência |
| RF-035 | ADMIN master e acesso organizacional; demais usuários em contextos autorizados; relevância contextual das aprovações | Aprovado: direção revista (D-F01) | P | 0 | Aprovação de outro perfil válida; aprovação especializada adicional sem bloqueio automático; ADMIN master; teste negativo de contexto |
| RF-036 | Atribuição manual e assistida | Proposto: detalhe/alinhamento | M | 26,35 | Sem responsável não inventa atribuição |
| RF-037 | Kanban contextual | Aprovado: direção | M | 28,36 | Salvamentos não duplicam cards |
| RF-038 | Prazo e condição de conclusão | Proposto: detalhe/alinhamento | M | 37 | Prazo sugerido não é confirmado |
| RF-039 | Conclusão verificável | Proposto: detalhe/alinhamento | M | 17,37 | DONE só com evidência aplicável |
| RF-040 | Proatividade limitada por política | Aprovado: direção | M | 23,56 | Sem monitoramento LLM contínuo |

## Agentes e EVAL
| RF | Regra resumida | Status | Fase | Dependências RF | Aceite candidato |
|---|---|---|---|---|---|
| RF-041 | Administração de agentes pela UI | Aprovado: direção | M | 42,43 | Configuração suportada sem código |
| RF-042 | Catálogo versionado mínimo | Proposto: detalhe/alinhamento | P | 35 | Identidade e limites recuperáveis |
| RF-043 | Teste isolado e publicação humana | Proposto: detalhe/alinhamento | P | 17,42 | Candidato não afeta versão vigente |
| RF-044 | Identificar evolução por referências | Aprovado: direção | F | 42,46 | Licença e valor analisados |
| RF-045 | Reusar antes de criar | Proposto: detalhe/alinhamento | P | 42 | Alternativa existente comparada |
| RF-046 | EVAL mínimo duas rodadas | Aprovado: direção | P | 17,42 | Resultados e regressões registrados |
| RF-047 | Controlar promoção e rollback | Proposto: detalhe/alinhamento | P | 43,46 | Regressão impeditiva bloqueia |

## Custos
| RF | Regra resumida | Status | Fase | Dependências RF | Aceite candidato |
|---|---|---|---|---|---|
| RF-048 | Selecionar modelo homologado | Aprovado: direção | P | 42,46 | Seleção justificada |
| RF-049 | Evitar escalonamento inútil | Proposto: detalhe/alinhamento | P | 48,28 | Lacuna gera pergunta |
| RF-050 | Medir custo/modelo/resultado | Proposto: detalhe/alinhamento | P | 48 | Estimado separado de real |
| RF-051 | Limitar orçamento | Proposto: detalhe/alinhamento | P | 50,57 | Saldo insuficiente impede nova chamada |
| RF-052 | Política equilibrada | Aprovado: direção | P | 48,51 | Qualidade obrigatória preservada |
| RF-053 | Controlar consumo antes de executar | Proposto: detalhe/alinhamento | P | 48,51 | Chamadas concorrentes respeitam autorização |
| RF-054 | Comparar roteamento com baseline | Proposto: detalhe/alinhamento | P | 46,50 | Custo total e qualidade medidos |

## Execução
| RF | Regra resumida | Status | Fase | Dependências RF | Aceite candidato |
|---|---|---|---|---|---|
| RF-055 | Persistência e controle de execução | Aprovado: direção | P | 13,57 | Fechar navegador não perde missão |
| RF-056 | Iniciativa humana e automações limitadas | Aprovado: direção | P | 35 | Opinião não inicia produção |
| RF-057 | Registrar e revogar autorização | Proposto: detalhe/alinhamento | P | 56,51 | Nova ação fora do escopo bloqueada |

## Conhecimento
| RF | Regra resumida | Status | Fase | Dependências RF | Aceite candidato |
|---|---|---|---|---|---|
| RF-058 | Base permanente organizacional | Aprovado: direção | M | 21,35 | Conhecimento sem projeto |
| RF-059 | Curadoria e versões de conhecimento | Proposto: detalhe/alinhamento | M | 58,19 | Fonte e escopo preservados |
| RF-060 | Alteração controlada | Proposto: detalhe/alinhamento | M | 59 | Conflito não sobrescreve regra |
| RF-061 | Recomendar lições generalizadas | Aprovado: direção | F | 60,35 | Sem promoção confidencial |
| RF-062 | Classificar melhoria por destino | Proposto: detalhe/alinhamento | F | 44,60,61 | Sem publicação automática |

## Colaboração externa
| RF | Regra resumida | Status | Fase | Dependências RF | Aceite candidato |
|---|---|---|---|---|---|
| RF-063 | Compartilhar versão externamente | Aprovado: direção | F | 19,35 | Convidado restrito à versão |
| RF-064 | Registrar comentário e impacto | Proposto: detalhe/alinhamento | F | 63,34 | Original separado da análise |
| RF-065 | Comunicação mediada pelo consultor | Aprovado: direção | F | 63 | Nenhum chat externo IA |
| RF-066 | Análise somente sob demanda do consultor | Aprovado: direção (D-F03) | F | 64,51 | Comentário não dispara LLM; análise exige solicitação |

## Decisões
| RF | Regra resumida | Status | Fase | Dependências RF | Aceite candidato |
|---|---|---|---|---|---|
| RF-067 | Registro de decisão com autoria | Aprovado: direção | P | 21,35 | Autor do registro distinto do decisor |
| RF-068 | Analisar impactos de decisão | Proposto: detalhe/alinhamento | M | 67,31 | Pendência proposta sem alterar aprovado |
| RF-069 | Histórico de decisões | Proposto: detalhe/alinhamento | M | 67,19 | Substituída continua consultável |

## Encerramento
| RF | Regra resumida | Status | Fase | Dependências RF | Aceite candidato |
|---|---|---|---|---|---|
| RF-070 | Encerramento terminal de projeto | Aprovado: direção | M | 39,17 | Não reabre escopo encerrado |
| RF-071 | Melhoria posterior em nova demanda | Aprovado: direção | M | 70 | Vínculo sem reabertura |
| RF-072 | Diagnóstico de encerramento | Proposto: detalhe/alinhamento | M | 70,39 | Pendência real impede recomendar fechamento |
| RF-073 | Reutilizar contexto anterior seletivo | Proposto: detalhe/alinhamento | M | 71,10 | Não herda orçamento/aceite |

## Gerencial
| RF | Regra resumida | Status | Fase | Dependências RF | Aceite candidato |
|---|---|---|---|---|---|
| RF-074 | Dashboard convencional e análise sob demanda | Aprovado: direção | M | 50,55 | Atualização objetiva sem LLM |
| RF-075 | Relatório gerencial contextualizado | Aprovado: direção | F | 74,17 | Período e fonte identificados |
| RF-076 | Definir métricas essenciais | Proposto: detalhe/alinhamento | M | 50,74 | Denominador e fonte explícitos |

## Cobertura
76 IDs únicos. P=31; M=36; F=9. Fase indica primeira capacidade mínima, não escopo completo de cada RF. RF034 e-mail/navegador configuráveis e WhatsApp posteriores; RF055 central visual no MVP, persistência PoC; RF041 administração mínima MVP, laboratório completo posterior; RF074 análise avançada posterior. RF051 custos de IA exclusivos do ADMIN (D-F02); RF066 análise sempre sob demanda do consultor (D-F03); RF001–009 confirmar desdobramento.
