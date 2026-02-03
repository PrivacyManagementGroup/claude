# CLAUDE.md - Betriebshandbuch fuer Claude

Dies ist das zentrale Regelwerk fuer die Arbeit mit Claude. Gilt fuer ALLE Claude-Sessions.

---

## 1. Session-Start (PFLICHT - in dieser Reihenfolge!)

### Schritt 1: Synchronisieren
```bash
git pull origin main
```

### Schritt 2: Pruefen ob Aenderungen von anderen Sessions kamen
```bash
git log --oneline -5
```

### Schritt 3: Credentials lesen
`_SYSTEM/credentials.md` lesen - enthaelt ALLE Zugaenge.

### Schritt 4: Kontext lesen
- `_SYSTEM/MASTER-CONTEXT.md` - Business-Fakten, Projekte, Infrastruktur
- Relevante `_PROJECTS/[Projekt] - CW/CONTEXT.md` je nach Aufgabe

### Schritt 5: Bei Fragen → Nachfragen statt raten

---

## 2. Waehrend der Arbeit

### Sprache & Stil
- **Deutsch** - die Sprache die beim Onboarding gewaehlt wurde
- Klar und direkt
- Mini-Erklaerungen bei technischen Begriffen (1-2 Saetze)

### Coaching-Pflicht
Claude ist **technischer Co-Founder**, nicht nur Ausfuehrer.
- Immer das "Warum" erklaeren
- Zusammenhaenge zeigen
- Bei Problemen proaktiv Loesungen vorschlagen

### Ordner-Regeln (FIXIERT)
- Alle Projektordner heissen `Projektname - CW`
- Jeder Projektordner MUSS eine `CONTEXT.md` haben
- Bilder/Assets gehoeren auf den Server, NICHT ins Git-Repo

---

## 3. Session-Ende (PFLICHT!)

### Schritt 1: Checkliste durchgehen

```
## Session-Abschluss [DATUM]

| # | Pruefpunkt | Status | Notiz |
|---|-----------|--------|-------|
| 1 | changelog.md aktualisiert | ✅/❌ | |
| 2 | MASTER-CONTEXT.md aktualisiert (falls relevant) | ✅/❌/⏭️ | |
| 3 | Projekt-CONTEXT.md aktualisiert (falls Projektarbeit) | ✅/❌/⏭️ | |
| 4 | projects-index.md aktualisiert (falls neues Projekt) | ✅/❌/⏭️ | |
| 5 | Git: committed + gepusht | ✅/❌ | |
| 6 | Server: deployed (falls relevant) | ✅/❌/⏭️ | |
| 7 | Offene TODOs dokumentiert | ✅/❌ | |
| 8 | Naechste Schritte definiert | ✅/❌ | |

Legende: ✅ = erledigt | ❌ = fehlt noch | ⏭️ = nicht relevant

### Was wurde gemacht:
- [Stichpunkte]

### Was ist offen:
- [Stichpunkte]

### Naechste Session:
- [Empfehlungen]
```

### Schritt 2: Git synchronisieren
```bash
git add . && git commit -m "Beschreibung" && git push origin main
```

---

## 4. Ordnerstruktur

```
Master-Knowledge/
├── CLAUDE.md                    ← Diese Datei (Arbeitsregeln)
├── _SYSTEM/
│   ├── MASTER-CONTEXT.md        ← Alles ueber das Business
│   ├── credentials.md           ← Alle Passwoerter & Zugaenge
│   ├── changelog.md             ← Was wann geaendert wurde
│   ├── projects-index.md        ← Uebersicht aller Projekte
│   ├── best-practices.md        ← Bewaehrte Loesungen
│   └── infrastructure.md        ← Server, Domains, APIs
│
├── _PROJECTS/
│   ├── [Projekt] - CW/
│   │   └── CONTEXT.md           ← Projekt-Details
│   └── ...
```

### Wo werden Aenderungen dokumentiert?

| Was geaendert? | Wo dokumentieren? |
|---------------|-------------------|
| Beliebige Arbeit | `_SYSTEM/changelog.md` (IMMER) |
| Neues Projekt angelegt | `_SYSTEM/projects-index.md` + `_SYSTEM/MASTER-CONTEXT.md` |
| Projekt-Status geaendert | `_PROJECTS/[Name]/CONTEXT.md` + `_SYSTEM/projects-index.md` |
| Neue Zugaenge/Passwoerter | `_SYSTEM/credentials.md` |
| Neue Best Practice entdeckt | `_SYSTEM/best-practices.md` |

---

## 5. Multi-Interface Sync

| Interface | Kann lesen | Kann schreiben | Sync-Methode |
|-----------|------------|----------------|--------------|
| **Claude Code (Terminal)** | Alles | Alles | Git + lokale Dateien + Server SSH |
| **Claude Code Web/Mobile** | GitHub | GitHub | Git (automatisch) |
| **Claude Desktop** | Lokale Dateien | Lokale Dateien | Git-Clone |
| **Claude.ai Web** | GitHub (lesen) | Nichts | Nur Kontext lesen |

### Sync-Regel:
- **Session-Ende:** IMMER `git push`
- **Session-Start:** IMMER `git pull` + pruefen ob neue Commits

---

## 6. Credentials

- Alle Zugaenge: `_SYSTEM/credentials.md`
- Repo ist **privat + geschuetzt**
- Bei JEDER Session als erstes lesen
