# Métricas Ágeis — Referência Operacional

Métricas utilizadas no contexto de stream. Nível operacional e de previsibilidade. Para cada métrica: definição, cálculo, como interpretar, thresholds e perguntas de coaching.

---

## Diagnóstico combinado de métricas

O Agile Coach deve usar métricas para compreender o sistema, não para classificar pessoas. A leitura correta requer contexto, comportamento e decisão.

### Regra prática
- Nunca interpretar uma métrica isoladamente.
- Cruzar pelo menos duas fontes de evidência: métrica + contexto, comportamento + cerimónia, ou fluxo + qualidade.
- As ações devem ser orientadas a reduzir fricção, melhorar previsibilidade e reforçar autonomia da equipa.

### Leituras comuns e intervenção

| Padrão observado | Leitura provável | Pergunta de coaching | Experimento sugerido |
| --- | --- | --- | --- |
| Velocity baixa + carry over alto | Compromisso superior à capacidade real ou refinamento insuficiente | Onde está a equipa a perder foco no sprint? | Rever a capacidade real, o Sprint Goal e o tratamento de carry over |
| Lead time alto + cycle time baixo | Gargalo de priorização, fila ou waiting time | O trabalho está a esperar por decisão ou por outra equipa? | Melhorar o fluxo de entrada, priorização e gestão de dependências |
| Defect rate crescente + throughput instável | Qualidade a ser empurrada para o fim e retrabalho crescente | Onde a qualidade está a ser comprometida? | Reforçar DoR/DoD, validação antecipada e revisão de risco |
| Flow efficiency baixa | Muito tempo em espera, WIP excessivo ou dependências | Onde os itens passam mais tempo parados? | Reduzir WIP, clarificar estados e remover bloqueios explícitos |

### Anti-patterns de leitura de métricas
- Usar velocity para comparar equipas ou pressionar resultados.
- Tratar carry over como “erro de estimativa” sem discutir contexto e dependências.
- Interpretar defeitos apenas pelo volume, sem olhar para causa raiz e impacto no utilizador.

---

## Níveis de Métricas

As métricas são classificadas em três níveis para apoiar decisões em diferentes momentos do ciclo de trabalho:

- **Estratégico** — métricas que suportam alinhamento de portfólio, QBR e decisão de investimento.
- **Tático** — métricas que ajudam a coordenar a execução entre streams, priorização e dependências.
- **Operacional** — métricas que suportam a entrega diária, o fluxo do board e a previsibilidade da equipa.

### Como usar no contexto MC Digital

- **QBR:** usa métricas estratégicas e táticas para validar prioridades do roadmap e decidir quais iniciativas avançam para NOW.
- **MBR:** usa métricas táticas e operacionais para acompanhar o pipeline de Now/Next/Later e identificar bloqueios antes do próximo QBR.

---

## Velocity (SP e %)

**O que é:** Permite analisar a estabilidade e previsibilidade dos sprints, comparando o que foi planeado, alterado e efetivamente entregue.

**Como é calculado:** Soma dos Story Points (SP) concluídos no sprint, comparando com os pontos comprometidos no início, considerando alterações feitas durante o ciclo.

**Como utilizar:** Usar para identificar padrões de variação (adições, remoções, cancelamentos) e a fiabilidade do cumprimento dos compromissos assumidos. Ajuda a perceber a capacidade real da equipa.

**Interpretação:**

- Velocity é um indicador de capacidade, não de produtividade. Nunca usar para comparar equipas.
- Variação de ±20% entre sprints é considerada normal.
- Queda sustentada (3+ sprints) indica problema de fluxo, dívida técnica ou instabilidade.
- Crescimento constante sem aumento de qualidade pode indicar inflação de estimativas.

**Thresholds:**

- Variação aceitável: ±20% da média dos últimos 3 sprints
- Alerta: queda >30% em sprint isolado — investigar causa
- Crítico: tendência de queda por 3 sprints consecutivos

**Perguntas de coaching:**

- "O que mudou neste sprint que pode explicar a variação?"
- "Estamos a planear com base na velocity real ou na que gostaríamos de ter?"
- "A velocity reflete entregas reais de valor ou há itens parcialmente concluídos?"

---

## Backlog Variation (SP e %)

**O que é:** Permite identificar e avaliar a estabilidade do sprint backlog, medindo quanto o âmbito variou face ao planeado inicial.

**Como é calculado:** Diferença percentual entre os Story Points planeados no início do sprint e o total após adições, remoções ou mudanças durante o período.

**Como utilizar:** Usar para atuar em sprints com mudanças excessivas que impactam previsibilidade e foco da equipa, e/ou identificar padrão de comportamento de alta variação entre sprints.

**Thresholds:**

- Aceitável: variação ≤15% do planeado inicial
- Alerta: variação entre 15–30%
- Crítico: variação >30% ou padrão recorrente de adições durante o sprint

**Perguntas de coaching:**

- "Porque é que estamos a adicionar itens durante o sprint? São urgências reais ou falta de planeamento?"
- "O refinamento está a ser feito com antecedência suficiente?"
- "O Sprint Goal está a proteger a equipa de interrupções externas?"

---

## Carried Over (%)

**O que é:** O quanto do esforço total do sprint a equipa está a dedicar a itens que já deveriam ter sido entregues, mas foram carregados de sprints anteriores por não terem sido finalizados.

**Como é calculado:** Proporção de Story Points não concluídos adicionados para o sprint atual, em relação ao total comprometido no sprint.

**Como utilizar:** Se for recorrente ou alto, rever capacidade, refinamento e critérios de compromisso nos sprints.

**Thresholds:**

- ~10–15%: estável / maduro
- 15–20%: equipas a estabilizar — monitorizar
- > 20–25%: alerta — investigar causas e atuar
- Crítico: mesmo item carregado por 2+ sprints consecutivos

**Nota importante:** NÃO se deve redimensionar os Story Points de um carried over. A "falha" na estimativa precisa acontecer para a equipa discutir e interpretar o que impediu a conclusão.

**Anti-patterns associados:** ver `references/praticas-e-cerimonias.md` → "Gestão de Carry Over"

**Perguntas de coaching:**

- "Quando identificámos que este item não seria entregue? O que nos impediu de agir antes?"
- "Este item estava bem refinado quando entrou no sprint?"
- "Estamos a planear para a equipa que temos ou para a que gostaríamos de ter?"

---

## Sprints Carried Over Items

**O que é:** Apresenta, por equipa, o número de vezes em sprints que um item foi carried over. Permite identificar a recorrência de itens que transitam entre sprints.

**Como é calculado:** Conta quantas vezes um mesmo item foi transportado entre sprints, identificando recorrência e impacto no fluxo de trabalho.

**Como utilizar:** Usar para detetar falta de foco, problemas de planeamento ou dependências frequentes. Pode evidenciar também uma falha da equipa na estimativa de SP dos cartões.

**Thresholds:**

- Alerta: mesmo item carried over 2 sprints consecutivos
- Crítico: item carried over 3+ sprints — requer análise de causa raiz imediata

---

## Defect Rate

**O que é:** Mede a qualidade das entregas, relacionando o número de incidentes e problems gerados com o volume total (Stories/Tasks/Improvements) de trabalho concluído.

**Como é calculado:** Conta todos os incidentes criados e resolvidos dentro do recorte mensal, com base nas datas de criação e resolução registadas no Jira.

**Como utilizar:** Usar para identificar iniciativas com maior taxa de defeitos nas sprints e com necessidade de melhoria no processo de desenvolvimento.

**Distinção importante (Bug vs Incident vs Problem):**

- **Bug:** erro antes da produção, identificado durante testes/verificação de qualidade
- **Incident:** erro em produção que exige ação da equipa; tem SLA e está integrado com o ITSM
- **Problem:** causa raiz que impacta múltiplos incidents; criado via integração ITSM-Jira

**Thresholds:**

- Alerta: aumento >20% em relação à média dos últimos 3 sprints
- Crítico: incidents de produção recorrentes no mesmo componente/funcionalidade

---

## Nº Incidentes Criados e Resolvidos

**O que é:** Mostra o número de Incidents ou Jira Legacy Incident criados e resolvidos em recorte mensal.

**Como é calculado:** Dividindo o número de incidentes e problems criados pelo total de Stories, Tasks e Improvements entregues no período, multiplicando por 100.

**Como utilizar:** Avaliar se a equipa está a reagir com eficácia aos incidentes de produção criados dentro do mês.

---

## Nº Problems Criados e Resolvidos

**O que é:** Mostra o número de Problems criados e resolvidos em recorte mensal.

**Como é calculado:** Soma os problems criados e resolvidos no mês, considerando apenas itens com status finalizado e data de resolução dentro do período.

**Como utilizar:** Perceber o volume de problems gerados no mês e se a equipa está a dar resposta mês a mês.

---

## Throughput Entregas

**O que é:** Permite acompanhar o volume de trabalho entregue ao longo do tempo comparado aos itens criados no mesmo período.

**Como é calculado:** Calcula o volume de itens concluídos num período e compara com os itens criados no mesmo intervalo, mostrando tendência de backlog ou capacidade.

**Como utilizar:** Se a criação de itens superar consistentemente o fecho de itens, investigar sobrecarga, prioridades ou necessidade de ajuste de capacidade.

**Alerta:** Backlog a crescer consistentemente = produto a gerar mais demanda do que a equipa consegue absorver. Decisão de priorização necessária.

---

## Lead Time

**O que é:** Permite medir o tempo total que um item leva desde ser criado até ser efetivamente entregue em produção.

**Como é calculado:** Diferença entre a data de criação do item e a data em que foi entregue em produção, incluindo todas as etapas do fluxo.

**Como utilizar:** Monitorizar se o tempo total das entregas está a melhorar ou a piorar e identificar etapas do fluxo onde existem atrasos.

**Interpretação combinada:**

- Lead time alto com cycle time baixo = gargalo de priorização/planeamento, não de execução
- Lead time alto com cycle time alto = gargalo no processo de desenvolvimento

**Thresholds:**

- Alerta: lead time médio >3x o cycle time médio (indica tempo em fila desproporcional)
- Crítico: itens com lead time >30 dias sem justificativa de complexidade

---

## Cycle Time

**O que é:** Mede o tempo que um item leva desde o início efetivo do trabalho (In Progress) até estar concluído (Done).

**Como é calculado:** Diferença entre a data em que o item entrou em "In Progress" e a data em que foi marcado como concluído (Done).

**Como utilizar:** Encontrar gargalos na fase de execução e ajustar práticas de trabalho, limites de WIP ou dependências para reduzir o tempo médio de conclusão.

**Thresholds (referência — calibrar com histórico da equipa):**

- Story: target ≤5 dias úteis
- Bug: target ≤3 dias úteis
- Alerta: itens com cycle time >2x a média da equipa

---

## Flow Efficiency

**O que é:** Mede a proporção de tempo em que um item está realmente a ser trabalhado versus o tempo total no fluxo, distinguindo estados de execução e de espera. Ajuda a identificar ineficiências e excesso de tempo parado no processo.

**Como é calculado:** Proporção entre o tempo em estados ativos (execução) e o tempo total no fluxo, incluindo períodos de espera, expressa em percentagem.

**Como utilizar:** Detetar onde as tarefas passam mais tempo em espera e atuar nesses pontos — ajustando WIP, removendo bloqueios e dando foco na fluidez do processo.

**Thresholds:**

- Referência de mercado: 15–40% (lean/ágil maduro)
- Alerta: <15%
- Excelente: >40%

**Perguntas de coaching:**

- "Onde os itens passam mais tempo parados? Em qual coluna do board?"
- "Temos handoffs desnecessários que introduzem espera?"
- "O WIP está controlado ou há muitos itens em paralelo?"

---

## Average Time in Status

**O que é:** Mostra quanto tempo (em dias), em média, os itens permanecem em cada estado do workflow.

**Como é calculado:** Média de dias que os itens permanecem em cada status do workflow, calculada com base nas transições registadas no Jira.

**Como utilizar:** Localizar gargalos específicos no fluxo e priorizar melhorias nesses estados — ajustando processos, responsabilidades ou automatizações para acelerar a passagem dos itens.

---

## Previsibilidade — Campos de Data no Jira

A previsibilidade das iniciativas baseia-se na comparação entre datas Estimado e Actual. Existem três categorias de campos:

### Campos "Estimated" (compromisso assumido no QBR)

| Campo                     | O que representa                                                                             | Quando é preenchido                                                                    |
| ------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| QBR Estimated Start Date  | Compromisso de quando a Initiative arranca (move para "In Progress")                         | Idea → ao mover para "Approval" / "Approved"; Initiative → ao mover para "In Progress" |
| QBR Estimated Launch Date | Compromisso da data de entrada em produção (estado "Launch")                                 | Mesmos momentos acima                                                                  |
| QBR Estimated End Date    | Compromisso de quando a Initiative transita completamente para Operação (estado "Operation") | Mesmos momentos acima                                                                  |

**Nota:** Alteração após QBR requer pedido por email ao PMO (se aprovado pelo Diretor).

### Campos "Current" (estimativa atualizada — alterável)

| Campo Jira  | Alcunha     | Alterável após QBR? | O que representa                                                                                                       |
| ----------- | ----------- | ------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Start Date  | Start Date  | ✅                  | Visão atualizada de quando a Initiative vai efetivamente arrancar. Não pode ser ajustado após entrar em "In Progress". |
| Launch Date | Launch Date | ✅                  | Visão atualizada da data de implementação em produção. Não pode ser ajustado após entrar em "Launch".                  |
| End Date    | Due Date    | ✅                  | Visão atualizada de quando a Initiative será concluída. Não pode ser ajustado após entrar em "Operation".              |

### Campos "Actual" (datas reais — não alteráveis)

| Campo                                      | O que representa                                                                                 |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| Actual Start Date (In Progress Start Date) | Data real em que a Initiative foi movida para "In Progress". Guardada automaticamente pelo Jira. |
| Actual Launch Date                         | Data real em que a Initiative foi movida para "Launch". Guardada automaticamente.                |
| Actual End Date                            | Data real em que a Initiative foi movida para "Operation". Guardada automaticamente.             |

---

## Diagnóstico Combinado de Métricas

| Sintoma observado                        | Métricas a cruzar                    | Hipótese provável                           |
| ---------------------------------------- | ------------------------------------ | ------------------------------------------- |
| Velocity caindo + carried over alto      | Velocity + Carried Over + Cycle Time | Overcommitment ou bloqueios não endereçados |
| Equipa "entrega" mas stakeholder reclama | Lead Time + Backlog Variation        | Fila de entrada alta; priorização ineficaz  |
| Muitos bugs após sprints rápidos         | Velocity + Defect Rate               | Velocidade a sacrificar qualidade           |
| Time parece ocupado mas entrega pouco    | Flow Efficiency + Cycle Time         | Muito WIP; trabalho em paralelo excessivo   |
| Backlog cresce sem controlo              | Throughput + Lead Time               | Ausência de depuração ativa do backlog      |
| Sprints instáveis com muitas alterações  | Backlog Variation + Velocity         | Refinamento insuficiente; scope creep       |
| Incidents a aumentar após releases       | Defect Rate + Throughput             | Qualidade a ser sacrificada por velocidade  |
