# Fábrica de Negócios | Orquestrador inteligente

**Baseline oficial de Discovery v1.0 · 24/11/2026 · Discovery do produto**

Nome comercial ainda não definido. Fábrica de Negócios é a categoria e o nome de trabalho.

## Propósito
Transformar ideias, oportunidades, problemas e necessidades em entregáveis úteis, soluções viáveis e resultados validados, através de uma inteligência consultiva que coordena agentes especializados sob direcionamento humano. Gerar valor antes da contratação e continuar útil após o encerramento. Não é uma fábrica de software nem um sistema de gestão de projetos, e não exige um projeto formal para funcionar.

## Documentação viva
- [Visão, escopo e cenários](docs/00-visao-e-cenarios.md)
- [Pilar 01 - Orquestrador](docs/01-orquestrador.md)
- [Pilar 02 - Agentes](docs/02-agentes.md)
- [Pilar 03 - Memória](docs/03-memoria.md)
- [Pilares 04 e 05 - engenharia e qualidade](docs/04-05-engenharia-e-qualidade.md)
- [Registro de decisões e pendências](docs/decisoes.md)

## Revisão crítica e especificação
- [Problema, personas e objetivos](docs/06-problema-personas-objetivos.md)
- [Indicadores de sucesso](docs/07-indicadores-de-sucesso.md)
- [Arquitetura conceitual](docs/08-arquitetura-conceitual.md)
- [Restrições e hipóteses](docs/09-restricoes-e-hipoteses.md)
- [Riscos e não-objetivos](docs/10-riscos-e-nao-objetivos.md)
- [Estratégia PoC e MVP](docs/11-estrategia-poc-mvp.md)
- [Glossário](docs/12-glossario.md)
- [Revisão crítica do Discovery](docs/13-revisao-discovery.md)
- [Casos de teste de negócio](docs/14-casos-de-teste-conceituais.md)

## Etapa 02 – Especificação funcional em elaboração
- [Workspace colaborativo, entregáveis e autonomia](docs/15-especificacao-funcional-workspace.md)
- [Auditoria da especificação funcional e roteiro para revisão independente (25/11/2026)](docs/16-auditoria-especificacao-funcional.md)

**Situação da etapa 02:** auditoria interna e segunda revisão externa registradas; consolidação candidata v0.1 publicada. 76 RF preservados, sem expansão de escopo. Priorização, permissões, estados e critérios aguardam decisões do idealizador e validação com usuários. Discovery v1.0 permanece preservado; doc/15 é histórico da discussão.

- [17 matriz requisitos funcionais](docs/17-matriz-requisitos-funcionais.md)
- [18 delimitacao poc mvp](docs/18-delimitacao-poc-mvp.md)
- [19 jornadas usuarios](docs/19-jornadas-usuarios.md)
- [20 modelo conceitual entidades](docs/20-modelo-conceitual-entidades.md)
- [21 permissoes responsabilidades](docs/21-permissoes-responsabilidades.md)
- [22 estados transicoes](docs/22-estados-transicoes.md)
- [23 requisitos nao funcionais lgpd](docs/23-requisitos-nao-funcionais-lgpd.md)
- [24 rastreabilidade aceite](docs/24-rastreabilidade-aceite.md)
- [25 validacao com usuarios](docs/25-validacao-com-usuarios.md)
- [26 backlog evolucao](docs/26-backlog-evolucao.md)

## Estado do trabalho
| Pilar | Estado |
|---|---|
| 01 Orquestrador | Aprovado pelo idealizador |
| 02 Agentes | Aprovado pelo idealizador |
| 03 Memória | Aprovado pelo idealizador |
| 04 Engenharia agêntica | Aprovado pelo idealizador; D28 não bloqueante |
| 05 Qualidade | Aprovado pelo idealizador |

Esta versão oficial foi autorizada pelo idealizador após revisão externa da documentação. Não equivale a validação com usuários, PoC técnica, homologação ou funcionalidades implementadas. Exemplos são ilustrativos. A matriz de restrições e hipóteses distingue requisitos, serviços definidos, preferências e candidatos técnicos; não há stack definitiva. Uma mesma pessoa pode exercer várias funções. Próxima etapa: especificação funcional; validar hipóteses de problema/personas, priorizar MVP e realizar validações técnica e operacional. Não iniciar desenvolvimento com base somente neste registro.

## Limites
O orquestrador é independente do Commander. Commander pode ser utilizado para controle de um projeto, sem assumir que todo trabalho será encaminhado a ele ou que a Fábrica termine na prototipação. Access Management Service e integração entre produtos não são escopo desta discussão. O produto pode atuar em desenvolvimento, implantação de sistemas de mercado, consultoria, dados, processos e outras demandas, sem esteira fixa.

O repositório é público na data deste registro. Não incluir credenciais, dados reais de clientes, transcrições confidenciais ou prompts proprietários completos sem revisão de exposição.
