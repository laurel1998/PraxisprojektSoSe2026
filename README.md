# Praxisprojekt SoSe2026 – Analyse und Visualisierung automatisierter Interaktionen

Willkommen im Repository **PraxisprojektSoSe2026**

Dieses Repository bildet die technische und organisatorische Grundlage des Praxisprojekts *„Analyse und Visualisierung automatisierter Interaktionen“*.
Es dient der Dokumentation, Planung und Entwicklung eines prototypischen Analyse- und Visualisierungssystems für automatisierte Kommentarinteraktionen auf Social-Media-Plattformen.

---

# Inhaltsverzeichnis

* Über das Projekt
* Forschungsfrage
* Projektziele
* Repository-Struktur
* Entwicklungsprozess

---

# Über das Projekt

Automatisierte Interaktionen sind ein fester Bestandteil des modernen Internets und begegnen Nutzern insbesondere auf Social-Media-Plattformen regelmäßig. Moderne Bots imitieren zunehmend menschliche Interaktionsmuster und erschweren dadurch die Unterscheidung zwischen menschlicher und automatisierter Aktivität.

Im Rahmen dieses Projekts wird ein prototypisches Analyse- und Visualisierungssystem entwickelt, das automatisierte Kommentarinteraktionen heuristisch analysiert und die Ergebnisse direkt im Nutzungskontext visualisiert.

---

# Forschungsfrage

Wie lassen sich automatisierte Interaktionen erkennen, analysieren und visualisieren?

---

# Projektziele

## Ziele des Projekts

* Entwicklung eines prototypischen Analyse- und Visualisierungssystems
* Analyse automatisierter Kommentarinteraktionen auf einer Social-Media-Plattform
* Kombination technischer, semantischer, verhaltensbasierter und koordinativer Analysemerkmale
* Visualisierung der Ergebnisse direkt im Nutzungskontext

---

# Repository-Struktur

| Pfad / Datei                                  | Beschreibung                                                 |
| --------------------------------------------- | ------------------------------------------------------------ |
| `/docs/`                                      | Enthält alle Projektdokumente                                |
| `/docs/ADR/`                                  | Architecture Decision Records (ADRs)                         |
| `/docs/Modelle/`                              | Architektur- und Domänenmodelle                              |
| `/docs/PoC/`                                  | Proof of Concepts (PoC)                                      |
| `/docs/PoC/MVP.md`                            | Definition des Minimal Viable Product                        |
| `/docs/Expose_Praxisprojekt.pdf`              | Exposé des Praxisprojekts                                    |
| `/docs/Risikoanalyse.md`                      | Risikoanalyse des Projekts                                   |
| `/docs/User-Stories.md`                       | User Stories und Nutzungsszenarien                           |
| `/prototype/`                                 | Prototypische Implementierung                                |
| `/datasets/`                                  | Testdaten und Beispieldatensätze                             |
| `CHANGELOG.md`                                | Dokumentation aller Änderungen                               |
| `README.md`                                   | Projektübersicht und Orientierung                            |

---

# Geplante Systemkomponenten

Das System soll verschiedene Analyseperspektiven kombinieren:

* Technische Analyse

  * Aktivitätsmuster
  * Timing
  * Wiederholungen

* Semantische Analyse

  * NLP-basierte Textanalyse
  * Ähnlichkeiten zwischen Kommentaren

* Verhaltensbasierte Analyse

  * Interaktionsmuster
  * Aktivitätsverhalten

* Koordinative Analyse

  * Beziehungen zwischen mehreren Accounts
  * Synchronisierte Aktivitäten

Die Analyseergebnisse sollen über eine verständliche Visualisierung, beispielsweise ein Ampelsystem oder Risk Scores, dargestellt werden.

---

# Technologien

Mögliche Technologien im Projekt:

* React
* Node.js
* PostgreSQL
* Selenium / Browser-Automation-Tools
* NLP-Bibliotheken
* JavaScript / TypeScript

Die konkrete technologische Umsetzung wird im Verlauf des Projekts festgelegt.

---

# Entwicklungsprozess

Das Projekt orientiert sich an folgenden Phasen:

1. Analyse des Problemraums
2. Konzeption und Entwicklung eines Proof of Concept
3. Entwicklung des Prototyps
4. Evaluation und Dokumentation

Alle wesentlichen Entscheidungen, Änderungen und Erkenntnisse werden fortlaufend dokumentiert.
