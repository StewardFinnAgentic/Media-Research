# Protocol: CEO-vertrekken in de Belgische pers

> Sector-specifieke invulling van het [Media-analyse Framework](../FRAMEWORK.md).  
> Versie: 1.1 | Opgesteld: 2026-04-17

---

## 1. Scope

**Wat valt in scope:**
- CEO's en gedelegeerd bestuurders van Belgische bedrijven (privé, beursgenoteerd, overheidsgebonden)
- Tijdvenster: 12 maanden trailing tenzij anders aangegeven
- Bronnen: De Tijd, L'Echo, Le Soir, La Libre, RTBF, Trends/Tendances

**Grensvallen (expliciete beslissing vereist per project):**
- Voorzitters RvB (geen CEO) → alleen opnemen als ze operationele rol hadden
- Sportclubs, vzw's → opnemen indien prominente Belgische instelling
- Belgische topmanagers bij buitenlandse bedrijven → case-by-case

---

## 2. Artikeltypologie

Elk artikel krijgt **één type**:

| Code | Type | Omschrijving | Typische signaalwoorden |
|------|------|-------------|------------------------|
| **A** | Aankondiging geplande successie | Vertrek vooraf aangekondigd, CEO nog in functie | "zal vertrekken", "mandaat loopt af", "opvolger gezocht" |
| **B** | Nieuwsbericht gepland vertrek | Bevestiging van eerder aangekondigde exit | Kort, feitelijk, opvolger vaak al bekend |
| **C** | Nieuwsbericht plots vertrek | Onverwacht, geen voorbereiding zichtbaar | "verrassend", "onmiddellijk", geen opvolger vermeld |
| **D** | Achtergrondstuk | Contextartikel: carrière, beslissingen, bedrijfsgeschiedenis | Lang, meerdere bronnen, historische duiding |
| **E** | Commentaar / opiniestuk | Standpunt journalist of expert over het vertrek | Expliciet oordeel, implicaties voor sector |

---

## 3. Analysedimensies

### Universele dimensies (uit framework)

| Dimensie | Schaal |
|----------|--------|
| Toon | −2 sterk kritisch → 0 neutraal → +2 sterk positief |
| Zekerheid | laag / middel / hoog |
| Transparantie | laag / middel / hoog |
| Agency | actief / passief / gemengd |

### CEO-specifieke dimensies

| Dimensie | Codering |
|----------|----------|
| Geciteerde actoren | CEO zelf / voorzitter RvB / analist / vakbond / anoniem / niemand |
| Reden voor vertrek | mandaatseinde / aandeelhoudersdruk / deontologie / strategisch / vrijwillig / onduidelijk |
| Opvolger | ja-naam / ja-intern / ja-extern / interim / nee |
| Verrassingsfactor | gepland / half-verwacht / plots |

---

## 4. Mappenstructuur per project

```
[project-naam]/                         bv. CEO-Research-2026/
├── artikelen/                          ← ruwe teksten (.md), ongewijzigd
├── analyses/                           ← één analysebestand per artikel
├── aggregatie.md                       ← overzichtstabel alle analyses
├── [hoofdtabel].md                     ← lijst van alle CEO-vertrekken
└── README.md                           ← projectbeschrijving + link naar protocol
```

---

## 5. Bestandsnaamconventie

**Artikelen:** `[publicatie]-[bedrijf]-[naam-ceo]-[datum].md`
- bv. `detijd-proximus-boutin-2025-02.md`
- bv. `lesoir-belfius-raisiere-2026-02-27.md`

**Analyses:** zelfde naam als het artikel, in `analyses/`
- bv. `analyses/detijd-proximus-boutin-2025-02.md`

---

## 6. Analysebestand — template

```markdown
# Analyse: [artikeltitel]

**Artikel-id:** [publicatie]-[bedrijf]-[naam]-[datum]
**Bron:** [publicatie]
**Datum publicatie:** YYYY-MM-DD
**Artikeltype:** [A / B / C / D / E]
**Ruwe tekst:** `../artikelen/[bestandsnaam].md`
**Geanalyseerd op:** YYYY-MM-DD

---

## Laag 1 — Observaties

### OBS-001
**Citaat:** "[exacte zin uit artikel]" (§[n])
**Spreker:** [naam/rol of "vertellerstem"]
**Type:** directe quote / parafrase / vertellerstem

### OBS-002
**Citaat:** "[...]" (§[n])
**Spreker:** [...]
**Type:** [...]

*(herhaal voor elke relevante passage)*

### Opvallende stiltes
- [wat ontbreekt: bv. CEO reageert niet, geen RvB-standpunt, geen opvolger vermeld]

---

## Laag 2 — Interpretaties

### INT-001 (→ OBS-001)
**Dimensie:** [toon / zekerheid / transparantie / actoren / reden / opvolger / verrassing]
**Oordeel:** [label + score indien van toepassing]
**Reden:** [waarom dit oordeel op basis van dit citaat]
**Alternatief:** [andere plausibele lezing]

### INT-002 (→ OBS-002)
*(zelfde structuur)*

---

## Laag 3 — Conclusies

### C-01
**Stelling:** [conclusie in één zin]
**Gedragen door:** INT-001, INT-003
**Alternatieve verklaring:** [wat zou dit anders kunnen verklaren]

---

## Samenvattende scores

| Dimensie | Score / label | Gedragen door |
|----------|--------------|---------------|
| Toon | | |
| Zekerheid | | |
| Transparantie | | |
| Agency | | |
| Geciteerde actoren | | |
| Reden vertrek | | |
| Opvolger | | |
| Verrassingsfactor | | |
| **Artikeltype** | | — |
```

---

## 7. Aggregatietabel — template

Bestand: `aggregatie.md` in de projectmap.

```markdown
# Aggregatie: [projectnaam]

| Artikel-id | Type | Toon | Zekerheid | Transparantie | Actoren | Reden | Opvolger | Verrassing |
|------------|------|------|-----------|---------------|---------|-------|----------|------------|
| | | | | | | | | |
```

---

## 8. Werkproces (stap voor stap)

1. Artikel ontvangen → opslaan als `.md` in `artikelen/` met metadata-header
2. Analyse uitvoeren via template (Laag 1 → 2 → 3)
3. Analysebestand opslaan in `analyses/`
4. Één rij toevoegen aan `aggregatie.md`
5. Committen + pushen → GitHub altijd in geldige tussenstand
6. Opdrachtgever valideert op GitHub
7. Feedback verwerken → nieuwe commit met reden

**Nooit meerdere artikelen in één run.** Elke stap is atomisch.

---

*Protocol op basis van: [Media-analyse Framework](../FRAMEWORK.md)*  
*Opgesteld door Ray | 2026-04-17*
