---
name: universal-dev-stack
description: Padrões de desenvolvimento e stack tecnológica preferencial (Node.js, Python, SQLite). Use sempre que iniciar um novo projeto, refatorar código ou quando o usuário fornecer feedback sobre padrões de engenharia.
---

# Universal Dev Stack

Este guia define a base tecnológica e os padrões de engenharia para todos os projetos, garantindo consistência, escalabilidade e evolução contínua baseada em feedbacks.

## 🛠 Stack Tecnológica Core

- **Backend / Scripts:** Python (Preferencial para lógica clínica e IA) e Node.js/TypeScript (Preferencial para ferramentas de sistema e integrações modernas).
- **Banco de Dados:** Supabase (PostgreSQL) - Padronizado para persistência em nuvem, escalabilidade e integração nativa com autenticação e storage.
- **Interface:** Next.js (Web), Streamlit ou CLI.
- **Configuração:** Sempre utilizar `.env` para chaves (`SUPABASE_URL`, `SUPABASE_ANON_KEY`, `GEMINI_API_KEY`).

## 📂 Padrões de Arquitetura

### 1. Estrutura de Pacotes (Python)
Sempre organize projetos Python seguindo o padrão modular:
- `src/`: Código fonte.
    - `core/`: Regras de negócio e motores de cálculo.
    - `api/`: Integrações externas (ex: Supabase Client).
    - `database/`: Camada de persistência (Migrations e SQL).
- `scripts/`: Entrypoints e utilitários.

### 2. Padrões de Banco de Dados (Supabase/Postgres)
- Utilizar **UUID** (gen_random_uuid()) como chave primária em todas as tabelas.
- Implementar **RLS (Row Level Security)** para proteção de dados do usuário.
- Centralizar a lógica de saúde em silos lógicos via `profile_id`.
- Utilizar extensões como `pg_vector` para buscas semânticas de exames.

## 📈 Ciclo de Evolução e Feedback

Esta skill é viva. Sempre que o usuário fornecer um feedback sobre um padrão de código ("prefiro X em vez de Y"), você deve:
1. Atualizar o arquivo [lessons-learned.md](references/lessons-learned.md) com o novo aprendizado.
2. Refletir a mudança na lógica das próximas implementações.

## ⚖️ Segurança e Garantia Legal

- **Disclaimers:** Todo sistema de recomendação (IA) deve possuir um campo obrigatório de `disclaimer` avisando sobre a natureza da ferramenta.
- **Travas de Segurança:** Implementar limites físicos (ex: dose máxima) em lógica de código, não apenas via prompt.
