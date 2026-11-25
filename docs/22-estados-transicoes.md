# Estados e transições | candidatos v0.1
Estados independentes, não uma única esteira. RF013,017,029,038–039,055,067–073. Nomenclatura candidata. Regras de autoria, divergência e acesso consolidadas em doc/21 v0.5.
| Objeto | Estados | Transições e condições |
|---|---|---|
| Workspace projeto | ativo, suspenso, em encerramento, encerrado, cancelado | suspenso retorna ativo; encerrado terminal para execução; cancelado não equivale a concluído; encerramento depende de responsável e escopo concluído |
| Oportunidade | aberta, aguardando, aceita, recusada, arquivada | aceite não cria projeto automaticamente; retomada de oportunidade não reabre projeto encerrado |
| Missão | proposta, autorizada, revogada, concluída | autorização define limites; revogação impede novas ações |
| Execução | enfileirada, executando, aguardando humano/fonte, pausada, concluída, falha, cancelada | retomada dentro de autorização; preservar resultados; efeito externo incerto exige conciliação antes de repetir |
| Produção de versão | rascunho, candidata à finalização, finalizada internamente, substituída | humano/agente apresenta versão pronta para avaliação; JEV aprovado e testes aplicáveis permitem finalização; alteração cria nova versão |
| JEV | não solicitado, pendente, avaliando, aprovado, reprovado, bloqueado | versão e rubrica identificadas; nova avaliação preserva parecer anterior; exceção registrada não muda reprovação em aprovação |
| Aprovações humanas internas | registros individuais de aprovação, reprovação ou revisão | múltiplas aprovações por versão; perfil correspondente qualifica relevância especializada, outros perfis são válidos; ADMIN master; não bloquear por diferença de perfil salvo exigência específica; preservar divergências; responsável pelo projeto decide após análise do orquestrador e consulta especializada se útil; JEV independente; autoria humana da própria especialidade com JEV favorável dispensa autoaprovação formal; aprovação especializada adicional não bloqueia por padrão |
| Aceite externo | não aplicável, pendente, aceito, recusado | autoridade e evidência por versão; não inferir silêncio como aceite |
| Compartilhamento | não compartilhado, ativo, expirado, revogado | autorização por versão; futura colaboração externa; exportação convencional registra evento, não concede link |
| Card | a fazer, em andamento, aguardando/bloqueado, revisão, concluído, cancelado | DONE requer condição verificável; invalidada condição, reabrir ou criar revisão vinculada, salvo projeto encerrado |
| Decisão | proposta, confirmada, rejeitada, substituída, revogada | autoridade confirma; nova decisão referencia anterior; história preservada |
| Conhecimento | identificado, em curadoria, aprovado, substituído, rejeitado | somente autorizado/aplicável recuperado como regra vigente |
| Agente candidato | experimental, em avaliação, aprovado para publicação, publicado, descartado | EVAL/JEV e humano; rollback preserva versões |
## Gatilhos e atrito
Automático sem LLM: salvar estado, registrar eventos, atualizar métricas, avisar pendência, avaliar condições determinísticas. Delegado: produção e análise solicitadas. Consultivo: recomendações novas aguardam autorização. Proposta de severidade: crítica bloqueia ação afetada; alta esclarecer antes de concluir; média agrupar; baixa registrar sugestão. Deduplicar, respeitar orçamento, não limitar alertas críticos por contador de sessão. Gatilhos semânticos ainda dependem de política aprovada; salvar rascunho não aciona análise obrigatória a cada edição. Pendências independentes continuam. Comentários externos analisados exclusivamente sob demanda do consultor responsável (D-F03).
