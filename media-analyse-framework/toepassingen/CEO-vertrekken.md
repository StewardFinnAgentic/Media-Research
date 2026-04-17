# Protocol: CEO-vertrekken in de Belgische pers

> Sector-specifieke invulling van het [Media-analyse Framework](../FRAMEWORK.md).  
> Versie: 1.2 | Opgesteld: 2026-04-17

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

## 2. Wat zoeken we — de zes dimensies

### Dimensie 1: Timing & moment

*Wanneer verschijnt het artikel in de levenscyclus van het vertrek?*

| Code | Type | Omschrijving | Signaalwoorden |
|------|------|-------------|----------------|
| **A** | Aankondiging geplande successie | Vertrek vooraf aangekondigd, CEO nog in functie | "zal vertrekken", "mandaat loopt af", "opvolger gezocht" |
| **B** | Nieuwsbericht gepland vertrek | Bevestiging van eerder aangekondigde exit | Kort, feitelijk, opvolger vaak al bekend |
| **C** | Nieuwsbericht plots vertrek | Onverwacht, geen voorbereiding zichtbaar | "verrassend", "onmiddellijk", geen opvolger |
| **D** | Achtergrondstuk | Context: carrière, beslissingen, bedrijfsgeschiedenis | Lang, meerdere bronnen, historisch |
| **E** | Commentaar / opiniestuk | Standpunt journalist of expert | Expliciet oordeel, implicaties sector |

Naast het type ook noteren:
- **Publicatiedatum t.o.v. vertrek:** dag van aankondiging / week erna / maanden later
- **Is dit het eerste artikel over dit vertrek, of een follow-up?**

---

### Dimensie 2: Artikeltype

Zie codes A–E hierboven. Elk artikel krijgt **één code**.

---

### Dimensie 3: Tone of voice

*Hoe spreekt het artikel over de CEO en het vertrek?*

| Score | Label | Wat het betekent |
|-------|-------|-----------------|
| −2 | Sterk kritisch | Expliciet negatief oordeel over CEO of vertrek |
| −1 | Licht kritisch | Nuance, vraagtekens, voorbehoud |
|  0 | Neutraal | Feitelijk, geen evaluatief taalgebruik |
| +1 | Licht positief | Erkentelijkheid, positieve bewoording |
| +2 | Sterk positief | Uitgesproken lof, eresaluut |

Elke score moet gedragen worden door minstens één citaat (OBS).

---

### Dimensie 4: Reden van vertrek

*Hoe wordt het vertrek verklaard in het artikel?*

| Code | Reden | Omschrijving |
|------|-------|-------------|
| **R1** | Mandaatseinde | Contract liep af, gepland vertrek |
| **R2** | Performance | Slechte resultaten, aandeelhoudersdruk, targets niet gehaald |
| **R3** | Visionsverschil | Strategische meningsverschillen met RvB of aandeelhouders |
| **R4** | Afwerving | CEO vertrekt voor andere functie elders |
| **R5** | Deontologie | Integriteitskwestie, gedragsprobleem, ethische grens |
| **R6** | Persoonlijk | Gezondheid, privéredenen, eigen keuze zonder externe druk |
| **R7** | Onduidelijk | Reden niet vermeld of expliciet vaag gehouden |

Meerdere codes mogelijk. Altijd met bewijs (citaat).

---

### Dimensie 5: Erkentelijkheid vanuit het bedrijf

*Wordt het vertrek positief geframed door het bedrijf zelf?*

Twee vragen:
1. **Is er een quote van aandeelhouders, RvB of voorzitter?** → ja / nee
2. **Wat is de toon van die quote?**

| Code | Toon institutionele reactie |
|------|----------------------------|
| **E1** | Warme erkentelijkheid ("we danken X voor zijn uitzonderlijke bijdrage") |
| **E2** | Formele erkenning ("het bestuur wenst X succes") |
| **E3** | Neutrale mededeling (geen waardering, enkel feit) |
| **E4** | Geen quote van bedrijf |
| **E5** | Afstandelijk of negatief ("met wederzijds akkoord", "na overleg") |

---

### Dimensie 6: Opvolging

*Wat weten we over de opvolger?*

| Code | Situatie |
|------|---------|
| **O1** | Opvolger bekend + naam vermeld |
| **O2** | Opvolger intern (geen naam) |
| **O3** | Opvolger extern gezocht |
| **O4** | Interim aangesteld |
| **O5** | Geen opvolger vermeld |

---

## 3. Mappenstructuur per project

```
[project-naam]/
├── artikelen/       ← ruwe teksten (.md), ongewijzigd
├── analyses/        ← één analysebestand per artikel
├── aggregatie.md    ← overzichtstabel alle analyses
├── [hoofdtabel].md  ← lijst van alle CEO-vertrekken
└── README.md        ← projectbeschrijving + link naar protocol
```

---

## 4. Bestandsnaamconventie

**Artikelen:** `[publicatie]-[bedrijf]-[naam-ceo]-[datum].md`
bv. `detijd-proximus-boutin-2025-02.md`

**Analyses:** zelfde naam, in `analyses/`
bv. `analyses/detijd-proximus-boutin-2025-02.md`

---

## 5. Analysebestand — template

```markdown
# Analyse: [artikeltitel]

**Artikel-id:** [publicatie]-[bedrijf]-[naam]-[datum]
**Bron:** [publicatie]
**Datum publicatie:** YYYY-MM-DD
**Artikeltype:** [A / B / C / D / E]
**Timing t.o.v. vertrek:** [dag van aankondiging / week erna / maanden later / onduidelijk]
**Eerste artikel of follow-up:** [eerste / follow-up]
**Ruwe tekst:** `../artikelen/[bestandsnaam].md`
**Geanalyseerd op:** YYYY-MM-DD

---

## Laag 1 — Observaties

### OBS-001
**Citaat:** "[exacte zin]" (§[n])
**Spreker:** [naam/rol of "vertellerstem"]
**Type:** directe quote / parafrase / vertellerstem

*(herhaal per relevante passage)*

### Opvallende stiltes
- [wat ontbreekt — bv. geen reactie CEO, geen quote RvB, opvolger niet vermeld]

---

## Laag 2 — Interpretaties

### INT-001 (→ OBS-001)
**Dimensie:** [toon / reden / erkentelijkheid / opvolging / timing]
**Oordeel:** [label + code]
**Reden:** [waarom dit oordeel]
**Alternatief:** [andere plausibele lezing]

*(herhaal per observatie)*

---

## Laag 3 — Conclusies

### C-01
**Stelling:** [conclusie in één zin]
**Gedragen door:** INT-001, INT-003
**Alternatieve verklaring:** [...]

---

## Samenvattende scores

| Dimensie | Score / code | Gedragen door |
|----------|-------------|---------------|
| Artikeltype | | — |
| Timing t.o.v. vertrek | | |
| Tone of voice | | |
| Reden vertrek | | |
| Erkentelijkheid bedrijf | | |
| Opvolging | | |
```

---

## 6. Aggregatietabel — template

```markdown
| Artikel-id | Type | Timing | Toon | Reden | Erkentelijkheid | Opvolging |
|------------|------|--------|------|-------|-----------------|-----------|
```

---

## 7. Werkproces

1. Artikel ontvangen → opslaan als `.md` in `artikelen/`
2. Analyse uitvoeren (Laag 1 → 2 → 3)
3. Opslaan in `analyses/`
4. Rij toevoegen aan `aggregatie.md`
5. Committen + pushen
6. Opdrachtgever valideert op GitHub
7. Feedback → nieuwe commit met reden

**Één artikel per run. Altijd committen voor het volgende.**

---

*Protocol op basis van: [Media-analyse Framework](../FRAMEWORK.md)*  
*Opgesteld door Ray | 2026-04-17*
