# 04 e 05 | Engenharia agêntica e qualidade
Baseline oficial v1.0, 24/11/2026. Pilares 04 e 05 aprovados pelo idealizador; validações operacional e técnica pendentes. D28 é hipótese técnica não bloqueante. Decisões não equivalem a implementação.

## 04 Engenharia agêntica
LLM interpreta; prompts estabelecem comportamento; Skills descrevem métodos; agentes têm missão, recursos e limites; memória fornece contexto e estado; MCP padroniza conectividade; orquestrador planeja e controla execução. Separar capacidade cognitiva da execução efetiva. LLM Gateway, Memory Manager, Agent Registry, Skills Registry, Agent Factory, motor de execução e JEV são responsabilidades conceituais, não microsserviços obrigatórios.

### Organização e padrões
Começar exclusivamente pela Consult Services; 7Consulting é expansão posterior por configuração de identidade, referências, conexões e padrões, sem duplicar especialistas. Biblioteca versionada no GitHub de componentes (CMOURASIGA/componentes_consult_services): componentes React, UX/UI, templates de propostas, Discovery, BPMN, Status Report, kick-off, documentação, homologação e encerramento. Utilização obrigatória dos padrões aplicáveis. Não modificar agentes para adaptar identidade de empresa.

### Modelos e benchmark
OpenAI como fornecedor inicial; preparar abstração Multi-LLM e outros fornecedores. Perfis estratégico, operacional e utilitário; selecionar por missão, complexidade, qualidade, custo, latência e modelos homologados. Não presumir que desenvolvimento sempre usa modelo menor. Trocas de modelo em agente homologado exigem validação. Epoch AI (https://epoch.ai/benchmarks) como referência externa, testes internos representativos como referência decisória. Medir custo total por entregável aprovado incluindo retrabalho, qualidade, aderência a componentes e tempo. Usuário vê custo/tempo/qualidade quando disponíveis; administrador vê comparação, consumo e taxa de aprovação. Preferências econômico/equilibrado/qualidade são propostas de interface, sem relaxar critérios obrigatórios. Números simulados não são medições.
Candidatos a avaliar, sem escolha definitiva: OpenAI Agents SDK (Python/JS), Vercel AI SDK, AI Gateway, LangGraph, LiteLLM. Evitar sobreposição; validar licenças, segurança, persistência e integração.

### Condições comerciais
Agente estrutura escopo e estima esforço, mas aguarda condições definidas/autorizadas pelo humano: valores, margem, licenciamento, assinatura, implantação, suporte, pagamento, validade, itens incluídos e não aplicáveis. Antecipar perguntas a partir de padrões autorizados; não copiar condições de outro cliente automaticamente. Não assumir compromisso ou enviar proposta final sem autorização. A espera não ocupa capacidade ativa.

### Entregáveis
| Entregável | Direção |
|---|---|
| Status Report | HTML interativo e PDF paginado para impressão |
| Proposta comercial | HTML interativo e PDF paginado para impressão |
| Discovery/storytelling | HTML interativo e PDF paginado para impressão |
| BPMN | Editor visual e conversacional, mesmo documento versionado; exportar BPMN 2.0 XML (.bpmn), SVG e PDF conforme necessidade; testar importação Bizagi |
| Protótipo | Aplicação navegável, GitHub e ambiente local; abrir após testes; ajustes por chat, sincronização e nova validação |
| Homologação | Painel de testes e evidências, relatório HTML/PDF; não confundir com aceite do cliente |
| Kick-off | Apresentação HTML interativa e PDF para impressão |
| Encerramento | Documento formal conforme template, PDF |
HTML e PDF derivados da mesma fonte estruturada e versão. PDF com margens, paginação, cabeçalhos e identidade apropriados. Editor bpmn-js (https://github.com/bpmn-io/bpmn-js) demonstrado e aprovado pelo usuário como referência de experiência; compatibilidade prática com Bizagi ainda não testada. Permitir edição manual e por chat, validar consistência e salvar versões.

### Ferramentas e execução real
Combinar ferramentas nativas (documentos, diagramas, relatórios), MCP/APIs/CLI e ambientes isolados. Não depender de plugins ChatGPT: serviços externos precisam de autenticação autorizada, custos e limites próprios. Central de conexões para cadastrar/configurar ferramentas e servidores MCP, permissões por agente e organização, sem integração obrigatória com Access Management Service. OpenAI, GitHub, Supabase, Google Drive, Vercel e executor local são direções iniciais; Figma opcional. Pesquisa web conforme necessidade. Banco da fábrica não impõe banco aos projetos.
Executor local instalado e autenticado, com pasta raiz configurável inicialmente C:\Projetos. Verificar pré-requisitos e estado do Git; criar pasta exclusiva, não sobrescrever trabalho existente; obter padrões, produzir código, compilar/testar, iniciar aplicação local e abrir para validação. Ajustes por chat, testes, commits autorizados e sincronização sem conflito; alternativa local-first ou remoto-first conforme missão. Publicação Vercel apenas quando autorizada. Modos local/remoto/híbrido. Máquina precisa estar disponível; se indisponível, pausar ou redirecionar mediante autorização. Restringir diretórios, comandos e credenciais; impedir ações destrutivas ou privilegiadas não autorizadas. Executor e compatibilidade ainda não implementados/testados.

### Memória e armazenamento
Google Drive como fonte documental, com pasta raiz previamente configurada e criação adaptativa de clientes, oportunidades e projetos, evitando duplicidade e registrando IDs. Supabase para persistência de memória, estados, decisões, filas, índices e relações; GitHub para código, prompts, Skills, padrões e templates. Proposta recomendada: conhecimento em Markdown armazenado centralmente no Supabase, com metadados, versão, origem, escopo, autorização e recuperação seletiva; pgvector é candidato para busca semântica com isolamento verificado. Obsidian opcional para visualizar/exportar vault Markdown; não tornar runtime dependente do aplicativo, nem criar múltiplas fontes oficiais. Interface de conhecimento inspirada em Obsidian e sincronização bidirecional são possibilidades posteriores, não requisitos aprovados. Escolha final do mecanismo Markdown/Obsidian é hipótese técnica não bloqueante, a avaliar na arquitetura. Não publicar memória confidencial em repositório público.
Google Drive: criar apenas pastas necessárias sob raiz autorizada, por exemplo Clientes/Cliente A/Projeto A/Discovery, Proposta, Processos, Kick-off, Entregáveis, Homologação, Encerramento. Não criar pastas vazias por fluxo fixo.

### Execução híbrida e performance
Modelo híbrido aprovado: chat responsivo para consultas rápidas e trabalhos extensos assíncronos com estado persistente e central de acompanhamento. Permitir acompanhar resultados intermediários, pausar, cancelar, redirecionar e aprovar. Controlar filas, prioridades, concorrência por recurso/organização, limites de APIs, orçamento, tokens, CPU/RAM local, dependências, recuperação após interrupção. Espera humana libera capacidade ativa. Evitar concorrência no mesmo projeto/arquivo e misturar contextos. Limites reais dependem de testes; não prometer performance sem medição. Avaliar workflows persistentes existentes. 
### Pendências técnicas
Selecionar SDK/framework, modelos e versões, autenticação, arquitetura de execução e fila, mecanismo de memória, esquemas, testes de concorrência, segurança, Bizagi e executor local. Não iniciar desenvolvimento nesta baseline.

## 05 Qualidade, JEV e homologação
Status: aprovado pelo idealizador em 24/11/2026; validações técnica e com usuários pendentes. JEV obrigatório para entregáveis produzidos pelos agentes; composição e profundidade adaptativas. Conversas simples não exigem júri completo. JEV (Jury of Expert Validators) avalia criticamente, não autoriza execução, não substitui testes objetivos nem aceite humano.

### Três níveis de validação
1. Objetiva: estrutura, sintaxe, renderização, testes técnicos/funcionais, regras, componentes e formatos.
2. JEV: avaliação independente do produtor, com critérios específicos da especialidade, evidências e parecer.
3. Humana: decisões comerciais, confirmação de expectativas, aprovação e aceite conforme aplicabilidade.
Não prometer ausência absoluta de erros. Não declarar homologação sem evidências. Defeito impeditivo não pode ser compensado por nota média elevada.

### Dimensões e composição dinâmica
Dimensões aplicáveis: conceitual, técnica, visual, funcional, padronização e integridade. Segurança e confidencialidade também devem ser verificadas conforme risco. Catálogo de competências: negócios, técnico, funcional, visual, documental, comercial, segurança e integridade. Selecionar um ou vários avaliadores segundo complexidade, risco e natureza; evitar mobilização desnecessária. Independência por instância, contexto e responsabilidade; modelos distintos não são obrigatórios, e instâncias separadas não eliminam vieses correlacionados.
Exemplos: BPMN (negócio, técnica, visual, integridade); proposta (negócio, comercial, documental, visual, integridade); protótipo (negócio, técnica, funcional, visual, segurança, integridade); Status Report (negócio, visual, documental, integridade); encerramento (negócio, documental, integridade). Combinações ilustrativas, não regras rígidas.

### Avaliar o artefato real
BPMN: validar XML e renderização, raias, legibilidade, conexões, sobreposições, semântica e regras. Exemplo motivador do usuário: fluxo correto mas desconfigurado deve ser reprovado. HTML: navegador, navegação, interatividade, dados e visual. PDF: renderizar todas as páginas, margens, paginação, cortes, tabelas, legibilidade. Protótipo: executar e navegar, testar botões e operações, aderência aos componentes. Código: compilação, testes, segurança aplicável. Discovery: fidelidade à conversa, separar hipótese de fato. Proposta: escopo e condições autorizadas. Status Report: indicadores consistentes. Kick-off: alinhamento ao escopo. Encerramento: entregáveis, evidências e aceite.
Ferramentas candidatas: navegador automatizado, screenshots, renderizador PDF, validador BPMN, executor de testes, consulta aos componentes e memória autorizada. Se não puder acessar ou executar artefato, marcar validação bloqueada, não aprovar por presunção.

### Ciclo de avaliação e correção
Orquestrador estabelece missão e critérios -> agente produz -> testes objetivos e JEV -> parecer aprovado/reprovado/bloqueado -> correção e nova avaliação quando autorizadas -> entrega validada internamente -> validação humana quando aplicável.
Agente produtor não aprova a própria entrega. Avaliador recebe objetivo, requisitos, critérios, artefato e evidências. Registrar achados, severidade, evidências, versão avaliada e direcionamento. Limitar tentativas, tempo e custo; escalonar se não resolver. Correção dentro da missão pode ser automática. Não apresentar reprovado ou bloqueado como homologado. Homologador técnico/funcional deve ser independente do desenvolvedor quando possível; resultados de testes reais, evidências, correções e retestes em HTML/PDF; aceite do cliente separado.

### Critérios versionados
Manter critérios por especialidade, independentes dos prompts produtores, em padrões versionados no GitHub. Exemplo ilustrativo: quality/bpmn/criteria.md, quality/status-report/criteria.md, quality/commercial-proposal/criteria.md, quality/prototype/criteria.md. Avaliar mudança em versão experimental, testes/regressão, aprovação humana e publicação controlada. Notas, escalas, pesos e limiares ainda a definir; não tratar exemplos simulados como métricas reais.

### Feedback e melhoria contínua
Usuário confirmou melhoria contínua como princípio permanente. Produzir -> validar -> receber feedback -> aprender -> melhorar. Feedback identifica deficiência não capturada pelo JEV, necessidade contextual, preferência ou oportunidade de melhoria. Registrar conhecimento relevante com escopo, evidência e origem; não transformar preferência de um cliente em padrão global automaticamente. Avaliar causa: orquestração, agente, memória, engenharia, componentes/templates ou qualidade. Corrigir entregável e revalidar; propor mudança permanente quando pertinente, submetida a testes e aprovação humana. Ausência de feedback negativo é sinal possível de satisfação, não prova de qualidade; manter avaliação preventiva. Não alterar automaticamente prompts, Skills ou critérios homologados. Preservar versões e rastreabilidade.

### Pendências de especificação
Definir rubricas, severidades, condições de bloqueio, limites de correção, critérios automatizáveis, ferramentas, evidências e métricas reais. Validar arquitetura e desempenho antes de implementar. Nenhuma ferramenta ou modelo específico de JEV selecionado.

## Nota de governança da baseline
A aprovação conceitual é do idealizador. A validação técnica e com usuários permanece pendente. Consultar a arquitetura conceitual, matriz de restrições e hipóteses e revisão crítica (docs/08, 09 e 13) para classificação vigente; exemplos não representam implementação.
