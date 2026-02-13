---
name: lidl-shopping
description: Erstellt aus Rezepten sortierte Einkaufslisten für Lidl in Deutschland. Verwende diesen Skill wenn: (1) Nutzer eine Rezept-URL schickt und eine Einkaufsliste braucht, (2) eine bestehende Liste "für Lidl sortieren" möchte, (3) "optimierte Einkaufsliste" anfordert. Extrahiert automatisch Zutaten aus Rezept-Webseiten und sortiert nach Lidl-Ladenaufbau.
---

# Lidl Einkaufslisten-Sortierung

Erstellt aus Rezepten oder Zutatenlisten sortierte Einkaufslisten für Lidl.

## Workflow

1. **Rezept erfassen**: 
   - Bei URL: web_fetch nutzen, Zutaten aus Seite extrahieren
   - Bei Zutatenliste: Direkt verwenden
2. **Zutaten analysieren**: Erkenne die Kategorie jeder Zutat
3. **Sortieren**: Ordnung nach Lidl-Ladenaufbau (siehe Referenz)
4. **Ausgabe**: Formatierte Liste mit Checkboxen und Mengenangaben

## Sortierreihenfolge

```
1. Obst & Gemüse
2. Backshop
3. Frühstück
4. Trockensortiment
5. Fleisch & Wurst
6. Molkereiprodukte
7. Süßwaren
8. Tiefkühl
9. Drogerie
10. Getränke
```

## Produkt-Kategorien

Siehe [references/lidl-store-layout.md](references/lidl-store-layout.md) für die vollständige Zuordnungstabelle.

## Ausgabeformat

```markdown
**🛒 Einkaufsliste - Lidl**

## Obst & Gemüse
- [ ] Paprika, rot – 200 g
- [ ] Zwiebeln – 75 g

## Molkereiprodukte
- [ ] Sahne – 100 ml

## Fleisch & Wurst
- [ ] Putengeschnetzeltes – 400 g

## Trockensortiment
- [ ] Penne Rigate – 350 g
- [ ] Tomaten, gehackt – 400 g

---
📋 X Artikel insgesamt
```

## Hinweise

- Unbekannte Produkte → in Kategorie "Sonstiges" am Ende
- Mengenangaben beibehalten
- Checkboxen `[ ]` für Abhaken im Laden
