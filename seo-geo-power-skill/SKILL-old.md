---
name: seo-geo-power-skill
description: >-
  Super skill unificada para SEO (Search Engine Optimization), GEO (Generative Engine Optimization) e AEO (Answer Engine Optimization). 
  Realiza auditorias completas de visibilidade em buscadores tradicionais e motores de IA (ChatGPT, Gemini, Perplexity, Claude, Google AI Overviews).
  Aplica os métodos de citabilidade de Princeton KDD 2024, valida rastreabilidade técnica, mapeia JSON-LD estruturado, planeja SEO programático e integra com CRO.
  Use esta skill para qualquer tarefa relacionada a auditoria de site, otimização de conteúdo para IA, criação de esquemas de metadados, análise de robots.txt ou melhorias de rankeamento e conversão.
---

# Power Skill: SEO, GEO & AEO (Otimização para Humanos e IA)

Esta skill unifica os conceitos de **SEO tradicional** (Search Engine Optimization), **GEO** (Generative Engine Optimization) e **AEO** (Answer Engine Optimization). Ela é construída sob a premissa de que a visibilidade em mecanismos de IA (como ChatGPT, Claude, Perplexity e Google AI Overviews) é uma extensão direta das boas práticas técnicas e de conteúdo recomendadas pelo Google, Moz e Semrush.

---

## 1. Diretrizes das Big Players (Google, Moz, Semrush)

Para validar e fundamentar esta Skill, seguimos as regras oficiais do mercado:
* **Google (Search Quality Rater & AI Overviews)**: O Google afirma que seus recursos de IA generativa usam os mesmos sistemas de classificação principais do buscador. Focar em conteúdo de alta qualidade, original e que responda à intenção de pesquisa do usuário é o caminho recomendado. hacks temporários são desencorajados.
* **Semrush (AI Visibility)**: A Semrush destaca que a autoridade de marca (menções no Reddit, Wikipedia, LinkedIn e mídias sociais) tem forte correlação com citações em respostas de LLMs.
* **Moz (Semantic Search & Featured Snippets)**: A Moz reforça a importância da estruturação de conteúdo ("Answer-First" - Resposta Direta de 1-2 frases no topo da página) e hierarquias semânticas claras de títulos (H1, H2, H3).

---

## 2. O Framework de 6 Camadas para Otimização

Qualquer análise ou otimização de site deve passar pelas seguintes etapas, em ordem de prioridade:

```
+-----------------------------------------------------------+
| CAMADA 1: Acessibilidade Técnica & Rastreabilidade de IA  |
| (robots.txt, Sitemap.xml, Velocidade, SSL)                |
+-----------------------------------------------------------+
                              |
+-----------------------------------------------------------+
| CAMADA 2: Estruturação Semântica & JSON-LD                |
| (Marcação de Schema, Metadados Open Graph)                |
+-----------------------------------------------------------+
                              |
+-----------------------------------------------------------+
| CAMADA 3: Conteúdo Answer-First & Hierarquia              |
| (Títulos Semânticos, Estrutura de Resposta Curta)         |
+-----------------------------------------------------------+
                              |
+-----------------------------------------------------------+
| CAMADA 4: Otimização GEO de Citação (Princeton KDD)       |
| (Estatísticas, Citações de Especialistas, Links Externos)  |
+-----------------------------------------------------------+
                              |
+-----------------------------------------------------------+
| CAMADA 5: E-E-A-T & Autoridade Externa                    |
| (Perfis de Autor, Backlinks e Menções Externas em Fóruns) |
+-----------------------------------------------------------+
                              |
+-----------------------------------------------------------+
| CAMADA 6: Escalabilidade (pSEO) & Conversão (CRO)         |
| (SEO Programático de Alta Qualidade, CTA de Alto Impacto) |
+-----------------------------------------------------------+
```

### Camada 1: Acessibilidade Técnica & Rastreabilidade de IA
* **Configuração de Robots.txt**:
  * **Permitir Citação**: Garantir que os robôs de citação direta de respostas tenham acesso total:
    * `OAI-SearchBot` (ChatGPT Search)
    * `PerplexityBot` (Perplexity)
    * `ClaudeBot` (Claude)
    * `Google-Extended` (Google AI Overviews / Gemini)
  * **Bloquear Treinamento (Se desejado)**: Impedir o uso do conteúdo para treino futuro de modelos sem bloquear o rastreamento ativo de respostas:
    * `GPTBot` (Treinamento OpenAI) -> `Disallow: /`
    * `anthropic-ai` (Treinamento Anthropic) -> `Disallow: /`
* **Performance & Renderização**: Tempo de carregamento rápido (Core Web Vitals) e renderização completa no servidor (SSR), essencial para que crawlers de IA efetuem o parse da página sem falhas de JavaScript.
* **Acessibilidade de Imagens**: Garantir que as imagens sejam carregadas usando tags HTML padrão (`<img>` com `src` e `alt`) em vez de propriedades de background de CSS, permitindo que crawlers e leitores indexem o conteúdo visual.

### Camada 2: Estruturação Semântica & JSON-LD
* **Mapeamento de Schema**: Adicionar marcações JSON-LD estruturadas para ajudar os LLMs a compreender o tipo de entidade da página:
  * `Article` ou `BlogPosting` para artigos de blog.
  * `FAQPage` para páginas de dúvidas frequentes.
  * `Product` com avaliações para e-commerce.
  * `LocalBusiness` ou `Organization` com propriedade `sameAs` conectando as redes sociais e fontes confiáveis oficiais.
  * `ImageObject` para vincular imagens cruciais (infográficos, diagramas) ao conteúdo principal e declarar legendas explícitas.

### Camada 3: Conteúdo Answer-First & Hierarquia
* **Método de Resposta Direta**: Iniciar artigos e seções principais com uma resposta clara e concisa (de até 240 caracteres) que responda diretamente à consulta principal.
* **Hierarquia de Títulos**: Utilizar títulos semânticos claros (`H1` único para a página, seguido de `H2` e `H3` estruturando subtemas) de forma a facilitar o RAG (Retrieval-Augmented Generation) de robôs de busca.

### Camada 4: Otimização GEO de Citação (Princeton KDD 2024)
Aplica melhorias de conteúdo ordenadas por impacto estatístico comprovado em motores de busca generativa (Perplexity e ChatGPT):
1. **Cite Sources (+30-115% de Citabilidade)**: Adicione links externos para fontes de alta autoridade para provar suas afirmações.
2. **Add Statistics (+40%)**: Substitua afirmações vagas por números concretos, porcentagens e datas.
3. **Quotation Addition (+30-40%)**: Insira citações diretas de especialistas reconhecidos no formato: `"Texto da Citação" — Nome, Cargo, Organização, Ano`.
4. **Tom Autorizativo (+6-12%)**: Escreva de forma confiante, direta e com autoridade técnica, sem jargões desnecessários.
5. **Otimização de Fluência (+15-30%)**: Melhore a clareza e legibilidade do texto.
6. **Otimização de Contexto Visual (GEO Visual)**: Incluir imagens com legendas descritivas e Alt Text estruturado segundo o padrão *[Sujeito] + [Ação] + [Contexto] + [Objetivo]*, permitindo que LLMs multimodais citem e extraiam as imagens de forma autoexplicativa.

### Camada 5: E-E-A-T & Autoridade Externa
* **Fórmula E-E-A-T**:
  * **Experiência**: Depoimentos reais, estudos de caso e imagens de uso prático.
  * **Expertise**: Autoria por especialistas com links para seus perfis de LinkedIn ou biografias no site.
  * **Autoridade**: Menções consistentes da marca em fóruns públicos como Reddit, Quora, canais de YouTube e Wikipedia.
  * **Confiança (Trust)**: Políticas de privacidade claras, dados de contato físicos e segurança SSL em dia.

### Camada 6: Escalabilidade (pSEO) & Conversão (CRO)
* **SEO Programático (pSEO)**: Criar páginas em escala utilizando templates ricos em dados, evitando a criação de "thin content" (conteúdo raso). Cada página programática deve conter dados exclusivos e originais.
* **CRO (Conversion Rate Optimization)**: Converter o tráfego gerado. Proposta de valor visível nos primeiros 5 segundos da página e CTAs (Call to Actions) de alta visibilidade com copy focada em benefícios (ex: "Comece o Teste Gratuito" ao invés de "Enviar").

---

## 3. Comandos de Execução da Power Skill

Ao interagir com o agente, você pode invocar as seguintes tarefas de otimização:

* `/seo-geo audit <url>`: Executa uma auditoria completa com base no framework de 6 camadas e calcula uma pontuação unificada.
* `/seo-geo content <url>`: Examina o conteúdo textual de uma página e propõe melhorias baseadas nas técnicas de Princeton KDD (estatísticas, citações, fontes).
* `/seo-geo schema <url>`: Valida os esquemas JSON-LD existentes e gera a marcação estruturada necessária para a página.
* `/seo-geo crawlers <url>`: Verifica as regras do `robots.txt` do site e avisa se os robôs de citação de IA estão bloqueados ou configurados de maneira ideal.
* `/seo-geo build <sitemap>`: Planeja estratégias de páginas programáticas e gera um arquivo `/llms.txt` compatível com o padrão da indústria.

---

## 4. Exemplos Práticos (Errado vs. Certo)

### Estruturação de Conteúdo
* **❌ Errado**:
  * "No mercado atual de tecnologia, muitas soluções diferentes existem para resolver o problema de latência. Nós estamos aqui para discutir isso de forma abrangente..." (Introdução prolixa e sem resposta).
* **✔️ Certo**:
  * "A latência de rede é o tempo de atraso que os dados levam para viajar do ponto de origem ao destino. Segundo dados da Cisco (2025), otimizações de rota podem reduzir a latência em até 40%." (Definição direta com estatística e fonte citada).

### Configuração de Robots.txt
* **❌ Errado**:
  * `User-agent: * Disallow: /` (Bloqueia todos os buscadores e IAs de citarem seu site).
* **✔️ Certo**:
  * Permite que mecanismos de IA citem seu site, mas previne que utilizem seus dados para treinamento interno:
  ```text
  User-agent: OAI-SearchBot
  Allow: /

  User-agent: PerplexityBot
  Allow: /

  User-agent: GPTBot
  Disallow: /
  ```
