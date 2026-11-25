# Requisitos não funcionais, segurança e LGPD | candidatos v0.1
Consolida RNF01–12 do doc/16. Não é parecer jurídico nem declaração de conformidade. Antes de dados pessoais reais, validar com responsável jurídico/privacidade as obrigações aplicáveis, inclusive Lei 13.709/2018. PoC preferencialmente fictícia. Mecanismos técnicos são candidatos.
| RNF | Requisito verificável | Evidência/gate |
|---|---|---|
| 01 | Isolamento organização/contexto e autorização de operações | Testes negativos em API, busca, arquivos, ferramentas; obrigatório PoC/MVP |
| 02 | Identidade, revogação e proteção de segredos | Credencial não aparece em prompt/log/repo; testes de revogação |
| 03 | Conteúdo externo não confiável | Tentativa de induzir ferramenta fora de autorização falha; HTML isolado quando aplicável |
| 04 | Privacidade e retenção | Inventário, finalidade, base legal, papéis controlador/operador, retenção e descarte, atendimento a direitos, revisão de fornecedores/transferências e incidentes; validação especializada antes de dados reais |
| 05 | Recuperação sem repetição indevida | Interrupção simulada, estado recuperado, efeitos incertos conciliados |
| 06 | Limites de consumo | Teste de concorrência e saldo insuficiente; estimado/real separados; não prometer teto externo exato |
| 07 | Desempenho | Medir latência p50/p95, primeira resposta, espera e tempo de missão; metas após baseline |
| 08 | Disponibilidade e recuperação de dados | Definir SLO, RPO/RTO antes de produção, restaurar backup em ambiente isolado |
| 09 | Auditoria | Autor, data, contexto, versão, ação e autorização recuperáveis, acesso restrito |
| 10 | Usabilidade e acessibilidade | Jornada testada com usuários, teclado, foco, responsividade, erro e ajuda |
| 11 | Portabilidade | Exportação autorizada com versão/metadados, interoperabilidade BPMN testada |
| 12 | Observabilidade | Correlacionar missão/execução/modelo/consumo/falha/resultado, sem segredos |
## Política de dados a decidir
Quais transcrições e documentos são permitidos; quais categorias de dados podem chegar a cada fornecedor; contratos, configurações de uso/retenção, acesso e eliminação; anonimização efetiva antes de reutilização organizacional; procedimento para solicitações de titulares, incidentes e backups. Repositório público não é armazenamento de dados reais. Minimizar dados e não confundir histórico preservado com retenção infinita. Não publicar prompts proprietários/credenciais. Nenhuma auditoria jurídica ou técnica executada.
