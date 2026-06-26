# Conselho Merkabah 🕎

> Protocolo aberto de deliberação colegiada inspirado em Open Source Judaism

Este repositório contém a governança deliberativa da comunidade Shomer Adamah,
organizada em 7 Sefirot que votam com pesos astrais calculados via Swiss Ephemeris.

## Conteúdo

- **haskamah/** — Deliberações formais com UUID, hash SHA-256 e assinatura astral
- **skills/** — Habilidades reutilizáveis do Conselho (5 principais)
- **docs/** — Arquitetura, holding 4 pilares, alinhamento com Open Source Judaism

## O que é o Conselho Merkabah?

O Conselho Merkabah é um protocolo de deliberação que combina:

1. **Cabala prática** — 7 Sefirot (Chesed, Gevurah, Tiphereth, Netzach, Hod, Yesod, Binah)
   como arquétipos de voto com pesos calculados via efemérides.
2. **Codex verificável** — Cada Haskamah tem UUID, hash SHA-256 duplo (pré/pós),
   e conformidade verificada contra princípios C-1 a C-13.
3. **Copyleft** — Tudo sob CC-BY-SA 4.0. Trabalhos derivados devem abrir o código.

A premissa é simples: deliberação auditável é deliberação legítima.
Se cada decisão tem UUID, hash, e assinatura astral, então qualquer pessoa
pode verificar a integridade do processo — em qualquer momento, em qualquer fuso.

## Como usar este repositório

### Ler uma Haskamah

Cada arquivo em `haskamah/` é auto-contido:

```bash
# Verificar integridade (quando o pipeline Python estiver rodando)
sha256sum haskamah/2026-06-26-memoria-reorg.md
```

### Usar uma skill

As skills em `skills/` são **standalone** — não dependem do Hermes Agent.
Cada uma tem seu próprio `SKILL.md` com frontmatter YAML e markdown descritivo.
Para usar:

```yaml
# Em qualquer framework compatível com SKILL.md
skill: sephiroth-chesed
acao: expand
target: "novo_curso_de_agricultura"
```

### Propor uma deliberação

Veja [CONTRIBUTING.md](CONTRIBUTING.md) para o fluxo completo de Haskamah.

## Estrutura

```
conselho-merkabah/
├── LICENSE                          # CC-BY-SA 4.0 (EN + PT)
├── README.md                        # este arquivo
├── CONTRIBUTING.md                  # como propor Haskamah
├── CODE_OF_CONDUCT.md               # Netzach Soul Clause
├── OPEN_SOURCE_JUDAISM.md           # declaração de alinhamento
├── .gitignore
├── .github/
│   └── ISSUE_TEMPLATE/
│       └── haskamah.md              # template de proposta
├── haskamah/                        # deliberações formais
│   ├── 2026-04-12-promessa-40-anos.md
│   ├── 2026-05-12-talmud-v6-2-astrologia-cabalistica.md
│   └── 2026-06-26-memoria-reorg.md
├── skills/                          # 5 skills standalone
│   ├── README.md
│   ├── conselho-merkabah-mestre/
│   ├── merkabah-talmud-v6-2/
│   ├── sephiroth-chesed/
│   ├── sephiroth-gevurah/
│   └── sephiroth-hod/
└── docs/
    ├── holding-4-pillars.md         # Wall Done + Adamah Tech + Daath + Merkabah AI
    └── architecture.md              # como funciona o Conselho
```

## Licença

CC-BY-SA 4.0 — Copyleft. Trabalhos derivados devem abrir o código sob a mesma licença.
Copyright © Fundação Shomer Adamah.

Veja [LICENSE](LICENSE) para o texto completo.

## Veja também

- Site público: https://shomeradamah.ca
- Open Source Judaism (Wikipedia): https://en.wikipedia.org/wiki/Open_Source_Judaism
- Repositório do site: github.com/fundacao-shomer-adamah/shomer-adamah-site
- Plano completo Open Source Judaism: ver [docs/](docs/) (versão resumida)

## Pseudônimos e atribuição

Pessoas mencionadas neste repositório são referidas por pseudônimos kabbalísticos
(Chokmah, Binah, Tiphereth, Chesed, Gevurah, Netzach, Hod, Yesod) ou pelo nome
coletivo **Fundação Shomer Adamah**. A convenção existe para:

1. Proteger privacidade dos cidadãos da comunidade
2. Manter o foco no protocolo, não nas pessoas
3. Permitir que forks do repositório usem a mesma estrutura sem revelar identidades

Veja [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) para detalhes completos.

---

*"O céu é um relógio, não uma causa." — Netzach, sobre astrologia cabalística*
