# Backlog de evolução | congelamento de levantamento
Autorização para revisão/consolidação não autoriza desenvolvimento nem adição automática de novos RF. Ideias futuras entram neste backlog, com origem, problema, valor, dependências, risco, hipótese de custo e decisão posterior. Não são compromissos.
| Tema | Referência | Situação |
|---|---|---|
| Evolução proativa de agentes/avaliadores | RF009,044 | Pós-MVP candidato |
| Aprendizagem organizacional avançada | RF061–062 | Pós-MVP candidato |
| Colaboração externa e comentários | RF063–066 | Visão preservada; posterior proposto |
| Relatórios gerenciais avançados | RF075 | Posterior proposto |
| Executor local e publicação de aplicações | docs/04-05,11 | Posterior |
| Multi-fornecedor em produção | docs/09,11 | Posterior; extensibilidade preservada |
| Notificações e-mail/navegador/WhatsApp | RF034 | Após internas; canais dependem de autorização |
| Laboratório visual EVAL completo | RF041–047 | Incremental, controles mínimos desde PoC |
| Formatos adicionais e integrações | RF018,020 | Após formatos selecionados |
| Expansão 7C | docs/09 | Após Consult Services |
## Decisões e direcionamentos de 25/11/2026
| ID | Situação | Direcionamento |
|---|---|---|
| D-F01 | Direção aprovada | Regra transversal para qualquer objeto, atividade ou entregável sujeito a aprovação humana interna, não exclusiva de BPMN: perfis humanos por especialidade dos agentes padrão qualificam a relevância contextual da aprovação, não restringem acionamento de agentes nem invalidam aprovação de outro perfil. Ex.: KAIROS aprova BPMN validamente e processo segue; perfil BPMN agrega evidência especializada; múltiplas aprovações são bem-vindas, não obrigatórias por padrão. ADMIN master transversal; orquestrador e JEV sem perfil humano próprio. Acesso ao workspace e autorização da missão independentes. Pesos numéricos não definidos. Complemento aprovado: produção humana da própria especialidade com JEV favorável dispensa autoaprovação redundante; em outra especialidade, aprovação correspondente agrega confiança sem bloquear por padrão. Divergências: orquestrador analisa argumentos e impactos, consulta especialista se útil, encaminha ao responsável pelo projeto, que decide dentro da autoridade. ADMIN acesso organizacional; demais usuários apenas contextos autorizados. Obrigações específicas de aceite e segregação permanecem aplicáveis; responsável de workspace sem projeto é extensão proposta. |
| D-F02 | Aprovado | Custos de IA exclusivos do ADMIN; comparação por modelo/agente, qualidade, latência, retrabalho e resultado aprovado para orientar consumo. Usuário operacional não vê valores financeiros de IA, inclusive via chat, relatório, exportação ou API. |
| D-F03 | Aprovado | Comentários externos analisados sempre sob demanda do consultor responsável; registro e notificação sem chamada LLM; sem comunicação IA direta ao externo. |
| D-F04 | Direção consolidada | PoC rápida mockada para compreensão da experiência; MVP mockado navegável e com possibilidade de operacionalização, em incrementos A/B/C. Validação técnica/econômica real separada antes de operação; detalhes de implementação e critérios de liberação são trabalho posterior. Nenhuma despesa autorizada. Doc/18 v0.2. |
| D-F05 | Direção consolidada | Desenvolvedor não amplia escopo aprovado; justificar e autorizar mudanças materiais. Orquestrador atua autonomamente dentro da missão autorizada, recomenda fora dela sem executar, questiona proporcionalmente, preserva estados independentes e continuidade de atividades não afetadas. Doc/22 v0.2; parâmetros de UX e mecanismos técnicos posteriores. |
| D-F06 | Direção aprovada | Seguir regulamentação aplicável e padrões de segurança pertinentes. Detalhar medidas, retenção e tratamento por fornecedores conforme obrigações e contexto; não presumir conformidade ou autorizar dados reais antes de validação. |
| D-F07 | Definido | Individualização dos RF001–009 confirmada pelo idealizador; preservar os 76 IDs e rastreabilidade ao bloco original. |
Ajustes de segurança ou lacunas essenciais são correções de especificação, não expansão indiscriminada. Nenhuma implementação, teste, entrevista ou chamada faturável realizada.
## Próximo marco
Entrevistar idealizador como usuário, incorporar evidências, submeter baseline funcional v1.0 à aprovação; avançar UX/UI e PoC mockada. Entrevista com outro profissional permanece pendente e pode ocorrer em paralelo à UX. Validação técnica/econômica e arquitetura real são etapas posteriores; não iniciar desenvolvimento nesta consolidação. 
