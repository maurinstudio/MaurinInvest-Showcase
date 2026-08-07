
<img align="right" width="150" src="https://github.com/user-attachments/assets/34f25e7a-fe2e-4828-8052-6422d8408e14">

# MaurinInvest-Showcase


MaurinInvest ist eine mit Python und Streamlit entwickelte Finance-Tech-Anwendung zur Analyse von Aktien und Portfolios. Die Plattform kombiniert Fundamentaldaten, technische Kennzahlen, Branchenvergleiche und KI-gestützte Unternehmensanalysen, um Finanzinformationen verständlicher einzuordnen.

Dieses Repository dient als Showcase und Dokumentation des Projekts MaurinInvest. Der vollständige Quellcode befindet sich in einem privaten Repository, da das Projekt meine eigene Entwicklungsarbeit darstellt.

## Projektidee

Das Projekt entstand aus meinem eigenen Interesse an Investitionen und der Frage, wie Finanzkennzahlen besser eingeordnet und verständlicher dargestellt werden können.

MaurinInvest verbindet quantitative Datenanalyse mit qualitativen Unternehmensinformationen, um eine strukturierte zweite Meinung bei der Analyse von Unternehmen und Portfolios zu ermöglichen.

---

# Funktionen

## Aktienanalyse

MaurinInvest lädt automatisch Finanzdaten aus verschiedenen Quellen und bereitet diese strukturiert auf.

Enthalten sind unter anderem:

- Fundamentaldaten (z.B. Bewertung, Profitabilität, Wachstum)
- Technische Kennzahlen (z.B. RSI, SMA)
- Branchenvergleiche
- Historische Entwicklungen
- Kontextbasierte Erklärungen zu Finanzkennzahlen

Die Daten werden visualisiert und in einen verständlichen Kontext gesetzt, damit Unternehmen einfacher verglichen werden können.

---

## Branchenvergleich

Eine einzelne Kennzahl ist oft schwer einzuordnen.

MaurinInvest vergleicht Unternehmen deshalb mit Branchenwerten und zeigt:

- ob Kennzahlen über oder unter dem Branchendurchschnitt liegen
- wie sich Unternehmen innerhalb ihrer Branche positionieren
- welche Stärken und Schwächen sichtbar werden

---

## Portfolio-Analyse

Nutzer können ihr Portfolio analysieren und mögliche Auswirkungen neuer Investments simulieren.

Funktionen:

- Übersicht der Portfolio-Struktur
- Analyse von Branchen- und Regionenrisiken
- Identifikation möglicher Konzentrationsrisiken
- Simulation potenzieller Käufe (z.B. ETFs)

---

## KI-gestützte Unternehmensanalyse

Ein integriertes KI-Modul unterstützt die qualitative Analyse eines Unternehmens.

Dabei werden unter anderem betrachtet:

- Wettbewerber
- Zulieferer
- Abnehmer
- Marktumfeld

Die Analyse wird über KI-Schnittstellen generiert und unterstützt Nutzer dabei, komplexe Zusammenhänge schneller zu verstehen.

Zusätzlich erstellt MaurinInvest aus den Analyseergebnissen einen strukturierten Prompt, der für weiterführende Analysen mit externen KI-Tools verwendet werden kann.

Verwendete KI-Dienste:

- Groq API
- Google AI Studio (Gemini)

---

## Automatisierung & Benachrichtigungen

MaurinInvest beinhaltet automatisierte Hintergrundprozesse.

Dazu gehören:

- regelmässige Aktualisierung von Marktdaten
- automatische Portfolio-Prüfungen
- Benachrichtigungssystem (COMI) für relevante Veränderungen

Die Prozesse werden über GitHub Actions automatisiert ausgeführt.

---

# Screenshots

---

## Demo

Kurze Demonstration der Aktien- und Portfolioanalyse von MaurinInvest.

> **Hinweis:** Das im Video gezeigte Portfolio und die ausgewählten Unternehmen sind fiktive Demo-Beispiele und stellen nicht mein persönliches Portfolio dar. Die dargestellten Bewertungen sind automatisch generierte Analyseergebnisse und keine Anlageberatung oder Kaufempfehlung.



https://github.com/user-attachments/assets/6cfb433a-3df0-4790-9d3a-0c48aa8de239





---

## Aktienanalyse

<img width="668" height="325" alt="image" src="https://github.com/user-attachments/assets/598d8ec8-d199-4901-816c-02039fe0ea1f" />



Automatische Darstellung von Finanzkennzahlen, technischen Indikatoren und Branchenvergleich.

---

## KI-gestützte Unternehmensanalyse
<img width="659" height="324" alt="image" src="https://github.com/user-attachments/assets/4f81da54-584d-41bb-8810-bccfbbb01636" />

Interaktive Erläuterung von Finanzkennzahlen und Analysen direkt in der Anwendung durch KI.


<img width="690" height="287" alt="image" src="https://github.com/user-attachments/assets/777fe266-7da9-44a5-8402-0a97dd080fba" />
<img width="692" height="354" alt="image" src="https://github.com/user-attachments/assets/cd99c2fe-03b8-47d6-a324-3340bf739163" />





Analyse des Unternehmensumfelds mit Wettbewerbern, Zulieferern und Abnehmern.

---

## Portfolio-Simulation

<img width="650" height="293" alt="image" src="https://github.com/user-attachments/assets/8f230ae1-5d60-407d-896b-60dc178596a1" />





Simulation der Auswirkungen neuer Investments auf die bestehende Portfolio-Struktur.

---

## Automatisierte Alarme & Wochenübersichten

<img width="430" height="404" alt="image" src="https://github.com/user-attachments/assets/b203813e-1280-4ffe-97e5-3eba9658c0c4" />


Automatisierte Push-Benachrichtigungen durch COMI: vordefinierte Alarme bei relevanten Portfolio-Veränderungen sowie regelmässige Wochenübersichten mit den wichtigsten Entwicklungen.

---


# Technologie

## Programmiersprachen & Frameworks

- Python
- Streamlit
- SQL

## Datenverarbeitung

- Pandas
- NumPy

## Datenbanken & Backend

- Supabase

## Finanzdaten

- Yahoo Finance
- Financial Modeling Prep
- Finnhub
- Alpha Vantage

## KI & Automatisierung

- Groq API
- Google AI Studio
- GitHub Actions
- Brevo API

## Sicherheit & Authentifizierung

- OAuth2
- Streamlit Secrets

---

# Technische Architektur

MaurinInvest verbindet mehrere Module:


```mermaid
graph TD
    A[Nutzer wählt Aktie] --> B{Daten vorhanden?}

    B -->|Ja| C[Bestehende Daten aus Supabase laden]
    B -->|Nein| D[Finanzdaten aus APIs abrufen]

    D --> E[Daten speichern und berechnen]
    
    C --> F[Finanzanalyse]
    E --> F

    F --> G[Vergleich mit Branchenwerten<br/>und Kennzahlen-Bewertung]

    G --> H[Portfolio-Kontext<br/>Risiken und Diversifikation]

    H --> I[KI-Analyse des Unternehmensumfelds]

    I --> J[Zusammenfassung & Bewertungssystem]

    J --> K[Individueller Analyse-Prompt<br/>für weitere Nutzung]
```

Besonderheiten der Architektur:

Caching mit Supabase: Bereits geladene Daten werden gespeichert, wodurch API-Anfragen reduziert und Ladezeiten verbessert werden.
Portfolio-Integration: Einzelne Aktien werden im Kontext des bestehenden Portfolios analysiert, um mögliche Klumpenrisiken zu erkennen.
Kombination aus Datenanalyse und KI: Finanzkennzahlen werden mit einer KI-gestützten Analyse des Unternehmensumfelds ergänzt.
KI-gestützte Weiterverarbeitung: Die Analyseergebnisse können als strukturierter Prompt für externe KI-Tools wie ChatGPT oder Claude genutzt werden.


---

# Projektumfang

Die aktuelle Version umfasst:

- mehrere tausend Zeilen Python-Code
- verschiedene externe APIs
- automatisierte Datenprozesse
- eigene Bewertungslogik
- Benutzerverwaltung und Authentifizierung

---


# Aktuelle Weiterentwicklung

Geplante Erweiterungen:

- Ausbau des Makroanalyse-Moduls
- Erweiterung der KI-Funktionen
- zusätzliche Portfolio-Analysen
- weitere Automatisierungen

---

# Autor

**Gian Fadri Jaecklin**  
Bachelor Wirtschaftswissenschaften (Schwerpunkt Banking & Finance)
Universität Zürich

Entwickelt als eigenes Finance-Tech-Projekt mit Fokus auf Datenanalyse, Investmentbewertung und Automatisierung.
