# Etapa 02 | Especificação funcional em elaboração
24/11/2026. Complementa Discovery oficial v1.0, sem substituir baseline ou iniciar desenvolvimento. Direções aprovadas pelo idealizador nesta discussão; detalhes de interface e identificadores são preliminares.

## Experiência e organização
Chat como entrada prioritária, acesso direto às rotinas, interface adaptativa com painéis retráteis e área de edição de artefatos. Não exigir cadastro de cliente/projeto/workspace para conversa livre. Workspace persistente pode representar oportunidade, projeto, cliente, produto próprio ou atividade interna; cliente e projeto são associações conforme aplicabilidade. Conversa, execução e entregável são entidades distintas. Um entregável pode ter várias conversas e execuções vinculadas ao contexto autorizado. Cinco áreas candidatas: Orquestrador, Espaços de trabalho, Central de execuções, Conhecimento e Administração. Layout final e MVP ainda em discussão.

## Entregáveis e edição
RF-001 a RF-009 (preliminares): edição humana; diff entre versões; interpretação semântica; justificativa seletiva quando relevante e incerta; análise de impacto; autoria e histórico; revalidação proporcional JEV; curadoria de memória; melhoria de agentes/avaliadores. Storytelling e relatórios em visualização interativa, BPMN em editor visual/manual e por chat, propostas HTML/PDF, protótipos e demais formatos conforme visão. Aprovação refere-se à versão efetivamente avaliada; edição não herda selo anterior. Preservar versão aprovada e distinguir versão atual pendente. Não inventar motivo de alteração nem atualizar dependências silenciosamente fora da autorização.

## Continuidade e colaboração
RF-010: retomar workspace com síntese baseada em registros reais, decisões, pendências e acesso aos entregáveis completos, inclusive versões aprovadas.
RF-011: linha horizontal de evolução do trabalho, com eventos reais, responsáveis, versões, estados e links aos artefatos. Não impor sequência fixa. Visão de dependências/paralelismo complementar proposta; distinguir histórico realizado de próximos passos sugeridos.
RF-012: permitir colaboração de diferentes humanos no mesmo workspace, respeitando permissões, escopo, autoria e histórico. Uma pessoa pode acumular funções. Modelo de permissões, conflitos concorrentes e controle de edição a detalhar.
RF-013: intervenção durante execução, avaliar impacto, continuar, ajustar, pausar, cancelar ou replanejar seletivamente; preservar resultados válidos e reavaliar afetados. Estados de execução, qualidade JEV e aceite humano independentes.

## Autonomia e produção manual
RF-014: autonomia adaptativa (alternativa C explicitamente escolhida). Orquestrador identifica competências e entregáveis necessários, executa dentro da missão autorizada, solicita intervenção em decisões relevantes, novos custos, riscos ou mudanças de escopo. Não exigir autorização individual de cada entregável nem interpretar autonomia como autorização ilimitada.
RF-015: usuário pode criar entregável não previsto pelo orquestrador, diretamente no editor (ex. BPMN), solicitar apoio parcial ou delegar produção; vincular ao mesmo workspace e projeto quando existente. Não exigir execução de agente nem projeto formal para criação manual. Registrar origem, autoria, versão e relações. Orquestrador deve reconhecer o artefato, interpretar alterações, avaliar dependências e sugerir continuidade. Aplicar testes e JEV proporcional antes de considerar artefato manual validado internamente (aprovado pelo idealizador em 24/11/2026; edição e rascunho não bloqueados). Não modificar artefato humano sem autorização.
RF-016: importar e incorporar trabalhos existentes é capacidade essencial aprovada pelo idealizador. Permitir associar artefatos externos ao workspace e ao projeto quando existente, inclusive BPMN criado manualmente no Bizagi e não previsto pelo orquestrador. Não presumir sincronização externa automática.

## Cenários de aceite candidatos
- Consultor B acessa workspace de consultor A e abre o documento aprovado completo, se autorizado; distingue JEV de aceite humano.
- Dois profissionais colaboram e cada ação mantém sua autoria, sem duplicar contexto.
- Usuário cria BPMN manualmente mesmo quando dispensado pelo orquestrador; aparece no workspace e histórico, sem criar projeto artificial.
- Orquestrador detecta nova versão de artefato, preserva aprovação anterior e sinaliza impactos; não inventa justificativa nem altera outros documentos sem autorização.
- Plano adaptativo muda durante execução sem reiniciar atividades não afetadas.
- Conversa livre continua possível, e atividades paralelas não são apresentadas como dependência sequencial obrigatória.
## JEV universal e incorporação de entregáveis externos
RF-017 (aprovado): JEV avalia entregáveis independentemente de autoria humana, colaborativa, artificial ou externa. Opcional durante elaboração e sob demanda para apoio; obrigatório para validação interna de entregáveis finalizados. Revalidação proporcional após alteração. Distinguir parecer JEV, aprovação humana e aceite do cliente. Preservar pareceres e evidências; permitir contestação fundamentada, segunda avaliação e exceção autorizada sem converter reprovação técnica em conformidade.
RF-018 (direção funcional): incorporar arquivos mantendo original, origem, autoria e contexto; distinguir importação de cópia, vínculo a fonte externa e atualização de versão. BPMN 2.0 XML (.bpmn) é formato prioritário para intercâmbio com Bizagi; testar importação, edição, exportação e round-trip, incluindo limitações de extensões e layout. Não presumir suporte nativo .bpm ou conversão fiel de qualquer formato. DOCX, PDF, XLSX/CSV, PPTX, HTML, Markdown, transcrições, Drive e GitHub são candidatos a priorização por formato, capacidade de leitura/edição e autorização.
RF-019 (proposta em discussão): identificar fonte oficial, histórico, versão, autoria, estado de sincronização e conflitos; preservar versão aprovada, não sobrescrever automaticamente, permitir recuperar versões anteriores. Atualização externa deve ser comparada antes de incorporação e reavaliação.
O orquestrador interpreta o conteúdo incorporado, identifica regras, lacunas, impactos e possíveis revisões de sua estratégia anterior. Não presumir correção ou aprovação do material importado. Arquivo original preservado; editabilidade depende de formato e ferramentas. Escopo de formatos no MVP e mecanismo de sincronização ainda a definir.
### Aceite candidato
- BPMN externo criado no Bizagi, mesmo não recomendado no plano inicial, é importado, associado ao trabalho, visualizado e interpretado; eventual perda de elementos é sinalizada.
- Entregável manual/importado em rascunho permanece editável; ao solicitar validação interna, passa pelo JEV proporcional; parecer fica vinculado à versão.
- Humano contesta parecer e solicita nova avaliação; histórico original permanece.
- Nova importação não sobrescreve versão aprovada; conflito sinalizado.

## Pendências
Detalhar criação/importação e associação de artefatos, conflitos de edição, permissões, aprovação/aceite e publicação; limites da autonomia, UX e escopo MVP. Nenhuma implementação ou teste realizado.
