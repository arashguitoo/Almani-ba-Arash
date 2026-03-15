# 🇩🇪 Lern Deutsch mit Arash

**Eine mobile-freundliche Deutsch-Lern-App für Persischsprachige**  
ساخته شده برای فارسی‌زبانانی که می‌خواهند آلمانی بیاموزند

---

## 🔗 Live Demo

Nach dem Aktivieren von GitHub Pages:  
`https://<dein-username>.github.io/<repo-name>/`

---

## 📁 Dateistruktur

```
/
├── index.html      ← Haupt-App (Lernpfad, Lektionen, Spiele, Quiz)
├── index2.html     ← Vollständiges Glossar (eigenständige Seite)
├── .gitignore
└── README.md
```

---

## 📚 Lektionen (aktueller Stand)

| Gam | Titel | Inhalt |
|-----|-------|--------|
| گام ۰ | Das deutsche Alphabet | Buchstaben, Ausspracheregeln, Umlaute |
| گام ۱ | Ich heiße Minoo | Personalpronomen, heißen/kommen/sprechen/sein |
| گام ۲ | Das ist ein Tisch | Präsens-Vertiefung, Ausnahmen, Artikelsystem (Nom.) |
| گام ۳ | Ich habe eine Schwester | haben, Akkusativ, Familie, kein/keine |
| گام ۴ | Wohin gehst du? | W-Fragen, Lokalpräpositionen: aus/von/zu/in/auf |

---

## 🛠️ GitHub Pages aktivieren

1. Repository auf GitHub erstellen und Dateien hochladen  
2. **Settings → Pages → Source:** `main` Branch, Root `/`  
3. Speichern — nach 1–2 Min ist die App live

---

## 🔄 Entwicklungsregeln (WICHTIG)

### ✅ Neue Lektion hinzufügen — Checkliste

**1. `index.html` — Lernpfad-Karte ergänzen:**
```html
<!-- In der .path-list, nach dem letzten .path-card -->
<div class="path-card stepN" onclick="openLesson('lessonN')">
  <div class="card-num">🔤</div>
  <div class="card-info">
    <div class="card-title"><span class="badge-new">جدید</span>گام N: Titel</div>
    <div class="card-desc">Kurzbeschreibung auf Persisch</div>
    ...
  </div>
</div>
```

**2. `index.html` — Lektion-Section ergänzen:**
```html
<section id="sec-lessonN" class="animate-in">
  <!-- Sub-Tabs, Lerninhalt, Spiele, Quiz -->
</section>
```

**3. `index.html` — GLOSSARY Array ergänzen:**
```javascript
// Am Ende des GLOSSARY_EXTRA Arrays:
{de:'neues Wort', fa:'معنی', src:'گام N'},
```

**4. `index2.html` — GLOSSARY Array IDENTISCH ergänzen:**
```javascript
// Gam N
{de:'neues Wort', fa:'معنی', src:'گام N'},
```

> ⚠️ **Regel:** Beide `GLOSSARY`-Arrays müssen immer identisch sein!  
> Der Fehler `];` doppelt am Ende ist das häufigste Problem — immer prüfen!

---

## 🎮 Spieltypen (wiederverwendbar)

| Funktion | Beschreibung | Aufruf |
|----------|-------------|--------|
| `buildFill(cid, data, st, key, nextFn)` | Lückentext-Spiel | Fill-Blank |
| `buildMatch(cid, data, st, key, nextFn)` | Jetzt-Paare-finden | Matching |
| `buildSBGen(cid, data, st, key, nextFn)` | Sätze per Klick bauen | Sentence Builder |
| `startGenQuiz(cid, data, st, key, backFn, lessonId)` | 4-Antworten-Quiz | Multiple Choice |

---

## 📖 Glossar-Sync

`index2.html` ist eine **eigenständige** Glossar-Seite.  
Bei jeder Änderung am `GLOSSARY_EXTRA` in `index.html` muss das `GLOSSARY`-Array in `index2.html` **manuell synchron gehalten** werden.

**Häufige Fehler:**
- Doppeltes `];` am Array-Ende → Script-Fehler
- Fehlende/unterschiedliche Einträge zwischen beiden Dateien
- Apostroph `'` in Wörtern → durch `&#39;` ersetzen

---

## 🚫 Projektregeln

- **Niemals** die Flagge der Islamischen Republik verwenden
- Alle Erklärungen **auf Persisch**
- Kein externes CSS/JS-Framework — alles inline

---

## 👨‍💻 Entwickler

**Arash Guitoo**  
*Entwickelt mit ❤️ für Persischsprachige, die Deutsch lernen*
