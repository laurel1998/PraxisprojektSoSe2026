# 01-ADR: Plattformwahl

**Status:** entschieden  
**Datum:** 10-07-2026

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

Für die prototypische Umsetzung wird Reddit als Zielplattform verwendet.

Die Plattformwahl basiert auf einer Abwägung zwischen Datenverfügbarkeit, technischer Umsetzbarkeit und Eignung für die im MVP vorgesehenen Analysemerkmale. Reddit bietet zwar nicht die umfassendste Abdeckung aller betrachteten Merkmale, stellt jedoch eine geeignete Grundlage für den Prototyp dar. Die Entscheidung basiert auf folgenden Kriterien:

- unkomplizierter Datenzugriff über API und DOM-Scraping
- gut rekonstruierbare Kommentar- und Threadstrukturen
- ausreichende Verfügbarkeit relevanter Account- und Interaktionsdaten
- technisch überschaubarer Implementierungsaufwand

Im Vergleich der untersuchten Plattformen zeigte sich, dass Mastodon zwar die größte Merkmalsabdeckung bietet, die föderierte Architektur jedoch eine einheitliche Datenerhebung erschwert. YouTube weist eine hohe Sichtbarkeit automatisierter Interaktionen auf und bietet umfangreiche Kommentar- und Threaddaten, ermöglicht jedoch keine vollständige Interaktionshistorie einzelner Nutzer. Threads weist einen höheren Authentifizierungsaufwand sowie Einschränkungen bei Account- und Interaktionsdaten auf.

---

## Folgen und To-dos

**Folgen**

- Die weitere Entwicklung erfolgt auf Basis von Reddit
- Alle nachfolgenden Proofs of Concept orientieren sich an der Reddit-Datenstruktur
- Die Datenerfassung wird auf den Zugriff öffentlicher Reddit-Daten ausgelegt

**To-dos**

- Datenzugriffsstrategie festlegen [(02-ADR)](/docs/ADR/02-adr-datenzugriffsstrategie.md)
- Umsetzung der Merkmalsanalyse [(02-PoC)](/docs/PoC/02-poc-merkmalsanalyse.md)

---

## Probleme

Reddit stellt keine Informationen über Follower oder das Verhältnis von Followern und Freunden bereit. Diese Merkmale können daher im MVP nicht berücksichtigt werden.

Stattdessen liegt der Schwerpunkt der Analyse auf verfügbaren verhaltens- und koordinationsbezogenen Merkmalen. Insbesondere auf Aktivitätsmustern, zeitlichen Zusammenhängen sowie der Analyse von Kommentar- und Threadstrukturen.