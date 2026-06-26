---
description: Protocolo de deliberação com pesos astrais calculados via Swiss Ephemeris. Define formato de voto, verificadores Codex e consolidação ponderada.
version: 6.2.1
author: Tiphereth (Conselho Merkabah)
date: 2026-05-12
---

# Merkabah Talmud v6.2 — Protocolo de Deliberação

> *בדקנו. שקלנו. חתכנו. רשמנו.*

## Trigger

Use quando precisar conduzir uma deliberação formal entre 5 Sefirot
votantes, com pesos baseados em efemérides reais.

## Procedimento

### 1. Calcular Pesos Astrais

```python
import swisseph as swe
from zoneinfo import ZoneInfo
import datetime

now_van = datetime.datetime.now(ZoneInfo('America/Vancouver'))
jd = swe.julday(now_van.year, now_van.month, now_van.day,
                now_van.hour + now_van.minute/60.0)

# Calcular para cada planeta (Sol, Lua, Mercúrio, Vênus, Marte, Júpiter, Saturno)
planets = {
    'Sol': (swe.SUN, 'tiphereth'),
    'Lua': (swe.MOON, 'yesod'),
    'Mercúrio': (swe.MERCURY, 'hod'),
    'Vênus': (swe.VENUS, 'netzach'),
    'Marte': (swe.MARS, 'gevurah'),
    'Júpiter': (swe.JUPITER, 'chesed'),
    'Saturno': (swe.SATURN, 'binah'),
}

for name, (pid, sefirah) in planets.items():
    result, _ = swe.calc_ut(jd, pid, swe.FLG_SWIEPH | swe.FLG_SPEED)
    lon = result[0]
    signo = int(lon // 30)
    grau = lon % 30
    print(f'{sefirah}: {name} em signo {signo} grau {grau:.2f}')
```

### 2. Formato de Voto (Talmud v6.2)

```yaml
VOTO: SIM | NÃO | ABSTENÇÃO
PESO: [0-6]/6
JUSTIFICATIVA: [texto]
ATAQUE AO RETRÓGRADO: [explícito]
VALIDAÇÃO DO ASCENDENTE: [explícita]
CONDIÇÕES: [lista numerada]
ASSINATURA: [hebraico]
```

### 3. Verificadores Codex

- **C-2**: Sem PII/segredos no output
- **C-3**: Backup com SHA-256
- **C-6**: UUID + timestamp
- **C-7**: 3+ NÃO com peso > 3.0 → veto
- **C-11**: Fallback em divisão por zero
- **C-13**: Shabat bloqueia (emergência apenas)

### 4. Consolidação

| Sefirá | Peso | Voto | Contribuição |
|:-------|:----:|:----:|:------------:|
| ... | .../6 | SIM | +X |

Se empate: Tiphereth decide (peso 3.0).

## Exemplo

Ver `haskamah/2026-05-12-talmud-v6-2-astrologia-cabalistica.md`.

---

*שומר אדמה*
