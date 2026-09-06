# Lições Aprendidas e Evolução da Stack

Este documento rastreia os feedbacks do usuário e as melhorias aplicadas aos padrões de desenvolvimento.

## 📅 Maio 2026
- **Modularização Obrigatória:** Feedbacks positivos sobre a transição de scripts soltos para a pasta `src/`. Este passa a ser o padrão ouro.
- **Configurações Centralizadas:** O uso de `src/config.py` para carregar `.env` provou ser eficiente para evitar redundância de caminhos.
- **Segurança Sistêmica:** A inclusão de disclaimers e travas de segurança (dose máxima) deve ser tratada como requisito de infraestrutura, não apenas de prompt.
- **Interface Conversacional:** Para sistemas interativos, a simulação de chat (estilo WhatsApp) no Streamlit é o formato preferencial de UI.
