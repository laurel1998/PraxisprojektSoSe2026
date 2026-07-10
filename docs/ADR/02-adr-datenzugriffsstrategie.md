# 02-ADR: Datenzugriffsstrategie

**Status:** entschieden  
**Datum:** 10-07-2026

---

## Kontext

Für die Umsetzung des MVP muss festgelegt werden, wie Kommentar-, Account- und Interaktionsdaten der ausgewählten Plattform erfasst werden.

Im Rahmen von PoC 01 wurde untersucht, welche Zugriffsmöglichkeiten Reddit für öffentliche Daten bereitstellt. Dabei zeigte sich, dass strukturierte Daten wie Kommentare, Zeitstempel und Accountinformationen über die Reddit API verfügbar sind. Gleichzeitig können öffentlich sichtbare Inhalte der Kommentaransicht direkt über das DOM der Webseite ausgelesen werden.

---

## Optionen

- Ausschließliche Nutzung der offiziellen API
- Ausschließliches DOM-Scraping
- Kombination aus API und DOM-Scraping

---

## Entscheidung

Für den Prototyp wird die Reddit API als primäre Datenquelle verwendet.

Die API stellt die für die Merkmalsanalyse benötigten Informationen wie Kommentare, Zeitstempel und Accountdaten strukturiert bereit und ermöglicht einen konsistenten Zugriff auf öffentliche Informationen. Ein ergänzender Zugriff über DOM-Scraping wird für die Datenerfassung im MVP nicht benötigt.

---

## Folgen und To-dos

**Folgen**

- Die Datenerfassung basiert vollständig auf der Reddit API

**To-dos**

- Analyse der Merkmale [(02-PoC)](/docs/PoC/02-poc-merkmalsanalyse.md)
- Ableitung des Merkmalsmodells [(03-ADR)](/docs/ADR/03-adr-merkmalsmodell.md)

---

## Probleme

Die Merkmalsanalyse ist auf die über die Reddit API verfügbaren Daten beschränkt. Einzelne Merkmale, beispielsweise Followerinformationen oder clientseitige Interaktionsdaten, können daher im MVP nicht berücksichtigt werden.