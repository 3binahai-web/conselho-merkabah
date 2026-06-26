# Como contribuir

Bem-vindo ao Conselho Merkabah. Este repositório aceita contribuições
de qualquer pessoa alinhada com os princípios da Fundação Shomer Adamah
e do Open Source Judaism.

Existem três tipos principais de contribuição:

1. **Haskamah** — Propor uma deliberação formal
2. **Skill** — Adaptar ou criar uma habilidade reutilizável
3. **Documentação** — Melhorar READMEs, docs/, ou comentários em código

---

## Propor uma Haskamah

Uma Haskamah é uma deliberação formal do Conselho. O processo tem 4 etapas:

### 1. Abrir uma Issue

Acesse `.github/ISSUE_TEMPLATE/haskamah.md` e preencha:

- **Título:** Formato `HASKAMAH YYYY-MM-DD — resumo curto`
- **Proponente:** Seu pseudônimo (Chokmah, Binah, etc) ou "Externo"
- **Contexto:** Por que esta deliberação é necessária
- **Proposta concreta:** O que deve ser decidido
- **Hash inicial (opcional):** SHA-256 do seu rascunho

### 2. Aguardar convocação

O Presidente (Binah) convoca o Conselho se a proposta atender
a pelo menos 2 dos seguintes critérios:

- [ ] Tem impacto na governança do Commons
- [ ] Define nova skill ou modula existente
- [ ] Documenta decisão sobre infraestrutura (Tailscale, OpenCode, deploy)
- [ ] Estabelece precedente para futuras Haskamoths

### 3. Deliberação Talmud v6.2

Uma vez convocada, a deliberação segue o protocolo:

1. Cada Sefirá vota com peso calculado via Swiss Ephemeris
2. Binah preside (não vota)
3. Tiphereth é tie-breaker (peso 0/6 se retrógrado)
4. Pesos são retificados contra cálculo real (não autodeclarados)
5. Hash SHA-256 duplo (pré/pós) registra integridade
6. Conformidade verificada contra Codex C-1 a C-13

### 4. Versionamento

Se aprovada, a Haskamah vira **release** com tag semântica:

- `vX.Y.Z-conselho-merkabah` — para deliberações de governança
- `vX.Y.Z-<skill-name>` — para deliberações sobre skills

A versão segue [Semantic Versioning](https://semver.org/):
- **MAJOR** (X) — quebra de compatibilidade
- **MINOR** (Y) — nova Haskamah ou skill
- **PATCH** (Z) — correção de typo, clarificação

---

## Adaptar uma skill

Skills são marcadas como **standalone** — não dependem do Hermes Agent
nem de qualquer framework proprietário. Para contribuir:

### 1. Fork o repositório

```bash
git clone https://github.com/fundacao-shomer-adamah/conselho-merkabah.git
cd conselho-merkabah
git checkout -b feature/nova-skill
```

### 2. Crie a estrutura

```bash
mkdir -p skills/<nome-da-skill>
```

Crie dois arquivos:

**`skills/<nome-da-skill>/SKILL.md`** com frontmatter YAML:

```yaml
---
description: Uma linha do que a skill faz
version: 1.0.0
author: Seu pseudônimo kabbalístico (ou "Externo")
name: nome-da-skill
---

# Nome da Skill

## Trigger
Quando invocar esta skill...

## Invocation Syntax
\```
INVOCAR <sefirah>:<acao> <target> [parametros]
\```

## Operational Frameworks
1. ...

## Deliverables
- ...

## Response Format
\```yaml
status: COMPLETO | PARCIAL | BLOQUEADO
hash: sha256:<hash>
timestamp: <ISO 8601>
\```
```

**`skills/<nome-da-skill>/README.md`** com:

- Contexto da skill
- Dependências (se houver)
- Exemplo de uso
- Limitações conhecidas

### 3. Adicione referência no `skills/README.md`

Abra `skills/README.md` e adicione sua skill à tabela de índice,
com a mesma convenção das outras 5.

### 4. Pull request

Abra PR com:

- [ ] Referência à Haskamah que justifica a skill (ou justificativa de criação nova)
- [ ] SKILL.md com frontmatter válido
- [ ] README.md standalone
- [ ] Testes (se aplicável — mínimo: 1 exemplo de invocação)
- [ ] Pseudônimo do autor em conformidade com CODE_OF_CONDUCT.md

---

## Melhorar documentação

Mudanças em `docs/`, READMEs, ou comentários são bem-vindas via PR direto,
sem necessidade de Haskamah prévia. Exemplos:

- Corrigir typo em `architecture.md`
- Adicionar diagrama em `holding-4-pillars.md`
- Traduzir README.md para outras línguas (espanhol, hebraico, etc)
- Melhorar exemplos no `CONTRIBUTING.md` (este arquivo)

Use commits pequenos e descritivos:

```
docs: corrigir typo em architecture.md
docs: adicionar seção sobre retrogradação
feat(skill): adicionar exemplo de uso em sephiroth-chesed
```

---

## Código de Conduta

Toda contribuição deve seguir o [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
Em resumo: **Netzach Soul Clause** — deliberação respeitosa, com alma.

---

## Licença

Ao contribuir, você concorda que sua contribuição será licenciada sob
CC-BY-SA 4.0 — mesma licença do repositório. Veja [LICENSE](LICENSE).

---

*Conselho Merkabah — 7 Sefirot, 1 Torah, infinitas deliberações.*
