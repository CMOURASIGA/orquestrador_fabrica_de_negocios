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
| D-F01 | Direção aprovada | Regra transversal para qualquer objeto, atividade ou entregável sujeito a aprovação humana interna, não exclusiva de BPMN: perfis humanos por especialidade dos agentes padrão qualificam a relevância contextual da aprovação, não restringem acionamento de agentes nem invalidam aprovação de outro perfil. Ex.: KAIROS aprova BPMN validamente e processo segue; perfil BPMN agrega evidência especializada; múltiplas aprovações são bem-vindas, não obrigatórias por padrão. ADMIN master transversal; orquestrador e JEV sem perfil humano próprio. Acesso ao workspace e autorização da missão independentes. Pesos numéricos não definidos; autoaprovação, tratamento de divergências e regras específicas de segregação a confirmar. |
| D-F02 | Aprovado | Custos de IA exclusivos do ADMIN; comparação por modelo/agente, qualidade, latência, retrabalho e resultado aprovado para orientar consumo. Usuário operacional não vê valores financeiros de IA, inclusive via chat, relatório, exportação ou API. |
| D-F03 | Aprovado | Comentários externos analisados sempre sob demanda do consultor responsável; registro e notificação sem chamada LLM; sem comunicação IA direta ao externo. |
| D-F04 | Direção revista | PoC rápida mockada para compreender experiência; MVP mockado navegável e com possibilidade de operacionalização. Validação técnica/econômica real separada é recomendação, ainda sem autorização de despesa. Corte incremental A/B/C e fronteira exata do que funciona realmente no MVP ainda candidatos. |
| D-F05 | Parcialmente esclarecido | Desenvolvedor não amplia escopo por iniciativa própria; se identificar necessidade, justificar e obter autorização antes de mudança material. Decisão técnica dentro do escopo pode ser fundamentada. Política de proatividade operacional do orquestrador e máquinas de estado ainda requerem confirmação; manter RF014/040/056. |
| D-F06 | Direção aprovada | Seguir regulamentação aplicável e padrões de segurança pertinentes. Detalhar medidas, retenção e tratamento por fornecedores conforme obrigações e contexto; não presumir conformidade ou autorizar dados reais antes de validação. |
| D-F07 | Pendente | Confirmar individualização RF001–009. |
Ajustes de segurança ou lacunas essenciais são correções de especificação, não expansão indiscriminada. Nenhuma implementação, teste, entrevista ou chamada faturável realizada.
## Próximo marco
Confrontar matriz com fontes, validar jornadas com usuários, decidir pendências e aprovar baseline funcional; então preparar arquitetura e backlog da PoC, sem iniciar desenvolvimento nesta etapa. 
