# CEO Research 2026

**Onderzoeksvraag:** Welke CEO's van Belgische bedrijven zijn ontslagen of zelf ontslag genomen in de laatste 12 maanden?

**Periode:** April 2025 – April 2026 (12 months trailing)
**Bronnen:** De Tijd, L'Écho, Le Soir, La Libre Belgique, Trends/TrendsTendances
**Opgesteld door:** Ray (all-purpose agent onder Steward)
**Datum aanmaak:** 2026-04-16

---

## Projectstructuur

```
CEO-Research-2026/
├── README.md                          # Dit bestand
├── ceo-vertrekken-belgie-2025-2026.md # Hoofdtabel CEO-vertrekken
├── artikelen/                         # Ruwe artikelteksten (.md)
├── analyses/                          # Één analysebestand per artikel
└── aggregatie.md                      # Overzichtstabel alle analyses
```

## Protocol

Analyse-aanpak: zie [`../media-analyse-framework/toepassingen/CEO-vertrekken.md`](../media-analyse-framework/toepassingen/CEO-vertrekken.md)  
Generiek framework: zie [`../media-analyse-framework/FRAMEWORK.md`](../media-analyse-framework/FRAMEWORK.md)

---

## Artikel-metadata conventie

Elk opgeslagen artikel begint met dit blok:

```
---
publicatie: [naam publicatie]
datum: YYYY-MM-DD
auteur: [naam auteur]
woordcount: [aantal]
url: [volledige URL]
---
```

---

## Methodologie

- Zoekopdrachten via De Tijd (browser, titels/snippets zonder login)
- Artikelteksten worden opgeslagen in `artikelen/` in .md formaat
- Default tijdvenster: 12 months trailing
- Gemarkeerd per betrouwbaarheidsniveau: ✅ Bevestigd | ⚠️ Verificatie aanbevolen
