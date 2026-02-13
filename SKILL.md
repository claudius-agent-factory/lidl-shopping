---
name: lidl-shopping
description: Sortiert Einkaufslisten nach dem typischen Ladenaufbau eines Lidl-Markts in Deutschland. Verwende diesen Skill, wenn der Nutzer eine Einkaufsliste "für Lidl sortieren" möchte, "in der richtigen Reihenfolge" braucht, oder eine "optimierte Einkaufsliste" für Lidl anfordert.
---

# Lidl Einkaufslisten-Sortierung

Sortiert Einkaufslisten nach dem typischen Weg durch einen Lidl-Markt (Eingang → Kasse, gegen den Uhrzeigersinn).

## Workflow

1. **Zutaten analysieren**: Erkenne die Kategorie jeder Zutat
2. **Sortieren**: Ordnung nach Ladenaufbau (siehe Referenz)
3. **Ausgabe**: Formatierte Liste mit Checkboxen

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
