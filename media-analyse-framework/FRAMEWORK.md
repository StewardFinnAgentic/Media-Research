# Media-analyse Framework: End-to-End Traceability

> Generiek raamwerk voor de analyse van mediaberichten.  
> Sector-specifieke toepassingen hangen hieronder als aparte documenten.  
> Versie: 1.0 | Opgesteld: 2026-04-17

---

## Kernprincipe

Een mediaanalyse is pas valide als elke conclusie herleidbaar is naar de ruwe tekst.  
Drie lagen, strikt gescheiden:

```
RUWE TEKST → OBSERVATIES → INTERPRETATIES → CONCLUSIES
```

Elke stap verwijst naar de vorige. Een conclusie zonder observatie is een mening. Een observatie zonder tekstanker is niet verifieerbaar.

---

## De drie lagen

### Laag 1 — Observatie
*Wat staat er letterlijk?*

- Exacte citaten met locatie (§ paragraafnummer)
- Wie spreekt? Directe quote / parafrase / enkel vermeld
- Wat ontbreekt opvallend? (stilte is ook data)

**Regel:** geen interpretatie op dit niveau. Alleen waarnemen.

---

### Laag 2 — Interpretatie
*Wat betekent dit?*

- Één interpretatie per observatie
- Altijd gelinkt aan de observatie die hem draagt
- Schaal waar mogelijk — niet "kritisch" maar "licht kritisch / kritisch / sterk kritisch"
- Alternatieve lezing vermelden als die plausibel is

**Regel:** geen conclusies op dit niveau. Alleen duiden.

---

### Laag 3 — Conclusie
*Wat is het patroon?*

- Alleen op basis van meerdere interpretaties
- Expliciet vermelden welke interpretaties de conclusie dragen
- Verplicht: alternatieve verklaring ("dit patroon kan ook verklaard worden door...")

**Regel:** geen nieuwe observaties introduceren. Alleen synthetiseren.

---

## Analysedimensies (universeel)

| Dimensie | Wat meten | Schaal |
|----------|-----------|--------|
| **Toon** | Evaluatief taalgebruik t.a.v. het onderwerp | −2 sterk kritisch → 0 neutraal → +2 sterk positief |
| **Zekerheid** | Modaliteit van uitspraken ("zou", "is", "lijkt") | laag / middel / hoog |
| **Transparantie** | Wat wordt gezegd vs. wat ontbreekt | laag / middel / hoog |
| **Bronstructuur** | Wie spreekt, wie zwijgt, wie wordt geparafraseerd | open codering |
| **Thema's** | Inductief eerste batch; daarna deductief codeboek | open codering |
| **Agency** | Wie handelt actief, wie ondergaat | actief / passief / gemengd |

---

## Traceability-structuur

Elke analyse volgt deze hiërarchie:

```
artikel-id
└── observatie-001
│     citaat: "exacte zin uit artikel"  §3
│     dimensie: toon
│     └── interpretatie: licht kritisch (−1)
│           reden: negatief modaal werkwoord + CEO krijgt geen weerga
│           alternatief: journalistieke stijl, niet per se intentioneel
│           └── bijdrage aan conclusie: C-02
└── observatie-002
      ...

conclusie-C-02
  gedragen door: observatie-001, observatie-004, observatie-007
  stelling: artikel kadert vertrek als probleem, niet als overgang
  alternatief: selectie van citaten beperkt — meer tekst nodig voor zekerheid
```

---

## Werkproces (atomisch)

1. **Artikel binnenkomt** → opslaan in `artikelen/` (ruwe tekst, ongewijzigd)
2. **Analyse uitvoeren** → één artikel per run, opslaan in `analyses/`
3. **Aggregatietabel updaten** → één rij toevoegen aan `aggregatie.md`
4. **Committen + pushen** → GitHub is altijd in geldige tussenstand
5. **Validatie** → opdrachtgever reviewt op GitHub, feedback als comment of issue
6. **Correctie indien nodig** → nieuwe commit met wijziging + reden

**Nooit batches.** Werkverlies is structureel onmogelijk als elke stap atomisch is.

---

## Mappenstructuur (generiek)

```
[project-naam]/
├── artikelen/          ← ruwe artikelteksten (.md), ongewijzigd
├── analyses/           ← één analysebestand per artikel (.md)
├── aggregatie.md       ← overzichtstabel alle analyses
└── FRAMEWORK.md        ← dit document (of link ernaar)
```

---

## Codering: open vs. gesloten

**Eerste batch (inductief):**  
Laat de teksten zelf de categorieën genereren. Geen vooraf bepaalde thema's.  
Na de eerste batch: codeboek opstellen op basis van wat gevonden werd.

**Volgende batches (deductief):**  
Codeer met het vastgestelde codeboek.  
Nieuwe categorieën zijn toegestaan maar worden expliciet gemarkeerd als `[NIEUW]`.

---

## Falsifieerbaarheid — checklist

Een analyse is falsifieerbaar als:

- [ ] Elk oordeel heeft minstens één citaat als anker
- [ ] Citaten zijn gelokaliseerd (§ of alineanummer)
- [ ] Alternatieve interpretatie is overwogen en vermeld
- [ ] Conclusies verwijzen expliciet naar de interpretaties die hen dragen
- [ ] Ontbrekende informatie is genoteerd, niet genegeerd

---

*Opgesteld door Ray | 2026-04-17*  
*Sector-specifieke toepassingen: zie `toepassingen/`*
