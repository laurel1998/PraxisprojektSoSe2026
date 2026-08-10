# 01-ADR: Plattformwahl

**Status:** entschieden  
**Datum:** 03-08-2026

---

## Kontext

Für die prototypische Umsetzung des Analyse- und Visualisierungssystems musste eine Social-Media-Plattform ausgewählt werden. Die Plattform bestimmt maßgeblich, welche Analysemerkmale umgesetzt werden können und welche technischen Möglichkeiten für Datenerfassung und Visualisierung bestehen.

Im Rahmen von PoC 01 wurden Reddit, YouTube, Mastodon und Threads hinsichtlich Datenzugang, verfügbarer Analysemerkmale sowie technischer Rahmenbedingungen untersucht.

---

## Optionen

- Reddit
- YouTube
- Mastodon
- Threads

---

## Entscheidung

Für die prototypische Umsetzung wird YouTube als Zielplattform verwendet.

Die Plattformwahl basiert auf einer Abwägung zwischen Datenverfügbarkeit, technischer Umsetzbarkeit und Eignung für die im MVP vorgesehenen Analysemerkmale. Reddit wurde im Projektverlauf zunächst als Zielplattform ausgewählt. Die praktische Validierung des Datenzugriffs zeigte jedoch, dass für die Nutzung der Reddit API ein Genehmigungsprozess erforderlich ist und der eingereichte Antrag für das Projekt abgelehnt wurde.

Die Entscheidung für YouTube basiert auf folgenden Kriterien:

- unkomplizierter Datenzugriff auf öffentliche Daten über API und DOM-Scraping
- gut rekonstruierbare Kommentar- und Threadstrukturen
- hohe Sichtbarkeit potenziell automatisierter Interaktionen
- ausreichende Verfügbarkeit relevanter Account- und Interaktionsdaten
- technisch überschaubarer Implementierungsaufwand

Im Vergleich der untersuchten Plattformen zeigte sich, dass Mastodon zwar die größte Merkmalsabdeckung bietet, die föderierte Architektur jedoch eine einheitliche Datenerhebung erschwert. Threads weist einen höheren Authentifizierungsaufwand sowie Einschränkungen bei Account- und Interaktionsdaten auf. Reddit bietet grundsätzlich geeignete Kommentar- und Threadstrukturen, steht aufgrund der Zugangsbeschränkungen jedoch nicht für die prototypische Umsetzung zur Verfügung. YouTube ermöglicht zwar keine vollständige Interaktionshistorie einzelner Nutzer, stellt jedoch eine geeignete Grundlage für die Analyse zeitlicher, semantischer und koordinationsbezogener Merkmale dar.

---

## Folgen und To-dos

**Folgen**

- Die weitere Entwicklung erfolgt auf Basis von YouTube
- Alle nachfolgenden Proofs of Concept orientieren sich an der YouTube-Datenstruktur
- Die Datenerfassung wird auf öffentliche Kommentar- und Interaktionsdaten ausgelegt

**To-dos**

- Datenzugriffsstrategie festlegen [(02-ADR)](/docs/ADR/02-adr-datenzugriffsstrategie.md)
- Umsetzung der Merkmalsanalyse [(02-PoC)](/docs/PoC/02-poc-merkmalsanalyse.md)

---

## Probleme

YouTube stellt keine vollständige Interaktionshistorie einzelner Nutzer bereit. Verhaltensmerkmale, die eine langfristige Analyse der Nutzeraktivität erfordern, können daher nur eingeschränkt berücksichtigt werden.

Der Schwerpunkt der Analyse liegt stattdessen auf verfügbaren semantischen, zeitlichen und koordinationsbezogenen Merkmalen. Insbesondere werden Kommentarinhalte, Antwortstrukturen sowie zeitliche Zusammenhänge zwischen Interaktionen betrachtet.