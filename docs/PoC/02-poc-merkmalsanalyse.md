# 02-PoC: Merkmalsextraktion und Analyse

**Status:** Done

---

## Problem / Fragestellung

Die Literatur beschreibt zahlreiche Merkmale zur Erkennung automatisierter Interaktionen. Allerdings ist unklar, welche dieser Merkmale im gewählten Plattformkontext tatsächlich verfügbar, technisch extrahierbar und für eine heuristische Bewertung sinnvoll nutzbar sind.

Es soll geprüft werden, welche Merkmale praktisch umsetzbar sind und welche Hinweise sie auf automatisierte Interaktionen liefern können.

---

## POC-Ziel

Validierung der definierten Merkmalsgruppen und Prüfung ihrer praktischen Umsetzbarkeit.

Zentrale Fragen:

* Welche Merkmale sind technisch messbar?
* Welche Merkmale eignen sich für die heuristische Bewertung?
* Welche Merkmale stehen auf YouTube tatsächlich zur Verfügung?

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

- ob das Merkmal auf YouTube verfügbar ist
- ob es technisch extrahiert werden kann
- welchen potenziellen Beitrag es zur heuristischen Bewertung leistet
- welcher Implementierungsaufwand für den MVP zu erwarten ist

Die Ergebnisse werden vergleichend dokumentiert.

---

Technische Merkmale: 

- Kanal-ID
- Kanalalter
- Kanalbeschreibung
- Profilbild
- Landesangabe
- Anzahl von Interaktionen: Kommentare
- Anzahl von Interaktionen: Videos
- Abonnentenzahl
- Verhältnis Followern und Freunden
- Anzahl der Videoaufrufe
- Kommentar-Likes
- Antwortanzahl (Threadtiefe/Intensität)

---

Semantische Merkmale:

- Benutzernamen(muster)
- Wortwahl und Sprachstil (Inhalt)
- Sentiment
- Hashtags
- Links

---

Verhaltensbasierte Merkmale:

- Posting-Frequenz
- Aktivitätszeiten und Aktivitätsmuster
- Antwortgeschwindigkeit
- Tippgeschwindigkeit
- Scrollverhalten

---

Koordinative Merkmale:

- zeitliche Synchronität
- ähnliche Verhaltensweisen und Kommentare
- koordinierte Verbreitung von Inhalten

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
2. Prüfung der ausgewählten Merkmale auf YouTube
3. Bewertung der Eignung für den MVP
4. Dokumentation der Ergebnisse

---

## Ergebnisse

Die Ergebnisse der Merkmalsanalyse sind in einer [Vergleichsmatrix](/docs/PoC/Artefakte/02-MerkmalsAnalyse.png) dokumentiert.

Technische und semantische Merkmale können überwiegend mit geringem bis mittlerem Aufwand über die YouTube API extrahiert werden. Insbesondere Kanalinformationen, Kommentarinhalte sowie Zeitstempel stehen strukturiert zur Verfügung und bilden eine geeignete Grundlage für die heuristische Bewertung.

Verhaltensbasierte Merkmale wie Posting-Frequenzen oder Aktivitätsmuster sind grundsätzlich analysierbar, können aufgrund der fehlenden Interaktionshistorie einzelner Nutzer jedoch nur eingeschränkt betrachtet werden. Clientseitige Merkmale wie Tippgeschwindigkeit oder Scrollverhalten stehen nicht zur Verfügung.

Koordinative Merkmale erfordern eine aufwendigere Analyse mehrerer Kommentare, Accounts und zeitlicher Zusammenhänge. Die Identifikation koordinierter Aktivitäten kann daher nur indirekt über Muster wie zeitliche Synchronität oder inhaltliche Ähnlichkeiten erfolgen.

---

## Entscheidung / Konsequenzen

Für die prototypische Umsetzung des MVP werden ausschließlich Merkmale berücksichtigt, die auf YouTube verfügbar sind und mit vertretbarem technischem Aufwand extrahiert werden können.

Die Merkmalsanalyse zeigt, dass technische und semantische Merkmale hierfür eine geeignete Grundlage bilden. Verhaltensbasierte Merkmale werden berücksichtigt, sofern sie auf Basis der verfügbaren Zeitstempel und Interaktionsdaten bestimmt werden können. Koordinative Merkmale werden aufgrund ihrer hohen Aussagekraft ebenfalls in den MVP aufgenommen, ihre Analyse beschränkt sich jedoch auf Verfahren, die mit den verfügbaren Plattformdaten realisierbar sind.

Nicht verfügbare Merkmale sowie Merkmale, die eine vollständige Interaktionshistorie oder clientseitige Informationen erfordern, werden für den MVP ausgeschlossen.

Die Ergebnisse bilden die Grundlage für:

* [03-ADR:](/docs/ADR/03-adr-merkmalsmodell.md) Merkmalsmodell
* [04-ADR:](/docs/ADR/04-adr-risc-score.md) Risk Score
