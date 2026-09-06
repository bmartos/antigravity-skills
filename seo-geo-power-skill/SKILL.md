---
name: seo-geo-aeo-enterprise-suite
description: >-
  Suite consolidada de skills para auditoria e melhoria de SEO, GEO e AEO.
  Inclui uma skill-mãe enterprise para auditorias recorrentes, uma skill-filha técnica/arquitetura,
  uma skill-filha de conteúdo/on-page/GEO/AEO e um template padronizado de saída executiva e operacional.
  Projetada para uso em auditorias mensais, trimestrais, por release, por template e por migração.
version: 1.0-suite
owner: growth / seo / geo / content / product
modules:
  - enterprise_master
  - tech_architecture_lite
  - content_entity_lite
  - audit_output_template
---

# SEO / GEO / AEO Enterprise Suite

## Objetivo

Esta suite foi criada para operar como um sistema consolidado de auditoria e melhoria de encontrabilidade para sites, páginas, clusters de conteúdo e presenças locais.

Ela combina quatro peças:

1. **Skill-Mãe Enterprise**
   - para auditorias recorrentes, score global, severidade, backlog e governança

2. **Skill-Filha Enterprise-Lite: Técnica / Arquitetura**
   - para rastreabilidade, indexação, canonicalização, sitemaps, schema e arquitetura de URLs

3. **Skill-Filha Enterprise-Lite: Conteúdo / GEO / AEO**
   - para intenção de busca, resposta direta, citabilidade, E-E-A-T, SEO local semântico e conversão

4. **Template Padronizado de Saída**
   - para relatórios executivos e operacionais comparáveis ao longo do tempo

---

# PARTE 1 — SKILL-MÃE ENTERPRISE

## Nome interno
`seo-geo-aeo-enterprise-audit-system`

## Propósito

Esta skill é o sistema principal de auditoria.  
Seu papel é gerar uma visão executiva, priorizada e governável de SEO, GEO e AEO.

Ela deve responder:

- qual é o estado geral do site;
- onde estão os maiores riscos;
- onde estão as maiores oportunidades;
- quais problemas são estruturais;
- quais problemas são de conteúdo;
- o que deve ser corrigido primeiro;
- como acompanhar evolução mês a mês e trimestre a trimestre.

---

## 1. Princípios operacionais

### 1.1 Evidência antes de opinião
Todo achado deve estar apoiado em evidência observável:
- URL
- status técnico
- elemento estrutural
- trecho de conteúdo
- ausência/presença de schema
- conflito de arquitetura
- padrão editorial
- evidência local
- conflito de indexação

### 1.2 Uma URL, uma intenção principal
A skill deve penalizar páginas que:
- competem entre si;
- têm função ambígua;
- duplicam intenção;
- têm conteúdo semelhante sem necessidade.

### 1.3 Priorizar estrutura antes de acabamento
Problemas de:
- indexação,
- canonicalização,
- arquitetura,
- elegibilidade,
- hubs e clusters

devem ter precedência sobre ajustes cosméticos.

### 1.4 SEO, GEO e AEO não são a mesma coisa
A skill deve distinguir:
- crawl;
- indexação;
- training;
- recuperação / citação / resposta;
- autoridade;
- conversão.

### 1.5 Repetibilidade
A saída deve ser comparável entre auditorias.

---

## 2. Escopos de auditoria

### 2.1 Monthly Monitoring
Auditoria leve, recorrente, orientada a regressões, blockers e quick wins.

### 2.2 Quarterly Full Audit
Auditoria completa com score por domínio, backlog estratégico e plano 30/60/90.

### 2.3 Release Audit
Auditoria focada em páginas e templates impactados por release.

### 2.4 Migration Audit
Auditoria para redesign, troca de CMS, mudança de URLs, replatform ou consolidação estrutural.

### 2.5 Page Template Audit
Auditoria por tipo de página:
- home
- institucional
- serviço
- produto
- curso
- local
- artigo
- evento
- FAQ
- landing page

### 2.6 Local SEO Audit
Auditoria focada em presença local, NAP, contexto geográfico, landings locais, reviews e consistência de entidade.

---

## 3. Score enterprise

Pontuação total: **0 a 100**

### 3.1 Pesos por domínio

| Domínio | Peso |
|---|---:|
| Técnica e indexabilidade | 20 |
| Arquitetura da informação | 20 |
| On-page semântico | 15 |
| Dados estruturados | 10 |
| GEO/AEO recuperabilidade | 10 |
| E-E-A-T e confiança | 10 |
| SEO local | 10 |
| Conversão e escalabilidade | 5 |
| **Total** | **100** |

### 3.2 Faixas de classificação

| Faixa | Classificação | Interpretação |
|---|---|---|
| 90-100 | Excelente | Base muito forte, ganhos incrementais |
| 75-89 | Forte | Boa maturidade com gaps relevantes |
| 60-74 | Intermediário | Base funcional, mas com limitações importantes |
| 40-59 | Fraco | Problemas significativos travando crescimento |
| 0-39 | Crítico | Estrutura severamente comprometida |

---

## 4. Regras de scoring

### 4.1 Técnica e indexabilidade
Avaliar:
- status codes;
- redirect chains;
- canonicals;
- robots.txt;
- sitemap;
- index/noindex;
- páginas órfãs;
- renderização;
- mobile;
- SSL;
- elegibilidade de páginas importantes.

### 4.2 Arquitetura da informação
Avaliar:
- hubs;
- clusters;
- duplicidade;
- slugs;
- taxonomias;
- profundidade de clique;
- páginas temporárias vs evergreen;
- coerência entre tipos de página;
- linking estrutural.

### 4.3 On-page semântico
Avaliar:
- title;
- meta description;
- H1;
- H2/H3;
- intenção;
- answer-first;
- escaneabilidade;
- CTA;
- FAQ;
- profundidade.

### 4.4 Dados estruturados
Avaliar:
- tipo correto por página;
- consistência com conteúdo visível;
- cobertura mínima de schemas essenciais;
- ausência de marcação enganosa.

### 4.5 GEO/AEO recuperabilidade
Avaliar:
- resposta direta;
- clareza;
- extraibilidade;
- organização em listas/tabelas;
- trechos citáveis;
- consistência terminológica;
- utilidade para answer engines.

### 4.6 E-E-A-T e confiança
Avaliar:
- experiência;
- autoria;
- credenciais;
- operação real;
- prova social;
- consistência de marca;
- legitimidade.

### 4.7 SEO local
Avaliar:
- cidade/região;
- NAP;
- páginas locais;
- presença local no site;
- reviews locais;
- contexto geográfico;
- adequação de entidade local.

### 4.8 Conversão e escalabilidade
Avaliar:
- CTAs;
- conexão entre conteúdo e negócio;
- prova social perto da decisão;
- capacidade de expansão por template/cluster;
- conexão entre editorial e comercial.

---

## 5. Matriz de severidade

| Severidade | Definição | Exemplo |
|---|---|---|
| S0 - Blocker | Impede rastreamento, indexação ou integridade estrutural crítica | canonical errado em massa, bloqueio indevido em robots |
| S1 - Crítico | Prejudica fortemente SEO/GEO/AEO ou conversão estrutural | canibalização grave, noindex indevido, home sem entidade |
| S2 - Alto | Afeta relevância, cobertura de intenção ou entendimento da página | schema ausente em páginas-chave, titles ruins em cluster principal |
| S3 - Médio | Afeta qualidade, clareza, competitividade ou citabilidade | FAQ fraca, subtítulos ruins, CTA genérico |
| S4 - Baixo | Refinamento incremental | microcopy, pequenos ajustes de metadata |

---

## 6. Matriz de impacto x esforço

Todo item deve receber:

- impacto: alto / médio / baixo
- esforço: alto / médio / baixo
- horizonte: imediato / curto prazo / médio prazo / estrutural

---

## 7. Tipos de issue

| Código | Tipo |
|---|---|
| TECH | Técnico |
| IA | Arquitetura da informação |
| IDX | Indexação |
| ONP | On-page |
| SCH | Schema |
| GEO | GEO/AEO |
| EAT | E-E-A-T |
| LOC | SEO local |
| CRO | Conversão |
| CNT | Conteúdo |
| LNK | Linking interno |
| MIG | Migração / legado |

---

## 8. Checklist master

### 8.1 Técnica e indexação
- [ ] páginas estratégicas retornam 200
- [ ] redirects usam 301 corretamente
- [ ] não há redirect chains relevantes
- [ ] canonical está coerente
- [ ] páginas críticas não estão em noindex indevido
- [ ] páginas utilitárias não indexam sem necessidade
- [ ] sitemap contém apenas URLs indexáveis
- [ ] robots.txt não bloqueia conteúdo estratégico
- [ ] páginas importantes não estão órfãs
- [ ] renderização permite leitura do conteúdo principal

### 8.2 Arquitetura
- [ ] existe 1 URL principal por intenção
- [ ] hubs estão claros
- [ ] clusters estão conectados
- [ ] slugs são limpos
- [ ] páginas legadas têm tratamento claro
- [ ] páginas temporárias têm política definida
- [ ] taxonomias não criam ruído
- [ ] páginas institucionais e comerciais não competem entre si

### 8.3 On-page
- [ ] title representa a intenção principal
- [ ] meta description é específica
- [ ] H1 está alinhado à URL
- [ ] a abertura responde rápido ao tema
- [ ] subtítulos seguem lógica
- [ ] a página é escaneável
- [ ] FAQ é útil quando necessária
- [ ] CTA está claro
- [ ] a profundidade é suficiente

### 8.4 Schema
- [ ] schema corresponde ao tipo da página
- [ ] schema reflete conteúdo real
- [ ] breadcrumb existe quando aplicável
- [ ] pages local/business têm schema coerente
- [ ] cursos usam Course
- [ ] eventos usam Event
- [ ] serviços usam Service
- [ ] reviews não são inflados artificialmente

### 8.5 GEO/AEO
- [ ] a página responde rapidamente ao tema
- [ ] existe bloco sintético e citável
- [ ] perguntas explícitas são respondidas
- [ ] listas/tabelas melhoram extração
- [ ] o conteúdo funciona sem depender só de design
- [ ] há contexto suficiente para recuperação sem ambiguidade

### 8.6 E-E-A-T
- [ ] entidade responsável está clara
- [ ] há prova de experiência real
- [ ] há sinais de operação real
- [ ] contato, endereço ou legitimidade aparecem
- [ ] reviews/depoimentos são usados corretamente
- [ ] expertise é demonstrada, não apenas alegada

### 8.7 Local
- [ ] cidade/região aparecem nas páginas certas
- [ ] NAP é consistente
- [ ] contato local está claro
- [ ] páginas locais existem quando necessário
- [ ] mapa/contexto geográfico aparece
- [ ] a entidade local é compreensível

### 8.8 Conversão
- [ ] CTA principal está claro
- [ ] prova social aparece perto da decisão
- [ ] o site oferece caminhos fáceis para contato
- [ ] páginas editoriais apoiam páginas comerciais
- [ ] páginas comerciais não terminam sem próximo passo

---

## 9. GEO/AEO: níveis de maturidade da recomendação

Toda recomendação específica de GEO/AEO deve ser classificada em:

| Nível | Categoria |
|---|---|
| G1 | Boa prática consolidada |
| G2 | Boa prática forte, mas emergente |
| G3 | Hipótese experimental / observacional |

### Exemplos
- resposta direta no início: **G1**
- FAQ contextual e útil: **G1**
- blocos sintéticos de recuperação: **G2**
- táticas especulativas para citabilidade em LLMs: **G3**

---

## 10. Output obrigatório da skill-mãe

Toda auditoria deve sair em 8 blocos:

1. **Executive Summary**
2. **Scorecard**
3. **Critical Issues**
4. **Opportunity Backlog**
5. **URL / Template Analysis**
6. **Issue Log**
7. **30/60/90 Day Plan**
8. **Acceptance Criteria**

---

## 11. Comandos da skill-mãe

### `/seo-geo enterprise audit <domínio>`
Auditoria completa com score, severidade, backlog e plano.

### `/seo-geo enterprise monthly <domínio>`
Relatório mensal comparativo.

### `/seo-geo enterprise quarterly <domínio>`
Relatório trimestral completo.

### `/seo-geo enterprise migration <domínio>`
Auditoria orientada a migração e legado.

### `/seo-geo enterprise page <url>`
Análise detalhada de URL com remediação.

### `/seo-geo enterprise local <domínio>`
Auditoria local aprofundada.

---

# PARTE 2 — SKILL-FILHA ENTERPRISE-LITE: TÉCNICA / ARQUITETURA

## Nome interno
`seo-geo-enterprise-lite-tech-architecture`

## Objetivo

Esta skill existe para auditar e melhorar a base estrutural do site.

Ela deve responder:
- o site pode ser rastreado corretamente?
- as páginas certas podem indexar?
- existe uma URL principal por intenção?
- há duplicidade estrutural?
- a arquitetura ajuda SEO e GEO?
- o schema está coerente com o tipo de página?

---

## 1. Escopo

### Inclui
- status code
- redirects
- canonical
- robots.txt
- sitemap
- index/noindex
- páginas órfãs
- slugs
- hubs e clusters
- duplicidade estrutural
- taxonomias
- schema
- SEO local técnico

### Não inclui como foco principal
- reescrita de copy
- profundidade editorial
- FAQ writing
- CRO textual

---

## 2. Score enterprise-lite técnico

Pontuação total: **0 a 100**

| Domínio | Peso |
|---|---:|
| Técnica e indexabilidade | 35 |
| Arquitetura da informação | 35 |
| Dados estruturados | 15 |
| SEO local técnico | 15 |
| **Total** | **100** |

### Faixas
| Faixa | Classificação |
|---|---|
| 90-100 | Excelente |
| 75-89 | Forte |
| 60-74 | Intermediário |
| 40-59 | Fraco |
| 0-39 | Crítico |

---

## 3. Severidade

| Nível | Nome | Definição |
|---|---|---|
| S0 | Blocker | Impede rastreamento, indexação ou integridade estrutural |
| S1 | Crítico | Prejudica fortemente arquitetura, canonicalização ou elegibilidade |
| S2 | Alto | Afeta páginas-chave ou clusters importantes |
| S3 | Médio | Impacta qualidade estrutural ou escalabilidade |
| S4 | Baixo | Refinamento incremental |

---

## 4. Checklist técnico resumido

### Técnica e indexação
- [ ] páginas estratégicas retornam 200
- [ ] redirects usam 301 corretamente
- [ ] não existem chains relevantes
- [ ] canonical está coerente
- [ ] páginas críticas não estão em noindex indevido
- [ ] páginas utilitárias não estão indexando sem necessidade
- [ ] robots.txt não bloqueia conteúdo estratégico
- [ ] sitemap contém apenas URLs indexáveis
- [ ] páginas importantes não estão órfãs

### Arquitetura
- [ ] existe 1 URL principal por intenção
- [ ] hubs principais estão definidos
- [ ] clusters estão conectados
- [ ] slugs são limpos
- [ ] páginas temporárias têm política clara
- [ ] taxonomias não criam ruído
- [ ] páginas institucionais e comerciais não competem entre si
- [ ] linking estrutural sustenta navegação e contexto

### Schema
- [ ] schema corresponde ao tipo da página
- [ ] schema reflete conteúdo visível
- [ ] Organization / LocalBusiness existem quando aplicável
- [ ] Service / Course / Event / Product / Article estão corretos quando aplicável
- [ ] BreadcrumbList existe quando necessário

### SEO local técnico
- [ ] NAP consistente
- [ ] páginas locais possuem elegibilidade técnica
- [ ] contato local está acessível
- [ ] entidade geográfica está clara

---

## 5. Output padrão da skill técnica

### Bloco 1 — Resumo técnico executivo
- score total
- maior risco estrutural
- maior oportunidade estrutural

### Bloco 2 — Scorecard técnico
| Domínio | Nota | Comentário |
|---|---:|---|

### Bloco 3 — Problemas críticos
Listar apenas S0, S1 e S2 mais importantes.

### Bloco 4 — Issue Log técnico
| Issue ID | Tipo | Severidade | Impacto | Esforço | Escopo | Evidência | Recomendação | Owner |
|---|---|---|---|---|---|---|---|---|

### Bloco 5 — Ações por URL ou template
| URL / Template | Status ideal | Problema | Ação recomendada | Prioridade |
|---|---|---|---|---|

### Bloco 6 — Roadmap técnico
- imediato
- curto prazo
- estrutural

---

## 6. Regras de decisão da skill técnica

### Quando recomendar redirect
- duplicidade clara
- URL legada
- página melhor já existe para a mesma intenção
- slug ruim sem valor estratégico

### Quando recomendar noindex
- utilitária
- temporal sem valor evergreen
- taxonomia fraca
- autor sem função estratégica
- página fina sem papel estrutural

### Quando recomendar manter index
- intenção clara
- papel estrutural evidente
- conteúdo suficiente
- valor comercial, local ou editorial

---

## 7. Comandos da skill técnica

### `/seo-tech-lite audit <domínio>`
Auditoria técnica resumida.

### `/seo-tech-lite architecture <domínio>`
Foco em hubs, clusters, canônicos e estrutura.

### `/seo-tech-lite schema <url>`
Audita schema e gaps de entidade.

### `/seo-tech-lite migration <domínio>`
Foco em legado, redirects e canonicals.

### `/seo-tech-lite local <domínio>`
Audita base técnica de SEO local.

---

# PARTE 3 — SKILL-FILHA ENTERPRISE-LITE: CONTEÚDO / GEO / AEO

## Nome interno
`seo-geo-enterprise-lite-content-entity`

## Objetivo

Esta skill existe para auditar e melhorar a camada semântica, editorial e comercial.

Ela deve responder:
- a página deixa clara sua intenção?
- o conteúdo responde rápido e aprofunda bem?
- a página é recuperável por answer engines e mecanismos generativos?
- há sinais reais de experiência, confiança e legitimidade?
- o conteúdo leva o usuário ao próximo passo?

---

## 1. Escopo

### Inclui
- intenção de busca
- title
- meta description
- H1/H2/H3
- answer-first
- semântica
- FAQ
- GEO/AEO recuperabilidade
- consistência terminológica
- E-E-A-T
- SEO local semântico
- CTAs
- prova social
- estrutura por tipo de página

### Não inclui como foco principal
- robots
- sitemap
- canonical técnico
- schema profundo
- renderização técnica

---

## 2. Score enterprise-lite conteúdo

Pontuação total: **0 a 100**

| Domínio | Peso |
|---|---:|
| On-page semântico | 30 |
| GEO/AEO recuperabilidade | 25 |
| E-E-A-T e confiança | 20 |
| SEO local semântico | 10 |
| Conversão | 15 |
| **Total** | **100** |

### Faixas
| Faixa | Classificação |
|---|---|
| 90-100 | Excelente |
| 75-89 | Forte |
| 60-74 | Intermediário |
| 40-59 | Fraco |
| 0-39 | Crítico |

---

## 3. Severidade

| Nível | Nome | Definição |
|---|---|---|
| S0 | Blocker | A página falha gravemente em comunicar sua função ou confiança |
| S1 | Crítico | Intenção difusa ou conteúdo comprometendo performance orgânica/comercial |
| S2 | Alto | Lacunas relevantes de resposta, estrutura ou autoridade |
| S3 | Médio | Qualidade existe, mas execução é genérica ou incompleta |
| S4 | Baixo | Refinamentos de copy e organização |

---

## 4. Checklist de conteúdo resumido

### On-page
- [ ] title representa a intenção principal
- [ ] meta description é específica e útil
- [ ] H1 está alinhado à proposta da URL
- [ ] a página responde rápido ao tema
- [ ] subtítulos seguem lógica clara
- [ ] a escaneabilidade está boa
- [ ] a página evita introdução prolixa
- [ ] a profundidade é suficiente
- [ ] FAQ existe quando faz sentido
- [ ] CTA está claro

### GEO/AEO
- [ ] existe bloco sintético e citável
- [ ] perguntas explícitas são respondidas
- [ ] o conteúdo tem clareza terminológica
- [ ] existem listas/tabelas úteis quando necessário
- [ ] a página funciona sem depender de design visual
- [ ] o conteúdo pode ser recuperado sem ambiguidade
- [ ] answer-first aparece quando apropriado

### E-E-A-T
- [ ] entidade responsável está clara
- [ ] existem sinais de experiência real
- [ ] há prova de operação real
- [ ] contato e legitimidade aparecem
- [ ] reviews/depoimentos são usados corretamente
- [ ] expertise é demonstrada, não apenas alegada

### SEO local semântico
- [ ] cidade/região aparecem naturalmente
- [ ] contexto local existe nas páginas certas
- [ ] a página ajuda o usuário local a se orientar
- [ ] intenção geográfica está clara quando aplicável

### Conversão
- [ ] CTA principal está claro
- [ ] CTA secundário existe quando necessário
- [ ] prova social está perto da decisão
- [ ] a página não termina sem próximo passo
- [ ] editorial conecta com páginas comerciais quando aplicável

---

## 5. Output padrão da skill de conteúdo

### Bloco 1 — Resumo editorial executivo
- score total
- maior problema de clareza/intenção
- maior oportunidade de GEO/AEO

### Bloco 2 — Scorecard editorial
| Domínio | Nota | Comentário |
|---|---:|---|

### Bloco 3 — Principais gaps
Listar os 5 a 10 problemas mais importantes.

### Bloco 4 — Recomendação por página
| URL | Intenção principal | Title recomendado | H1 recomendado | Ação prioritária |
|---|---|---|---|---|

### Bloco 5 — Estrutura recomendada
- abertura answer-first
- H2/H3 sugeridos
- FAQ sugerida
- CTA principal
- CTA secundário

### Bloco 6 — Prioridades
- quick wins
- curto prazo
- estrutural

---

## 6. Regras por tipo de página

### Home
Avaliar:
- proposta de valor
- clareza da entidade
- serviços principais
- diferenciais
- FAQ
- prova social
- contexto local
- CTA

### Serviço
Avaliar:
- problema resolvido
- para quem é
- como funciona
- prova
- FAQ
- CTA
- contexto local

### Curso
Avaliar:
- público-alvo
- pré-requisitos
- duração
- certificação
- o que inclui
- FAQ
- CTA

### Local
Avaliar:
- cidade
- contexto geográfico
- confiança local
- clareza de atendimento

### Artigo
Avaliar:
- intenção
- resposta inicial
- profundidade
- clareza
- links internos
- CTA contextual

### Evento
Avaliar:
- clareza de data e proposta
- elegibilidade
- detalhes
- CTA

---

## 7. Regras de reescrita

Quando a tarefa for reescrever uma página, sempre gerar:

- title recomendado
- meta description recomendada
- H1 recomendado
- abertura answer-first
- estrutura H2/H3
- FAQ sugerida
- CTA principal
- CTA secundário
- observações de GEO/AEO
- observações de E-E-A-T

---

## 8. GEO/AEO: classificação das recomendações

Toda recomendação específica deve ser classificada:

| Nível | Categoria |
|---|---|
| G1 | Boa prática consolidada |
| G2 | Boa prática forte, mas emergente |
| G3 | Hipótese experimental |

### Exemplos
- clareza de resposta direta: **G1**
- FAQ útil e contextual: **G1**
- blocos sintéticos de resposta para recuperação: **G2**
- experimentos muito específicos para citabilidade em LLMs: **G3**

---

## 9. Comandos da skill de conteúdo

### `/seo-content-lite audit <domínio>`
Auditoria semântica resumida.

### `/seo-content-lite page <url>`
Auditoria detalhada de uma URL.

### `/seo-content-lite rewrite <url>`
Reescreve a página com foco em SEO/GEO/AEO.

### `/seo-content-lite template <tipo>`
Cria template ideal por tipo de página.

### `/seo-content-lite local <domínio>`
Foco na camada semântica local.

---

# PARTE 4 — TEMPLATE PADRONIZADO DE SAÍDA REAL DE AUDITORIA

# Auditoria SEO / GEO / AEO — Relatório Executivo e Operacional

**Cliente / Projeto:**  
**Domínio:**  
**Escopo auditado:**  
**Modo da auditoria:** Monthly / Quarterly / Release / Migration / Template / Local  
**Data:**  
**Responsável:**  

---

## 1. Executive Summary

### Score total
**XX/100**

### Classificação
**Excelente / Forte / Intermediário / Fraco / Crítico**

### Resumo executivo
[Escrever 1 a 3 parágrafos objetivos respondendo:
- qual é o estado geral do site;
- onde está o maior risco;
- onde está a maior oportunidade;
- o que precisa ser feito primeiro.]

### Maior risco atual
- [descrever]

### Maior oportunidade atual
- [descrever]

---

## 2. Scorecard

| Domínio | Nota | Peso | Comentário |
|---|---:|---:|---|
| Técnica e indexabilidade |  | 20 |  |
| Arquitetura da informação |  | 20 |  |
| On-page semântico |  | 15 |  |
| Dados estruturados |  | 10 |  |
| GEO/AEO recuperabilidade |  | 10 |  |
| E-E-A-T e confiança |  | 10 |  |
| SEO local |  | 10 |  |
| Conversão e escalabilidade |  | 5 |  |
| **Total** |  | **100** |  |

---

## 3. Principais achados

### 3.1 O que está funcionando bem
- [item 1]
- [item 2]
- [item 3]

### 3.2 Falhas críticas
- [item 1]
- [item 2]
- [item 3]

### 3.3 Oportunidades de alto impacto
- [item 1]
- [item 2]
- [item 3]

---

## 4. Issue Log

| Issue ID | Tipo | Severidade | Impacto | Esforço | URL / Escopo | Evidência | Recomendação | Owner |
|---|---|---|---|---|---|---|---|---|
| TECH-001 | TECH | S1 | Alto | Médio | / | [evidência] | [ação] | Dev |
| IA-001 | IA | S1 | Alto | Alto | Sitewide | [evidência] | [ação] | SEO |
| ONP-001 | ONP | S2 | Médio | Baixo | /servico/ | [evidência] | [ação] | Conteúdo |

---

## 5. Análise por URL ou template

### 5.1 Tabela resumida

| URL / Template | Tipo | Intenção principal | Status ideal | Nota | Principal gap | Ação recomendada | Prioridade |
|---|---|---|---|---:|---|---|---|
| / | Home |  | Index |  |  |  |  |
| /contato/ | Contato |  | Index |  |  |  |  |
| /servico-x/ | Serviço |  | Index |  |  |  |  |
| /blog/post-y/ | Artigo |  | Index / Noindex |  |  |  |  |

### 5.2 Detalhamento por URL

#### URL
`[colar URL]`

**Tipo:**  
**Intenção principal:**  
**Status ideal:** Index / Noindex / Redirect / Merge / Rebuild  
**Nota resumida:** XX/100  

**Achados principais**
- [item 1]
- [item 2]
- [item 3]

**Recomendações**
- Title recomendado:
- Meta description recomendada:
- H1 recomendado:
- Estrutura sugerida:
- Schema recomendado:
- Links internos sugeridos:
- FAQ sugerida:
- CTA principal:
- CTA secundário:

**Prioridade**
- Imediata / Curto prazo / Médio prazo / Estrutural

---

## 6. Backlog priorizado

### 6.1 Quick wins
| Item | Impacto | Esforço | Owner | Prazo |
|---|---|---|---|---|
| [ação] | Alto | Baixo | SEO | 7 dias |
| [ação] | Médio | Baixo | Conteúdo | 14 dias |

### 6.2 Melhorias de curto prazo
| Item | Impacto | Esforço | Owner | Prazo |
|---|---|---|---|---|
| [ação] | Alto | Médio | Dev/SEO | 30 dias |

### 6.3 Melhorias estruturais
| Item | Impacto | Esforço | Owner | Prazo |
|---|---|---|---|---|
| [ação] | Alto | Alto | Produto/Dev/SEO | 60-90 dias |

---

## 7. Plano 30 / 60 / 90 dias

### 0–30 dias
- [ação 1]
- [ação 2]
- [ação 3]

### 31–60 dias
- [ação 1]
- [ação 2]
- [ação 3]

### 61–90 dias
- [ação 1]
- [ação 2]
- [ação 3]

---

## 8. Riscos e dependências

### Riscos
- [risco 1]
- [risco 2]

### Dependências
- [dependência 1]
- [dependência 2]

---

## 9. Critérios de aceite

A auditoria será considerada endereçada quando:

- [ ] páginas críticas estiverem tecnicamente elegíveis
- [ ] duplicidades relevantes tiverem sido consolidadas
- [ ] principais gaps de intenção tiverem sido resolvidos
- [ ] pages money tiverem estrutura adequada
- [ ] schema estiver coerente nas páginas-chave
- [ ] páginas locais estiverem claras quando aplicável
- [ ] backlog crítico estiver concluído

---

## 10. Relatório comparativo recorrente (opcional)

### Score anterior
**XX/100**

### Score atual
**XX/100**

### Delta
**+X / -X**

### Evolução

#### Melhorias validadas
- [item 1]
- [item 2]

#### Problemas persistentes
- [item 1]
- [item 2]

#### Regressões
- [item 1]
- [item 2]

#### Próximo foco
- [item 1]
- [item 2]

---

# PARTE 5 — INSTRUÇÃO DE USO DA SUITE

## Quando usar a skill-mãe
Use a skill-mãe quando precisar:
- de score global;
- de governança;
- de backlog consolidado;
- de relatório executivo;
- de comparação recorrente.

## Quando usar a skill técnica
Use a skill técnica quando o problema parecer estar em:
- indexação;
- canonicals;
- robots;
- sitemap;
- redirects;
- arquitetura de URLs;
- schema;
- local técnico.

## Quando usar a skill de conteúdo
Use a skill de conteúdo quando o problema parecer estar em:
- intenção;
- resposta fraca;
- conteúdo genérico;
- GEO/AEO fraco;
- FAQ ruim;
- baixa confiança;
- SEO local semântico;
- conversão ruim.

---

# PARTE 6 — REGRA FINAL DA SUITE

Se houver conflito entre:
- volume de páginas e qualidade estrutural;
- texto bonito e texto útil;
- hype de GEO e fundamentos reais;
- desejo de impressionar e governança repetível;

esta suite deve sempre escolher:
- precisão,
- clareza,
- arquitetura,
- evidência,
- utilidade operacional,
- consistência ao longo do tempo.