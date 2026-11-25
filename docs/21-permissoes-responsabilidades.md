# Matriz de permissões | candidata v0.1
RF012,026,035,041,057,063–066. Dois perfis operacionais aprovados. Autorização de contexto e responsabilidade não são novos perfis. Proposta conservadora: USUARIO somente workspaces autorizados, ADMIN no âmbito da organização autorizada, sem bypass de restrições legais/contratuais. A abrangência exata depende do idealizador.
| Ação | ADMIN | USUARIO | Convidado (futuro) | Orquestrador/agente |
|---|---|---|---|---|
| Configurar organização, usuários e limites | Sim no âmbito | Não | Não | Não |
| Consultar workspace | Âmbito autorizado | Contexto concedido | Não | Contexto da missão |
| Criar/editar entregável | Autorizado | Autorizado | Não | Missão autorizada |
| Registrar decisão | Com autoria/autoridade | Com autoria/autoridade | Não | Operacional ou registro de decisão humana |
| Aprovar negócio/aceite | Se autoridade atribuída | Se autoridade atribuída | Aceite da versão se concedido | Não substituir humano |
| Conceder acesso/compartilhar | Autorizado | Se delegado expressamente | Não | Não unilateralmente |
| Visualizar/comentar versão externa | Autorizado | Autorizado | Somente concessão | Análise interna autorizada |
| Configurar/publicar agentes | Sim após evidências | Não | Não | Sugere, não promove |
| Consultar custos | Global autorizado | Pendente de decisão | Não | Somente missão/política |
| Ampliar orçamento | Administrador autorizado | Não | Não | Não |
| Encerrar trabalho | Se responsável autorizado | Se responsável autorizado | Não | Recomenda |
| Revogar execução | Dentro de autoridade | Própria missão ou delegação | Não | Pausa por política/limite |
## Regras transversais
Negar quando autorização não definida; verificar também arquivos, buscas, links, exportações e ferramentas. Atribuição de card não concede acesso automaticamente. Revogação bloqueia novas ações, preserva efeitos confirmados e histórico conforme retenção. Convidado não é terceiro perfil operacional e não conversa com IA. Comentários são dados não confiáveis. Testes negativos antes do MVP; mecanismo de identidade não definido.
