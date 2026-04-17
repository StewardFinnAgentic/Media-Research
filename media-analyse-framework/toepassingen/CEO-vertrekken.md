# Toepassing: CEO-vertrekken in de Belgische pers

> Sector-specifieke invulling van het generieke Media-analyse Framework.  
> Basisprincipes: zie `../FRAMEWORK.md`  
> Versie: 1.0 | Opgesteld: 2026-04-17

---

## Artikeltypologie (milestones)

Elk artikel krijgt één type toegewezen:

| Type | Omschrijving | Typische kenmerken |
|------|-------------|-------------------|
| **A — Aankondiging geplande successie** | Vertrek wordt vooraf aangekondigd, CEO blijft nog aan | "zal vertrekken", "mandaat loopt af", "opvolger gezocht" |
| **B — Nieuwsbericht gepland vertrek** | Bevestiging van eerder aangekondigde exit | Kort, feitelijk, opvolger vaak bekend |
| **C — Nieuwsbericht plots vertrek** | Onverwacht, geen voorbereiding | "verrassend", "onmiddellijk", geen opvolger vermeld |
| **D — Achtergrondstuk** | Context, carrière, redenen, bedrijfsgeschiedenis | Lang, meerdere bronnen, historische duiding |
| **E — Commentaar / opiniestuk** | Mening of analyse van journalist/expert | Expliciet standpunt, implicaties voor sector |

---

## Extra analysedimensies (CEO-specifiek)

Bovenop de universele dimensies uit het framework:

| Dimensie | Wat meten | Schaal / codering |
|----------|-----------|-------------------|
| **Geciteerde actoren** | Wie spreekt in het artikel | CEO zelf / voorzitter RvB / analist / vakbond / anoniem / niemand |
| **Reden voor vertrek** | Hoe wordt het vertrek verklaard | mandaatseinde / aandeelhoudersdruk / deontologie / strategisch / vrijwillig / onduidelijk |
| **Opvolger** | Is een opvolger vermeld | ja-naam / ja-intern / ja-extern / interim / nee |
| **Verrassingsfactor** | Hoe gepland was het vertrek | gepland / half-verwacht / plots |

---

## Analysebestand per artikel

Bestandsnaam: `analyses/[publicatie]-[bedrijf]-[naam-ceo]-[datum].md`

```markdown
# Analyse: [artikeltitel]

**Artikel-id:** [publicatie]-[bedrijf]-[naam]-[datum]
**Bron:** [publicatie]
**Datum:** YYYY-MM-DD
**Artikeltype:** [A / B / C / D / E]
**Ruwe tekst:** `../artikelen/[bestandsnaam].md`

---

## Laag 1 — Observaties

### OBS-001
**Citaat:** "[exacte zin]" (§[n])
**Spreker:** [wie]
**Type:** directe quote / parafrase / vertellerstem

### OBS-002
...

### Opvallende stiltes
- [wat ontbreekt: bv. geen reactie van CEO zelf]

---

## Laag 2 — Interpretaties

### INT-001 (→ OBS-001)
**Dimensie:** toon
**Oordeel:** licht kritisch (−1)
**Reden:** [uitleg]
**Alternatief:** [andere lezing]

### INT-002 (→ OBS-002)
...

---

## Laag 3 — Conclusies

### C-01
**Stelling:** [conclusie]
**Gedragen door:** INT-001, INT-003
**Alternatieve verklaring:** [...]

---

## Samenvattende scores

| Dimensie | Score / label | Gedragen door |
|----------|--------------|---------------|
| Toon | −1 licht kritisch | INT-001, INT-002 |
| Zekerheid | hoog | INT-003 |
| Transparantie | laag | INT-004 |
| Geciteerde actoren | voorzitter RvB, analist | OBS-002, OBS-005 |
| Reden vertrek | mandaatseinde | OBS-001 |
| Opvolger | nee | OBS-003 |
| Verrassingsfactor | gepland | INT-002 |
| Artikeltype | B | — |
```

---

## Aggregatietabel

Bestand: `aggregatie.md`  
Één rij per geanalyseerd artikel. Wordt aangevuld na elke analyse.

```markdown
| Artikel-id | Type | Toon | Zekerheid | Transparantie | Actoren | Reden | Opvolger | Verrassing |
|------------|------|------|-----------|---------------|---------|-------|----------|------------|
| detijd-proximus-boutin-2025-02 | C | −1 | hoog | laag | RvB | strategisch | nee | plots |
| lesoir-belfius-raisiere-2026-02 | B | 0 | hoog | middel | — | mandaatseinde | nee | gepland |
```

---

*Toepassing op basis van: `../FRAMEWORK.md`*  
*Opgesteld door Ray | 2026-04-17*
