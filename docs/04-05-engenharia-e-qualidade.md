# 04 e 05 | Engenharia agêntica e qualidade
Baseline v0.3, 24/11/2026. Pilar 04 consolidado conceitualmente; pilar 05 em aberto. Decisões não equivalem a implementação.

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
Google Drive como fonte documental, com pasta raiz previamente configurada e criação adaptativa de clientes, oportunidades e projetos, evitando duplicidade e registrando IDs. Supabase para persistência de memória, estados, decisões, filas, índices e relações; GitHub para código, prompts, Skills, padrões e templates. Proposta recomendada: conhecimento em Markdown armazenado centralmente no Supabase, com metadados, versão, origem, escopo, autorização e recuperação seletiva; pgvector é candidato para busca semântica com isolamento verificado. Obsidian opcional para visualizar/exportar vault Markdown; não tornar runtime dependente do aplicativo, nem criar múltiplas fontes oficiais. Interface de conhecimento inspirada em Obsidian e sincronização bidirecional são possibilidades posteriores, não requisitos aprovados. Escolha final do mecanismo Markdown/Obsidian ainda sujeita à confirmação do usuário. Não publicar memória confidencial em repositório público.
Google Drive: criar apenas pastas necessárias sob raiz autorizada, por exemplo Clientes/Cliente A/Projeto A/Discovery, Proposta, Processos, Kick-off, Entregáveis, Homologação, Encerramento. Não criar pastas vazias por fluxo fixo.

### Execução híbrida e performance
Modelo híbrido aprovado: chat responsivo para consultas rápidas e trabalhos extensos assíncronos com estado persistente e central de acompanhamento. Permitir acompanhar resultados intermediários, pausar, cancelar, redirecionar e aprovar. Controlar filas, prioridades, concorrência por recurso/organização, limites de APIs, orçamento, tokens, CPU/RAM local, dependências, recuperação após interrupção. Espera humana libera capacidade ativa. Evitar concorrência no mesmo projeto/arquivo e misturar contextos. Limites reais dependem de testes; não prometer performance sem medição. Avaliar workflows persistentes existentes. 
### Pendências técnicas
Selecionar SDK/framework, modelos e versões, autenticação, arquitetura de execução e fila, mecanismo de memória, esquemas, testes de concorrência, segurança, Bizagi e executor local. Não iniciar desenvolvimento nesta baseline.

## 05 Qualidade
JEV (Jury of Expert Validators) avalia criticamente entregas, premissas, fundamentação, consistência, aderência e qualidade; não autoriza execução nem comprova persistência. Pode atuar em diferentes etapas, incluindo avaliação de propostas e alternativas, agentes temporários e mudanças de versão. Não confundir JEV com QA: homologação técnica/funcional executa testes, registra evidências, identifica defeitos e exige retestes; independência desejável entre desenvolvedor e homologador. Não prometer zero erros absolutos. Aprovação humana e aceite do cliente permanecem distintos da avaliação por IA. Definir critérios, métricas, evidências, avaliação de regressão e escalonamento no pilar 05. Nenhuma ferramenta de avaliação escolhida.
