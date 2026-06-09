## Was sind Web Bots? 

Web Bots sind automatisierte Programme, die wiederholt Aktionen auf Webseiten ausführen. Sie können legitime Aufgaben wie Web Crawling übernehmen, werden aber auch für Web Scraping, automatisierte Formularübermittlung, Massenerstellung von Accounts oder Spam eingesetzt (vgl. New biostatistics features for detecting web bot activity on web applications - [Rahman u. Tomar 2020]).

---

## Was sind Social Bots?

Social Bots sind automatisierte Accounts auf sozialen Plattformen, die Inhalte erzeugen, verbreiten und mit anderen Nutzern interagieren. Ihr Ziel ist häufig, menschliches Verhalten möglichst glaubwürdig nachzuahmen. Dabei beschränkt sich die Nachahmung nicht nur auf die Erstellung von Inhalten, sondern umfasst auch soziale Interaktionen, zeitliche Aktivitätsmuster und Kommunikationsverhalten (vgl. The Rise of Social Bots - [Ferrara u. a. 2016]).

Allerdings gibt es keine einheitliche Definition, da Social Bots unterschiedlich stark automatisiert sein können und teilweise menschliche Unterstützung erhalten s.g. Cyborg Accounts (vgl. A Decade of Social Bot Detection - [Cresci 2020]).

---

## Warum sind Social Bots relevant?

Social Bots werden sowohl für legitime als auch für schädliche Zwecke eingesetzt.

### Legitime Anwendungen:
 - Newsfeeds
 - automatische Benachrichtigungen
 - Kundenservice
 - Informationsaggregation

### Problematisch wird der Einsatz bei:
 - Desinformation
 - Manipulation politischer Diskussionen
 - künstlicher Verstärkung von Meinungen
 - Spam und generell Betrug

Es gibt zahlreiche Beispiele, bei denen Social Bots politische Diskussionen beeinflusst, die Wahrnehmung von Popularität verzerrt oder die Verbreitung von Fehlinformationen verstärkt haben z.B. Boston Marathon bombing (vgl. The Rise of Social Bots - [Ferrara u. a. 2016]).

---

## Welche Merkmale unterscheiden menschliche und automatisierte Interaktionen?

Es existiert bereits Forschung, die untersucht, welche Merkmale besonders geeignet sind, um automatisierte Accounts von menschlichen Nutzern zu unterscheiden. Die Ergebnisse deuten darauf hin, dass insbesondere die Kombination verschiedener Merkmalsgruppen robuste Hinweise auf automatisierte Interaktionen liefern kann. Einzelne Merkmale besitzen dagegen meist nur begrenzte Aussagekraft (vgl. Exploring Social Bots - [Lopez-Joya u. a. 2024]).

---

## Warum wird Bot Detection schwieriger?

Frühe Social Bots konnten oft anhand einfacher Merkmale erkannt werden, beispielsweise durch hohe Aktivitätsraten oder offensichtlich automatisierte Inhalte.

Moderne Bots entwickeln sich jedoch kontinuierlich weiter und passen sich bestehenden Detection-Methoden an. Dadurch entsteht ein fortlaufender Wettlauf zwischen Bot-Entwicklern und Detection-Systemen.

Aktuelle Bots imitieren zunehmend:
 - menschliche Sprache
 - Aktivitätsrhythmen
 - soziale Interaktionen
 - Netzwerkverhalten
 - Meinungsäußerungen

Einzelne Bots können durch moderne KI-Technologien zunehmend nicht mehr zuverlässig von echten Nutzern unterschieden werden. Künftige Forschung sollte daher stärker koordinierte und unauthentische Gruppenaktivitäten untersuchen, statt ausschließlich einzelne Accounts zu klassifizieren (vgl. A Decade of Social Bot Detection - [Cresci 2020]).

---

## Welche Detection-Ansätze existieren?

Grundlegende Ansätze zur Bot Detection (vgl. The Rise of Social Bots - [Ferrara u. a. 2016]):

1. Netzwerkbasierte Verfahren = Analyse der Beziehungen zwischen Accounts

    Beispiele:
    - Follower-Beziehungen
    - Community-Strukturen

    Vorteile:
    - geeignet zur Erkennung koordinierter Aktivitäten

    Nachteile:
    - benötigt umfangreiche Daten

2. Crowd-Sourcing = Menschliche Bewertungen zur Identifikation von Bots

    Beispiele:
    - Meldungen durch Nutzer
    - Manuelle Überprüfung von Accounts
    - Expertenbewertungen

    Vorteile:
    - Menschen können komplexe Zusammenhänge interpretieren
    - Neue Bot-Typen können erkannt werden
    
    Nachteile:
    - Hoher personeller Aufwand
    - Begrenzte Skalierbarkeit

3. Feature-basierte Verfahren = Analyse von Merkmalen einzelner Accounts

    Beispiele:
    - Merkmale des Benutzerkontos: Profilinformationen, Accountalter, Anzahl von Followern
    - Merkmale des zeitlichen Aktivitätsmuster: Posting-Frequenz, Aktivitätszeiten und Aktivitätsmuster
    - Merkmale veröffentlichter Inhalte: Wortwahl, Sprachstil, Sentiment, Hashtags, Links

4. Hybride Ansätze = Kombination mehrerer Detection-Ansätze

    Vorteile:
    - Höhere Erkennungsgenauigkeit
    - Ausgleich der Schwächen einzelner Verfahren

    Nachteile:
    - Höhere Komplexität
    - Größerer Datenbedarf

---

## Relevanz für das Praxisprojekt

Die aktuelle Forschung deutet darauf hin, dass die Kombination mehrerer Analyseperspektiven robuster ist als die Betrachtung einzelner Merkmale (vgl. The Rise of Social Bots - [Ferrara u. a. 2016]). Gleichzeitig imitieren moderne Bots zunehmend menschliche Kommunikations- und Verhaltensmuster. Dadurch verlieren einzelne Merkmale an Aussagekraft und die Erkennung automatisierter Interaktionen wird zunehmend schwieriger. Erfolgreiche Detection-Strategien sollten daher mehrere Analyseperspektiven betrachten gleichzeitig mit einem Fokus auf koordinierte und unauthentische Gruppenaktivitäten (vgl. A Decade of Social Bot Detection - [Cresci 2020]). Neuere Arbeiten zeigen zudem, dass insbesondere Merkmale wie soziale Interaktionsmerkmale (z. B. Follower-Friend-Verhältnis) wichtige Hinweise auf automatisierte Accounts liefern können (vgl. Exploring Social Bots - [Lopez-Joya u. a. 2024]). Dieser Ansatz wird ergänzt um sogenannte Biostatistik-Merkmale, die charakteristische menschliche Interaktionsmuster wie Tippgeschwindigkeit oder Maus- und Scrollverhalten erfassen (vgl. New biostatistics features for detecting web bot activity on web applications - [Rahman u. Tomar 2020]). Durch die Kombination mehrerer Analyseperspektiven soll eine robustere Einschätzung automatisierter Interaktionen ermöglicht werden als durch die isolierte Betrachtung einzelner Merkmale.

Für das geplante Analyse- und Visualisierungssystem erscheinen insbesondere folgende Merkmalsgruppen relevant:
 - technische Merkmale z. B. Profilinformationen, Accountalter, Anzahl und Verhältnis von Followern und Freunden
 - semantische Merkmale z. B. Sprachstil, Wortwahl, Sentiment, Hashtags und Links
 - verhaltensbasierte Merkmale z. B. Posting-Frequenz, Tippgeschwindigkeit, Scrollverhalten, Aktivitätszeiten und Aktivitätsmuster
 - koordinative Merkmale z. B. synchronisierte Aktivitäten, ähnliche Verhaltensweisen oder koordinierte Verbreitung von Inhalten