# 📋 Procedimento Operacional Padrão (SOP): Auditoria, Correção Dinâmica e Validação (SEO / GEO / AEO)

Este guia estabelece o processo passo a passo para **auditar**, **corrigir dinamicamente (sem quebrar layouts visuais)** e **validar empiricamente** a presença digital de qualquer website em mecanismos de busca tradicionais (Google/Bing) e motores de resposta de IA (ChatGPT, Perplexity, Gemini, Claude, Copilot).

---

## 🎯 1. Fluxo de Trabalho em 3 Fases

`mermaid
graph TD
    A[Fase 1: Auditoria Empírica e Diagnóstico] -->|Score 0-100| B(Identificação de Gargalos)
    B --> C[Fase 2: Implementação de Correções]
    C -->|CMS/Elementor/GTM/Theme| D[Script Dinâmico de Injeção & Sanitização]
    D --> E[Fase 3: Validação Live via Playwright/Browser]
    E -->|Score >= 90| F[Relatório de Entrega & Monitoramento]
    E -->|Score < 90| C
`

---

## 🔍 Fase 1: Matriz de Auditoria e Escala de Pontuação (100 Pontos)

Toda auditoria gera um relatório inicial com pontuação de 0 a 100 distribuída pelas 6 camadas:

| Camada | Peso | Itens Auditados | Critério de Sucesso |
| :--- | :---: | :--- | :--- |
| **1. Técnica & Rastreabilidade** | **20 pts** | obots.txt, Sitemap XML, SSL, CWV, renderização SSR | Bots de citação liberados (OAI-SearchBot, PerplexityBot, ClaudeBot, Google-Extended); treino bloqueado se desejado (GPTBot). |
| **2. Estrutura & Schemas** | **20 pts** | JSON-LD (LocalBusiness, Organization, FAQPage, etc.) | Schema rico com catálogo, endereço, geo-coordenadas, horário e sameAs (redes/certificações). |
| **3. Semântica & Answer-First** | **20 pts** | H1 único, limpeza de H2/H3 ruidosos, resposta de 240 char | Tag <h1> única no Hero; textos longos ou reviews não usam tags de cabeçalho. |
| **4. GEO & Citabilidade (Princeton 2024)** | **20 pts** | Alt texts descritivos em imagens, estatísticas, fontes | 100% das imagens com alt descritivo; links para autoridade/certificação externa. |
| **5. E-E-A-T & Autoridade** | **10 pts** | Links de certificações, bio de especialistas, trust badges | Menção e link para entidade emissora de certificados (ex: SSI, PADI, ISO, Google Partner). |
| **6. CRO & Conversão** | **10 pts** | Proposta de valor em 5s, CTAs claros, canal de contato direto | Botão de WhatsApp/Chat visível, formulário sem atrito, proposta clara no Hero. |

---

## 🛠️ Fase 2: Padrões de Correção Dinâmica (WordPress, Elementor, GTM, JS)

Quando não for possível ou conveniente alterar templates complexos diretamente no CMS sem risco de quebrar layouts visuais, aplica-se o **Padrão de Injeção Dinâmica via Custom Code / GTM**:

### A. Prevenção de Corrupção de Acentuação (Unicode Escape)
Em ambientes com bancos de dados legados ou inconsistência de charset (ISO-8859-1 vs UTF-8), converta caracteres acentuados em escapes \uXXXX dentro dos scripts de injeção:
* São Paulo &rarr; S\u00e3o Paulo
* Câmera &rarr; C\u00e2mera
* Técnico &rarr; T\u00e9cnico
* Próximas &rarr; Pr\u00f3ximas
* máscaras &rarr; m\u00e1scaras
* manutenção &rarr; manuten\u00e7\u00e3o

### B. Correção Dinâmica de H1 (Hero Heading)
Garante tag <h1> única preservando estilos CSS do elemento original:
`javascript
const heroHeading = Array.from(document.querySelectorAll('h2, h3, div.elementor-heading-title'))
  .find(el => el.innerText && el.innerText.toUpperCase().includes('PALAVRA_CHAVE_HERO'));

if (heroHeading && heroHeading.tagName !== 'H1') {
  const h1 = document.createElement('h1');
  h1.className = heroHeading.className;
  h1.innerHTML = heroHeading.innerHTML;
  h1.setAttribute('style', heroHeading.getAttribute('style') || '');
  heroHeading.parentNode.replaceChild(h1, heroHeading);
}
`

### C. Higienização de Ruídos de Hierarquia (Reviews & Menus)
Converte elementos de texto longo que foram indevidamente marcados como <h2> ou <h3> em parágrafos <p>:
`javascript
// Heurística: cabeçalhos com mais de 45 caracteres que não sejam o título principal
document.querySelectorAll('h2, h3').forEach(heading => {
  const text = heading.innerText.trim();
  if (text.length > 45 && !text.toUpperCase().includes('TITULO_PRINCIPAL')) {
    const p = document.createElement('p');
    p.className = heading.className;
    p.innerHTML = heading.innerHTML;
    p.setAttribute('style', heading.getAttribute('style') || '');
    heading.parentNode.replaceChild(p, heading);
  }
});
`

### D. Enriquecimento de Alt Text de Imagens (GEO Visual)
Atribui descrições precisas no formato [Sujeito] + [Ação/Serviço] + [Local/Contexto]:
`javascript
const imageRules = [
  { match: 'logo-ssi', alt: 'Certifica\u00e7\u00e3o Internacional SSI Scuba Schools International' },
  { match: 'curso-basico', alt: 'Curso b\u00e1sico de mergulho Open Water com instrutor credenciado' },
  { match: 'equipamentos', alt: 'Equipamentos completos de mergulho aut\u00f4nomo e manuten\u00e7\u00e3o' }
];

document.querySelectorAll('img').forEach(img => {
  imageRules.forEach(rule => {
    if (img.src.includes(rule.match) && (!img.alt || img.alt.trim() === '')) {
      img.alt = rule.alt;
    }
  });
});
`

### E. Injeção de Links de Autoridade e Certificações (E-E-A-T)
Encapsula badges de entidades parceiras ou certificadoras com links el="noopener noreferrer":
`javascript
const badgeImg = Array.from(document.querySelectorAll('img'))
  .find(img => img.src.includes('parceiro_oficial.webp') || img.src.includes('ssi'));

if (badgeImg && badgeImg.parentElement && badgeImg.parentElement.tagName !== 'A') {
  const a = document.createElement('a');
  a.href = 'https://www.divessi.com/'; // URL da entidade oficial
  a.target = '_blank';
  a.rel = 'noopener noreferrer';
  badgeImg.parentNode.insertBefore(a, badgeImg);
  a.appendChild(badgeImg);
}
`

### F. Injeção Dinâmica de JSON-LD Schema
Injeta o Schema estruturado no <head> caso o CMS não possua plugin nativo configurado:
`javascript
const schemaData = {
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Nome da Empresa",
  "url": "https://seusite.com.br",
  "telephone": "+5511999999999",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Rua Exemplo, 123",
    "addressLocality": "S\u00e3o Paulo",
    "addressRegion": "SP",
    "postalCode": "01000-000",
    "addressCountry": "BR"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": -23.5505,
    "longitude": -46.6333
  },
  "sameAs": [
    "https://www.instagram.com/empresa",
    "https://www.facebook.com/empresa",
    "https://www.divessi.com/"
  ]
};

const scriptTag = document.createElement('script');
scriptTag.type = 'application/ld+json';
scriptTag.text = JSON.stringify(schemaData);
document.head.appendChild(scriptTag);
`

---

## 🧪 Fase 3: Validação Empírica (Playwright & Live Tests)

Após a aplicação dos patches, a validação é executada via script automatizado ou navegador:

1. **Validação de Tags de Cabeçalho**:
   - document.querySelectorAll('h1').length === 1 (deve ser exatamente 1).
   - Todos os h2 e h3 devem conter títulos concisos (< 60 caracteres).
2. **Validação de Imagens e Alt Texts**:
   - Array.from(document.querySelectorAll('img')).filter(img => !img.alt || img.alt.trim() === '') (deve retornar 0 imagens críticas sem alt).
3. **Validação de Schemas**:
   - Presença de tags <script type="application/ld+json"> válidas e parseáveis via JSON.parse.
4. **Validação de Links Externos**:
   - Badges de certificação devem possuir tag <a> válida com 	arget="_blank" e el="noopener noreferrer".
5. **Cálculo da Pontuação Final**:
   - Se score >= 90/100, a otimização é considerada homologada.
