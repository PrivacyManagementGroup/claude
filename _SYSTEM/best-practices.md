# Best Practices - Bewaehrte Loesungen

Hier werden Loesungen dokumentiert, die sich bewaehrt haben.
Format: Problem → Loesung → Warum es funktioniert.

---

## Server & Deployment

### Website auf Server deployen
```bash
scp datei.html root@65.109.167.139:/var/www/html/
```
Funktioniert zuverlaessig fuer einzelne Dateien.

### SSL Zertifikat einrichten
```bash
certbot --nginx -d deinedomain.com
```
Kostenloses SSL von Let's Encrypt. Erneuert sich automatisch.

---

## Git Workflow

### Tagesablauf
1. `git pull origin main` (Start)
2. Arbeiten
3. `git add . && git commit -m "Beschreibung" && git push origin main` (Ende)

### Konflikte vermeiden
- Immer erst pullen bevor du arbeitest
- Am Ende immer pushen
- Nicht an mehreren Orten gleichzeitig die gleiche Datei bearbeiten

---

## Neue Best Practice hinzufuegen

Wenn du ein Problem geloest hast (>20 Min Debugging), dokumentiere es hier:
1. **Problem:** Was war das Problem?
2. **Loesung:** Was hat funktioniert?
3. **Warum:** Warum funktioniert es?

---

*Letzte Aktualisierung: 2026-02-03*
