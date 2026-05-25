# Modelo Operativo

O Modelo Operativo da stream organiza o ciclo de vida das iniciativas em três horizontes temporais — **Later, Next e Now** — que refletem o nível de maturidade e compromisso de cada iniciativa, desde a sua identificação até à entrega e operação contínua.

---

## Horizontes Temporais (Now / Next / Later)

O processo é contínuo e on-going: as iniciativas evoluem ao longo do roadmap sem depender de ciclos rígidos de aprovação.

| Horizonte | O que representa | Estado típico das iniciativas |
|---|---|---|
| **NOW** | Iniciativas em execução ativa | In Progress, Rollout, concluídas no mês (Done), a arrancar no mês seguinte (Committed) |
| **NEXT** | Iniciativas em exploração ativa ou planeamento com MBR de confirmação definido | Exploration, Planning, Ready to Commit |
| **LATER** | Iniciativas identificadas sem arranque previsto a curto prazo | Draft, Exploration sem MBR de confirmação |

---

## Formas de Trabalho Suportadas

O modelo adapta-se à natureza de cada iniciativa:

- **Equipas de Produto** — entrega incremental e contínua de valor, com backlog gerido pelo Product Manager.
- **Equipas de Projeto** — âmbito, prazo e orçamento definidos, coordenados pelo Project Manager.
- **Fluxo Contínuo (Kanban)** — equipas que gerem um volume constante de trabalho sem sprints fixos.

---

## MBR — Monthly Business Review

**O que é:** Mecanismo mensal de reporte e alinhamento sobre a evolução das iniciativas, adotando a abordagem de Roadmap Contínuo Now/Next/Later. Fórum onde as streams comunicam o estado atual do roadmap e garantem visibilidade aos stakeholders.

**O MBR não substitui o QBR** — complementa-o. O QBR é o momento de alinhamento executivo trimestral com decisão de prioridades; o MBR é o mecanismo de acompanhamento contínuo entre QBRs.

### Para que serve:
- **Visibilidade:** manter os stakeholders informados sobre o estado real das iniciativas.
- **Alinhamento:** garantir que as prioridades do roadmap continuam alinhadas com as necessidades do negócio; identificar e resolver bloqueadores antes que impactem o NOW.
- **Continuidade:** evitar picos de esforço associados ao modelo de reporte apenas trimestral; permitir ajustes de prioridade de forma ágil.

### Como funciona:

| Dimensão | Detalhe |
|---|---|
| Cadência | Mensal — tipicamente no fim do mês |
| Formato principal | Documento estruturado enviado aos stakeholders, organizado por horizonte |
| Reunião | Facultativa — apenas se existirem temas que exijam discussão estratégica |
| Participantes | Primeiras linhas dos stakeholders. Não requer envolvimento de Executivos |
| Relação com QBR | O MBR não se realiza no mês do QBR — o QBR substitui-o |

### Estrutura do documento por horizonte:

| Horizonte | O que reportar | Datas obrigatórias |
|---|---|---|
| NOW | Iniciativas em execução, concluídas no mês e a arrancar no mês seguinte | Committed Start · Launch · End Date |
| NEXT | Iniciativas em exploração ativa ou planeamento | MBR de confirmação definido |
| LATER | Iniciativas identificadas sem arranque previsto | Sem promessa de datas |

### Quem prepara:
- **PM:** prepara e envia o documento; garante que o estado de cada iniciativa no Jira está correto antes do envio.
- **PSL:** revê o documento antes do envio; participa na reunião facultativa se convocada.
- **Stakeholders:** recebem e reveem o documento; participam se temas estratégicos o justificarem.

### O que NÃO vai ao MBR:
Epics, User Stories, Tasks, Bugs, Incidents, CFIs, POs, XRAYs, Minors, Iniciativas em Draft sem atividade de exploração relevante, Itens duplicados entre streams.

---

## Issue Types no Jira

| Issue Type | Função | Aplica-se a |
|---|---|---|
| **Idea** | Estágio inicial de uma potencial iniciativa — proposta originada de uma necessidade ou oportunidade identificada | Todas as equipas |
| **Initiative Aggregator** | Agrupa iniciativas, por exemplo dentro de um programa | Todas |
| **Initiative** | Produto/incremento maior que um Epic; sempre entrega valor ao negócio | Todas |
| **Dependency** | Representa dependência entre equipas — entrega, ação ou capacidade necessária de outra equipa | Equipas de Produto (principalmente) |
| **Epic** | Agrupador de Stories; representa grandes partes de trabalho (features ou componentes); habitualmente não é entregue dentro de um Sprint | Todas |
| **Story** | Funcionalidade que entrega valor ao utilizador final, por norma numa Sprint; fragmentação de um Epic | Todas |
| **Task** | Pequena tarefa para concluir um item | Todas |
| **Bug** | Erro antes da produção, priorizado por criticidade; identificado durante testes/verificação de qualidade | Todas |
| **Incident** | Erro em produção que exige ação da equipa; tem SLA; integrado com ITSM | Todas |
| **Problem** | Reflete em Jira o ticket de Problema registado em ITSM; criado via integração ITSM-Jira | Todas |
| **Change Request** | Planear, aprovar e executar implementações em Produção; integrado com ITSM | Todas |
| **CFI** | Planear o fecho da Iniciativa do tipo Projeto junto à equipa de Change Enablement | Projetos (não aplica a Product Teams) |
| **Test Plan** | Plano formal dos testes a executar numa determinada entrega | Todas |
| **Xray Test** | Caso de teste manual ou automatizado, com passos e resultados esperados | Todas |
| **Test Set** | Conjunto agrupado de testes relacionados | Todas |
| **Test Execution** | Registo da execução de um conjunto de Xray Tests | Todas |
| **Go Live** | Momento em que uma Iniciativa do tipo Projeto implementa em produção | Projetos (não aplica a Product Teams) |
| **Milestone** | Marco que representa o fecho de uma etapa no projeto | Projetos (não aplica a Product Teams) |
| **Purchase Order Request** | Pedidos de emissão de POs | Todas |

---

## Story Points — Guia por Issue Type

Story Points refletem trabalho planeado, previsível e de valor direto.

| Issue Type | Story Points? | Motivo |
|---|---|---|
| Story | ✅ Sim | Valor direto; sempre estimar |
| Improvement | ✅ Sim | Valor direto; sempre estimar |
| Task | ✅ Sim | Sempre estimar, mesmo tarefas técnicas |
| Problem | ✅ Sim | Causa raiz com valor direto; estimativa útil |
| Test Plan (Regression) | ✅ Sim | Manual e automatizado |
| Test Plan (Maintenance) | ✅ Sim | Manual e automatizado |
| Sub Task | ❌ Não | Estimativa está no Parent Story |
| Bug | ❌ Não | Trabalho corretivo e reativo; pontuar distorce métricas |
| Spike | ❌ Não | Esforço incerto; valor indireto |
| Test Plan (Features) | ❌ Não | Associado à validação de novas funcionalidades |
| Incident | ❌ Não | Reativo e urgente; fora do planeamento |

**Princípio:** itens imprevisíveis, corretivos ou reativos não são pontuados, mas continuam a ser rastreados via workflow. Recomenda-se separar um % de cada sprint para tratar eventualidades (Bugs e Incidents) para evitar sobrecarga.

---

## Gestão de Dependências

Uma dependência representa a necessidade de alinhamento, colaboração ou integração entre equipas que impacta diretamente a capacidade de entrega, caso não haja a intervenção ou contributo da outra equipa.

### Princípios:
- A equipa que identifica a dependência efetua o seu registo para a equipa que irá receber.
- Alinhar a dependência com a equipa responsável para análise e resolução.
- Estabelecer uma relação clara 1 para 1, promovendo responsabilidade, transparência e alinhamento.
- As dependências estão associadas a Ideas e Initiatives.

### Quando criar uma Dependency no Jira:

**Iniciativas do tipo Produto:** uso mais comum. A dependência deve ser aberta diretamente para a Product Team responsável, que gere o trabalho no seu próprio espaço. O mais relevante para a equipa solicitante é a entrega nas datas alinhadas.

**Iniciativas do tipo Projeto:** quando o trabalho de uma ou mais PTs está claramente definido no âmbito, não é necessário registar dependências — usar Épicos referenciados à Initiative. Se surgem necessidades não identificadas no âmbito inicial, o uso de dependências é recomendado.

**Equipas Transversais:** não criam nem recebem dependências — o seu modelo é de fluxo contínuo.

**Product Teams da mesma Stream ou com o mesmo PM:** o registo não é obrigatório. O alinhamento tende a ser mais direto; usar Épicos associados à Initiative.

### Momentos de identificação:
- Fase de exploração
- Avaliação
- Fases mais avançadas do projeto

O compromisso formal ocorre quando a equipa responsável aceita a dependência — o issue deve estar ligado à iniciativa via link "é uma dependência de".

### Como escalar dependências não resolvidas:

| Nível | Quando usar | Ação |
|---|---|---|
| 1 — Resolução direta | Equipas com autonomia e boa vontade | AC facilita conversa entre SMs/TLs |
| 2 — PM/PO | Envolve priorização de backlog | PM da equipa fornecedora é envolvido |
| 3 — Liderança/AAC | Não resolvível no nível das equipas (orçamento, alocação, conflito de prioridades) | Escalada formal |

**Regra prática:** se uma dependência está aberta há mais de 1 sprint sem progresso, escale para o próximo nível.
