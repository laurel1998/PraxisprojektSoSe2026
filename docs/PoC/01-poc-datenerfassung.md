# 01-PoC: Datenerfassung

**Status:** In Progress

---

## Problem / Fragestellung

Für das geplante Analyse- und Visualisierungssystem müssen Kommentar-, Account- und Interaktionsdaten einer Social-Media-Plattform erfasst werden. Die Wahl der Plattform beeinflusst maßgeblich, welche Analysemerkmale später umgesetzt werden können.

Es soll geprüft werden, welche Plattform die für das Projekt relevanten Daten in ausreichender Qualität und Zugänglichkeit bereitstellt.

---

## PoC-Ziel

Evaluation geeigneter Plattformen und Datenzugriffsstrategien für die spätere prototypische Umsetzung.

Zentrale Fragen:

* Welche Plattform eignet sich am besten?
* Welche Daten sind verfügbar?
* Welche Zugriffsmöglichkeiten existieren?
* Welche Einschränkungen bestehen?

---

## Scope

Untersucht werden folgende Plattformen:

* Reddit
* YouTube
* Mastodon
* Threads

Im Fokus stehen ausschließlich öffentlich zugängliche Daten.

---

## Methodik

Für jede Plattform wird geprüft:

* Existenz einer API
* Zugriffsmöglichkeiten durch Scraping
* Authentifizierungsaufwand
* Rate Limits
* Moderationsform
* Sichtbarkeit automatisierter Interaktionen
* Validierungsmöglichkeiten
* Verfügbarkeit von:
  * Kommentaren
  * Replies (Rekonstruierbarkeit von Threadstrukturen)
  * Timestamps
  * Accountinformationen
  * Profilinformationen
  * Interaktionshistorien

Die Ergebnisse werden vergleichend dokumentiert.

---

## Evaluationskriterien

Eine Plattform gilt als geeignet, wenn:

* relevante Daten zuverlässig abrufbar sind
* der Zugriff technisch realisierbar ist
* ausreichend Merkmale für die Analyse extrahiert werden können
* der Aufwand im Projektkontext vertretbar bleibt

---

## Ressourcen

* Plattform APIs
* API-Dokumentationen
* Browser Developer Tools

---

## Durchführung

1. Analyse der offiziellen API-Dokumentationen der ausgewählten Plattformen
2. Prüfung der öffentlich sichtbaren Plattformstrukturen im Browser
3. Systematische Erfassung und Gegenüberstellung der Ergebnisse in einer Vergleichsmatrix
4. Bewertung der Plattformen auf Grundlage der Evaluationskriterien

---

## Ergebnisse

Wird im Verlauf ergänzt.

---

## Entscheidung / Konsequenzen

Wird nach Abschluss des PoC dokumentiert.

Die Ergebnisse bilden die Grundlage für:

* [01-ADR:](/docs/ADR/01-adr-plattformwahl.md) Plattformwahl
* [02-ADR:](/docs/ADR/02-adr-datenzugriffsstrategie.md) Datenzugriffsstrategie
