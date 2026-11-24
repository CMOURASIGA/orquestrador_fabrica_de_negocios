# Casos de teste de negócio | v1.0
Critérios conceituais convertidos em cenários candidatos de aceite. Não executados; detalhar dados, evidências e automação na especificação.
| ID | Dado / Quando | Então |
|---|---|---|
| CT01 | Conversa consultiva sem autorização de execução | Responder sem disparar ações |
| CT02 | Pedido isolado de BPMN | Selecionar competência pertinente sem criar projeto obrigatório |
| CT03 | Duas demandas de naturezas diferentes | Planos distintos e justificáveis, sem esteira fixa |
| CT04 | Dependências e tarefas independentes | Coordenar sequência/paralelismo autorizado |
| CT05 | Usuário escolhe alternativa distinta | Registrar justificativa e recalcular plano |
| CT06 | Proposta recusada | Não iniciar projeto; preservar contexto para retomada |
| CT07 | Mesmo agente em dois setores | Núcleo/versionamento intactos, contexto e missão distintos |
| CT08 | Lacuna de competência | Justificar antes de constituir temporário; escalar se insuficiente |
| CT09 | Colaboração entre agentes | Registrar interações e respeitar limites/escopo |
| CT10 | Dois projetos do mesmo cliente/sistema | Não aplicar regra específica do outro projeto |
| CT11 | Informação substituída | Recuperar versão vigente e histórico autorizado |
| CT12 | Fornecedor rejeitado com motivo | Preservar motivo e reavaliar somente se contexto mudar |
| CT13 | Hipótese sem confirmação | Não tratá-la como decisão aprovada |
| CT14 | Proposta sem preço/licença definidos | Aguardar humano, preservar estado, não inventar valores |
| CT15 | HTML/PDF mesma versão | Dados consistentes; PDF legível e imprimível |
| CT16 | BPMN correto com sobreposições | JEV reprova visual, solicita correção e reavalia |
| CT17 | Artefato inacessível | Validação bloqueada, nunca aprovada por presunção |
| CT18 | Entrega com defeito impeditivo | Reprovar independentemente de nota média |
| CT19 | Feedback específico de cliente | Corrigir contexto local; mudança global só após curadoria e aprovação |
| CT20 | Execução aguardando humano | Liberar capacidade ativa e retomar com contexto íntegro |
| CT21 | Limite de concorrência atingido | Enfileirar sem misturar contexto, chat permanece utilizável |
| CT22 | Usuário sem autorização de outro cliente | Negar acesso inclusive na recuperação semântica |
| CT23 | Mesma pessoa em múltiplas funções | Permissões e responsabilidades conforme autorização, sem exigir contas distintas |
| CT24 | Alteração de modelo/agente homologado | Testar regressão e obter aprovação antes de promover |
| CT25 | Correção excede limites | Escalar com evidências, sem falsa homologação |
Critérios de desempenho, custo, segurança e aceitação por formato dependem de baseline e especificação. CT21 e demais metas não representam testes realizados.
