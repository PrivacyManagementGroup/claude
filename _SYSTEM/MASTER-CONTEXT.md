# MASTER-CONTEXT.md - Christian Workerts Wissensdatenbank

Letzte Aktualisierung: 2026-02-03

---

## Quick Facts

| Eigenschaft | Wert |
|-------------|------|
| **Name** | Christian Workert |
| **Kuerzel** | CW |
| **Email** | cw@uaeandmore.com |
| **GitHub** | github.com/PrivacyManagementGroup |
| **Server** | 65.109.167.139 |
| **Command Center** | http://65.109.167.139:8080 |

---

## Team

| Name | Kuerzel | Email | Rolle |
|------|---------|-------|-------|
| Christian Workert | CW | cw@uaeandmore.com | Owner |

---

## Aktive Projekte

| Projekt | Status | Prioritaet | Beschreibung | Ordner |
|---------|--------|------------|--------------|--------|
| Website-Redesign | In Arbeit | Hoch | Testprojekt: Fiktive Website-Ueberarbeitung | `_PROJECTS/Website-Redesign - CW/` |
| Kunden-Onboarding | In Arbeit | Mittel | Testprojekt: Fiktiver Kunden-Prozess | `_PROJECTS/Kunden-Onboarding - CW/` |
| Internes-Tool | Ideensammlung | Niedrig | Testprojekt: Fiktives internes Werkzeug | `_PROJECTS/Internes-Tool - CW/` |
| Mein-Erstes-Projekt | Neu | - | Leere Vorlage fuer dein erstes echtes Projekt | `_PROJECTS/Mein-Erstes-Projekt - CW/` |

> **Hinweis:** Die ersten 3 Projekte sind Test-Projekte mit Beispieldaten. Du kannst sie loeschen sobald du eigene Projekte hast.

---

## Ordnerstruktur

```
Master-Knowledge/
├── CLAUDE.md
├── _SYSTEM/
│   ├── MASTER-CONTEXT.md      ← Diese Datei
│   ├── credentials.md
│   ├── changelog.md
│   ├── projects-index.md
│   ├── best-practices.md
│   └── infrastructure.md
│
└── _PROJECTS/
    ├── Website-Redesign - CW/
    ├── Kunden-Onboarding - CW/
    ├── Internes-Tool - CW/
    └── Mein-Erstes-Projekt - CW/
```

---

## Technische Infrastruktur

### Server
| Eigenschaft | Wert |
|-------------|------|
| **IP** | 65.109.167.139 |
| **OS** | Debian (Linux) |
| **User** | root |
| **Firewall** | Ports 22, 80, 443, 8080 offen |

### GitHub
| Eigenschaft | Wert |
|-------------|------|
| **Organisation** | PrivacyManagementGroup |
| **Repo** | claude (privat) |

---

## Arbeitsregeln

Alle Regeln stehen in `CLAUDE.md` (wird automatisch gelesen).
Kurzfassung: Session-Start → git pull + Kontext lesen. Session-Ende → Checkliste + git push.

---

## Letzte Aenderungen

### 2026-02-03
- Initiales Setup via Team-Onboarding durchgefuehrt
- Ordnerstruktur erstellt, 4 Test-Projekte angelegt
- Server konfiguriert, Command Center deployed
