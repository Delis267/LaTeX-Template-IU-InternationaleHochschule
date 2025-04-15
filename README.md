# 📄 IU LaTeX-Template – Advanced Workbook

Dieses LaTeX-Template ist für wissenschaftliche Arbeiten an der **IU Internationale Hochschule** optimiert und basiert auf LuaLaTeX. Es folgt dem APA-Zitierstil und bietet benutzerdefinierte Umgebungen für Tabellen, Abbildungen und Codelistings sowie viele sinnvolle Voreinstellungen.

---

## 🚀 Setup

### Voraussetzungen

- Compiler für das PDF muss auf **LuaLaTeX** gestellt werden in Overleaf zb.
- **Biber** (für Bibliographie mit `biblatex`)
- Editor mit LaTeX-Support (z. B. VS Code + LaTeX Workshop, Overleaf, TeXstudio)


## 📦 Enthaltene Pakete (Auswahl)

| Paket         | Funktion                                              |
|---------------|-------------------------------------------------------|
| `babel`       | Deutsche Sprache & Trennregeln                       |
| `geometry`    | Seitenränder (2 cm rundum)                           |
| `setspace`    | 1,5-facher Zeilenabstand                             |
| `fontspec`    | Arial als Hauptschriftart                            |
| `biblatex`    | Literaturverwaltung im APA-Stil                      |
| `listings`    | Darstellung von Quellcode inkl. Formatierung         |
| `caption`     | Anpassung von Abbildungs-/Tabellenbeschriftungen     |
| `acronym`     | Abkürzungsverzeichnis                                 |
| `titlesec`    | Überschriftengrößen anpassbar                         |
| `adjustbox`   | Größe von Bildern anpassen                           |

---

## 🧩 Eigene Befehle & Umgebungen

### `apatable` – APA-konforme Tabellen

```latex
\begin{apatable}{Titel}{label}{|p{3cm}|p{2.5cm}|p{8cm}|}{Quellenangabe}
  % Tabelleninhalt
\end{apatable}
```

- Automatisch beschriftet mit „**Tab. X: Titel**“
- Quelle wird unterhalb angegeben
- Für das Tabellenverzeichnis vorbereitet

---

### `\abbildung` – Bilder mit Quellenangabe

```latex
\abbildung{Titel der Abbildung}{label}{bilddatei.png}{Quelle: Eigene Darstellung}
```

- Bild aus dem Pfad `resources/img/` wird eingebunden
- Automatische Beschriftung mit „**Abb. X: Titel**“

---

### `\codelisting` – Quellcode im Abbildungsverzeichnis

```latex
\codelisting{Titel}{label}{dateiname.java}{Sprache}{Quelle: Eigene Darstellung}
```

- Code aus `resources/code/` wird eingebunden (Ordner sollte vorher erstellt werden.)
- Titel wird als **Abbildung** („Abb. X“) für Listingverzeichnis behandelt, da der Zitierleitfaden nicht auf Codelistings eingeht.

Unterstützte Sprachen: `json`, `xml`, `java`, `python`, etc.

---

## ✍️ Gliederung mit Sections

Überschriften sind auf IU-konformes Format angepasst (Schriftgröße 12pt, fett):

```latex
\section{Hauptüberschrift}
\subsection{Unterüberschrift}
\subsubsection{Weitere Ebene}
```

---

## 📚 Literaturverwaltung

- Verwendet `biblatex` mit APA-Stil
- Bibliographie-Datei: `resources/references.bib`
- Einfügen im Text: `\parencite{Schlüssel}` oder `\textcite{Schlüssel}`
- Ausgabe: `\printbibliography`

---

## 🔠 Abkürzungsverzeichnis

- Abkürzungen definieren im Bereich:

```latex
\begin{acronym}
\acro{iu}[IU]{IU Internationale Hochschule}
\acro{csv}[CSV]{Comma-separated values}
\end{acronym}
```

- Anzeige erfolgt mit `\ac{iu}` etc.

---

## 🧳️ Verzeichnisse

Die folgenden Verzeichnisse sind bereits vorbereitet und einkommentierbar:

- Inhaltsverzeichnis (`\tableofcontents`)
- Abbildungs-, Tabellen- und Listingverzeichnis
- Abkürzungsverzeichnis

---

## 🔧 Anpassung

- Passe bei Bedarf die Schriftart über `\setmainfont{Arial}` an.
- Farbe, Stil oder Logik für Code kannst du im `\lstset` Block verändern.

---

## 🧪 Beispielkompilierung

Ein Beispiel-Dokument liegt als `main.tex` vor. Nach dem Einfügen eigener Inhalte kannst du es direkt kompilieren.

---

## 👤 Autor

Template erstellt von **Dennis Lätsch**  
Lizenz: frei nutzbar für IU-Zwecke (persönliche Nutzung)

