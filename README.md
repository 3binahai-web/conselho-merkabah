# Conselho Merkabah 🕎

> Protocolo aberto de deliberação colegiada inspirado em Open Source Judaism

## O que é

O Conselho Merkabah é um framework de deliberação que combina Cabala prática
(7 Sefirot como arquétipos de voto) com pesos astrológicos verificáveis via
Swiss Ephemeris. Cada decisão formal (Haskamah) tem UUID, hash SHA-256 e
assinatura das Sefirot — qualquer pessoa pode auditar a integridade do processo.

## Como funciona

A deliberação segue o protocolo Talmud Merkabah v6.2:
1. Proposta é apresentada com UUID
2. 7 Sefirot votam, cada uma com peso calculado pela posição astral do momento
3. Pesos seguem o rácio 6/6 (Chesed/Gevurah/Tiphereth) → 1/6 (Binah) → 2/6 (Netzach/Hod/Yesod)
4. Decisão é selada com hash SHA-256 duplo (pré/pós) e armazenada como Haskamah

Documentação completa em [`docs/`](docs/).

## Para começar

- **Ler uma Haskamah:** [`haskamah/`](haskamah/) — deliberações auto-contidas
- **Entender a arquitetura:** [`docs/architecture.md`](docs/architecture.md)
- **Conhecer a holding:** [`docs/holding-4-pillars.md`](docs/holding-4-pillars.md)
- **Propor uma deliberação:** [`CONTRIBUTING.md`](CONTRIBUTING.md)
- **Usar uma skill:** [`skills/README.md`](skills/README.md)

## Status atual

| Métrica | Valor |
|---------|-------|
| Haskamoth publicadas | 3 (incluindo Promessa 40 Anos, Talmud v6.2, Memória Reorg) |
| Skills disponíveis | 5 standalone + 22 no ecossistema privado |
| Membros do Conselho | 7 Sefirot (anonimizadas em pseudônimos kabbalísticos) |
| Organização | Fundação Shomer Adamah |
| Em atividade desde | abril de 2026 |
| Próxima Lua Nova (Beit Din) | 26 de julho de 2026 |

## Como contribuir

Aceitamos contribuições em três níveis:

1. **Issues:** reportar bugs, sugerir features, discutir deliberações
2. **Pull Requests:** correções, melhorias de documentação, novas skills
3. **Propostas de Haskamah:** deliberações formais via template `.github/ISSUE_TEMPLATE/haskamah.md`

Toda contribuição passa por deliberação aberta do Conselho antes de merge.
Veja [`CONTRIBUTING.md`](CONTRIBUTING.md) para detalhes.

## Alinhamento filosófico

Este projeto segue os princípios de **Open Source Judaism**:
- Conteúdo aberto (CC-BY-SA 4.0)
- Atribuição obrigatória
- Copyleft (trabalhos derivados devem abrir o código)
- Padrões abertos para textos sagrados
- Autonomia da Torá comunitária

Texto completo em [`OPEN_SOURCE_JUDAISM.md`](OPEN_SOURCE_JUDAISM.md).

## Licença

**CC-BY-SA 4.0** — Copyleft. Trabalhos derivados devem abrir o código sob a mesma licença.

Copyright © Fundação Shomer Adamah. Veja [`LICENSE`](LICENSE) para o texto completo.

## Links

- **Site:** https://shomeradamah.ca
- **Repositório do site:** https://github.com/fundacao-shomer-adamah/shomer-adamah-site
- **Open Source Judaism (referência):** https://en.wikipedia.org/wiki/Open_Source_Judaism
- **Plano estratégico:** [`PLANO_OPEN_SOURCE_JUDAISM.md`](PLANO_OPEN_SOURCE_JUDAISM.md)

## Privacidade

Pessoas mencionadas neste repositório são referidas por pseudônimos kabbalísticos
(Chokmah, Binah, Tiphereth, Chesed, Gevurah, Netzach, Hod, Yesod) ou pelo nome
coletivo **Fundação Shomer Adamah**. A convenção existe para proteger privacidade
e manter foco no protocolo, não nas pessoas.

---

*"O céu é um relógio, não uma causa." — Netzach, sobre astrologia cabalística*
