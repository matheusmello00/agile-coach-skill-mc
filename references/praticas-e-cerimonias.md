# Práticas e Cerimónias
 
Referência completa das práticas ágeis e cerimónias utilizadas na stream, com metodologia, owners, participantes, duração e boas práticas.
 
---
 
## Cadência de Cerimónias — Sprint de 2 Semanas
 
| Cerimónia | Frequência | Duração | Owner/Interlocutor |
|---|---|---|---|
| Sprint Planning | Quinzenal (2ª feira, 1ª semana do sprint) | 1h | Product Manager |
| Daily Scrum | Diário (exceto fins de semana) | 15min | DEV Team (rodízio) |
| Functional Refinement | Quinzenal (2ª feira, 2ª semana do sprint) | 1h | Product Manager |
| Technical Refinement | Quinzenal (ter/qua/qui/sex, 2ª semana do sprint) | 4x 30min | Tech Lead |
| Sprint Review | Quinzenal (2ª semana do sprint) | 1h | Product Manager |
| Sprint Retrospective | Quinzenal (2ª semana do sprint) | 1h | DEV Team (rodízio) c/ apoio do SAC |
| Passagem de conhecimento p/ Suporte + Changes | Semanal ou Adhoc | 1h30min | Tech Lead |
| Passagem de conhecimento de Iniciativas (Projetos) | Sob Demanda | Mínimo 1h | Product Manager |
 
---
 
## Cerimónias — Detalhe
 
### Sprint Planning
 
**Owner:** Product Manager
**Participantes obrigatórios:** PM e DEV Team
**Participantes opcionais:** Tech Lead
 
**Metodologia:** Sessão de 1h onde o PM e o DEV Team constroem o Sprint Backlog. Deve-se finalizar o sprint anterior para criar o novo, e o acceptance do sprint deve ser feito por todo o DEV Team.
 
**Nota:** Os cartões não completados no sprint anterior devem ser movidos para o backlog, e somente depois movidos para o novo sprint, consoante avaliação do PM com os developers.
 
**Objetivo:** Montar o Sprint Backlog, construir os objetivos do Sprint Goal e seus incrementos.
 
**Estrutura recomendada:**
1. Contexto e Sprint Goal (15 min) — PM apresenta o objetivo; equipa alinha
2. Seleção de itens (30 min) — equipa puxa itens com base na velocity e capacidade real
3. Discussão de carry overs — separar momento específico para discutir itens carregados
4. Confirmação do Goal e comprometimento (15 min)
**Sinais de planning saudável:** Sprint Goal definido antes de selecionar itens; equipa questiona e negoceia escopo; capacidade real (férias, feriados, alocações) considerada.
 
---
 
### Daily Scrum
 
**Owner:** DEV Team (rodízio)
**Participantes obrigatórios:** DEV Team, PM e TL
 
**Metodologia:** Sessão de 15 minutos onde o DEV Team inspeciona o Sprint Progress com o board aberto. A partir disso, identifica o que falta para fechar e se existe algum bloqueio — preferencialmente do item mais próximo de "Done" para o menos próximo, sempre a respeitar as raias de prioridade.
 
**Nota:** Esta sessão NÃO é um status report, nem para discussões de temas ou inputs de produto. É uma sessão para garantir diariamente que a meta definida não seja comprometida.
 
**Objetivo:** Identificar o progresso e as dificuldades/bloqueios observados, garantindo visibilidade e tempo de reação.
 
**Formato recomendado (evitar o "o que fiz / o que vou fazer"):**
- Foco no Sprint Goal: "Estamos no caminho certo para atingir o goal?"
- Impedimentos: "Há algo a bloquear alguém agora?"
- Colaboração: "Alguém precisa de ajuda para avançar?"
---
 
### Functional Refinement
 
**Owner:** Product Manager
**Participantes obrigatórios:** PM, TL e DEV Team
 
**Metodologia:** Sessão de 1h ou mais (se necessário). É o marco inicial do novo sprint, onde o PM debate com o DEV Team os temas funcionais dos cartões no Board de refinamento. É nesta hora que o DEV Team deve cobrar a escrita funcional dos cartões e os critérios de aceitação, para entender todo o direcionamento do negócio. O PM já pode direcionar quanto às priorizações do próximo sprint.
 
**Nota:** Por ser um trabalho cíclico e contínuo, com o objetivo de facilitar as Plannings, os envolvidos precisam compreender a necessidade de reunir informações funcionais que facilitem a compreensão técnica. O PM consegue ter um termómetro do entendimento do DEV Team sobre as expectativas de entrega.
 
**Objetivo:** Garantir que a construção da coluna Technical Refinement aconteça sem dúvidas e dentro da prioridade orquestrada pelo PM.
 
---
 
### Technical Refinement
 
**Owner:** Tech Lead
**Participantes obrigatórios:** DEV Team e TL
**Participantes opcionais:** PM
 
**Metodologia:** Necessidade de 2h. Esta sessão serve para garantir um planeamento dentro das premissas do Definition of Ready. O TL e todo o DEV Team constroem toda a conceituação técnica dos cartões priorizados no Board de refinamento. Na coluna de Technical Refinement, o DEV Team garante a escrita técnica, informações não funcionais, dependências, e descreve minimamente como o desenvolvimento deverá transcorrer. Foco no que o PM já priorizou e na estimativa para conclusão do cartão sem riscos de transição.
 
**Nota:** Por ser cíclico e contínuo, os envolvidos precisam compreender a necessidade de reunir informações técnicas que facilitem o desenvolvimento e evitem bloqueios por ausência de informações.
 
**Objetivo:** Construir a coluna de Ready Candidate do board de refinamento com cartões documentados funcional e tecnicamente, atendendo os requisitos do Definition of Ready (DoR).
 
---
 
### Sprint Review
 
**Owner:** Product Manager
**Participantes obrigatórios:** PM, DEV Team e TL
**Participantes opcionais:** Suporte e Stakeholders
 
**Metodologia:** Sessão de 1h dividida em três momentos:
1. **15 min** — Inspecionar o Sprint Goal: algum cartão não completado tem impacto sobre a meta?
2. **30 min** — Demonstrações dos incrementos planeados no Planning (e qualquer outro que entrou e foi completado). Não é apresentação de slides — é demonstração de software funcionando.
3. **15 min** — Gestão de expectativas: PM fala sobre os next steps dos próximos sprints.
**Nota:** Foco em revisar o trabalho feito e nas entregas comprometidas em planeamento. NÃO é o momento de falar de processos e melhorias.
 
**Objetivo:** A Review é a sessão em que a equipa apresenta/vende o que foi feito internamente. É fundamental que os Stakeholders estejam presentes para contribuir na adaptação. A apresentação é comandada pelo PM com o DEV Team (de forma rotativa) a demonstrar os incrementos.
 
---
 
### Sprint Retrospective
 
**Owner:** DEV Team (rodízio), com apoio do SAC
**Participantes obrigatórios:** PM, TL, DEV Team e SAC
 
**Metodologia:** Sessão de 1h dividida em três momentos:
1. **15 min** — Inspeção do sprint report: entender comportamentos que levaram aos resultados obtidos.
2. **30 min** — Exercício de melhoria com foco nas relações de trabalho, processos e ferramentas — o que funcionou, o que não funcionou, o que poderia ser melhorado.
3. **15 min** — Definir qual o pain point que será abordado no próximo sprint. O líder desta iniciativa pode ser em rodízio — a cada ciclo um membro do DEV Team responsabiliza-se por acompanhar e resolver o pain point no sprint subsequente.
**Nota:** A Retro é uma sessão de conflitos de pensamentos e perceções, mas também de proporcionar aumento gradativo da sinergia e maturidade da equipa.
 
**Objetivo:** A equipa demonstra as suas dores, receios e anseios. É necessário focar na evolução contínua e nas adaptações — é a hora de saber falar e ouvir.
 
**Formatos alternativos:**
- 4Ls: Liked, Learned, Lacked, Longed for
- Start / Stop / Continue
- Sailboat / Speed Car
- Mad / Sad / Glad
- Timeline da equipa (retros de final de PI ou trimestre)
**Pergunta de encerramento invariável:**
> "Qual é o único experimento que vamos tentar neste sprint? Quem é responsável? Como vamos medir?"
 
---
 
### Passagem de Conhecimento para Suporte + Changes
 
**Owner:** Tech Lead
**Participantes obrigatórios:** TL, DEV Team e Suporte
 
**Metodologia:** Sessão semanal de ~1h30min. O DEV Team (com o TL) realiza a passagem de conhecimento para a equipa de Suporte de tudo que existe de Change criado para entradas em PRD (na semana seguinte) ou algum tema específico que seja necessário antecipar. Podem ocorrer sessões Adhoc em entradas de PRD alinhadas com 48h de antecedência.
 
**Nota:** O DEV Team deve reportar ao TL se tem pauta para a sessão, garantindo que o Suporte esteja disponível.
 
**Objetivo:** Realizar a passagem do que se quer levar para PRD na semana seguinte ou 48h depois. Validar os changes em aprovação.
 
---
 
### Passagem de Conhecimento de Iniciativas/Projetos
 
**Owner:** Product Manager
**Participantes obrigatórios:** PM, TL, DEV Team e Suporte
 
**Metodologia:** Sob demanda, conforme avanço das Iniciativas. Ocorre entre os steps de Piloto e Painel do rollout. Por ser de caráter mais funcional que técnico, PM e TL organizam em conjunto.
 
**Nota:** Sessão formal de handover tem de ter escopo pré-definido e a sessão precisa ser gravada e postada no Confluence para consulta futura.
 
**Objetivo:** Garantir passagem de conhecimento à equipa de Suporte de forma contínua de tudo que foi desenvolvido para a Iniciativa.
 
---
 
## Gestão de Carry Over
 
**O que é:** Item dentro de um sprint que não foi concluído no tempo planeado e precisa ser movido para um sprint seguinte (não necessariamente o próximo).
 
**Objetivo do processo:** Garantir boas práticas, visibilidade, controlo e orientações para lidar com itens não concluídos. A aprendizagem é contínua e melhora a capacidade de entrega.
 
### Como gerir no Jira:
1. **Identificar itens não concluídos** — no final de cada Sprint, o Jira sinaliza automaticamente os itens em aberto no Sprint Report.
2. **Reavaliar a relevância** — rever no próximo Refinement ou Sprint Planning: se perdeu prioridade → volta para o Product Backlog; se ainda é prioritário → mantém-se para o próximo Sprint. Confirmar se há impedimentos ou dependências a resolver.
3. **Replanear com consciência** — mover o item para a nova Sprint apenas se houver capacidade e alinhamento com o Sprint Goal. Documentar o motivo usando comentários ou labels ("prioridade alterada", "reavaliar", "carry over").
### Boas práticas para reduzir carry over:
- Separar momento na Planning para discutir Carry Over.
- Usar padrões recorrentes como input para a Retro.
- Usar ferramentas de análise (ex: Diagrama de Ishikawa) para identificar causas raiz.
- Não sobrecarregar o sprint — capacidade baseada em dados reais.
- Dividir histórias grandes em partes menores e entregáveis.
- Identificar e gerir dependências e bloqueios cedo.
- Rever métricas e causas no Retro e Sprint Review.
### Boas práticas para gerir um carry over:
- Documentar o motivo com comentários ou labels.
- Rever no Refinement, Retro ou Planning seguinte.
- NÃO mover automaticamente sem discussão e visibilidade da equipa.
- Revisar com o PM: o item ainda tem valor?
- Repriorizar no Backlog conforme nova avaliação.
**Nota importante:** NÃO redimensionar os Story Points de um carry over. A "falha" na estimativa precisa acontecer para a equipa discutir o que impediu a conclusão.
 
### Thresholds de alerta:
- Aceitável: ≤10–15% dos pontos do sprint
- A estabilizar: 15–20%
- Alerta: >20–25%
- Crítico: mesmo item carregado por 2+ sprints consecutivos
---
 
## Estimativas
 
### Story Points
Expressam o esforço global para implementar um item do backlog. Refletem complexidade, risco/incerteza, volume de trabalho e dependências. Usamos a **Sequência de Fibonacci** (1, 2, 3, 5, 8, 13...) para facilitar a comparação.
 
### Planning Poker
Técnica ágil de estimativa colaborativa. Cada membro escolhe individualmente e em sigilo uma carta com um valor; todos revelam ao mesmo tempo; discutem-se diferenças; re-estima-se até consenso.
 
### T-Shirt Size Estimation
Categoriza o esforço em tamanhos (S, M, L) em vez de números exatos. Útil em fases iniciais com pouca informação ou para estimativa de alto nível de iniciativas.
 
### INVEST Model
User Stories de qualidade devem ser: **I**ndependent, **N**egotiable, **V**aluable, **E**stimable, **S**mall, **T**estable.
 
---
 
## Priorização
 
### Lógica de Priorização ao Longo do Workflow
 
**Priorização Alto Nível (L1):** feita entre Ideação e Exploração. Considera a Classe de Serviço e o Benefício da Ideia. Realizada via Idea Card no Jira.
 
**Priorização Baixo Nível (L2):** feita entre Exploração e Avaliação. Identifica Tamanho, Esforço, Complexidade e Custo. Ordenação por Classe de Serviço e Value Idea (Score no Idea Card). Deve estar fechada na fase de Avaliação para fornecer todos os elementos para Aprovação.
 
**Priorização de Execução (Sprint/Backlog):** durante Sprint Planning, Refinamento e gestão de fluxo. Métodos: MoSCoW, Story Mapping, T-Shirt Sizing / Planning Poker.
 
### MoSCoW
- **Must Have** (Crítico) — itens essenciais, bloqueadores para a entrega
- **Should Have** (Importante) — relevantes, mas não impedem o progresso imediato
- **Could Have** (Desejável) — melhorias opcionais, sem impacto crítico
- **Won't Have** (Fora de âmbito) — não priorizados nesta fase
---
 
## DevOps e CI/CD
 
### DevOps
Abordagem cultural, metodológica e tecnológica que promove colaboração contínua entre desenvolvimento (Dev) e operações (Ops). Objetivos: acelerar time-to-market, garantir estabilidade, automatizar processos, reduzir silos, fomentar melhoria contínua.
 
**Princípios:** CI (Integração Contínua), CD (Entrega/Deployment Contínuo), IaC (Infraestrutura como Código), Monitorização Contínua, Cultura de colaboração.
 
### CI/CD
- **CI:** commits frequentes → código automaticamente testado e validado → builds geradas automaticamente.
- **CD (Delivery):** código preparado para produção; equipa pode aprovar manualmente o deploy.
- **CD (Deployment):** se os testes forem bem-sucedidos, nova versão lançada automaticamente para produção. Requer mecanismo robusto de rollback.
**Melhores práticas:** automatizar testes, manter pipelines simples, monitorizar e fazer logging, implementar rollback, Security by Design (DevSecOps).
 
---
 
## Road to Production (RTP)
 
Processo estruturado de levar uma aplicação desde o desenvolvimento até à produção.
 
**Etapas:**
1. Desenvolvimento — implementação do código e testes unitários
2. Testes End-to-End (E2E) — validação da integração e funcionamento completo
3. UAT — validação pelo negócio
4. Change Enablement — criação, aprovação e gestão da Change Request (CR)
5. Preparação para Produção — configuração do ambiente, migração de dados, validação final
6. Go Live — implementação em produção
7. Monitorização e Estabilização — acompanhamento da nova versão
---
 
## Rollout — Estabilização Incremental
 
Processo faseado de implementação. Adotamos uma estratégia de estabilização incremental estruturada em 4 fases:
 
| Fase | O que acontece | Objetivo |
|---|---|---|
| **Experimentação** | Feature ativada em número limitado de devices | Validar a jornada completa com segurança; captar pontos de melhoria antecipadamente |
| **Piloto** | Feature ativada para número reduzido de lojas | Testar comportamento em ambiente real; identificar e corrigir primeiros defects |
| **Painel** | ~Dobro das lojas do Piloto | Reforçar estabilização; monitorizar em escala ampliada; corrigir defects residuais. **Aqui ocorre o Handover para a equipa de Suporte** |
| **Full Rollout** | Feature disponível para toda a Operação | Problemas residuais passam a ser tratados pelo Suporte (Operação) |
 
### Gestão de Problems após Full Rollout:
1. Suporte reporta o problem no ITSM
2. Problem é espelhado no board de refinamento da equipa responsável com descrição mínima da causa-raiz
3. Validação funcional e técnica + priorização conjunta (PM, TL, DEV Team)
4. Incluído no sprint corrente e tratado com caráter prioritário
### Feature Toggle (Feature Flag)
Permite ativar/desativar funcionalidades sem alterar o código ou fazer novos deployments. Tipos: Release Toggle, Experiment Toggle, Ops Toggle, Permission Toggle. Usar estratégia de limpeza periódica para evitar acumulação de flags.
 
### Canary Release
Lançamento para subconjunto reduzido de utilizadores/servidores antes de disponibilizar para toda a base. Se estável, expande gradualmente. Se há problemas, reverte rapidamente.
 
---
 
## Calendário de Release e Freezing
 
Planeamento estruturado que define datas de lançamento e períodos de congelamento.
 
**Tipos de Freezing:**
- **Code Freeze** — nenhuma nova funcionalidade; apenas correções de bugs
- **Feature Freeze** — funcionalidades desenvolvidas; podem sofrer ajustes ou testes finais
- **Deployment Freeze** — nenhuma nova versão em produção durante período crítico (ex: Black Friday)
---
 
## Práticas de Operação
 
### Shadowing
Técnica de aprendizagem em que um profissional observa diretamente outro no desempenho das suas funções. Tipos: Observacional, Interativo, Prático (Reverse Shadowing). Aplicações: onboarding, gestão de produto, qualidade e suporte. A sessão formal deve ter objetivos claros e o shadowing deve ser natural, sem pressão para o observado.
 
### Ciclos de Feedback
Em Equipas de Produto, os principais ciclos ocorrem durante: Sprint Planning, Daily, Functional Refinement, Technical Refinement, Sprint Review, Sprint Retrospective, Passagem de Conhecimento (Suporte/Change Enablement), Passagem de Conhecimento (Suporte/Handover).
 
### Painel com o Negócio
Prática colaborativa que reúne representantes das áreas de negócio e das equipas de desenvolvimento com o PM, para alinhar prioridades, esclarecer requisitos e tomar decisões estratégicas sobre produtos, projetos ou iniciativas.
 
### Story Map / User Story Map
Técnica de planeamento e visualização para organizar e priorizar funcionalidades de forma lógica e centrada na experiência do utilizador. Alinha o backlog com a jornada do utilizador e os objetivos do negócio.
 
---
 
## Prompt: Resumo Executivo de Retrospectiva
 
Usar este prompt sempre que o utilizador fornecer uma transcrição de retrospectiva e pedir resumo, síntese ou consolidação. Não alterar a estrutura de output — é o formato canónico acordado para publicação na ferramenta de documentação interna.
 
**Goal:**
Gerar um resumo executivo e acionável a partir da transcrição de retrospectivas da equipa.
 
**Context:**
Estas retrospectivas são realizadas em ambiente ágil (sprints). O objetivo é extrair insights estratégicos e padrões relevantes, evitando detalhes operacionais excessivos, para publicação numa ferramenta de documentação interna.
 
**Source:**
Transcrição de reunião do Microsoft Teams (incluindo comentários informais, diferentes participantes e possíveis redundâncias).
 
**Instructions:**
Analisa a transcrição da retrospectiva e produz um resumo claro, estruturado e orientado a tomada de decisão. Foca-te em identificar padrões, temas recorrentes e impacto geral no desempenho da equipa.
 
**Output format:**
 
1. **Resumo Executivo (máx. 5 bullets)**
   - Principais conclusões da retrospectiva
   - Tendências relevantes da sprint
   - Nível geral de performance da equipa
     
2. **Pontos Positivos (What went well)**
   - Bullet points objetivos
   - Foco em práticas ou comportamentos que devem ser mantidos
     
3. **Pontos de Melhoria (What could be improved)**
   - Bullet points claros e acionáveis
   - Agrupar por tema quando possível (ex: comunicação, processos, tooling)
     
4. **Plano de Ação (Next Sprint Actions)**
   - Lista de ações concretas
   - Sempre que possível incluir:
     - ação
     - objetivo
     - responsável (se identificado na conversa)
     - prazo sugerido
5. **Insights Estratégicos (opcional mas recomendado)**
   - Padrões recorrentes vs retros anteriores
   - Riscos potenciais para próximas sprints
   - Oportunidades de melhoria contínua
     
**Additional Guidelines:**
- Evitar repetir conteúdo redundante da transcrição
- Priorizar clareza e linguagem executiva
- Não incluir informações pessoais desnecessárias
- Resumir discussões longas em insights objetivos
- Se existirem conflitos ou divergências, sintetizar de forma neutra
