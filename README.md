# 🇩🇪 Lern Deutsch mit Arash

**Deutsch A1 für Persischsprachige – Lernpfad mit Codes, Duell, Live-Raum und Lehrer-Konsole**
ساخته شده برای فارسی‌زبانانی که آلمانی یاد می‌گیرند

---

## 📁 Dateien

```
/
├── index.html      ← Lern-App (Lernpfad, Duell, Live-Raum, Rangliste)
├── konsole.html    ← Lehrer-Konsole (Login wie Liga-Konsole)
├── index2.html     ← Glossar (eigenständige Seite)
└── README.md
```

## 🚉 Stationen

Lesen & Aussprache · Präsens · Personalpronomen · Artikel · Akkusativ · Akkusativpronomen · Possessivpronomen · Modalverben · Einkaufen & Bestellen · war & hatte · Perfekt

Jede Station: Erklärung (Persisch) → Wörter (Paare) → Üben → Sätze bauen → Profi-Runde → Hausaufgabe mit Zertifikat.
Stufe **Basis**: Profi-Runde freiwillig. Stufe **Profi**: Profi-Runde Pflicht, schwerere Fragen in Duell und Live-Raum.

## 🔑 Codes & Daten

- Personen und Codes werden in `konsole.html` angelegt (Tab „Codes“).
- Firebase-Projekt `lern-deutsch-arash`, Bereich `lernpfad/`: `members`, `points`, `progress`, `best`, `log`, `seen`, `rooms`.
- Ohne Code kann man als Gast üben (nur lokal gespeichert). Alter Fortschritt aus der früheren Version wird beim ersten Öffnen übernommen.

## ➕ Neue Station hinzufügen

In `index.html` ein Objekt in `NEW_STATIONS` ergänzen (gleiches Format wie die anderen: `explain`, `match`, `practice`, `build`, `hw`, optional `plus`) und die `id` in die `ORDER`-Liste eintragen. Die Konsole enthält eine Stationsliste (`const STATIONS`) – dort die neue Station ebenfalls eintragen.

## 🚫 Projektregeln

- **Niemals** die Flagge der Islamischen Republik verwenden
- Alle Erklärungen **auf Persisch**, keine arabischen Vokalzeichen als Aussprachehilfe
- Kein externes CSS/JS-Framework – alles inline (außer Firebase)

## 👨‍💻 Entwickler

**Arash Guitoo**
