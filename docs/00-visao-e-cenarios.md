# 00 | Visão e cenários
Baseline oficial v1.0, 24/11/2026. Fonte: debate de concepção do produto.

## Visão
Uma plataforma independente de inteligência consultiva e engenharia agêntica para identificar, estruturar, viabilizar, executar e validar negócios, projetos e soluções. A engenharia é o meio; a geração de valor é a finalidade. Não confundir com fábrica de software ou pipeline industrial rígido.

## Origem
O debate partiu de quatro GPTs personalizados reconhecidos pelo usuário: BPMN Master Architect, Status Report Executive Architect, Storyboard Intelligence Architect (SIA) e PM AI Partner. PM AI Partner = KAIROS para esta iniciativa; o usuário considera KAIROS mais eficiente. Não duplicar essa especialidade. KAIROS no Commander possui core e 23 Skills registradas; a inspeção do prompt e roteador confirmou seleção por Regex, até cinco Skills por mensagem e fallback de diagnóstico. Isso é referência de experiência, não requisito de replicação. Configurações atuais dos GPTs não foram inspecionadas. JEV (Jury of Expert Validators) foi identificado como avaliador consultivo no core, sem comprovação de sua execução completa. MCP foi introduzido como protocolo de acesso a ferramentas, dados e serviços; não é o próprio motor de decisão.

## Modos de uso
- Conversar, consultar, debater e questionar, sem executar atividades.
- Preparar abordagem comercial, inclusive antes de uma reunião: pesquisa autorizada, hipóteses, roteiro de discovery, apresentação consultiva, questionário de maturidade.
- Delegar uma atividade pontual, por exemplo um BPMN, sem criar projeto.
- Delegar um conjunto de entregáveis, por exemplo storytelling, diagnóstico e proposta.
- Coordenar um ciclo completo ou parte dele, acompanhar aprovações, retomar trabalho interrompido e validar resultados.
- Pós-projeto: avaliação de resultados, lições e novas oportunidades.

O chat é a interface prioritária; workspace de documentos, decisões, aprovações e execuções é uma proposta de experiência ainda a detalhar. A ferramenta deve distinguir opinião, plano e autorização de execução.

## Ciclo possível, não obrigatório
1. Pré-venda consultiva: investigar contexto público, estruturar hipóteses e abordagem.
2. Discovery: reunião, transcrição, documentos; SIA estrutura necessidades, problemas, objetivos, restrições e lacunas. Cliente valida entendimento antes de tratá-lo como aprovado.
3. Pré-projeto: avaliar alternativas, viabilidade e proposta técnica/comercial; processos preliminares se pertinentes. Aprovação comercial pode iniciar projeto, exigir revisão, ficar pendente ou encerrar oportunidade. Preservar registro mesmo sem contratação.
4. Projeto: kick-off, plano e agentes conforme objetivo contratado; protótipo mockado, implantação, consultoria, desenvolvimento ou outros caminhos conforme caso. Protótipo deve seguir padrões de componentes e fluxos aplicáveis; aprovação antes de assumir direção definitiva.
5. Homologação: testes técnicos e funcionais, evidências, correções e retestes. Não prometer ausência absoluta de erros; buscar ausência de defeitos conhecidos impeditivos e atendimento aos critérios acordados.
6. Documentação e aceite: evidências, documentação operacional/técnica e aceite humano; termo de encerramento e transferência de conhecimento.
7. Pós-projeto: resultados e oportunidades futuras.

O fluxo pode voltar etapas, executar tarefas simultâneas e alterar o plano com controle de impacto. Status Report é transversal quando aplicável. JEV pode avaliar entregáveis ao longo de todo o trabalho, não substitui aceite.

## Cenários debatidos
### Sistema de eventos
Reunião -> storytelling -> aprovação do entendimento -> proposta e BPMN se aplicável -> aprovação comercial -> kick-off -> protótipo navegável mockado -> validação -> desenvolvimento -> QA -> documentação -> aceite -> encerramento. Exemplo de rastreabilidade: cliente pede limite de vagas; requisito de capacidade, gateway de disponibilidade, escopo, US, tela, regra de concorrência, testes de lotação e evidência de aceite derivam da necessidade original.
### Painel de gestão educacional
Discovery pode demandar indicadores educacionais/financeiros, fontes de dados, integração, modelagem, dashboard demonstrativo, validação dos dados, parametrização, treinamento. BPMN ou desenvolvimento de aplicação podem ser dispensados. Antes da reunião, preparar perguntas sobre maturidade, sistemas e indicadores; depois comparar hipóteses com fatos da transcrição.
### Manutenção predial
Avaliar preventivas/corretivas, chamados, ativos, prestadores, custos, alertas. Comparar soluções de mercado, construção própria e híbrida; inclusive reorganização de processos e ferramentas existentes. Avaliar aderência, custo total, prazo, autonomia, dependência, risco, capacidade operacional. Consultor e cliente decidem. Implantação pode exigir parametrização, migração e treinamento; desenvolvimento pode exigir arquitetura, UX, código e testes.
### Consultoria, implantação e outros
Diagnóstico, recomendações e plano de ação podem constituir a entrega final. Integrações, dados/analytics, auditoria, governança, sustentação, estudos de viabilidade e gestão de processos também são modalidades possíveis. Um trabalho pode combinar várias delas; não classificar obrigatoriamente em um único tipo.

## Fronteiras
Não pressupor que a fábrica termina em prototipação. Commander é uma ferramenta de controle de projetos quando pertinente, não requisito para o orquestrador. Não presumir liberação de acesso ou integração com Access Management Service. Não definir arquitetura de integração, comercialização ou stack agora. Nome comercial em aberto.

## Nota de governança da baseline
A aprovação conceitual é do idealizador. A validação técnica e com usuários permanece pendente. Consultar a arquitetura conceitual, matriz de restrições e hipóteses e revisão crítica (docs/08, 09 e 13) para classificação vigente; exemplos não representam implementação.
