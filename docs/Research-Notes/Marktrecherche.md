# Marktrecherche

Diese Marktrecherche untersucht bestehende Systeme zur Erkennung automatisierter Interaktionen. Ziel ist es, bestehende Ansätze, Technologien und Visualisierungskonzepte zu analysieren und mögliche Inspirationsquellen sowie Abgrenzungen für das geplante Analyse- und Visualisierungssystem abzuleiten.

---

## 1. Botometer X (OSoMe - Indiana University)

https://botometer.osome.iu.edu/

**Ansatz:**

* Historisch trainierte Klassifikationsmodelle
* Archivbasierte Scores
* Bot Repository als Trainingsgrundlage

**Beschreibung:**
Botometer ist eines der bekanntesten wissenschaftlichen Systeme zur Erkennung von Social Bots. Ursprünglich kombinierte das System zahlreiche Analyseperspektiven wie Netzwerkstruktur, Inhalte, Sentiment und Aktivitätsmuster, um differenzierte Risk Scores zu erzeugen. Aufgrund geänderter API-Richtlinien von X (ehemals Twitter) wurde das System 2024 als **Botometer X** neu veröffentlicht.

Im Gegensatz zur ursprünglichen Version arbeitet Botometer X nicht mehr in Echtzeit, sondern greift auf historische Daten bis Mai 2023 zurück. Die aktuelle Version liefert nur noch einen Gesamtscore auf Basis von User Metadata. Botometer betont selbst, dass Bot Detection eine schwierige Aufgabe ist und die Ergebnisse das menschliche Urteil ergänzen, aber nicht ersetzen sollen.

**Relevanz:**

* Ähnliche Grundidee: Risk Score statt binäre Klassifikation
* Bestätigung, dass Unsicherheit transparent kommuniziert werden sollte
* Verdeutlicht die Bedeutung zusätzlicher Verhaltens- und Kontextanalysen


---

## 2. DeBot (University of New Mexico)

https://www.cs.unm.edu/~chavoshi/debot/

**Ansatz:**

* Koordinationsanalyse
* Echtzeit-Erkennung

**Beschreibung:**
DeBot ist ein Echtzeit-Bot-Detection-System zur Erkennung automatisierter Accounts auf Twitter. Im Gegensatz zu klassischen accountbasierten Detection-Systemen betrachtet DeBot nicht einzelne Accounts isoliert, sondern analysiert die zeitliche Korrelation zwischen mehreren Accounts. Die Grundannahme ist, dass menschliche Nutzer über längere Zeiträume keine hoch synchronisierten Aktivitäten aufweisen. Stark korrelierte Aktivitätsmuster gelten daher als Hinweis auf automatisiertes Verhalten. DeBot arbeitet vollständig unüberwacht und benötigt keine gelabelten Trainingsdaten.

**Relevanz:**

* Grundlage für koordinative Analysemerkmale
* Bestätigung, dass Synchronität ein relevanter Indikator für Bot-Verhalten ist
* Inspiration für gruppenbasierte Analyse von Kommentarinteraktionen

---

## 3. CopyCatch (Facebook)

**Ansatz:**

* Graphbasierte Detection
* Koordinationsanalyse
* Lockstep Behavior Detection

**Beschreibung:**
CopyCatch ist ein von Facebook entwickeltes System zur Erkennung koordinierter Gruppenangriffe innerhalb sozialer Netzwerke. Im Fokus stehen nicht einzelne Accounts, sondern Gruppen von Nutzern, die innerhalb kurzer Zeit ähnliche Aktionen durchführen. Das System analysiert ausschließlich die Struktur des sozialen Graphen und die Zeitpunkte der Interaktionen.
Die Grundannahme lautet: Wenn viele Accounts in kurzer Zeit die gleichen Ziele mit ähnlichem Verhalten verfolgen, ist dies ein starkes Indiz für koordinierte oder automatisierte Aktivität.

CopyCatch wird produktiv auf Facebook eingesetzt und analysiert dort Milliarden von Interaktionen.

**Relevanz:**

* Methodische Grundlage für koordinative Merkmale
* Zeigt, dass bereits einfache Graph- und Zeitinformationen wichtige Signale liefern können
* Inspiration für spätere Netzwerkvisualisierungen

---

## 4. SynchroTrap (Facebook / Instagram)

**Ansatz:**

* Clustering-basierte Koordinationsanalyse
* Zeitliche Partitionierung von Aktivitätsdaten

**Beschreibung:**
SynchroTrap ist ein von Facebook entwickeltes Detection-System zur Identifikation großer Gruppen bösartiger Accounts in sozialen Netzwerken. Das System basiert auf der Beobachtung, dass schädliche Accounts häufig ähnliche Aktionen in zeitlicher Nähe ausführen. 

Im Gegensatz zu CopyCatch sucht SynchroTrap nicht nach strikt synchronisiertem Verhalten, sondern nach locker synchronisierten Aktivitätsmustern („loose synchrony“). Dadurch lassen sich auch komplexere und weniger offensichtliche koordinierte Kampagnen erkennen. Das System wurde produktiv bei Facebook und Instagram eingesetzt.

**Relevanz:**

* Grundlage für koordinative Analysemerkmale
* Bestätigung, dass zeitlich ähnliche Aktivitäten ein zentraler Indikator für koordinierte Automatisierung sind
* Unterstützt die Idee, Gruppenverhalten statt Einzelaccounts zu analysieren

---

## 5. Renren Sybil Detector

**Ansatz:**

* Feature-basierte Detection
* Echtzeit-Detection
* Heuristische Klassifikation

**Beschreibung:**
Ein hybrides System zur Erkennung von Sybil-Accounts durch Kombination verschiedener Analyseperspektiven. Der Renren Sybil Detector ist kein eigenständiges öffentlich verfügbares Produkt, sondern ein im Rahmen einer wissenschaftlichen Studie entwickeltes und innerhalb der Social-Media-Plattform Renren eingesetztes Detection-System. Es basiert auf verhaltens- und netzwerkbezogenen Merkmalen, um gefälschte Accounts (Sybil Accounts) in Echtzeit zu identifizieren. Eine zentrale Erkenntnis der Studie ist, dass sich Sybil Accounts häufig erfolgreich in normale soziale Netzwerke integrieren und nicht zwingend in auffälligen Gruppen auftreten.

**Relevanz:**

* Bestätigung des Hybridansatzes
* Kombination technischer und verhaltensbasierter Merkmale
* Zeigt, dass einfache heuristische Merkmale bereits wirksam sein können

---

## 6. FollowerAnalyzer (ViralLab)

https://github.com/ViralLab/FollowerAnalyzer

**Ansatz:**

* Wissenschaftliches Analysewerkzeug
* Anomalieerkennung
* Follower-Map-Visualisierung

**Beschreibung:**
FollowerAnalyzer ist ein wissenschaftliches Tool zur Analyse verdächtiger Follower-Kampagnen. Das System untersucht zeitliche Auffälligkeiten im Follower-Wachstum. Durch die Schätzung von Follow-Zeitpunkten und die Erkennung ungewöhnlicher Aktivitätsmuster können verdächtige Gruppen von Fake-Followern identifiziert werden. Zusätzlich bietet das Tool Visualisierungen in Form von Follower Maps.

**Relevanz für das Projekt:**

* Grundlage für zeitliche Verhaltensanalyse
* Inspiration für Visualisierung von Aktivitätsmustern

---

## 7. HUMAN Sightline Cyberfraud Defense

https://www.humansecurity.com/

**Ansatz:**

* Enterprise Bot Detection
* Fraud Prevention
* Fingerprinting

**Beschreibung:**
HUMAN bietet eine kommerzielle Enterprise-Lösung zur Erkennung und Abwehr automatisierter Angriffe auf Webseiten, mobile Anwendungen und APIs. Im Gegensatz zu wissenschaftlichen Detection-Systemen liegt der Fokus nicht auf Analyse oder Transparenz für Endnutzer, sondern auf Unternehmensschutz, Fraud Prevention und Infrastruktur-Sicherheit.

**Relevanz:**

* Marktstandard im Enterprise-Bereich
* Fokus auf Plattformschutz statt Endnutzertransparenz


---

## 8. Fingerprint

https://fingerprint.com/

**Ansatz:**

* Device Intelligence
* Browser- und Geräte-Fingerprinting
* VPN Detection

**Beschreibung:**
Fingerprint ist eine kommerzielle Device-Intelligence-Plattform zur Identifikation von Web- und Mobile-Nutzern anhand technischer Geräte- und Browsermerkmale. Das System erzeugt persistente Gerätekennungen und nutzt zusätzliche Signale zur Erkennung von Bots, manipulierten Browsern oder verdächtigen Aktivitäten. Im Gegensatz zu klassischen Social-Bot-Detection-Systemen liegt der Fokus weniger auf Inhalten oder sozialen Interaktionen, sondern auf technischen Identitätsmerkmalen.

**Relevanz:**

* Bestätigung für Browser- und Geräte-Fingerprinting als Detection-Signal
* Fokus auf technische Identität statt inhaltliche und koordinative Analyse

---

## 9. CHEQ

https://cheq.ai/

**Ansatz:**

* Traffic Analysis
* Behavioral Analysis
* Real-Time Detection

**Beschreibung:**
CHEQ ist eine kommerzielle Sicherheitsplattform zur Erkennung und Abwehr automatisierter und betrügerischer Interaktionen im Web. Im Gegensatz zu klassischen Bot-Management-Systemen liegt der Fokus besonders auf dem Schutz digitaler Marketingkanäle, Werbebudgets und Analyse-Daten. Das System analysiert Traffic in Echtzeit, filtert ungültige oder automatisierte Interaktionen und verbessert dadurch Datenqualität und Kampagneneffizienz. 

**Relevanz:**

* Referenz für Risk-Score-orientierte Analyse
* Fokus auf Unternehmens- und Marketingschutz statt Endnutzerunterstützung

---

## 10. Piloterr

https://piloterr.com/

**Ansatz:**

* Web Data Extraction
* API-basierte Social-Media-Analyse
* Automatisierte Datenerfassung

**Beschreibung:**
Piloterr bietet APIs zur strukturierten Extraktion von Social-Media-Daten und Webinhalten. Das Tool selbst dient nicht primär der Bot Detection, ist aber relevant als potenzielle Datenquelle für Kommentar-, Profil- und Interaktionsdaten.

**Relevanz:**

* Potenzielle Infrastruktur für Datenerhebung

---

## 11. Copyleaks AI Detector

https://copyleaks.com/

**Ansatz:**

* Inhaltsbasierte Analyse
* AI-Generated Text Detection

**Beschreibung:**
Copyleaks ist ein kommerzielles Tool zur Erkennung KI-generierter Texte. Es analysiert sprachliche Muster, Stilmerkmale und Wahrscheinlichkeiten für maschinell erzeugte Inhalte.

**Relevanz:**

* Interessant für semantische Merkmale
* Inspiration für textbasierte Analyse
* Relevant für Erkennung KI-generierter Kommentare

---

## 12. Bot Sentinel (Firefox)

https://botsentinel.com/

**Ansatz:**

* Toxicity Detection
* Browser Extension

**Beschreibung:**
Bot Sentinel ist ein browserbasiertes Analysewerkzeug zur Erkennung toxischer, manipulativer oder koordinierter Social-Media-Accounts. Das Tool analysiert vor allem Twitter/X-Accounts und visualisiert Bewertungen direkt für Endnutzer. Das System bewertet dabei primär Accounts und deren langfristiges Verhalten, um problematische oder potenziell schädliche Akteure sichtbar zu machen. Im Fokus stehen dabei weniger automatisierte Interaktionen selbst als vielmehr toxisches Verhalten, Belästigung und koordinierte Angriffe.

**Relevanz:**

* Referenz für Endnutzertransparenz
* Direkte Sichtbarkeit im Nutzungskontext
* Inspiration für Risiko-Visualisierung

---

# Erkenntnisse für das Praxisprojekt

Die Marktrecherche zeigt, dass bestehende Systeme zur Erkennung automatisierter Interaktionen unterschiedliche Schwerpunkte setzen. Es wird deutlich, dass erfolgreiche Detection-Ansätze selten auf einzelnen Merkmalen basieren, sondern verschiedene Analyseperspektiven kombinieren. Vor allem koordinative und zeitliche Muster spielen dabei eine zentrale Rolle. Viele der kommerziellen Systeme fokussieren primär den Schutz von Plattformen, Infrastrukturen und Unternehmen vor Fraud, Scraping oder automatisierten Angriffen. Die Analyse dient hier meist der automatischen Abwehr und nicht der transparenten Darstellung für Endnutzer. Auffällig ist zudem, dass die untersuchten Systeme Analyseergebnisse überwiegend in separaten Dashboards, APIs oder internen Plattformwerkzeugen bereitstellen.

Für das geplante Analyse- und Visualisierungssystem lassen sich folgende zentrale Erkenntnisse ableiten:
 - Koordinative Muster und zeitliche Synchronität sind wichtige Indikatoren für automatisierte Aktivitäten
 - Technische Merkmale wie Fingerprinting oder Account-Metadaten können zusätzliche Hinweise liefern
 - Risk-Score-basierte Systeme eignen sich besser zur Darstellung von Unsicherheit als binäre Klassifikationen
 - Verbindung von Analyse, heuristischer Bewertung und kontextueller Visualisierung automatisierter Interaktionen, sowie Fokus auf die  Analyse einzelner Kommentarinteraktionen und deren Kontext (USP)