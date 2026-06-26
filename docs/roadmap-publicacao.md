# Roadmap de Publicação — Open Source Judaism
**Data:** 27 de junho de 2026
**Mandato:** Ordem Binah v2 — Parte I, Ordem 7
**Status:** Documento de planejamento. Nenhuma publicação automática.

---

## Filosofia de Publicação

> "Publicar é aterrar, aterrar é publicar" — Binah

A publicação não é evento único — é processo contínuo de **aterrar** conteúdo no
mundo digital com mesma reverência que se aterra semente em solo fértil.

**Princípios:**
1. Cada item publicado deve ter propósito claro
2. Cada publicação deve ser verificada (UUID + hash)
3. Tudo sob CC-BY-SA 4.0 (copyleft)
4. **NUNCA publicar:** dados pessoais, localização do terreno, detalhes financeiros

---

## Fase 1 — AGORA (junho-julho 2026)

### ✅ Já publicado
- Repositório `conselho-merkabah` (GitHub, público)
- Repositório `shomer-adamah-site` (GitHub, público)
- LICENSE CC-BY-SA 4.0
- 3 Haskamoth canônicas (Promessa 40 Anos, Talmud v6.2, Memória Reorg)
- 5 Skills standalone
- Site https://shomeradamah.ca com SEO estático (meta tags, JSON-LD, robots.txt, sitemap.xml, llms.txt)

### 🟡 Em revisão (auditoria concluída, aguardando aprovação)
- **Haskamoth Tier 1:** 2 docs curados (já no repo)
- **Haskamoth Tier 2:** 7 docs precisam edição editorial
- **Skills Tier 1 + Sefirot:** 10 skills prontas para migração
- **README.md:** atualizado (este commit)

### 🔴 Bloqueado (Ordem Binah v2 Parte III)
- ❌ Modificar shomeradamah.ca (aguarda ratificação Chokmah)
- ❌ Listar membros do Conselho (aguarda decisão)
- ❌ Configurar GitHub Pages (aguarda auditoria)

---

## Fase 2 — Curto-Médio Prazo (3-6 meses: julho-dezembro 2026)

### Publicações previstas

#### Repositório `conselho-merkabah`
- **+5 Haskamoth** (após edição editorial das Tier 2)
- **+10 Skills** (Tier 1 + Sefirot individuais, formato standalone)
- **+3 documentos `docs/`:**
  - `protocolo-haskamah.md` (procedimento detalhado)
  - `sefirot-glossario.md` (vocabulário canônico)
  - `casos-estudo.md` (exemplos históricos de deliberação)

#### Repositório `shomer-adamah-site`
- **+1 página:** `/governanca` (link para repo conselho-merkabah)
- **+1 página:** `/transparencia` (Haskamoth públicas + licenças)
- **+1 página:** `/contato` (canais de comunicação)

#### Novos repositórios (sob critério)
- **`adamah-tech`** (quando houver conteúdo agroflorestal real)
- **`wall-done`** (quando houver código de construção real)
- **`daath`** (database de Torá + textos sagrados estruturados)

### Marcos da Fase 2
- ✅ 8+ Haskamoth publicadas (Tier 1 + Tier 2)
- ✅ 15+ Skills standalone disponíveis
- ✅ Site com seção "Governança" pública
- ✅ Primeiras contribuições externas (issues + PRs)

### NÃO publicar na Fase 2
- ❌ Identidade real dos membros
- ❌ Localização do terreno da comunidade
- ❌ Detalhes financeiros ou de governança interna
- ❌ Decisões pré-deliberação (rascunhos)

---

## Fase 3 — Médio-Longo Prazo (6-12 meses: janeiro-julho 2027)

### Publicações previstas

#### Expansão da infraestrutura
- **GitHub Pages ativo** — mirror estático do `conselho-merkabah` para SEO público
- **CI/CD pipeline** — validação automática de UUID + hash em cada commit
- **Issue bot** — triagem automática baseada em templates de Haskamah

#### Repositórios avançados
- **`merkaba-council`** (camada IA da Merkabah, se separado do principal)
- **`open-data-torah`** (database estruturado de textos sagrados, se aplicável)
- **`adamah-protocols`** (protocolos agroflorestais abertos)

#### Integração externa
- **RSS feed** de Haskamoth publicadas
- **API pública** para consulta de deliberações (somente leitura)
- **MIRROR em outros hosts** (Codeberg, GitLab, Internet Archive)

### Marcos da Fase 3
- ✅ 20+ Haskamoth publicadas
- ✅ 25+ Skills standalone
- ✅ 5+ repositórios públicos
- ✅ Contribuições externas regulares (issues + PRs)
- ✅ Tráfego orgânico mensurável (Google, llms.txt consumers)

---

## Critérios de Aprovação por Publicação

### Para cada Haskamah publicada
1. ✅ UUID único gerado e verificado
2. ✅ Hash SHA-256 gerado e assinado
3. ✅ Revisão editorial (mascarar nomes próprios)
4. ✅ Assinatura formal da Sefirah autora
5. ✅ Ratificação por Beit Din (Lua Nova)

### Para cada Skill publicada
1. ✅ Formato `SKILL.md` com YAML frontmatter
2. ✅ README próprio com exemplos de uso
3. ✅ `requirements.txt` se usar libs externas
4. ✅ Testado em pelo menos 1 framework fora do Hermes

### Para cada Página no Site
1. ✅ Aprovação explícita de Chokmah (devido à proteção do design)
2. ✅ i18n: 4 locales (pt/en/es/he)
3. ✅ Meta tags + JSON-LD + SEO estático
4. ✅ Backup antes do deploy

---

## Riscos e Mitigações

| Risco | Mitigação |
|-------|-----------|
| Vazamento de informação privada | Revisão editorial obrigatória antes de publicar |
| Conflito com ordens diretas de Chokmah | Verificação cruzada com ordens recentes antes de cada publicação |
| Reputação danificada por publicação prematura | Fase 1 conservadora, escalar após tração |
| Dependência de GitHub | Mirror em Codeberg/GitLab na Fase 3 |
| Sobrecarga de manutenção | Publicações em batches, não item por item |

---

## Decisões Pendentes (Chokmah/Binah)

1. **Identidade dos membros:** Listar como "7 Sefirot" ou manter sigilo absoluto?
2. **Org `shomer-adamar`:** Criar manualmente ou aguardar token admin?
3. **GitHub Pages:** Ativar mirror estático do repo conselho-merkabah?
4. **Domínio próprio:** Usar `merkaba.council` para o Conselho (separado do site)?
5. **Mirror em Codeberg:** Criar desde já ou esperar Fase 3?

---

## Métricas de Sucesso

### Fase 1 (agora)
- [x] 2 repos públicos com LICENSE
- [x] 3 Haskamoth curadas
- [x] Site com SEO básico
- [ ] README atualizado ← **executado hoje**

### Fase 2 (julho-dezembro 2026)
- [ ] 8+ Haskamoth publicadas
- [ ] 15+ Skills standalone
- [ ] 10+ estrelas no GitHub
- [ ] 3+ contribuidores externos

### Fase 3 (janeiro-julho 2027)
- [ ] 5+ repos públicos
- [ ] 25+ Skills standalone
- [ ] GitHub Pages ativo
- [ ] Tráfego orgânico mensurável

---

**Autor:** Tiphereth — sob autoridade de Chokmah e mandato de Binah v2
**Próxima revisão:** Lua Nova 2026-07-26 (Beit Din Merkabah)
**Bloqueios ativos:** Nenhum para este documento de planejamento
