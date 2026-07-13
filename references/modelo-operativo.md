# Modelo Operativo

O Modelo Operativo da stream organiza o ciclo de vida das iniciativas em três horizontes temporais — **Later, Next e Now** — que refletem o nível de maturidade e compromisso de cada iniciativa, desde a sua identificação até à entrega e operação contínua.

---

## Leitura sistémica do modelo operativo

O Agile Coach deve usar o modelo operativo para verificar se o sistema de decisão está a apoiar a execução, ou se está a introduzir sobrecarga, ambiguidade e atraso.

### O que observar
- Se Now, Next e Later refletem o contexto real e não apenas a vontade da equipa.
- Se as iniciativas em Now têm capacidade real para avançar sem comprometer qualidade e fluxo.
- Se as dependências e os compromissos de confirmação estão claros antes de se moverem para a frente.
- Se MBR e QBR estão a traduzir sinais de execução em decisões úteis para a stream.

### Anti-patterns frequentes

| Anti-pattern | Sinal | Pergunta de coaching | Experimento |
| --- | --- | --- | --- |
| Muitas iniciativas em Now sem capacidade real | Fluxo congestionado, pouca previsibilidade | O que está a ser comprometido para manter tudo em execução? | Reavaliar prioridade e reduzir o número de iniciativas simultâneas |
| Next sem confirmação ou clareza | Iniciativas a “andar” sem decisão | Que evidência existe para avançar a esta iniciativa? | Reforçar a definição de confirmação e critérios de entrada |
| Dependências mal geridas | Espera, bloqueios recorrentes e baixa previsibilidade | Qual é o ponto de decisão que está a falhar? | Definir responsável, prazo e canal de resolução |
| MBR/QBR sem ligação à execução | Relatórios sem impacto nas decisões | O que mudou porque este relatório foi analisado? | Vincular o review a um conjunto de ações concretas e um follow-up |

---

## Horizontes Temporais (Now / Next / Later / Pending)

O processo é contínuo e on-going: as iniciativas evoluem ao longo do roadmap sem depender de ciclos rígidos de aprovação.

| Horizonte | O que representa                                                               | Estado típico das iniciativas                                                          |
| --------- | ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------- |
| **NOW**   | Iniciativas em execução ativa                                                  | In Progress, Rollout, concluídas no mês (Done), a arrancar no mês seguinte (Committed) |
| **NEXT**  | Iniciativas em exploração ativa ou planeamento com MBR de confirmação definido | Exploration, Planning, Ready to Commit                                                 |
| **LATER** | Iniciativas identificadas sem arranque previsto a curto prazo                  | Draft, Exploration sem MBR de confirmação                                              |
| **PENDING** | Iniciativas em Draft sem exploração activa nem prioridade definida           | Draft                                                                                 |

---

## PENDING

O horizonte **PENDING** agrupa iniciativas em `Draft` que ainda não têm exploração ativa, prioridade definida nem horizonte de arranque.

- Estado Jira: `Draft`
- Sem `Committed Start Date`, `Launch Date` ou `End Date`
- Repositório do roadmap aguardando momento certo
- Não é reportado por defeito no MBR/QBR

---

## Formas de Trabalho Suportadas

O modelo adapta-se à natureza de cada iniciativa:

- **Equipas de Produto** — entrega incremental e contínua de valor, com backlog gerido pelo Product Manager.
- **Equipas de Projeto** — âmbito, prazo e orçamento definidos, coordenados pelo Project Manager.
- **Fluxo Contínuo (Kanban)** — equipas que gerem um volume constante de trabalho sem sprints fixos.

---

## Cultura de Produto e Equipas Autogeridas

A execução do Modelo Operativo pressupõe uma cultura de produto centrada em autonomia responsável e alinhamento colaborativo.

- **Produto como sistema integrado** — o produto é gerido como um fluxo de valor contínuo, não apenas como entregas pontuais.
- **Equipas autogeridas** — assumem responsabilidades sobre qualidade, previsibilidade e comunicação com stakeholders.
- **Transparência e visibilidade** — resultados de métricas e status do roadmap devem ser visíveis para as equipas e para os principais stakeholders.
- **Alinhamento com o Playbook** — o AC deve apoiar a adoção das práticas de produto e dos WS de trabalho locais, sem substituir decisões de negócio.

---

## MBR — Monthly Business Review

**O que é:** Mecanismo mensal de reporte e alinhamento sobre a evolução das iniciativas, adotando a abordagem de Roadmap Contínuo Now/Next/Later. Fórum onde as streams comunicam o estado atual do roadmap e garantem visibilidade aos stakeholders.

**O MBR não substitui o QBR** — complementa-o. O QBR é o momento de alinhamento executivo trimestral com decisão de prioridades; o MBR é o mecanismo de acompanhamento contínuo entre QBRs.

### Para que serve:

- **Visibilidade:** manter os stakeholders informados sobre o estado real das iniciativas.
- **Alinhamento:** garantir que as prioridades do roadmap continuam alinhadas com as necessidades do negócio; identificar e resolver bloqueadores antes que impactem o NOW.
- **Continuidade:** evitar picos de esforço associados ao modelo de reporte apenas trimestral; permitir ajustes de prioridade de forma ágil.

### Como funciona:

| Dimensão          | Detalhe                                                                  |
| ----------------- | ------------------------------------------------------------------------ |
| Cadência          | Mensal — tipicamente no fim do mês                                       |
| Formato principal | Documento estruturado enviado aos stakeholders, organizado por horizonte |
| Reunião           | Facultativa — apenas se existirem temas que exijam discussão estratégica |
| Participantes     | Primeiras linhas dos stakeholders. Não requer envolvimento de Executivos |
| Relação com QBR   | O MBR não se realiza no mês do QBR — o QBR substitui-o                   |

### Estrutura do documento por horizonte:

| Horizonte | O que reportar                                                          | Datas obrigatórias                  |
| --------- | ----------------------------------------------------------------------- | ----------------------------------- |
| NOW       | Iniciativas em execução, concluídas no mês e a arrancar no mês seguinte | Committed Start · Launch · End Date |
| NEXT      | Iniciativas em exploração ativa ou planeamento                          | MBR de confirmação definido         |
| LATER     | Iniciativas identificadas sem arranque previsto                         | Sem promessa de datas               |

### Quem prepara:

- **PM:** prepara e envia o documento; garante que o estado de cada iniciativa no Jira está correto antes do envio.
- **PSL:** revê o documento antes do envio; participa na reunião facultativa se convocada.
- **Stakeholders:** recebem e reveem o documento; participam se temas estratégicos o justificarem.

### O que NÃO vai ao MBR:

Epics, User Stories, Tasks, Bugs, Incidents, CFIs, POs, XRAYs, Minors, Iniciativas em Draft sem atividade de exploração relevante, Itens duplicados entre streams.

---

## MBR de Confirmação

O MBR de Confirmação é um conceito de planeamento usado para indicar quando uma iniciativa em `NEXT` deve ser considerada para avanço a `NOW`.

- É o MBR do mês imediatamente anterior ao `Committed Start Date` previsto.
- Não é um campo do Jira; é um input de governança usado no documento do MBR ou QBR.
- Serve para priorizar o pipeline e preparar os dados do QBR, sem comprometer a iniciativa até a decisão formal.

---

## Rebaseline — Committed Dates

O Rebaseline é o processo formal de atualização das datas comprometidas após o início da execução.

- Pré-compromisso (`Draft/Exploration/Planning`): as datas podem ser atualizadas diretamente; não é Rebaseline.
- Pós-compromisso (`Committed/In Progress/Rollout`): qualquer alteração de `Committed Start Date`, `Launch Date` ou `End Date` segue o processo de Rebaseline do Jira.
- O Jira mantém os valores originais em campos como `First Committed Dates` e incrementa contadores como `Launch/End Rebaseline Count`.
- O campo `Rebaseline Reason` é obrigatório para justificar a alteração.

---

## QBR — Quarterly Business Review

**O que é:** Fórum trimestral de alinhamento executivo das iniciativas estratégicas da stream. É o momento em que se confirmam os compromissos para o próximo horizonte NOW.

### Para que serve:

- **Alinhamento executivo:** garantir visibilidade de prioridades e decisões de investimento.
- **Revisão de prioridades:** validar estado e horizonização de iniciativas em Now/Next/Later.
- **Compromisso formal:** confirmar iniciativas que passarão a NOW no mês seguinte.

### Como funciona:

| Dimensão          | Detalhe                                                          |
| ----------------- | ---------------------------------------------------------------- |
| Cadência          | Trimestral — no último mês do trimestre                          |
| Formato principal | Reunião síncrona ou presencial com documento de suporte          |
| Participantes     | Executivos e stakeholders de primeira linha com poder de decisão |
| Relação com MBR   | Em mês de QBR, o MBR não se realiza                              |

### Estrutura por horizonte temporal:

- **NOW:** Committed, In Progress, Rollout ou Done. Committed Start, Launch e End Date obrigatórias.
- **NEXT:** Exploration, Planning ou Ready to Commit. MBR de confirmação definido; sem datas fixas.
- **LATER:** Draft ou Exploration. QBR tentativo opcional; sem promessa de datas.

### O que NÃO vai ao QBR:

Epics, User Stories, Tasks, Bugs, Incidents, CFIs, POs, XRAYs, Minors, Iniciativas em Draft sem atividade de exploração relevante, Itens duplicados entre streams, detalhes operacionais de execução.

---

## Issue Types no Jira

| Issue Type                 | Função                                                                                                                                  | Aplica-se a                           |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| **Idea**                   | Estágio inicial de uma potencial iniciativa — proposta originada de uma necessidade ou oportunidade identificada                        | Todas as equipas                      |
| **Initiative Aggregator**  | Agrupa iniciativas, por exemplo dentro de um programa                                                                                   | Todas                                 |
| **Initiative**             | Produto/incremento maior que um Epic; sempre entrega valor ao negócio                                                                   | Todas                                 |
| **Dependency**             | Representa dependência entre equipas — entrega, ação ou capacidade necessária de outra equipa                                           | Equipas de Produto (principalmente)   |
| **Epic**                   | Agrupador de Stories; representa grandes partes de trabalho (features ou componentes); habitualmente não é entregue dentro de um Sprint | Todas                                 |
| **Story**                  | Funcionalidade que entrega valor ao utilizador final, por norma numa Sprint; fragmentação de um Epic                                    | Todas                                 |
| **Task**                   | Pequena tarefa para concluir um item                                                                                                    | Todas                                 |
| **Bug**                    | Erro antes da produção, priorizado por criticidade; identificado durante testes/verificação de qualidade                                | Todas                                 |
| **Incident**               | Erro em produção que exige ação da equipa; tem SLA; integrado com ITSM                                                                  | Todas                                 |
| **Problem**                | Reflete em Jira o ticket de Problema registado em ITSM; criado via integração ITSM-Jira                                                 | Todas                                 |
| **Change Request**         | Planear, aprovar e executar implementações em Produção; integrado com ITSM                                                              | Todas                                 |
| **CFI**                    | Planear o fecho da Iniciativa do tipo Projeto junto à equipa de Change Enablement                                                       | Projetos (não aplica a Product Teams) |
| **Test Plan**              | Plano formal dos testes a executar numa determinada entrega                                                                             | Todas                                 |
| **Xray Test**              | Caso de teste manual ou automatizado, com passos e resultados esperados                                                                 | Todas                                 |
| **Test Set**               | Conjunto agrupado de testes relacionados                                                                                                | Todas                                 |
| **Test Execution**         | Registo da execução de um conjunto de Xray Tests                                                                                        | Todas                                 |
| **Go Live**                | Momento em que uma Iniciativa do tipo Projeto implementa em produção                                                                    | Projetos (não aplica a Product Teams) |
| **Milestone**              | Marco que representa o fecho de uma etapa no projeto                                                                                    | Projetos (não aplica a Product Teams) |
| **Purchase Order Request** | Pedidos de emissão de POs                                                                                                               | Todas                                 |

---

## Story Points — Guia por Issue Type

Story Points refletem trabalho planeado, previsível e de valor direto.

| Issue Type              | Story Points? | Motivo                                                  |
| ----------------------- | ------------- | ------------------------------------------------------- |
| Story                   | ✅ Sim        | Valor direto; sempre estimar                            |
| Improvement             | ✅ Sim        | Valor direto; sempre estimar                            |
| Task                    | ✅ Sim        | Sempre estimar, mesmo tarefas técnicas                  |
| Problem                 | ✅ Sim        | Causa raiz com valor direto; estimativa útil            |
| Test Plan (Regression)  | ✅ Sim        | Manual e automatizado                                   |
| Test Plan (Maintenance) | ✅ Sim        | Manual e automatizado                                   |
| Sub Task                | ❌ Não        | Estimativa está no Parent Story                         |
| Bug                     | ❌ Não        | Trabalho corretivo e reativo; pontuar distorce métricas |
| Spike                   | ❌ Não        | Esforço incerto; valor indireto                         |
| Test Plan (Features)    | ❌ Não        | Associado à validação de novas funcionalidades          |
| Incident                | ❌ Não        | Reativo e urgente; fora do planeamento                  |

**Princípio:** itens imprevisíveis, corretivos ou reativos não são pontuados, mas continuam a ser rastreados via workflow. Recomenda-se separar um % de cada sprint para tratar eventualidades (Bugs e Incidents) para evitar sobrecarga.

---

## Gestão de Dependências

Uma dependência representa a necessidade de alinhamento, colaboração ou integração entre equipas que impacta diretamente a capacidade de entrega, caso não haja a intervenção ou contributo da outra equipa.

### O que é uma dependência?

- É um compromisso explícito entre uma Requester Stream e uma Delivery Stream.
- É usada quando parte do trabalho necessário para entregar uma Iniciativa depende de outra equipa.
- Não deve ser usada para trabalho interno à mesma Stream; nesses casos, prefira Épicos ou Initiatives locais.

### Tipos de dependência

- **Delivery**: trabalho a ser entregue pela equipa responsável pela execução.
- **Discovery**: apoio necessário nas fases iniciais de descoberta, análise ou definição.

### Princípios

- A equipa que identifica a dependência efetua o registo para a equipa que irá receber.
- Alinhar a dependência com a equipa responsável para análise e resolução.
- Estabelecer uma relação clara 1 para 1, promovendo responsabilidade, transparência e alinhamento.
- As dependências devem estar associadas a Ideas e Initiatives.
- Depois de aceite, a Delivery Stream é responsável por manter o estado atualizado.

### Quando criar uma Dependency no Jira

**Iniciativas do tipo Produto:** uso mais comum. A dependência deve ser aberta diretamente para a Product Team responsável, que gere o trabalho no seu próprio espaço. O mais relevante para a equipa solicitante é a entrega nas datas alinhadas.

**Iniciativas do tipo Projeto:** quando o trabalho de uma ou mais PTs está claramente definido no âmbito, não é necessário registar dependências — use Épicos referenciados à Initiative. Se surgem necessidades não identificadas no âmbito inicial, o uso de dependências é recomendado.

**Equipas Transversais:** não criam nem recebem dependências — o seu modelo é de fluxo contínuo.

**Product Teams da mesma Stream ou com o mesmo PM:** o registo não é obrigatório. O alinhamento tende a ser mais direto; use Épicos associados à Initiative.

### Cenários de uso

**Cenário 1 — Dependência como Épico:**
- Quando apenas parte do trabalho depende de outra Stream.
- A dependência é criada como um issue do tipo Dependency e a Delivery Stream cria os child work items necessários (Stories, Tasks, Spikes).
- Use este modelo quando o trabalho for suficientemente focado e não justificar uma iniciativa própria.

**Cenário 2 — Dependência corresponde a uma Initiative:**
- Quando o trabalho necessário da Delivery Stream tem dimensão ou complexidade suficientes para justificar uma Initiative própria.
- A Delivery Stream analisa a dependência, aceita o pedido e cria a Initiative no seu board.
- Deve haver links claros: Initiative A "Depends On" Initiative B e Dependency "Duplicates" Initiative B, além da associação à Initiative Aggregator.

**Cenário 3 — Iniciativa totalmente entregue por outra Stream:**
- Exceção: a iniciativa pertence à Requester Stream, mas a execução é integralmente realizada pela Delivery Stream.
- Se já existir um Dependency, a dependência deve ser aceite e associada à nova Initiative movida para a Stream B.
- A Requester Stream deve preencher obrigatoriamente os campos `Requester Stream` e `Delivery Stream` e solicitar a movimentação da Initiative para o board da Stream B.
- Após a movimentação, o card de Dependency original deve ser fechado para preservar rastreabilidade.

### Ciclo de vida no Jira

- **Open:** criação inicial. A dependência é uma proposta de trabalho.
- **In Analysis:** a Delivery Stream avalia o pedido para decidir se aceita e em que formato.
- **Waiting for Info:** pausa para esclarecer dúvidas; pode alternar com In Analysis.
- **Accept:** compromisso formal; define-se due date e o status passa a ser mantido pela Delivery Stream.
- **Not Accept:** o pedido não é assumido; deve ser realinhado entre os Product Managers.
- **In Progress:** trabalho em execução pela Delivery Stream.
- **In Acceptance:** entrega concluída e em validação pela Requester Stream.
- **Done:** entrega validada, dependência concluída.
- **Cancelled / Delete:** usados quando a dependência deixa de fazer sentido ou foi criada por engano.

### Responsabilidades e rastreabilidade

- Campos obrigatórios no Jira: `Requester Stream`, `Delivery Stream`, `Dependency Type`.
- Ao aceitar, a Delivery Stream define a due date e mantém o estado atualizado.
- Sempre que a dependência gera uma Initiative, associe-a à Initiative Aggregator da Delivery Stream.
- Use links de rastreabilidade claros, incluindo "Depends On" e "Duplicates", conforme aplicável.

### Como escalar dependências não resolvidas

| Nível                | Quando usar                                                                        | Ação                                 |
| -------------------- | ---------------------------------------------------------------------------------- | ------------------------------------ |
| 1 — Resolução direta | Equipas com autonomia e boa vontade                                                | AC facilita conversa entre SMs/TLs   |
| 2 — PM/PO            | Envolve priorização de backlog                                                     | PM da equipa fornecedora é envolvido |
| 3 — Liderança/AAC    | Não resolvível no nível das equipas (orçamento, alocação, conflito de prioridades) | Escalada formal                      |

**Regra prática:** se uma dependência está aberta há mais de 1 sprint sem progresso, escale para o próximo nível.
