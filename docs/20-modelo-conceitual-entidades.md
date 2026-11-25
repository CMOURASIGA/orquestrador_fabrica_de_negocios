# Modelo conceitual de entidades | candidato v0.1
Não é esquema SQL nem arquitetura. Referências: RF010–022,026–040,055–076. Um workspace pode ser oportunidade, projeto, produto, cliente ou atividade interna. Conversa livre pode existir sem workspace persistente; execução com efeitos exige contexto e autorização identificáveis.
| Entidade | Identidade e relações | Autoridade |
|---|---|---|
| Organização | 1:N usuários, workspaces, padrões | Cadastro autorizado |
| Usuário/vínculo | Pertence à organização; perfil ADMIN/USUARIO; responsabilidades e acessos | Cadastro e concessões autorizadas |
| Cliente/projeto | Associação opcional ao workspace, relações entre trabalhos | Cadastro/registro humano |
| Workspace | N conversas, missões, artefatos, decisões, atividades; vínculo a anterior opcional | Registro do trabalho |
| Conversa/mensagem | Autor humano/IA; contexto opcional; fontes e direção original | Mensagem original |
| Missão/autorização | Objetivo, limites, escopo, orçamento, autorizador, validade/revogação; N execuções | Autorização humana/política |
| Execução | Missão, agente/modelo/versão, dependências, eventos e consumo | Eventos verificáveis de execução |
| Artefato | Contexto, tipo, origem, N versões | Identidade estável |
| Versão | Conteúdo/referência imutável após finalização, origem, autor, base, evidência | Versão selecionada e fonte oficial |
| Parecer JEV | Versão, critérios, avaliador, evidências, resultado | Avaliação efetiva |
| Aceite | Versão, decisor, autoridade, evidência | Registro humano/cliente autorizado |
| Decisão | Autor do registro, decisor, fundamento, estado e vínculo a versões | Decisão vigente confirmada |
| Atividade/card | Responsável, condição de conclusão, prazo, vínculo a execução/artefato/decisão | Registro operacional da atividade |
| Notificação | Destinatário, referência, leitura; resolução deriva da pendência | Evento e estado de leitura |
| Conhecimento | Escopo, origem, versão, estado e curadoria | Conhecimento vigente aprovado |
| Fonte externa | Referência, acesso, data/versão consultada | Sistema oficial para o dado |
| Agente/Skill/modelo | Catálogo e versões; combinações homologadas | Versão publicada |
| Experimento EVAL | Candidato, controle, casos, rodadas, resultados e decisão de promoção | Evidências experimentais |
| Consumo | Missão/execução, custo estimado/real, atribuição e reserva | Telemetria/cobrança reconciliada |
| Concessão externa/comentário | Versão, convidado, validade/revogação; manifestação original | Registro de acesso/comentário; pós-MVP |
## Regras
Não duplicar estado entre card e execução. Histórico e memória ativa são distintos; síntese não substitui decisão ou documento. Conflitos de fontes: identificar escopo, validade e autoridade; pedir confirmação se material, sem escolher arbitrariamente. Contexto antigo não transmite automaticamente autorização. Retenção e exclusão legal/contratual podem limitar histórico; documentar política antes de dados reais. Modelo ainda requer validação.
