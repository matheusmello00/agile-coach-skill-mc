# Qualidade

Qualidade não é apenas "testar" ou "não ter bugs" — é criar valor sustentável para o utilizador e para o negócio, de forma consistente, colaborativa e evolutiva. É responsabilidade partilhada por toda a equipa.

---

## Cultura de Qualidade no Produto

A qualidade está integrada em todas as etapas do ciclo de vida — não é uma fase isolada no final.

**Valores fundamentais:**

1. **Foco no utilizador** — qualidade começa em resolver o problema certo, da forma mais simples e eficaz, com usabilidade e experiência relevantes.
2. **Responsabilidade de toda a equipa** — PM, UX, Developers, Operações e QAE têm papel na definição, construção, validação e melhoria do produto. Não é função exclusiva do QAE.
3. **Incorporada no processo** — práticas de qualidade presentes em todas as etapas: Ideação, Planeamento, Desenvolvimento, Validação, Release e Operação.
4. **Prevenção > Correção** — investir em clareza, alinhamento, testes automatizados, arquitetura escalável e boas práticas para evitar problemas antes que cheguem ao utilizador.
5. **Métricas e aprendizagem contínua** — usar métricas claras para avaliar qualidade, tomar decisões baseadas em dados e evoluir continuamente. Qualidade é melhoria contínua, não um estado final.

**Nota importante:** Entregas rápidas são importantes, mas não à custa de dívida técnica, má experiência ou instabilidade.

---

## Work Items de Qualidade no Jira

| Issue Type         | O que é                                                                                |
| ------------------ | -------------------------------------------------------------------------------------- |
| **Xray Test**      | O teste em si — caso de teste manual ou automatizado com passos e resultados esperados |
| **Precondition**   | O que tem de estar pronto antes de começar                                             |
| **Test Set**       | Agrupa testes relacionados                                                             |
| **Test Plan**      | Define o que vai ser testado naquela entrega                                           |
| **Test Execution** | Regista a execução do teste                                                            |

---

## Boas Práticas por Fase do Ciclo

### Ideação

- Participar ativamente das sessões de discovery e refinamento.
- Contribuir para a definição de critérios de aceitação e hipóteses de valor/testabilidade.
- Apoiar na análise de riscos técnicos e funcionais desde o início.
- Garantir que requisitos sejam claros, testáveis e priorizados.
- Sugerir estratégias de validação contínua (ex: feature flags, A/B testing).
- Identificar, de forma preliminar, os requisitos ou fluxos críticos que serão P-Zero nas fases posteriores.

### Planeamento / Estruturação

- Estimar esforço de testes junto à equipa (incluindo automação).
- Definir estratégias e âmbito de testes (unitários, integração/APIs, E2E, regressão).
- Planear dados e ambientes necessários para validação.
- Documentar cenários de teste com base nos critérios de aceitação.
- Validar que a DoR foi cumprida sob a ótica da qualidade.
- O developer deve desenhar os cenários de testes unitários durante o refinamento técnico da User Story.
- Definir NFRs com apoio do QAE e TDL: performance, segurança, escalabilidade, acessibilidade.
- Definir quais testes serão automatizados, por quem, em que momento, e se serão integrados no CI/CD.

### Execução / Desenvolvimento

- Garantir que testes unitários, análise estática de código e testes de integração/APIs estão sendo implementados.
- Desenvolver testes automatizados baseados em BDD ou critérios funcionais.
- Realizar code review com foco em qualidade e testabilidade.
- Implementar mocks, dados e estruturas de teste conforme estratégia definida.
- Validar cobertura e resultados dos testes unitários nas pipelines de CI/CD.
- QAE pode atuar como revisor ou observador de PRs, sugerindo melhorias de cobertura.

### Testes End-to-End Internos

- Garantir a execução de testes de regressão e cenários críticos (P-Zero).
- Registar e analisar falhas; colaborar ativamente na triagem de bugs.
- Executar testes exploratórios e funcionais (automatizados e manuais).
- Validar que a DoD foi cumprida sob a ótica da qualidade.
- Confirmar que todos os critérios de aceitação foram validados com sucesso.
- Definir plano de instalação/validação em produção: quem valida o quê e com horários definidos.

### Lançamento / Estabilização / Operação

- Validar artefactos antes da passagem para produção.
- Apoiar na automação de testes pós-deploy e rollback seguro.
- Acompanhar deploys e executar validação pós-release.
- Monitorizar métricas de qualidade em produção (incidentes, problems, logs).
- Contribuir para análises de causa raiz e planos de melhoria contínua.
- Incluir na retrospectiva o tópico da qualidade — refletir sobre o processo de instalação, cobertura, automação e release.

---

## Qualidade nas Etapas — Detalhe

### Fase de Ideação

**Foco:** garantir que a qualidade seja pensada desde a origem da solução.

| Tipo                                             | Descrição                                                                                         |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------- |
| Análise de risco inicial e dependências          | Levantar possíveis falhas ou impactos críticos (integrações, dados sensíveis, alto volume de uso) |
| Identificação de requisitos críticos             | Identificar preliminarmente requisitos ou fluxos que serão P-Zero nas fases posteriores           |
| Discussão de critérios de aceitação preliminares | Explorar com PMs e TDLs o que será considerado sucesso ou falha. Registar no One Pager            |
| Estratégia preliminar de testabilidade           | Definir preliminarmente a estratégia de pirâmide de testes (estático, unitário, integração, E2E)  |
| Requisitos não funcionais iniciais (NFRs)        | Discutir performance, segurança, usabilidade, escalabilidade e rastreabilidade                    |
| Discussão sobre observabilidade                  | O que precisa ser medido em produção (erros, latência, comportamento do utilizador)               |

**Entregável:** pontos de qualidade documentados no One Pager.

---

### Fase de Estruturação & Planeamento

**Foco:** garantir que histórias, épicos e incrementos estejam claros, testáveis, rastreáveis e priorizados.

| Tipo                                      | Descrição                                                                                                                                                            |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Validação do DoR                          | Validar DoR de acordo com os critérios definidos                                                                                                                     |
| Critérios de Aceitação                    | Apoiar o PM na refinação — clareza, mensurabilidade e rastreabilidade. Para regressão: sem bugs críticos (Top of Mind e High), podendo existir exceções justificadas |
| Desenho técnico da solução                | Apoiar PM e TL no desenho inicial (componentes, integrações, dependências)                                                                                           |
| Discussão de cobertura de testes          | Planear níveis de testes necessários; definir responsável por cada tipo                                                                                              |
| Cenários funcionais Alto Nível e Críticos | Desenhar cenários dos requisitos críticos; classificar os que devem ser sempre validados (P-Zero)                                                                    |
| NFRs                                      | Performance, segurança, escalabilidade, acessibilidade                                                                                                               |
| Planeamento de automação                  | Definir quais testes serão automatizados, por quem e quando                                                                                                          |

**Entregáveis:**

- DoR validado → User Story no status "Ready Candidate"
- Critérios de aceitação registados no Jira
- Desenho técnico no Confluence (Technical Description da User Story)
- Cobertura de testes no One Pager + Test Plans criados
- Cenários criados/atualizados no Xray com campo Criticidade
- NFRs na Technical Description no Confluence

---

### Fase de Desenvolvimento & Testes Unitários

| Tipo                                        | Descrição                                                                                      |
| ------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| Revisão contínua dos critérios de aceitação | Garantir alinhamento constante entre Developers, QAE e PM                                      |
| Testes unitários                            | Developers escrevem e executam; QAE apoia na definição dos casos; integrados no CI/CD          |
| Análise estática de código                  | Developers executam; conformidade com critérios da equipa; integrada no CI/CD                  |
| Testes de API e integração                  | Cobertura de fluxos de backend e contratos; atenção a edge cases e falhas; integrados no CI/CD |
| Casos de teste da User Story                | Especificação dos casos que cubram todos os critérios de aceitação                             |
| Testes E2E automatizados                    | Implementar/manter com base nos critérios de aceitação; usar frameworks padronizadas           |
| Atualização da classificação P-Zero         | Rever e confirmar classificação de cenários críticos com base no entendimento técnico          |

**Entregáveis:**

- Testes unitários com cobertura mínima (resultado na pipeline + cobertura via Sonar)
- Código sem apontamentos bloqueantes/críticos (Sonar)
- Testes de API e integração (Pipeline e/ou Xray)
- Casos de teste no Xray
- Testes E2E automatizados criados na framework + atualizados no Xray

---

### Fase de Testes End-to-End Internos

| Tipo                                         | Descrição                                                               |
| -------------------------------------------- | ----------------------------------------------------------------------- |
| Confirmação de testes unitários e integração | Validar se foram executados com sucesso                                 |
| Estabilidade dos ambientes                   | Verificar ambiente estável, dados apropriados, respostas consistentes   |
| Execução de P-Zero                           | Executar (preferencialmente via CI/CD) os cenários críticos             |
| Execução de testes E2E                       | Executar de acordo com critérios de aceitação da User Story             |
| Testes de regressão                          | Garantir que testes existentes continuam válidos após novas alterações  |
| Validação de NFRs                            | Performance, segurança, compatibilidade, escalabilidade, acessibilidade |
| Validação de critérios de aceitação          | Confirmar que todos foram validados com sucesso                         |
| Plano de instalação/validação em produção    | Definir quem valida o quê e com horários definidos                      |

**Entregáveis:**

- Evidências no Xray de P-Zero, E2E e regressão
- Bugs no Jira
- Report de NFRs
- Plano de instalação/validação

---

### Fase UAT

**Foco:** PM valida se a solução desenvolvida responde às necessidades do negócio e dos utilizadores finais.

- Confirmar que os requisitos de negócio estão de acordo com o pretendido.
- Testes manuais funcionais pelos utilizadores/PM.
- Critérios de DoD verificados.
- Planos de teste baseados em processos reais do negócio.
- Testes exploratórios para identificar falhas não previstas.

---

### Fase de Release / Pós-Produção

| Tipo                                  | Descrição                                                                                                   |
| ------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| Checklist de release                  | Confirmar todos os critérios técnicos, funcionais e de qualidade; preferencialmente via gates nas pipelines |
| Participação na janela de release     | Executar plano de instalação/validação definido                                                             |
| Monitorização ativa com suporte       | Acompanhar logs, alertas e indicadores em tempo real                                                        |
| Validação de métricas de sucesso      | Confirmar se métricas da funcionalidade estão a ser atingidas                                               |
| Registo de incidents e problems       | Classificar e documentar com análise de causa e planos de prevenção                                         |
| Retrospectiva com tópico de qualidade | Refletir sobre processo de instalação, cobertura, automação e release                                       |

**Entregáveis:**

- Change Request atualizado (em "Done")
- Evidências de incidents e problems no ITSM e Jira

---

## UAT, Go Live e Operação

A qualidade da entrega não termina no desenvolvimento — inclui validação de negócio, Go Live e estabilização em produção.

- **UAT (User Acceptance Testing)** deve ser definido pelo negócio ou representante de negócio, em ambiente de pré-produção sempre que possível. É o momento de validar a solução contra os requisitos de negócio e a experiência esperada.
- **Go Live** deve ser acompanhado por um plano de implementação e rollback, com responsabilidade clara do TL e do PM/PjM. A passagem para produção só deve ocorrer após validação técnica, de qualidade e de risco.
- **Operação** deve incluir monitorização ativa, gestão de incidents e problems, e um plano de mitigação para regressões ou falhas pós-release.
- **Change Enablement** faz parte do fluxo de qualidade: o AC deve garantir que o processo está alinhado com stakeholders, que a documentação está pronta e que o suporte foi preparado.
- **Checklist de aceitação final** deve incluir testes automatizados, evidências de UAT, revisão de qualidade e alinhamento com o Go Live.

---

## Tipos de Testes

| Tipo                              | O que valida                                                               |
| --------------------------------- | -------------------------------------------------------------------------- |
| **Testes Unitários**              | Componentes individuais do código                                          |
| **Testes de Integração**          | Comunicação e interação entre módulos/sistemas/APIs                        |
| **Testes Funcionais**             | Se o sistema funciona conforme os requisitos funcionais definidos          |
| **Testes de Regressão**           | Que novas alterações não quebram funcionalidades já existentes             |
| **Testes E2E**                    | Fluxo completo da funcionalidade em ambiente próximo de produção           |
| **UAT (User Acceptance Testing)** | Se o software cumpre requisitos de negócio e necessidades dos utilizadores |
| **Testes de Performance/Carga**   | Rapidez e estabilidade sob diferentes condições                            |
| **Testes Exploratórios**          | Navegação livre para identificar falhas não previstas                      |

---

## Cobertura de Código

- **Referência:** entre 70% e 90%, dependendo do contexto.
- 100% não garante ausência de bugs, mas ajuda a reduzir riscos.
- Foco na cobertura de testes críticos e de negócio, não apenas em métricas.
- Medição via Sonar integrado no pipeline de CI/CD.

---

## Code Review

Processo de revisão do código-fonte por outro(s) programador(es) antes de ser integrado no repositório principal.

**Quando fazer:** sempre que há novo desenvolvimento, após refactoring, antes de release crítica, quando há mudanças em regras de negócio ou arquitetura.

**O QAE pode atuar como revisor ou observador de PRs**, sugerindo melhorias de cobertura, modularidade e estrutura de testes.
