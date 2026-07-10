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

Für den Prototyp wird ein hybrider Datenzugriff gewählt, der API und DOM-Scraping kombiniert.

Die Reddit API dient als primäre Datenquelle für strukturierte Informationen wie Kommentare, Zeitstempel und Accountdaten. DOM-Scraping wird ergänzend eingesetzt, sofern dies für die Erfassung öffentlich sichtbarer Inhalte erforderlich ist. Die Kombination beider Ansätze ermöglicht einen flexiblen Datenzugriff und reduziert die Abhängigkeit von einer einzelnen Schnittstelle. Dadurch kann der Datenzugriff an die jeweiligen Anforderungen der Anwendung angepasst werden und schafft zugleich die technische Grundlage für eine Darstellung der Analyseergebnisse direkt im Nutzungskontext.

---

## Folgen und To-dos

**Folgen**

- Die Datenerfassung wird aufgeteilt und muss sowohl API- als auch DOM-Daten berücksichtigen
- Änderungen einer einzelnen Datenquelle können leichter kompensiert werden durch flexible Kombination der Zugriffsstrategie 

**To-dos**

- Umsetzung der Merkmalsanalyse [(02-PoC)](/docs/PoC/02-poc-merkmalsanalyse.md)
- Ableitung des Merkmalsmodells [(03-ADR)](/docs/ADR/03-adr-merkmalsmodell.md)

---

## Probleme

API und DOM stellen Informationen in unterschiedlicher Struktur und unterschiedlichem Umfang bereit. Diese Unterschiede müssen bei der Merkmalsanalyse berücksichtigt werden. Im Rahmen der Merkmalsanalyse wird daher festgelegt, welche Datenquellen für die einzelnen Merkmale genutzt werden und wie diese konsistent verarbeitet werden können.