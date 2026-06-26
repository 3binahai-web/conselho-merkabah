# Alinhamento com Open Source Judaism 🕎

> Este repositório é parte da infraestrutura da Fundação Shomer Adamah
> e segue os princípios do **Open Source Judaism**.

---

## O que é Open Source Judaism?

**Open Source Judaism** (OSJ) é um movimento contemporâneo que aplica os
princípios do software livre e de código aberto à tradição, prática e
governança judaica. O termo foi cunhado em analogia ao "Open Source Christianity"
e ganhou força no início dos anos 2020 entre comunidades progressistas
e reconstrucionistas.

Fonte: [Wikipedia — Open Source Judaism](https://en.wikipedia.org/wiki/Open_Source_Judaism)

Os princípios centrais são:

1. **Conteúdo aberto** — Textos, traduções, comentários disponíveis em formato digital,
   versionado, e livremente reutilizável.
2. **Atribuição correta** — Cada contribuidor é creditado; nada é plagiado ou anonimizado
   sem critério.
3. **Commons intelectual** — Conhecimento judaico como patrimônio coletivo, não como
   propriedade de editoras ou autoridades.
4. **Tecnologias future-proof** — Uso de formatos abertos (Markdown, JSON, HTML semântico)
   em vez de formatos proprietários.
5. **Autonomia pessoal no estudo** — Cada pessoa tem o direito e o recurso para estudar
   diretamente as fontes primárias, sem intermediação de autoridade religiosa.

---

## Como este repositório aplica OSJ

### 1. Conteúdo aberto

- Todas as Haskamoths estão em `haskamah/` como Markdown puro.
- Nenhuma Haskamah requer software proprietário para ser lida.
- O formato é versionado: cada Haskamah tem UUID, hash SHA-256, e timestamp.

### 2. Atribuição correta

- Cada contribuidor é creditado por pseudônimo (Chokmah, Binah, Tiphereth, etc).
- A convenção de pseudônimos kabbalísticos tem dois propósitos:
  - Proteger a privacidade dos cidadãos da comunidade
  - Sublinhar que o papel importa mais que a pessoa no protocolo
- A Fundação Shomer Adamah é a entidade coletiva mantenedora.

### 3. Commons intelectual

- Licença CC-BY-SA 4.0 (copyleft) garante que derivados permaneçam abertos.
- Trabalhos derivados devem abrir o código — não podem ser fechados.
- O Plano Open Source Judaism (2026-06-26) prevê templates para que
  outras comunidades intencionais possam forkar a estrutura Merkabah.

### 4. Tecnologias future-proof

- Markdown como formato primário (lê em qualquer lugar, em qualquer tempo)
- YAML frontmatter para metadados estruturados (parseável por qualquer linguagem)
- JSON para datasets derivados (ata de deliberação, efemérides, etc)
- Sem dependência de framework proprietário para leitura

### 5. Autonomia pessoal

- Haskamoths documentam **como** e **por que** uma decisão foi tomada
- Pesos astrais são calculados, não autodeclarados
- Qualquer pessoa pode verificar a integridade via hash
- C-1 a C-13 (Codex) são públicos e auditáveis

---

## Diferenças e ressalvas

Open Source Judaism é um movimento amplo, e este repositório representa
nossa aplicação específica. Algumas divergências notáveis:

| OSJ genérico | Shomer Adamah |
|--------------|---------------|
| Conteúdo em hebraico/inglês | Adicionamos português (comunidade brasileira) |
| Autoria nominal | Autoria por pseudônimo kabbalístico |
| Licenças variam (MIT a CC-BY-SA) | Padronizamos em CC-BY-SA 4.0 (copyleft forte) |
| Foco em texto | Inclui protocolo deliberativo (7 Sefirot) |
| Geralmente textual | Inclui efemérides astrais como camada deliberativa |

A última divergência é a mais polêmica. Astrologia cabalística é prática
**interna** do Conselho Merkabah — não impomos a ninguém e não a usamos
para prever eventos externos. Servem como framework de pesos para
deliberação colegiada, análogo a como um sistema de votação ponderada
usa coeficientes. Veja [docs/architecture.md](docs/architecture.md) para detalhes.

---

## Roadmap de alinhamento

Curto prazo (executado):

- [x] LICENSE CC-BY-SA 4.0
- [x] README com manifesto + link Wikipedia
- [x] CONTRIBUTING com fluxo de Haskamah
- [x] CODE_OF_CONDUCT com Netzach Soul Clause
- [x] Este arquivo (OPEN_SOURCE_JUDAISM.md)

Médio prazo (em planejamento — ver [docs/holding-4-pillars.md](docs/holding-4-pillars.md)):

- [ ] Mirror público GitHub (este repositório)
- [ ] Versionamento semântico das Haskamoths
- [ ] Open Data pipeline para Reshimot (JSON público)
- [ ] Torah database com Sefaria-like interface
- [ ] Template repo para forkar Merkabah (outras comunidades)

Longo prazo (visão):

- [ ] Digital humanities tools (Gematria calculator, Hebrew OCR, etc)
- [ ] Lista de discussão aberta para forks
- [ ] Governance genérico substituível por qualquer comunidade de 3-7 pessoas

---

## Referências

- [Open Source Judaism — Wikipedia (EN)](https://en.wikipedia.org/wiki/Open_Source_Judaism)
- [Open Source Judaism — Wikipedia (PT)](https://pt.wikipedia.org/wiki/Juda%C3%ADsmo_de_c%C3%B3digo_aberto) *(se disponível)*
- [Sefaria](https://www.sefaria.org/) — exemplo de Torah database aberta
- [Open Siddur](https://opensiddur.org/) — exemplo de siddur copyleft
- [Plano Open Source Judaism (Shomer Adamah, 2026-06-26)](docs/holding-4-pillars.md) — versão interna resumida

---

## Licença

Este documento é parte do repositório Conselho Merkabah e está licenciado
sob CC-BY-SA 4.0. Veja [LICENSE](LICENSE).

---

*Que a Torá seja aberta como a terra. שומר אדמה.*
