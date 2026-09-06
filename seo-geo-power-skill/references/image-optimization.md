# Otimização de Imagens para SEO, GEO e AEO (Motores de IA Multimodais)

Com a evolução dos buscadores e motores de IA para modelos **multimodais** (capazes de processar texto, imagem e áudio simultaneamente, como GPT-4o, Gemini 1.5 Pro e Claude 3.5 Sonnet), a otimização de imagens tornou-se essencial para garantir citações e inclusão de conteúdo visual nas respostas generativas.

Este guia orienta como estruturar suas imagens para que humanos as visualizem rapidamente e robôs/LLMs consigam extrair seu significado sem margem para erros.

---

## 1. O Padrão de Ouro para Alt Text (Texto Alternativo)

O Alt Text continua sendo o sinal mais forte para indexação de imagem. No contexto de IA, ele não serve apenas para acessibilidade, mas como o rótulo semântico principal da imagem para o LLM.

* **Fórmula do Alt Text Ideal**: **[Sujeito] + [Ação] + [Atributo/Contexto] + [Objetivo]**
  * ❌ *Ruim (Keyword Stuffing)*: `alt="seo geo aeo otimizar imagens trafego de busca"`
  * ❌ *Fraco (Muito simples)*: `alt="gráfico de conversão"`
  * ✔️ *Excelente*: `alt="Gráfico de barras mostrando um aumento de 20% nas conversões do site após a implementação do framework de otimização para IA (GEO)."`

* **Regras para Alt Text**:
  * **Seja contextual**: O texto deve descrever a imagem e explicar qual argumento ela apoia no texto.
  * **Imagens decorativas**: Para ícones estéticos, divisores ou backgrounds, use `alt=""` para que os LLMs e leitores de tela os ignorem.

---

## 2. Ancoragem Semântica (Proximidade de Texto)

Mecanismos de IA e algoritmos RAG (Retrieval-Augmented Generation) analisam o conteúdo ao redor do elemento visual para validar a relevância da imagem.

* **Texto Adjacente**: Coloque a imagem imediatamente abaixo ou acima do parágrafo onde o assunto é discutido. O texto deve referenciar a imagem diretamente (ex: *"Como mostrado no gráfico a seguir..."*).
* **Legendas (Captions)**: Sempre inclua legendas de texto (`<figcaption>`) para imagens informativas. Os LLMs leem as legendas de forma prioritária como o resumo descritivo do elemento visual.
* **Autoexplicabilidade**: A imagem e sua legenda/alt text combinados devem ser "extraíveis". Se o LLM recortar a imagem para exibi-la na resposta ao usuário, o contexto dela deve continuar fazendo sentido por si só.

---

## 3. Diretrizes Técnicas de Rastreabilidade

* **Tags HTML Padrão**: Sempre utilize a tag HTML tradicional `<img>` com os atributos `src` e `alt`. Evite carregar imagens informativas via propriedades CSS de background (`background-image`), pois a maioria dos crawlers de IA ignora ou tem grande dificuldade de indexar arquivos de folha de estilo.
* **Nome do Arquivo**: Use nomes descritivos separados por hifens (ex: `seo-geo-conversao-grafico.webp` em vez de `IMG_9824.jpg`).
* **Formatos de Nova Geração**: Utilize WebP ou AVIF para compressão eficiente, garantindo carregamento rápido. A performance do site afeta a pontuação de qualidade global monitorada pelos buscadores de IA.
* **Sitemap de Imagens**: Adicione as tags `<image:image>` e `<image:loc>` no seu `sitemap.xml` para apontar diretamente a existência de imagens cruciais de produtos, infográficos e diagramas.

---

## 4. Marcação de Dados Estruturados (JSON-LD Schema)

Use marcações estruturadas para associar explicitamente as imagens às entidades da página:

* **Vinculação de Imagem Principal**:
  No JSON-LD de um artigo (`Article` ou `Product`), garanta a presença do objeto `image`:
  ```json
  {
    "@context": "https://schema.org",
    "@type": "Article",
    "headline": "Como otimizar seu site para busca de IA",
    "image": {
      "@type": "ImageObject",
      "url": "https://seusite.com/imagens/seo-geo-grafico.webp",
      "width": "1200",
      "height": "630",
      "caption": "Gráfico de barras ilustrando melhorias de visibilidade em IA."
    }
  }
  ```
