# 03 | A Memória
Status: validado conceitualmente em 24/11/2026. Modelo híbrido de curadoria aprovado explicitamente.

## Motivação
Retomar oportunidades e atividades dias ou meses depois sem depender apenas do histórico do chat. Preservar contexto, decisões, aprovações, documentos, entregáveis, estado das execuções e pendências. Exemplo: retomar manutenção predial após um mês, saber o que foi produzido e próximos passos. Vários clientes e trabalhos em estados distintos.

## Seis tipos de memória
- Conversacional: conversas, direcionamentos, preferências.
- Cliente: histórico, contexto e relacionamento.
- Oportunidade/projeto: discovery, requisitos, proposta, aprovações, entregáveis.
- Organizacional: metodologias, padrões, componentes e modelos de documentos.
- Operacional: agentes acionados, resultados, falhas, pendências.
- Experiencial: lições aprendidas e práticas bem-sucedidas.
Não tratar tudo como repositório indiscriminado. Separar memória de trabalho e persistente; detalhes a definir.

## Conhecimento entre clientes
Direção aprovada: curadoria, generalização, anonimização e autorização antes de reutilizar experiências. Ex.: padrões de problemas de manutenção predial podem enriquecer roteiro de discovery futuro, sem revelar dados, contratos, valores ou documentos de outros clientes. Hipóteses da IA não viram conhecimento validado automaticamente. Memória pode enriquecer missão sem modificar núcleo dos agentes.
Estados sugeridos: hipótese, identificado, confirmado, aprovado, implementado, homologado. Preservar origem, versão, evidência e autoridade da aprovação; não equiparar fala do cliente a aceite formal.

## Modelo híbrido aprovado
Recuperar informações sob demanda e sugerir conhecimento relevante espontaneamente, respeitando escopo e confidencialidade. A inteligência identifica e classifica candidatos à memória; confirmação humana proporcional à natureza e ao impacto. Usuário também pode solicitar registro, correção e revisão.
Não guardar indiscriminadamente tudo que foi debatido. Preservar funcionamento operacional consolidado, requisitos, exceções, decisões e justificativas relevantes, incluindo alternativas descartadas e motivos (ex.: fornecedor descartado por limitação técnica, para evitar recomendação repetida). Reavaliar alternativas caso premissas mudem. Histórico bruto não é memória ativa; retenção e descarte serão definidos posteriormente.
Preferências de apresentação podem ser registradas automaticamente; necessidades mencionadas ficam como identificadas, não aprovadas; regra de negócio exige evidência de confirmação; compromisso comercial exige autorização; lição aprendida é candidata à curadoria organizacional. Não promover hipótese da IA a verdade. Informação confidencial nunca é transferida automaticamente entre clientes.

## Escopos de conhecimento
| Escopo | Conteúdo e isolamento |
|---|---|
| Organização | Metodologias, modelos, boas práticas e componentes autorizados |
| Segmento | Conhecimento generalizado e curado sobre mercado |
| Produto/sistema | Funcionalidades, APIs, limitações e documentação por versão, conforme autorização |
| Cliente | Particularidades, histórico e regras corporativas isoladas |
| Oportunidade | Discovery, hipóteses, proposta e decisões comerciais isoladas |
| Projeto | Requisitos, processos, decisões e entregáveis específicos, isolados inclusive dentro do mesmo cliente |
| Execução | Missões, resultados, falhas, pendências e evidências no contexto autorizado |

Exemplo aprovado: Projeto A e Projeto C do Sistema B podem seguir rumos distintos. Não misturar regras específicas mesmo quando produto e cliente coincidam. Conhecimento técnico compartilhável sobre o sistema é referência, não regra de implantação. Exemplo ERP: aprovação simples versus múltipla, API versus CSV, estoque centralizado versus por unidade, implantação gradual versus integral e treinamento presencial versus remoto.

## Gestão da memória (Memory Manager, nome provisório)
Captura -> extração de fatos, regras, decisões e lições -> classificação por relevância, origem, escopo e confidencialidade -> validação proporcional -> persistência -> recuperação autorizada e relevante -> revisão de contradições, obsolescência e substituições. Aprendizado organizacional não altera prompts ou Skills protegidos e não implica treinamento da LLM.
Versionar regras, origem, data, evidência, status e autoridade de aprovação. Exemplo: RN-001 v1.0 aprovação pelo gerente; v1.1 compras acima de R$ 10 mil requerem diretor adicional. Recuperar versão vigente para execução e anterior para auditoria histórica. Preservação sujeita a política de retenção e exclusão.
 
## Critérios conceituais
- Retomar trabalho sem depender de histórico integral de chat.
- Não recuperar regras de outro projeto como se fossem locais.
- Preservar decisões e razões relevantes, inclusive rejeições.
- Distinguir hipóteses, fatos identificados, confirmados e aprovados.
- Reutilizar conhecimento generalizado autorizado, sem expor informações confidenciais.
- Aplicar versão vigente, mantendo rastreabilidade de mudanças.
- Permitir correção, revisão e controle humano.
 
## Pendências técnicas
Definir armazenamento, recuperação, controle de estado, isolamento verificável, políticas de retenção/exclusão, autorização, curadoria e testes de segurança no detalhamento futuro. Nenhuma escolha de banco, RAG, fornecedor ou infraestrutura foi aprovada neste pilar.
