# Arquitetura conceitual | v1.0
Cinco pilares são estrutura histórica de discovery, não cinco módulos ou microsserviços obrigatórios.
## Núcleo
Orquestrador: intenção, plano adaptativo, seleção de especialistas, supervisão, intervenção e consolidação.
Agentes: catálogo, identidade protegida, contexto/missão variáveis, colaboração híbrida e criação temporária excepcional.
Memória: curadoria híbrida, contexto isolado, recuperação seletiva, origem, versão e status.
## Capacidades transversais
| Capacidade | Responsabilidade |
|---|---|
| Inteligência | Abstração de modelos, seleção homologada e consumo |
| Conectividade | Ferramentas nativas, MCP, APIs, CLI, permissões |
| Execução | Estados, dependências, filas, concorrência, pausa, retomada e cancelamento |
| Entregáveis | Produção, edição, renderização, exportação e versionamento |
| Padrões | Componentes, templates e critérios da organização |
| Armazenamento | Dados operacionais, conhecimento, documentação e ativos técnicos |
| Qualidade | Testes objetivos, JEV independente obrigatório para entregáveis, júri adaptativo, evidências |
| Governança | Autorização humana, isolamento, auditoria, segurança, melhoria controlada |
## Fluxo conceitual
Usuário -> orquestrador -> recuperar contexto autorizado -> planejar ou responder -> selecionar competências -> executar com ferramentas -> verificar artefato real -> JEV -> corrigir/revalidar ou escalar -> entrega -> feedback e curadoria. Etapas não aplicáveis são omitidas; espera humana persiste estado sem ocupar execução ativa. Não é pipeline rígido.
## Limites
Não define stack, topologia, API, esquema ou modelo específico. A arquitetura técnica deve demonstrar viabilidade e tratar custo, latência e falhas. Código determinístico preferível para verificações objetivas. Ver docs/09-restricoes-e-hipoteses.md.
