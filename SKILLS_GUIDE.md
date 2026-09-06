# 📚 Guia Definitivo e Inventário de Skills Unificadas (.agents/skills)

Este documento descreve a estrutura, o catálogo de competências e as melhores práticas de uso para o repositório centralizado de **Skills** do seu ambiente de desenvolvimento (`C:\Users\bmart\.antigravity\.agents\skills`).

---

## 🎯 O que é uma Skill?
Uma **Skill** é um módulo de instrução especializada (composto por um `SKILL.md` e opcionalmente scripts, referências ou templates) que ensina o agente de IA como executar tarefas complexas com precisão, seguindo padrões rigorosos de engenharia, arquitetura, produto e marketing.

---

## 🛠️ Catálogo Completo de Skills Unificadas

Ao todo, o ambiente conta com **mais de 100 Skills Nativas**, divididas por domínios:

---

### 💻 1. SKILLS TÉCNICAS (Engenharia, Arquitetura e IA)

#### 🏗️ Arquitetura, Design e Modelagem de Software
- **`codebase-design`**: Diretrizes para design e estruturação de código limpo e sustentável.
- **`domain-modeling`**: Modelagem de domínio (DDD), tipos e lógica de negócios.
- **`improve-codebase-architecture`**: Análise e refatoração arquitetural de codebases legadas ou complexas.
- **`setup-ts-deep-modules`**: Configuração e arquitetura avançada de módulos TypeScript.

#### 🧪 Desenvolvimento, Testes e Qualidade
- **`implement`**: Execução focada na implementação de features com alta qualidade.
- **`tdd`**: Desenvolvimento Orientado a Testes (Test-Driven Development) rigoroso.
- **`diagnosing-bugs`**: Metodologia sistemática para rastreamento, reprodução e correção de bugs.
- **`code-review`**: Revisão técnica de código, segurança e performance.
- **`resolving-merge-conflicts`**: Resolução segura e inteligente de conflitos de merge no Git.

#### 🔀 Workflow, Triage e Navegação no Codebase
- **`triage`**: Triagem e categorização rápida de issues, bugs e tarefas.
- **`wayfinder`**: Mapeamento e navegação eficiente em novos repositórios ou codebases extensos.
- **`wizard`**: Assistente para automação e execução de tarefas complexas de desenvolvimento.
- **`git-guardrails-claude-code`**: Proteções e regras de segurança para operações de Git via IA.
- **`setup-pre-commit`**: Configuração de hooks automatizados de pre-commit.

#### ⚙️ Bancos de Dados, Automações e Backend
- **`supabase`**: Integração completa com Supabase (Auth, Database, Edge Functions, Realtime, Storage, Vector).
- **`supabase-postgres-best-practices`**: Otimização de performance, indexação e boas práticas SQL/Postgres.
- **`n8n-architect`**: Criação, edição, validação e sincronização de workflows de automação no n8n.
- **`website-tagging-architect`**: Metodologia em 7 etapas para auditoria de analytics, Playwright diagnostics, refatoramento nativo de GTM via API, DataLayer no GitHub PR e loop de re-validação.

#### 🎨 Mídia, Geração de Arte, Jogos e Web Apps (Higgsfield AI)
- **`higgsfield-generate`**: Geração de imagens, vídeos, áudios e assets 3D por IA.
- **`higgsfield-websites`**: Criação, edição e deploy de websites completos React/TanStack na Cloudflare.
- **`higgsfield-game-generation`**: Criação de jogos de navegador jogáveis e sprites/assets de jogos.
- **`higgsfield-product-photoshoot`**: Fotos profissionais de produtos, e-commerce e criativos de marketing.
- **`higgsfield-marketplace-cards`**: Criação de cards de produtos e conteúdo A+ para e-commerce.
- **`higgsfield-soul-id`**: Treinamento de avatares/gêmeos digitais consistentes (Soul ID).
- **`higgsfield-video-explainer`**: Produção automatizada de vídeos explicativos e narrados.

---

### 📊 2. SKILLS DE NEGÓCIO, PRODUTO E PRODUTIVIDADE

#### 📋 Especificação de Produto e Gestão de Tarefas
- **`to-spec`**: Transformação de ideias, conversas ou briefings em especificações técnicas detalhadas.
- **`to-tickets`**: Quebra de especificações e requisitos em tickets/tasks acionáveis.
- **`prototype`**: Prototipagem rápida de validação de negócios e MVP.
- **`research`**: Pesquisa de viabilidade técnica, bibliotecas e soluções de mercado.

#### 🤝 Alinhamento, Entrevistas e Tomada de Decisão
- **`grill-me`**: Entrevista interativa promovida pela IA para sabatinar o usuário e alinhar requisitos obscuros antes de codificar.
- **`grilling`**: Técnica de questionamento aprofundado para mitigar riscos de projeto.
- **`grill-with-docs`**: Alinhamento de requisitos confrontando com documentações existentes.
- **`wait-what`**: Pausa estratégica para esclarecer ambiguidades e premissas equivocadas.

#### 📝 Comunicação, Documentação e Transmissão de Conhecimento
- **`handoff`**: Geração de resumos e passagens de bastão entre sessões de trabalho ou times.
- **`claude-handoff`**: Handoff estruturado especificamente para sessões do Claude.
- **`teach`**: Explicação didática de conceitos técnicos e decisões de código.
- **`writing-for-agents`**: Escrita de prompts e documentações otimizadas para consumo por agentes de IA.
- **`to-questionnaire`**: Conversão de requisitos em formulários/questionários de levantamento.

#### ✍️ Estruturação de Conteúdo e Narrativa de Produto
- **`writing-shape`**: Formatação e estruturação da visão geral do produto.
- **`writing-beats`**: Definição dos marcos/momentos chave de uma narrativa ou apresentação.
- **`writing-fragments`**: Redação de trechos e componentes de conteúdo.
- **`loop-me`**: Criação de loops de feedback e melhoria contínua de produto.

---

### 🚀 3. SKILLS DE MARKETING & GROWTH

Conjunto consolidado de **49 Skills** originadas de `coreyhaines31/marketingskills`, cobrindo todo o ciclo de marketing, conversão, atração e retenção:

#### 🎯 Contexto Base & Produto
- **`product-marketing`**: Contexto central do produto/serviço utilizado por todas as outras skills de marketing.

#### 🔎 SEO & Arquitetura de Busca
- **`seo-audit`**, **`ai-seo`**, **`site-architecture`**, **`programmatic-seo`**, **`schema`**, **`aso`**

#### ⚡ CRO & Conversão de Páginas
- **`cro`**, **`signup`**, **`onboarding`**, **`popups`**, **`paywalls`**

#### ✍️ Copywriting & Conteúdo
- **`copywriting`**, **`copy-editing`**, **`content-strategy`**, **`cold-email`**, **`emails`**, **`social`**, **`video`**, **`image`**, **`sms`**

#### 📣 Mídia Paga & Experimentação
- **`ads`**, **`ad-creative`**, **`ab-testing`**, **`analytics`**, **`attribution`**

#### 📈 Growth, Retenção & Viralidade
- **`referrals`**, **`free-tools`**, **`churn-prevention`**, **`community-marketing`**, **`lead-magnets`**, **`co-marketing`**, **`marketing-loops`**

#### 💼 Vendas, GTM & Estratégia
- **`revops`**, **`sales-enablement`**, **`launch`**, **`pricing`**, **`competitors`**, **`competitor-profiling`**, **`directory-submissions`**, **`prospecting`**, **`public-relations`**, **`offers`**

#### 🧠 Estratégia, Pesquisa & Psicologia
- **`marketing-ideas`**, **`marketing-psychology`**, **`customer-research`**, **`marketing-plan`**, **`marketing-council`**

---

## 🚀 Como Usar as Skills

### 1. Invocação Direta na Mensagem
Sempre que for iniciar uma tarefa, mencione a Skill desejada ou o conceito relacionado na conversa:
- *"Execute uma revisão de código usando a skill `code-review`."*
- *"Quero criar um banco no Supabase seguindo as boas práticas da `supabase-postgres-best-practices`."*
- *"Planeje uma campanha de SEO usando a skill `ai-seo`."*
- *"Faça uma entrevista comigo usando `grill-me` para alinhar os requisitos antes de programar."*

### 2. Leitura Automática
Ao acionar uma Skill, o assistente abre o arquivo `SKILL.md` dentro de `.agents/skills/<nome-da-skill>` para carregar todas as regras e rotinas especializadas.
