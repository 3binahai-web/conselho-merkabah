# Skills do Conselho Merkabah

> Procedimentos reutilizáveis (skills) das 7 Sefirot, adaptados para
> execução standalone fora do Hermes Agent.

## Índice

| Skill | Função | Versão |
|:------|:-------|:-------|
| [`conselho-merkabah-mestre`](./conselho-merkabah-mestre/) | Skill mestre — orquestra as outras 6 Sefirot | v7.0 |
| [`merkabah-talmud-v6-2`](./merkabah-talmud-v6-2/) | Protocolo de deliberação com pesos astrais | v6.2 |
| [`sephiroth-chesed`](./sephiroth-chesed/) | Expansão, parcerias, captação | v1.0 |
| [`sephiroth-gevurah`](./sephiroth-gevurah/) | Segurança, auditoria, limites | v1.0 |
| [`sephiroth-hod`](./sephiroth-hod/) | Comunicação, infraestrutura, diplomacia | v1.0 |

## Como usar uma skill standalone

```bash
# Clone o repositório
git clone https://github.com/shomer-adamar/conselho-merkabah.git
cd conselho-merkabah/skills/sephiroth-chesed

# Leia o SKILL.md
cat SKILL.md

# Cada skill inclui:
# - YAML frontmatter (description, version, author, date)
# - Trigger conditions (quando invocar)
# - Step-by-step procedure
# - Examples
# - Pitfalls
```

## Formato SKILL.md

```markdown
---
description: [resumo de uma linha]
version: [semver]
author: [Sefirá ou pseudônimo]
date: [YYYY-MM-DD]
---

# [Título da Skill]

## Trigger

Quando usar esta skill.

## Procedimento

1. Passo 1
2. Passo 2
...

## Exemplos

[exemplos concretos]

## Pitfalls

[erros comuns a evitar]
```

## Versionamento

Cada skill segue [Semantic Versioning](https://semver.org/):
- **MAJOR**: mudança incompatível de comportamento
- **MINOR**: nova funcionalidade compatível
- **PATCH**: correção de bug

Mudanças radicais em skills requerem **Haskamah** ratificada pelo Conselho.

## Privacidade

- ❌ Nenhum nome real em `author` — usar pseudônimo (Chesed, Binah, etc)
- ❌ Nenhum dado pessoal em exemplos
- ✅ Use "Fundação Shomer Adamah" para instituição
- ✅ Use localizações genéricas ("interior da Bahia") em vez de endereços

---

*שומר אדמה*
