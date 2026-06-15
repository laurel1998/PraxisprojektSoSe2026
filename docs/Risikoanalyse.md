# Risikoanalyse

## Beschreibung des Problemraums

Das Projekt adressiert die Herausforderung, automatisierte Interaktionen für Endnutzer sichtbar und nachvollziehbar zu machen. Hierzu soll ein prototypisches Analyse- und Visualisierungssystem entwickelt werden, das verschiedene Merkmalsgruppen kombiniert, um verdächtige Muster zu erkennen und verständlich darzustellen.

---

## 1. Datenzugang und Plattformbeschränkungen

### Welche Plattform eignet sich für die Analyse?

Mögliche Plattformen:

* Reddit
* YouTube
* Mastodon
* Threads

Die Wahl hängt maßgeblich von der Verfügbarkeit relevanter Daten und Schnittstellen ab.

### Welche Daten stehen tatsächlich zur Verfügung?

Nicht alle Plattformen stellen die für eine Analyse benötigten Informationen bereit.

Möglicherweise fehlen:

* Accountinformationen
* Netzwerkbeziehungen
* Interaktionshistorien
* Aktivitätsdaten

### Risiko

Bestimmte Analyseansätze können aufgrund fehlender Daten nicht umgesetzt werden.

### Risikominderung

* Frühe Evaluation geeigneter Plattformen
* Fokus auf öffentlich verfügbare Daten
* Anpassung des Analyseumfangs an die verfügbaren Daten

---

## 2. Erkennung automatisierter Interaktionen

### Welche Merkmale liefern tatsächlich belastbare Hinweise?

Die Literatur beschreibt zahlreiche Merkmale:

* technische Merkmale
* semantische Merkmale
* verhaltensbasierte Merkmale
* koordinative Merkmale

Nicht alle Merkmale sind jedoch gleichermaßen aussagekräftig.

### Risiko

Einzelne Merkmale erzeugen Fehlbewertungen oder liefern keine ausreichende Trennschärfe.

### Risikominderung

* Orientierung am Forschungsstand
* Kombination mehrerer Analyseperspektiven
* Heuristischer Ansatz statt automatischer Klassifikation (d.h. Sammlung verschiedener Indikatoren als Grundlage für Bewertung)

---

## 3. Risk Score und Nachvollziehbarkeit

### Wie kann Unsicherheit verständlich dargestellt werden?

Automatisierte Interaktionen lassen sich nicht eindeutig nachweisen.

Die Visualisierung muss daher Wahrscheinlichkeiten und Unsicherheiten kommunizieren.

### Risiko

Nutzer interpretieren Ergebnisse als sichere Aussagen.

### Risikominderung

* Verwendung eines Risk Scores statt einer binären Entscheidung
* Transparente Darstellung der zugrunde liegenden Merkmale
* Kennzeichnung von Unsicherheiten

---

## 4. Visualisierung im Nutzungskontext

### Wie können Analyseergebnisse verständlich dargestellt werden?

Die Visualisierung soll direkt im Nutzungskontext erfolgen, beispielsweise innerhalb einer Kommentaransicht.

### Risiko

Zu viele Informationen überfordern Nutzer.

### Risikominderung

* Reduzierte Visualisierung (z. B. Ampelsystem)
* Fokus auf wesentliche Kennzahlen
* Iterative Verbesserung der Darstellung

---

## 5. Technische Umsetzung

### Welche Systemarchitektur eignet sich?

Mögliche Umsetzungsformen:

* Browser-Extension
* Webanwendung

Die Entscheidung hängt von den technischen Anforderungen und verfügbaren Daten ab.

### Risiko

Die gewählte Architektur erschwert den Zugriff auf benötigte Informationen.

### Risikominderung

* Proof of Concept vor der eigentlichen Implementierung
* Architekturentscheidung erst nach Evaluation der Anforderungen