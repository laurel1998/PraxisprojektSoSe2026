# 02-PoC: Merkmalsextraktion und Analyse

**Status:** In Progress

---

## Problem / Fragestellung

Die Literatur beschreibt zahlreiche Merkmale zur Erkennung automatisierter Interaktionen. Allerdings ist unklar, welche dieser Merkmale im gewählten Plattformkontext tatsächlich verfügbar, technisch extrahierbar und für eine heuristische Bewertung sinnvoll nutzbar sind.

Es soll geprüft werden, welche Merkmalsgruppen praktisch umsetzbar sind und welche Hinweise sie auf automatisierte Interaktionen liefern können.

---

## POC-Ziel

Validierung der definierten Merkmalsgruppen und Prüfung ihrer praktischen Umsetzbarkeit.

Zentrale Fragen:

* Welche Merkmale sind technisch messbar?
* Welche Merkmale liefern brauchbare Hinweise bzw. eignen sich für die heuristische Bewertung?
* Welche Merkmale stehen auf Reddit tatsächlich zur Verfügung?

---

## Scope

Untersucht werden die im Forschungsstand abgeleiteten Merkmalsgruppen:

* technische Merkmale
* semantische Merkmale
* verhaltensbasierte Merkmale
* koordinative Merkmale

Im Fokus steht zunächst die Analyse einzelner Kommentarinteraktionen und ihrer unmittelbaren Kontexte. Nicht verfügbare Merkmale werden dokumentiert und für den MVP ausgeschlossen.

---

## Methodik

Für jede Merkmalsgruppe wird untersucht:

- ob das Merkmal auf Reddit verfügbar ist
- ob es technisch extrahiert werden kann
- welchen potenziellen Beitrag es zur heuristischen Bewertung leistet
- welcher Implementierungsaufwand für den MVP zu erwarten ist

Die Ergebnisse werden vergleichend dokumentiert.

---

Technische Merkmale: 

MERKMALE spezifizieren!!

* Accountinformationen (u.a. Accountalter,... ???)
* Anzahl von Interaktionen

NICHT verfügbar: 

* Anzahl und Verhältnis von Followern und Freunden

---

Semantische Merkmale:

* Wortwahl und Sprachstil
* Sentiment
* Links und Hashtags

---

Verhaltensbasierte Merkmale:

* Posting-Frequenz
* Aktivitätszeiten und Aktivitätsmuster

NICHT verfügbar: 

* Tippgeschwindigkeit
* Scrollverhalten

---

Koordinative Merkmale:

* zeitliche Synchronität
* ähnliche Verhaltensweisen und Kommentare
* koordinierte Verbreitung von Inhalten

Die Ergebnisse werden hinsichtlich Aussagekraft und Umsetzbarkeit, sowie Verfügbarkeit und Aufwand bewertet. (doppelt?)

---

## Evaluationskriterien

Ein Merkmal gilt als relevant, wenn:

* es zuverlässig extrahierbar ist
* es im Plattformkontext verfügbar ist
* es nachvollziehbare Hinweise auf automatisierte Interaktionen liefert
* es sinnvoll in die heuristische Bewertung integriert werden kann

---

## Ressourcen

* [Forschungsstand](/docs/Research-Notes/Forschungsstand.md)
* Plattformdaten aus [01-PoC:](/docs/PoC/01-poc-datenerfassung.md) Datenerfassung
* Testdatensätze
* API Dokumentation

---

## Durchführung

1. Ableitung relevanter Merkmale aus dem Forschungsstand
2. Prüfung der Verfügbarkeit auf Reddit
3. Bewertung der technischen Extrahierbarkeit
4. Bewertung der Eignung für den MVP
5. Dokumentation der Ergebnisse

---

## Ergebnisse

Wird im Verlauf ergänzt.

---

## Entscheidung / Konsequenzen

Wird nach Abschluss des PoC dokumentiert.

Die Ergebnisse bilden die Grundlage für:

* [03-ADR:](/docs/ADR/03-adr-merkmalsmodell.md) Merkmalsmodell
* [04-ADR:](/docs/ADR/04-adr-risc-score.md) Risk Score
