---
name: brain-explorer
description: Explore, inspect, search, and recover past session artifacts, implementation plans, walkthroughs, research notes, general knowledge, scratch scripts, and interaction transcripts from Antigravity CLI (.brain-cli) and IDE (.brain-ide). Use when asked to check session history, find past plans, recover scratch code, search general knowledge, or retrieve past technical decisions.
---

# 🧠 Brain Explorer Skill

Use esta skill para buscar, visualizar e recuperar qualquer informação, documento ou **conhecimento geral acumulado** em sessões anteriores do **Antigravity CLI** e **Antigravity IDE**.

As pastas `.brain-cli` e `.brain-ide` servem como **memória histórica expandida** do sistema. Sempre que precisar reutilizar aprendizados passados, decisões de arquitetura, análises de dados ou respostas explicativas anteriores, consulte estes caminhos antes de reconstruir a solução do zero.

---

## 📍 Localizações dos Atalhos no Workspace

No workspace `C:\Users\bmart\.antigravity`, existem dois junctions diretos para as pastas brain:
- **CLI Brain:** `C:\Users\bmart\.antigravity\.brain-cli` (origem: `C:\Users\bmart\.gemini\antigravity-cli\brain`)
- **IDE Brain:** `C:\Users\bmart\.antigravity\.brain-ide` (origem: `C:\Users\bmart\.gemini\antigravity-ide\brain`)

---

## 🔍 Como explorar os dados da Brain

### 1. Consultar Conhecimentos Gerais e Documentos (`*.md`)
Para buscar relatórios de pesquisa, notas técnicas, análises ou documentações geradas em sessões passadas:
```powershell
# Listar todos os relatórios e notas de conhecimento criados em sessões anteriores
Get-ChildItem -Path "C:\Users\bmart\.antigravity\.brain-cli", "C:\Users\bmart\.antigravity\.brain-ide" -Filter "*.md" -Recurse | Where-Object { $_.Name -notmatch "robots.txt" } | Sort-Object LastWriteTime -Descending | Select-Object -First 15 FullName, LastWriteTime

# Buscar termos específicos dentro de notas e documentos de conhecimento
Get-ChildItem -Path "C:\Users\bmart\.antigravity\.brain-cli", "C:\Users\bmart\.antigravity\.brain-ide" -Filter "*.md" -Recurse | Select-String -Pattern "TERMO_DE_INTERESSE" | Select-Object -First 20
```

### 2. Encontrar Planos de Implementação e Walkthroughs
Para recuperar planos de arquitetura e resumos de tarefas concluídas:
```powershell
# Buscar os últimos arquivos de plano de implementação
Get-ChildItem -Path "C:\Users\bmart\.antigravity\.brain-cli", "C:\Users\bmart\.antigravity\.brain-ide" -Filter "implementation_plan.md" -Recurse | Sort-Object LastWriteTime -Descending | Select-Object -First 5

# Buscar os últimos walkthroughs
Get-ChildItem -Path "C:\Users\bmart\.antigravity\.brain-cli", "C:\Users\bmart\.antigravity\.brain-ide" -Filter "walkthrough.md" -Recurse | Sort-Object LastWriteTime -Descending | Select-Object -First 5
```

### 3. Recuperar Scripts de Rascunho e Funções (`scratch/`)
Scripts temporários em Python, PowerShell, TypeScript, SQL ou Shell criados em sessões anteriores ficam salvos na subpasta `scratch`:
```powershell
Get-ChildItem -Path "C:\Users\bmart\.antigravity\.brain-cli\*\scratch\*", "C:\Users\bmart\.antigravity\.brain-ide\*\scratch\*" | Sort-Object LastWriteTime -Descending | Select-Object -First 15
```

### 4. Pesquisar Histórico de Conversas e Explicações Passadas (`transcript.jsonl`)
Para buscar dúvidas que o usuário já tirou ou explicações conceituais fornecidas anteriormente:
```powershell
# Buscar requisições anteriores do usuário sobre um tema específico
Get-ChildItem -Path "C:\Users\bmart\.antigravity\.brain-cli", "C:\Users\bmart\.antigravity\.brain-ide" -Filter "transcript.jsonl" -Recurse | ForEach-Object {
    Select-String -Path $_.FullName -Pattern '\"type\":\"USER_INPUT\"' | Select-String -Pattern "TERMO_DE_INTERESSE"
} | Select-Object -First 20
```

---

## 💡 Diretrizes de Reutilização de Conhecimento

1. **Reuso de Contexto:** Antes de formular uma nova explicação longa ou planejar uma refatoração complexa, a IA deve checar se a brain possui notas de pesquisa (`research_notes.md`) ou planos passados sobre o mesmo assunto.
2. **Preservação de Scripts Utilitários:** Em vez de recriar scripts de raspagem ou tratamento de dados do zero, verifique primeiro se um script correspondente já existe em `.brain-cli/*/scratch/` ou `.brain-ide/*/scratch/`.
3. **Leitura Segura:** Ao ler arquivos `.jsonl` grandes, utilize `grep_search` ou `Select-String` com filtros específicos para evitar sobrecarregar o contexto.
