# Analyse und Prognose des Individualverkehrs in Zürich

**Team 5:** Nicolas Wyss, Reto Furrer, Felix Schilling, Josa Preisig, Raphael Hug

## Projektübersicht

Ziel des Projekts war die Analyse und Prognose des Individualverkehrs in der Stadt Zürich. Eine fundierte Verkehrsplanung ist zentral für Mobilität, Lebensqualität und Nachhaltigkeit in urbanen Räumen. Mithilfe von Daten aus verschiedenen Quellen haben wir Einflussfaktoren identifiziert und ein Prognosemodell entwickelt, das Verkehrsaufkommen vorhersagen kann.

## Fragestellungen & Hypothesen

Wir wollten herausfinden, wie verschiedene externe Faktoren den Verkehr beeinflussen. Dazu haben wir folgende Hypothesen aufgestellt:

1. Wochentage: An Werktagen ist das Verkehrsaufkommen höher als an Wochenenden und Feiertagen.
2. Wetter: Bei schlechtem Wetter (z. B. Regen, Schnee) nimmt der Individualverkehr ab.
3. Ferien: Während Schulferien sinkt das Verkehrsaufkommen deutlich.
4. Temperatur: Höhere Temperaturen im Sommer führen zu mehr Verkehr (z. B. Freizeitaktivitäten).

## Datenquellen

### 1. Individualverkehr
- Quelle: Open Data Zürich – Verkehrszählstellen
- Zeitraum: 2018–2024, stündliche Fahrzeugzählungen
- Verarbeitung: Aggregation auf Tageswerte, Fokus auf Werktage

### 2. Wetterdaten
- Quelle: Open-Meteo API
- Features: Temperatur, Niederschlag, Wind etc.
- Verarbeitung: Tagesdurchschnittswerte, Extremwerte, Feature Engineering

### 3. Ferien- und Feiertagsdaten
- Quelle: Open Data Zürich & manuell gepflegte Kalenderdaten
- Features: Dummy-Variablen für Schulferien, Feiertage, Brückentage

## Methoden & Analyse

- Explorative Datenanalyse mit Cluster-Vergleichen nach Durchschnitt und Varianz
- Analyse der Auswirkungen von Feiertagen, Wetter und Temperatur auf den Verkehr
- Feature Engineering: z. B. Lag-Features, Dummy-Variablen, gleitende Mittelwerte
- Modellierung mit:
  - Linear Regression
  - Decision Tree
  - Random Forest
  - KNN

## Ergebnisse & Erkenntnisse

- Wochentage: Deutlich höheres Verkehrsaufkommen an Werktagen bestätigt
- Wetter: Kein klarer Einfluss durch leichten Niederschlag
- Schnee + Kälte: Deutlicher Rückgang bei starkem Schneefall und Temperaturen unter 0 Grad
- Ferien: Reduziertes Verkehrsaufkommen während Schulferien und Feiertagen
- Temperatur: Extremtemperaturen (unter 0 °C und über 30 °C) senken das Verkehrsaufkommen

## Prognosemodell

- Ziel: Vorhersage des Verkehrsaufkommens auf Basis von Wettervorhersagen und Ferientagen
- Ergebnis: Nur geringe Vorhersagekraft (R² knapp über 0)
- Erklärung: Exogene Faktoren wie Baustellen, ÖV-Störungen oder Events wirken sich stärker aus als ursprünglich angenommen

## Highlights

- Kombination mehrerer Datenquellen (Wetter, Verkehr, Kalender)
- Aussagekräftige Visualisierungen zur Mustererkennung
- Anwendung verschiedener Modelle und Feature Engineering Methoden
- Prognose unter Verwendung von Wetter-Forecast-Daten

## Nutzen für das Management

- Identifikation von Verkehrsmustern für bessere Planung
- Entscheidungsgrundlage für Baustellenplanung, ÖV-Anpassungen, Ferienverkehr
- Quantifizierung des Einflusses von Wetter, Feiertagen und Schulferien
- Datengetriebene Empfehlungen für eine vorausschauende Verkehrspolitik

## Ressourcen
- [Colab](https://colab.research.google.com/drive/10U9uM-OGZqwP-IzEv9xVvSO8sVotGobW)
