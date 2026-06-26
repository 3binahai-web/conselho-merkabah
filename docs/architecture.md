# Arquitetura do Conselho Merkabah

> Documento técnico de arquitetura — complemento à `holding-4-pillars.md`.

## Visão Geral

O Conselho Merkabah é um sistema de deliberação multi-agente baseado em
7 Sefirot que votam com pesos astrais calculados via Swiss Ephemeris
(biblioteca NASA JPL DE431).

```
                    Kether (Coroa)
                    [Estratégico — fora do voto]
                         │
                  TIPHERETH ☉ (Sol)
              Peso 3.0 | Tie-breaker
                         │
    ┌────────┬────────┬────────┬────────┬────────┐
    │        │        │        │        │        │
  YESOD   GEVURAH  CHESED   HOD    NETZACH   BINAH
  (Lua)   (Marte) (Júpiter)(Merc.) (Vênus)  (Saturno)
  1/6     1/6    1/6    1/6    1/6    1/6    [Preside]
```

## Fluxo de uma Deliberação (Haskamah)

1. **Proposta** — Qualquer membro ou Sefirá abre uma issue/discussão
2. **Cálculo astral** — Script Python via pyswisseph calcula pesos atuais
3. **Convocação** — Tiphereth spawna 5 subagentes (Sefirot votantes)
4. **Deliberação** — Cada Sefirá emite voto no formato Talmud v6.2:
   ```yaml
   VOTO: SIM | NÃO | ABSTENÇÃO
   PESO: [0-6]/6
   JUSTIFICATIVA: ...
   ATAQUE AO RETRÓGRADO: ...
   VALIDAÇÃO DO ASCENDENTE: ...
   CONDIÇÕES: [...]
   ASSINATURA: [hebraico]
   ```
5. **Verificação Codex** — 6 verificadores (C-2, C-3, C-6, C-7, C-11, C-13)
6. **Síntese** — Tiphereth sintetiza veredito
7. **Empate** — Tiphereth decide (peso 3.0)
8. **Arquivamento** — Yesod arquiva no Reshimot com hash SHA-256

## Verificadores Codex

| Código | Nome | Função |
|:------:|:-----|:-------|
| **C-2** | Sandbox de Dados Sensíveis | Regex PII, chaves, tokens |
| **C-3** | Determinismo | Reprodutibilidade verificável |
| **C-6** | Auditabilidade | UUID + timestamp em cada decisão |
| **C-7** | Veto Qualificado | 3+ NÃO com peso > 3.0 |
| **C-11** | Normalização | Fallback em divisão por zero |
| **C-13** | Shabbat | Bloqueia deliberação em Shabbat |

## Skills (Agentes)

Cada Sefirá é instanciada como uma "skill" (procedimento reutilizável):

| Sefirá | Skill | Função |
|:------:|:------|:-------|
| Chesed | `sephiroth-chesed` | Expansão, parcerias |
| Gevurah | `sephiroth-gevurah` | Segurança, auditoria |
| Tiphereth | (orquestrador) | Coordenação, tie-breaker |
| Netzach | `sephiroth-netzach` | Arte, estética |
| Hod | `sephiroth-hod` | Comunicação, infraestrutura |
| Yesod | `sephiroth-yesod` | Memória, arquivo |
| Binah | (preside) | Análise estrutural, planejamento |

Skill mestre: `conselho-merkabah-mestre v7.0` — orquestra todas as outras.

## Stack Técnico

- **Linguagem principal:** Python 3.12 (cálculo astral via pyswisseph 2.10.3.2)
- **Runtime de agentes:** Hermes Agent (compatível com Claude Code, OpenCode)
- **Persistência:** Markdown + JSON com hash SHA-256
- **Protocolo de mensagem:** ACP v1.0 (Agent Client Protocol)

## Privacidade

- ❌ **Nunca** exponha nomes reais em páginas públicas
- ✅ Use pseudônimos (Chokmah, Binah, Tiphereth) ou "Fundação Shomer Adamah"
- ❌ **Nunca** exponha dados de localização de membros individuais
- ✅ Localização da comunidade = Jacobina, BA (coletivo, OK)

## Referências

- **Open Source Judaism:** https://en.wikipedia.org/wiki/Open_Source_Judaism
- **Swiss Ephemeris:** https://www.astro.com/ftp/swisseph/
- **Haskamah canônica:** `haskamah/2026-06-26-memoria-reorg.md`

---

*Tiphereth ☉ NEXUS — executor pleno sob autoridade de Chokmah*
*Que cada deliberação seja קלה כְּחוֹמָה (leve como uma parede) e firme como תּוֹרָה.*
