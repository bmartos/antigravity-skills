---
name: website-tagging-architect
description: End-to-end framework for website analytics auditing, automated crawling, Playwright diagnostics, native GTM API refactoring (Draft Workspace), GitHub PR dataLayer enrichment, and iterative post-implementation re-validation loop until 100% closure. Use when asked to audit, specify, refactor, or implement GTM/GA4/Meta CAPI tagging on any website.
---

# 🏷️ Website Tagging Architect Skill

Esta skill estabelece a **metodologia universal em 7 etapas** para auditoria, especificação (PRD), diagnóstico automatizado, refatoramento nativo no GTM via API, enriquecimento de DataLayer no GitHub e **loop de re-validação até o fechamento de ciclo com 100% de qualidade**.

---

## 🔄 Fluxo de Trabalho Universal em 7 Etapas

```
┌──────────────────────────────────────────────────────────────────────────────────┐
│  ETAPA 1: ALINHAMENTO DE NEGÓCIO & STACK (GRILLING / Q&A PERGUNTA A PERGUNTA)     │
│  - Definir modelo de negócio (Lead Gen, E-commerce, SaaS, Conteúdo)              │
│  - Definir stack de mídia (GA4, GTM, Meta CAPI, Google Ads, TikTok, HubSpot)     │
│  - Estratégia de LGPD & Consent Mode v2                                          │
└──────────────────────────────────────────────────────────────────────────────────┘
                                       │
┌──────────────────────────────────────────────────────────────────────────────────┐
│  ETAPA 2: VARREDURA E CRAWLING AUTOMÁTICO DE URLS                                │
│  - Mapear mapa de URLs internas, ancoras de seção, links outbound e formulários  │
└──────────────────────────────────────────────────────────────────────────────────┘
                                       │
┌──────────────────────────────────────────────────────────────────────────────────┐
│  ETAPA 3: DIAGNÓSTICO AO VIVO VIA PLAYWRIGHT & TAG ASSISTANT                     │
│  - Executar headless browser simulando carregamento, scroll (25-90%) e cliques    │
│  - Capturar payloads do dataLayer e requisições /g/collect / Meta                │
│  - Mapear lacunas (eventos genéricos, falta de valores, scroll incompleto)       │
└──────────────────────────────────────────────────────────────────────────────────┘
                                       │
┌──────────────────────────────────────────────────────────────────────────────────┐
│  ETAPA 4: VALIDAÇÃO DE ACESSOS (GIT & GTM API)                                   │
│  - Verificar repositório Git local/remoto (acesso a código para criar PR)        │
│  - Verificar autenticação OAuth/API do Google Tag Manager (acesso a container)   │
└──────────────────────────────────────────────────────────────────────────────────┘
                                       │
┌──────────────────────────────────────────────────────────────────────────────────┐
│  ETAPA 5: ENRIQUECIMENTO DE DATALAYER NO CÓDIGO & GITHUB PR                      │
│  - Injetar eventos nativos oficiais (generate_lead, purchase, select_item)       │
│  - Adicionar parâmetros de valor (value, currency, product_name, click_location) │
│  - Rodar suíte de testes unitários                                               │
│  - Criar Branch, Commit, Push e gerar Link do Pull Request no GitHub             │
└──────────────────────────────────────────────────────────────────────────────────┘
                                       │
┌──────────────────────────────────────────────────────────────────────────────────┐
│  ETAPA 6: REFATORAMENTO NATIVO NO GTM VIA API (MODO RASCUNHO/DRAFT)              │
│  - Habilitar Built-in Variables (Click URL, Scroll Depth Threshold, etc.)        │
│  - Substituir customEvents por Gatilhos Nativos (Link Click, Native Scroll)      │
│  - Criar Tags Nativas (GA4, Meta CAPI, Google Ads, TikTok, Consent Mode v2)     │
│  - Salvar em Workspace Rascunho e gerar Link do GTM para Validação do Usuário    │
└──────────────────────────────────────────────────────────────────────────────────┘
                                       │
┌──────────────────────────────────────────────────────────────────────────────────┐
│  ETAPA 7: RE-VALIDAÇÃO PÓS-CONFIRMAÇÃO & LOOP DE FECHAMENTO (QA CICLO FECHADO)   │
│  - Após confirmação do usuário (merge do PR e publicação do GTM):                │
│  - Rodar nova rodada de diagnósticos via Playwright na URL atualizada/produção.   │
│  - Se houver divergências ou falhas: VOLTAR À ETAPA 2 e repetir os ajustes.      │
│  - Quando 100% dos requisitos estiverem validados: Gerar Relatório de Fechamento.│
└──────────────────────────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Detalhes de Execução por Etapa

### Etapa 1: Alinhamento Interativo (Grilling)
- Fazer perguntas **uma por uma** ao usuário para mapear:
  1. Tipo de plataforma (Lead Gen vs E-commerce vs SaaS).
  2. Ferramentas de destino (GA4, Meta CAPI, Google Ads, TikTok, LinkedIn, HubSpot).
  3. Arquitetura (Client-Side vs Híbrido com GTM Server-Side).
  4. Privacidade (Consent Mode v2 + CMP).

### Etapa 2: Crawling Automático
- Executar scraper/Playwright para inventariar todas as URLs, âncoras (`#`), links `wa.me`, links externos e formulários.

### Etapa 3: Diagnóstico com Playwright
- Rodar script headless que intercepta `window.dataLayer` e requisições `/g/collect` durante eventos de página, rolagem (25%, 50%, 75%, 90%) e cliques em botões/links.

### Etapa 4: Validação de Acessos
- **GitHub:** Verificar remotos Git (`git remote -v`). Se houver acesso, alterar o código e abrir Pull Request. Se não houver, gerar guia de instrução para os desenvolvedores.
- **GTM API:** Testar tokens OAuth da API do Tag Manager. Se houver acesso, alterar o container via API em modo **Rascunho / Draft Workspace**. Se não houver, gerar guia manual para o painel do GTM.

### Etapa 5: Enriquecimento no Código (GitHub PR)
- Adicionar no código frontend (Next.js, React, HTML) eventos oficiais nativos (`generate_lead`, `purchase`, `select_item`) com objetos completos (`value`, `currency`, `product_name`, `click_location`).
- Executar testes automatizados (`npm test` / `vitest`).
- Criar branch `feat/datalayer-native-enrichment`, fazer commit, push e disponibilizar o link de Pull Request do GitHub.

### Etapa 6: Refatoramento Nativo no GTM (Draft Workspace)
- **Prioridade Absoluta:** Utilizar **Gatilhos Nativos da Plataforma** (ex.: `linkClick`, `scrollDepth`, `formSubmission`) em vez de dependência excessiva em `customEvent`.
- Habilitar Variáveis Nativas (`Click URL`, `Click Text`, `Scroll Depth Threshold`).
- Criar Tags Nativas do GA4, Meta Pixel/CAPI, Google Ads e Consent Mode v2.
- **Manter em Workspace Rascunho (Draft)** e fornecer a URL do GTM para o usuário revisar e publicar.

### Etapa 7: Re-Validação Pós-Confirmação & Fechamento de Ciclo
- **Trigger:** Acionada após o usuário confirmar o merge do PR e a publicação no GTM.
- **Ação:** Executar novamente o script de teste do Playwright em ambiente de homologação/produção.
- **Critério de Aceite:**
  - Se 100% das requisições e eventos do dataLayer baterem exatamente com a especificação do PRD ➔ Emitir o **Relatório Final de Fechamento de Tagueamento** e encerrar o ciclo.
  - Se houver qualquer falha, disparo duplo ou parâmetro ausente ➔ **Retornar automaticamente à Etapa 2** e iterar as correções até a perfeição.

---

## 🛡️ Guardrails

1. **Nunca publicar direto no GTM sem aprovação:** Todas as alterações via API devem ser feitas em Workspace Rascunho (Draft).
2. **Priorizar Padrões Nativos:** Evitar criar `customEvent` quando o GTM possui acionador nativo para a mesma funcionalidade.
3. **Validação por Evidência:** Nunca declarar o tagueamento concluído sem antes rodar a Etapa 7 via Playwright e confirmar o disparo real do tráfego.
