# 02 | Os Agentes
Baseline oficial v1.0. Status: aprovado pelo idealizador em 24/11/2026, comunicação híbrida aprovada explicitamente.

## Catálogo e preservação
Agentes representam competências, não apenas nomes ou prompts de personagem. Preservar especialistas existentes, evitando alteração frequente que degrade sua entrega. KAIROS representa PM AI Partner; BPMN Master Architect, SIA e Status Report Executive Architect são referências existentes. Não afirmar que já estão integrados ao novo produto.
Catálogo de capacidades candidatas, não lista definitiva: pesquisa de mercado/soluções, consultoria, discovery/storytelling, BPMN, propostas, KAIROS, status report, arquitetura, UX/UI, prototipação, desenvolvimento, integrações, engenharia de dados, analytics, viabilidade financeira, parametrização, implantação, homologação/QA, segurança, documentação, treinamento e encerramento. JEV é avaliador, não executor/autorizador.

## Contrato conceitual de agente
Identidade, propósito, versão, prompt mestre, Skills homologadas, conhecimento, ferramentas permitidas, entradas, saídas, critérios de qualidade, permissões, dependências e limites. Três camadas:
- Núcleo protegido: identidade, prompt, Skills, metodologias e regras; orquestrador não altera em execução.
- Contexto variável: cliente, setor, documentos, restrições e decisões autorizadas.
- Missão temporária: objetivo, entregável, prazo, critérios de aceite e limites.
Mudar contexto e missão, não essência. KAIROS atende hospital ou escola sem mudar sua especialidade.

## Reutilização antes de criação
1. Buscar agente existente adequado.
2. Complementar contexto com conhecimento verificável, sem alterar núcleo.
3. Combinar agentes existentes.
4. Constituir excepcionalmente agente temporário se houver lacuna real.
5. Solicitar apoio humano quando conhecimento ou ferramentas forem insuficientes.
Agente temporário é configuração de instância de LLM em execução, não treinamento, publicação de GPT ou criação de servidor MCP. Agent Factory é nome provisório de mecanismo interno, não decisão de implementação. Composição pode incluir LLM, prompt de missão, Skills reutilizáveis, fontes externas, recuperação documental (RAG), memória autorizada e ferramentas MCP. Título de especialista não prova competência. JEV não garante expertise.
Exemplo: manutenção hospitalar pode exigir conhecimento técnico específico; antes de criar agente, combinar SIA, pesquisa de mercado, BPMN, KAIROS e propostas, fornecendo contexto. Se lacuna persistir, configurar temporário com diagnóstico operacional, pesquisa, análise de riscos, fontes verificáveis, limites e entregáveis claros; validar com JEV e humano competente quando necessário.
Agente composto: combinação/adaptação de contexto e capacidades permitidas sem alterar a versão de produção; conceito de composição ainda a detalhar.

## Evolução controlada
Agente permanente em produção permanece protegido. Sugestão de melhoria -> versão experimental isolada -> testes de qualidade e regressão -> avaliação JEV -> aprovação humana -> publicação versionada ou descarte. Agente temporário recorrente pode ser candidato a permanente após curadoria, documentação, testes e aprovação humana. Não promover automaticamente nem ampliar permissões. Preservar versões anteriores e competência original.

## Autonomia e comunicação híbrida
Modelo aprovado: coordenação centralizada com colaboração descentralizada controlada.
Agentes podem compartilhar resultados, solicitar esclarecimento e revisão entre si dentro da missão autorizada, com rastreabilidade e ciência do orquestrador. Ex.: BPMN identifica lacuna no storytelling e solicita revisão a SIA; ambos registram interação e resultado. Orquestrador mantém responsabilidade pelo plano e consolidação. Mudanças de objetivo, escopo, orçamento, acionamento de novos especialistas ou ampliação de permissões passam por controle central e autorização humana quando aplicável.
Evitar ciclos infinitos, chamadas indiscriminadas, duplicidade e custos fora da missão. Definir limites de interações, tentativas e escalonamento; detalhes técnicos pendentes.
Orquestrador pode selecionar, delegar, contextualizar, combinar, solicitar revisão, sugerir melhoria e constituir temporário sob critérios. Não pode alterar prompts/Skills homologados em produção nem conceder novas permissões. Publicação permanente requer aprovação humana.

## Critérios conceituais (propostos)
- Mesma versão do agente preservada em missões de setores distintos.
- Lacuna é fundamentada antes de criação temporária.
- Comunicação entre agentes registrada e interrompível.
- Revisões não ultrapassam escopo e limites autorizados.
- Versão experimental não afeta produção; regressão avaliada antes de publicar.
- Resultados sem fundamentação ou competência suficiente são escalados.

## Nota de governança da baseline
A aprovação conceitual é do idealizador. A validação técnica e com usuários permanece pendente. Consultar a arquitetura conceitual, matriz de restrições e hipóteses e revisão crítica (docs/08, 09 e 13) para classificação vigente; exemplos não representam implementação.
