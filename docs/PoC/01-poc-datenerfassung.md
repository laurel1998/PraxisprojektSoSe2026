# 01-PoC: Datenerfassung

**Status:** Done

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

Die Ergebnisse der Plattformanalyse sind in einer [Vergleichsmatrix](/docs/PoC/Artefakte/01-PlattformVergleich.png) dokumentiert.

Die Auswertung zeigt, dass sich die untersuchten Plattformen insbesondere hinsichtlich der verfügbaren Account- und Interaktionsdaten sowie der technischen Rahmenbedingungen unterscheiden. Während alle Plattformen grundsätzlich öffentliche Daten für eine Analyse bereitstellen, bestehen deutliche Unterschiede beim Datenzugriff, der Verfügbarkeit relevanter Account-Merkmale sowie der Rekonstruierbarkeit von Interaktionsstrukturen.

Mastodon bietet die umfassendste Abdeckung der betrachteten Analysemerkmale. Die föderierte Architektur führt jedoch dazu, dass Datenzugang, Richtlinien und API-Funktionalitäten je nach Instanz variieren und eine einheitliche Datenerhebung erschweren. Reddit zeichnet sich durch gut rekonstruierbare Kommentar- und Threadstrukturen aus. YouTube weist eine hohe Sichtbarkeit automatisierter Interaktionen auf und bietet umfangreiche Kommentar- und Threaddaten, ermöglicht jedoch keine vollständige Interaktionshistorie einzelner Nutzer. Threads ist aufgrund höherer Zugangshürden und eingeschränkter Account- und Interaktionsdaten für den Projektkontext weniger geeignet.

---

## Entscheidung / Konsequenzen

Auf Basis der theoretischen Evaluation wurde Reddit zunächst als primäre Plattform für den MVP ausgewählt. Die praktische Validierung des API-Zugriffs zeigte jedoch, dass der Zugriff auf die Reddit API einen Genehmigungsprozess voraussetzt und der entsprechende Antrag abgelehnt wurde.

Aus diesem Grund wird YouTube als neue Plattform für die prototypische Umsetzung des MVP weiterverfolgt. Ausschlaggebend sind insbesondere der technisch unkomplizierte Zugang über die YouTube Data API und die gute Verfügbarkeit von Kommentar- und Threadstrukturen sowie die ausreichende Verfügbarkeit relevanter Merkmale für den MVP. Die detaillierte Begründung erfolgt im zugehörigen ADR.

Die Ergebnisse bilden die Grundlage für:

* [01-ADR:](/docs/ADR/01-adr-plattformwahl.md) Plattformwahl
* [02-ADR:](/docs/ADR/02-adr-datenzugriffsstrategie.md) Datenzugriffsstrategie