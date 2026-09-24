# ENIAC A/B-Test Analyse: Optimierung der Button-Conversion 📊

Ein datengetriebenes Projekt zur Evaluierung von UI-Design-Änderungen und deren Auswirkungen auf die Customer Journey für den E-Commerce-Anbieter ENIAC. 

Dieses Projekt wurde im Rahmen der Weiterbildung zur IT-Fachkraft für Data Analytics & AI an der WBS Coding School erstellt.

## 📌 Projektübersicht
Das Ziel dieser Analyse war es, durch statistische Hypothesentests herauszufinden, welches Button-Design (Farbe und Call-to-Action-Text) den höchsten geschäftlichen Wert generiert. Getestet wurden vier Varianten in einem A/B/C/D-Test:
* **Version A:** Weiß / "SHOP NOW"
* **Version B:** Rot / "SHOP NOW"
* **Version C:** Weiß / "SEE DEALS"
* **Version D:** Rot / "SEE DEALS"

## 🛠️ Tech-Stack & Tools
* **Sprache:** Python 3
* **Umgebung:** Jupyter Notebook / Google Colab
* **Bibliotheken:** `pandas`, `numpy`, `scipy.stats` (Chi-Quadrat-Test)
* **Präsentation:** PowerPoint (automatisierte Foliengenerierung via `python-pptx`)

## 📂 Repository-Struktur
* `Eniacs_A_B_Test.ipynb`: Das vollständige Jupyter Notebook mit der Datenbereinigung und der statistischen Modellierung.
* `ENIAC_Finale_Praesentation.pptx` / `.pdf`: Die Management-Präsentation mit den visuellen Ergebnissen.
* `data/`: Ordner mit den zugrundeliegenden Rohdaten (`eniac_a.csv` bis `eniac_d.csv`).

## 🧮 Methodik
1. **Datenbereinigung:** Extraktion von Klick- und Visit-Zahlen aus unstrukturierten Text-Strings mittels Python-String-Methoden (`.split()`, `.strip()`).
2. **Globaler Test:** Ein Chi-Quadrat-Test über alle vier Varianten (Signifikanzniveau α = 0.05).
3. **Post-Hoc-Analyse:** Paarweise Chi-Quadrat-Tests der Gewinner-Varianten. Zur Vermeidung des Alpha-Fehlers bei multiplen Vergleichen wurde eine strenge **Bonferroni-Korrektur** (α = 0.00833) angewendet.
4. **Business-Metriken:** Auswertung der Klickrate (CTR) als primäre Metrik und der Drop-Off Rate (Abbruchrate im Funnel) als sekundäre Metrik.

## 🏆 Schlüsselergebnisse & Fazit
* **Farbe ist entscheidend:** Die roten Buttons (B & D) performten bei der Klickrate signifikant schlechter und wurden frühzeitig aussortiert.
* **Statistisches Unentschieden:** Der korrigierte Post-hoc-Test zeigte keinen statistisch signifikanten Unterschied (p-Wert: 0.46) in der Klickrate zwischen den weißen Versionen A und C.
* **Der Tie-Breaker (Drop-Off Rate):** Bei genauerer Betrachtung der Customer Journey nach dem Klick zeigte sich, dass Version C über 70 % der Nutzer direkt wieder verlor. Version A hingegen hielt die Abbruchrate bei ca. 62 %.
* **Finale Empfehlung:** **Version A (Weiß "SHOP NOW")** ist der klare Gewinner. Sie generiert initial die gleiche Menge an Traffic wie Version C, führt diesen aber wesentlich zuverlässiger durch den Conversion-Funnel.

---
**Autor:** Georgij Vinnichenko  
**GitHub:** [georgijvinnichenko97](https://github.com/georgijvinnichenko97)
