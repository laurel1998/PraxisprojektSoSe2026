# 03-ADR: Merkmalsmodell

**Status:** entschieden
**Datum:** 20-08-2026

---

## Kontext

Im Rahmen von [02-PoC](/docs/PoC/02-poc-merkmalsanalyse.md) wurden die im Forschungsstand identifizierten Merkmale hinsichtlich ihrer Verfügbarkeit und technischen Umsetzbarkeit auf YouTube untersucht. Für die prototypische Umsetzung muss nun festgelegt werden, welche dieser Merkmale Bestandteil des Merkmalsmodells werden und wie sie für die spätere heuristische Bewertung strukturiert werden.

Ziel ist die Definition eines Merkmalsmodells, das auf den verfügbaren Plattformdaten basiert und gleichzeitig die im Forschungsstand identifizierten Merkmalsgruppen möglichst vollständig abbildet.

---

## Optionen

- Verwendung einzelner Merkmale
- Verwendung kombinierter Merkmale
- Kombination von Merkmalen mit zusätzlichen Kontextinformationen

---

## Entscheidung

Für den MVP wird ein Merkmalsmodell verwendet, das auf den in PoC 02 identifizierten und für die prototypische Umsetzung geeigneten Merkmalen basiert.

Kommentarinteraktionen bilden den Ausgangspunkt der Analyse. Die Merkmale können dabei den Kommentar selbst, den kommentierenden Kanal oder die Beziehung zu anderen beobachtbaren Kommentaren beschreiben. Merkmale mit einer nachvollziehbaren Beziehung zueinander werden zu kombinierten Merkmalen zusammengeführt, dadurch sollen mehrere schwache Hinweise zu aussagekräftigeren Indikatoren automatisierter Aktivitäten verbunden werden. Andere Merkmale können als zusätzliche Kontextinformationen in die Bewertung einfließen.

Für den MVP werden zunächst folgende Kombinationen betrachtet:

---

**Identifikation eines Kanals**

- Kanal-ID
- Benutzernamen(muster)

---

**Kanalprofil**

Kombination aus:

- Kanalalter
- Kanalbeschreibung
- Landesangabe
- Anzahl von Interaktionen: Videos
- Abonnentenzahl
- Anzahl der Videoaufrufe

Ziel ist die Einordnung der Glaubwürdigkeit eines Kanals.

---

**Sprachprofil**

Kombination aus:

- Wortwahl und Sprachstil
- Sentiment

Ziel ist die Beschreibung charakteristischer sprachlicher Eigenschaften eines Kommentars.

---

**Kommentarprofil**

Kombination aus:

- Likes
- Antwortanzahl
- Links
- Hashtags

Ziel ist die Analyse von Auffälligkeiten im Interaktionsverhalten.

---

**Kommentaraktivität**

Kombination aus:

- Antwortgeschwindigkeit
- ähnlichen Kommentaren
- zeitlicher Synchronität

Ziel ist die Identifikation zeitlich und inhaltlich auffälliger Interaktionen zwischen Kommentaren.

---

Weitere Analysemerkmale können im Verlauf der prototypischen Umsetzung ergänzt werden.

Das vollständige Merkmalsmodell ist nach Gruppen sortiert im Artefakt [03-Merkmalsmodell](/docs/ADR/Artefakte/03-Merkmalsmodell-Tabelle.png) dokumentiert. Die grafische Visualisierung finden Sie [hier](/docs/Modelle/Risk-Score/Merkmalsmodell.jpg).

---

## Folgen und To-dos

### Folgen

- Nicht verfügbare Merkmale werden für den MVP ausgeschlossen
- Das Merkmalsmodell bildet die Grundlage für die spätere heuristische Bewertung

### To-dos

- Entwicklung des heuristischen Risk Scores (04-ADR)

---

## Probleme

Einzelne Merkmale besitzen häufig nur eine begrenzte Aussagekraft. Dieser Einschränkung wird begegnet, indem mehrere Einzelmerkmale zu Analysemerkmalen kombiniert werden. Die konkrete Bewertung, sowie Gewichtung der Merkmale erfolgt im nachfolgenden [ADR zum heuristischen Risk Score](/docs/ADR/04-adr-risc-score.md).