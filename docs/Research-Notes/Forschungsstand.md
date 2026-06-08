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
    - Retweet-Netzwerke

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
    - Merkmale des sozialen Umfelds: Netzwerkcharakteristika, Network Features
    - Merkmale des zeitlichen Aktivitätsmuster: Posting-Frequenz, Aktivitätszeiten, Interaktionsrhythmen
    - Merkmale veröffentlichter Inhalte: Wortwahl, Sprachstil, Hashtags, Links

4. Hybride Ansätze = Kombination mehrerer Detection-Ansätze

    Vorteile:
    - Höhere Erkennungsgenauigkeit
    - Ausgleich der Schwächen einzelner Verfahren

    Nachteile:
    - Höhere Komplexität
    - Größerer Datenbedarf

---

## Relevanz für das Praxisprojekt

Die aktuelle Forschung deutet darauf hin, dass die Kombination mehrerer Analyseperspektiven deutlich robuster ist als die Betrachtung einzelner Merkmale (vgl. The Rise of Social Bots - [Ferrara u. a. 2016]). Darüber hinaus imitieren moderne Bots zunehmend menschliche Kommunikations- und Verhaltensmuster. Dadurch verlieren einzelne Merkmale an Aussagekraft und die Erkennung automatisierter Interaktionen wird zunehmend schwieriger. Erfolgreiche Detection-Strategien betrachten daher mehrere Analyseperspektiven gleichzeitig (vgl. A Decade of Social Bot Detection - [Cresci 2020]).

Für das geplante Analyse- und Visualisierungssystem erscheinen insbesondere folgende Merkmalsgruppen relevant:
    - technische Merkmale z. B. Profilinformationen, Accountalter, Anzahl und verhältnis von Followern und Freunden
    - semantische Merkmale z. B. Sprachstil, Wortwahl, Textähnlichkeiten oder wiederkehrende Inhalte, Hashtags und Links
    - verhaltensbasierte Merkmale z. B. Posting-Frequenz, Aktivitätszeiten und Aktivitätsmuster
    - koordinative Merkmale z. B. synchronisierte Aktivitäten, ähnliche Verhaltensweisen oder koordinierte Verbreitung von Inhalten

Die Merkmalsgruppen wurden aus den von Ferrara et al. beschriebenen Feature-Kategorien sowie den von Cresci hervorgehobenen koordinativen Analyseansätzen abgeleitet. Die Auswahl der Merkmalsgruppen orientiert sich an den Feature-, Netzwerk- und Hybridansätzen. Durch die Kombination mehrerer Analyseperspektiven soll eine robustere Einschätzung automatisierter Interaktionen ermöglicht werden als durch die isolierte Betrachtung einzelner Merkmale.