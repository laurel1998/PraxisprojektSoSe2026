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
* Welche Merkmale liefern brauchbare Hinweise?
* Welche Merkmale lassen sich sinnvoll kombinieren?

---

## Scope

Untersucht werden die im Forschungsstand abgeleiteten Merkmalsgruppen:

* technische Merkmale
* semantische Merkmale
* verhaltensbasierte Merkmale
* koordinative Merkmale

Im Fokus steht zunächst die Analyse einzelner Kommentarinteraktionen und ihrer unmittelbaren Kontexte.

---

## Methodik

Für jede Merkmalsgruppe werden exemplarische Features definiert und auf Testdaten angewendet.

Technische Merkmale: 

* Accountalter
* Profilinformationen
* Anzahl und Verhältnis von Followern und Freunden
* Anzahl von Interaktionen

Semantische Merkmale:

* Wortwahl und Sprachstil
* Sentiment
* Links und Hashtags

Verhaltensbasierte Merkmale:

* Posting-Frequenz
* Aktivitätszeiten und Aktivitätsmuster
* Tippgeschwindigkeit
* Scrollverhalten

**Koordinative Merkmale**

* zeitliche Synchronität
* ähnliche Verhaltensweisen und Kommentare
* koordinierte Verbreitung von Inhalten

Die Ergebnisse werden hinsichtlich Aussagekraft und Umsetzbarkeit bewertet.

---

## Evaluationskriterien

Ein Merkmal gilt als relevant, wenn:

* es zuverlässig extrahierbar ist
* es im Plattformkontext verfügbar ist
* es nachvollziehbare Hinweise auf automatisierte Interaktionen liefert
* es sinnvoll in die heuristische Bewertung integriert werden kann

---

## Ressourcen

* Forschungsstand
* Plattformdaten aus [01-PoC:](/docs/PoC/01-poc-datenerfassung.md) Datenerfassung
* Testdatensätze
* NLP-Bibliotheken
* Analyse-Skripte

---

## Durchführung

1. Auswahl geeigneter Testdaten
2. Definition exemplarischer Features
3. Implementierung erster Extraktionslogiken
4. Analyse und Vergleich der Ergebnisse
5. Bewertung der Umsetzbarkeit und Relevanz

---

## Ergebnisse

Wird im Verlauf ergänzt.

---

## Entscheidungen / Konsequenzen

Wird nach Abschluss des PoC dokumentiert.

Die Ergebnisse bilden die Grundlage für:

* [03-ADR:](/docs/ADR/03-adr-merkmalsmodell.md) Merkmalsmodell
* [04-ADR:](/docs/ADR/04-adr-risc-score.md) Risc Score
