## **Themenfokus von Tag 3** 
- **Algorithmisches Denken**: Wie zerlegen wir Probleme in logische Schritte?  
- **Suchalgorithmen**: Lineare Suche vs. binäre Suche.  
- **Sortieralgorithmen**: Bubble Sort, Selection Sort (ggf. weitere einfache Sortiermethoden).  
- **Big-O-Notation**: Einführung in Zeitkomplexität und Effizienzbewertung.  

---

## **Struktur und Zeitplan (09:00 - 13:00 Uhr)**

| Zeit              | Thema                                                      | Inhalt/Aktivität                                                                                                    |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **09:00 - 09:15** | **Begrüßung & Rückblick**                                 | - Kurze Zusammenfassung von Tag 2 (z.B. fortgeschrittene OOP-Konzepte)<br>- Ziele und Ablauf des heutigen Tages.      |
| **09:15 - 09:45** | **Einführung in Computational Thinking**                  | - Bedeutung des algorithmischen Denkens<br>- Problemzerlegung, Pseudocode, Flussdiagramme.<br>- **Kurzes Beispiel**: Wie löst man ein Alltagsproblem in Schritten? |
| **09:45 - 10:30** | **Suchalgorithmen & Big-O-Grundlagen**                    | - **Lineare Suche** (Vorgehen, Vor- und Nachteile)<br>- **Binäre Suche** (Voraussetzungen, Vorgehen)<br>- Erste Einblicke in Big-O-Notation (O(n), O(log n)). |
| **10:30 - 11:00** | **Pause (30 Minuten)**                                    | - Zeit für Erholung, Austausch oder Fragen                                                                           |
| **11:00 - 11:30** | **Sortieralgorithmen I – Bubble Sort & Selection Sort**    | - Funktionsweise beider Algorithmen, Schritt-für-Schritt-Visualisierung<br>- Implementierung in Python.              |
| **11:30 - 12:00** | **Sortieralgorithmen II – Zeitkomplexität & Praxis**       | - Vertiefung Big-O: O(n²) für Bubble/Selection Sort <br>- Praxisbeispiel: Sortieren einer Liste von Zahlen/Stringlisten.|
| **12:00 - 12:30** | **Übungen & Mini-Projekte**                                | - Studierende implementieren und vergleichen Such- und Sortieralgorithmen.<br>- Analyse der Laufzeiten mit kleinen Datensätzen. |
| **12:30 - 12:55** | **Fragen, Diskussion & Reflexion**                         | - Gemeinsame Auswertung der Übungen<br>- Diskussion zu Vor- und Nachteilen verschiedener Algorithmen.<br>- Wo kommt Big-O im Alltag vor? |
| **12:55 - 13:00** | **Abschluss & Ausblick**                                   | - Zusammenfassung der Kernthemen<br>- Ausblick auf Tag 4 (z.B. Rekursion, Datenstrukturen, weiterführende Themen).    |

---

## **Detailbeschreibung der Einheiten**

### **09:00 - 09:15: Begrüßung & Rückblick**
- **Kurzer Rückblick** auf Tag 2 (z.B. Abschluss der OOP-Themen wie Kapselung, abstrakte Klassen).  
- Vorstellung der heutigen **Lernziele**:
  1. Verständnis für algorithmisches Denken und Big-O-Notation.
  2. Implementierung grundlegender Such- und Sortieralgorithmen in Python.
  3. Erste Einschätzung von Effizienz und Laufzeit.

### **09:15 - 09:45: Einführung in Computational Thinking**
- **Definition & Bedeutung** von Computational Thinking:
  - Problemanalyse, Problemzerlegung, Pseudocode, Diagramme.
- **Kurzes Beispiel**:
  - Alltagsproblem wie „Finde eine bestimmte Zutat in der Küche“ in Arbeitsschritte zerlegen.
  - Überleitung zu Suchalgorithmen.

> **Aktivität:**  
> - Die Teilnehmenden formulieren in Kleingruppen ein Mini-Pseudocode für ein einfaches Problem (z.B. „Finde den kleinsten Wert in einer Liste“).

### **09:45 - 10:30: Suchalgorithmen & Big-O-Grundlagen**
- **Lineare Suche**:
  - Funktionsweise (iteratives Durchgehen der Liste).
  - Komplexität O(n).
- **Binäre Suche**:
  - Voraussetzung: sortierte Daten.
  - Komplexität O(log n).
- **Big-O-Grundlagen**:
  - Was ist Big-O, warum ist es nützlich?
  - Verschiedene Komplexitätsklassen (O(n), O(log n), O(n²) ...).

> **Kurze Demo in Python**  
> ```python
> def lineare_suche(liste, wert):
>     for i, elem in enumerate(liste):
>         if elem == wert:
>             return i
>     return -1
> 
> def binaere_suche(sortierte_liste, wert):
>     links, rechts = 0, len(sortierte_liste) - 1
>     while links <= rechts:
>         mitte = (links + rechts) // 2
>         if sortierte_liste[mitte] == wert:
>             return mitte
>         elif sortierte_liste[mitte] < wert:
>             links = mitte + 1
>         else:
>             rechts = mitte - 1
>     return -1
> ```
> - Diskutiere Vor-/Nachteile und Laufzeiten.

### **10:30 - 11:00: Pause (30 Minuten)**
- Zeit zum Durchatmen, Kaffee holen und Austausch untereinander.

### **11:00 - 11:30: Sortieralgorithmen I – Bubble Sort & Selection Sort**
- **Bubble Sort**:
  - Idee: wiederholtes „Blubbern“ der größten Elemente nach hinten.
  - Schritt-für-Schritt-Visualisierung.
  - Komplexität O(n²) im Worst Case.
- **Selection Sort**:
  - Idee: Suche das kleinste Element und platziere es am Anfang.
  - Ebenfalls O(n²) im Worst Case.

> **Demo in Python**  
> ```python
> def bubble_sort(liste):
>     n = len(liste)
>     for i in range(n):
>         for j in range(0, n-i-1):
>             if liste[j] > liste[j+1]:
>                 liste[j], liste[j+1] = liste[j+1], liste[j]
> 
> def selection_sort(liste):
>     n = len(liste)
>     for i in range(n):
>         min_index = i
>         for j in range(i+1, n):
>             if liste[j] < liste[min_index]:
>                 min_index = j
>         liste[i], liste[min_index] = liste[min_index], liste[i]
> ```

### **11:30 - 12:00: Sortieralgorithmen II – Zeitkomplexität & Praxis**
- **Analysiere** Zeitkomplexität (O(n²)) von Bubble/Selection Sort.
- **Vergleich** mit verbesserten Verfahren (z.B. Insertionsort – optional).
- **Praxisbeispiel**:
  - Sortierung einer zufälligen Liste von Zahlen.
  - Optional: Messung der Laufzeit (z.B. `time`-Modul oder `%timeit` in Jupyter).

> **Diskussion:**  
> - Warum sind diese Algorithmen in der Praxis selten die erste Wahl?
> - Wann könnten sie trotzdem sinnvoll sein (z.B. kleine Datenmengen)?

### **12:00 - 12:30: Übungen & Mini-Projekte**
- **Übung 1:**  
  - Implementierung oder Vergleich von zwei Sortieralgorithmen (Bubble/Selection) an zufällig generierten Listen.  
  - Bestimmung der Laufzeiten für Listen verschiedener Größe (z.B. 100, 1.000, 10.000 Elemente).

- **Übung 2 (optional):**  
  - Schreib eine Funktion, die eine Liste zunächst sortiert (z.B. Bubble Sort) und dann eine binäre Suche aufruft, um ein Element zu finden.  

> **Ziel:**  
> - Verständnis für die Kombination von Sortier- und Suchverfahren.
> - Sammeln erster Erfahrungen mit Laufzeitmessung in Python.

### **12:30 - 12:55: Fragen, Diskussion & Reflexion**
- **Gemeinsame Auswertung**:
  - Ergebnisse der Übungen besprechen.
  - Stolpersteine und Aha-Momente.
- **Anknüpfungspunkte**:
  - Welche Sortier-/Suchverfahren kennst du aus dem Alltag? (z.B. Wörterbuchsuche, Google-Suche)
  - Erste Ideen, wie man Big-O auch in komplexeren Szenarien (z.B. Datenbanken) einordnen könnte.

### **12:55 - 13:00: Abschluss & Ausblick**
- **Tag 3 Zusammenfassung**:
  - Wichtige Punkte: Algorithmisches Denken, lineare/binäre Suche, Bubble/Selection Sort, Big-O-Basics.
- **Ausblick auf Tag 4**:
  - Vertiefte Datenstrukturen und/oder Rekursion.
  - Oder erste Schritte in Richtung Datenanalyse (NumPy, Pandas), je nach Kursstruktur.

---

## **Tipps zur Durchführung**
1. **Interaktive Beispiele**: Nutze Jupyter Notebook oder Live-Coding, um Such-/Sortierverfahren zu demonstrieren.  
2. **Visualisierung**: Kurze Grafiken oder Online-Animationen (z.B. „VisuAlgo“) helfen, Sortiervorgänge zu verdeutlichen.  
3. **Arbeitsblätter**: Bereite kleine Übungsaufgaben vor, damit die Teilnehmenden direkt ausprobieren können.  
4. **Leistungsstarke vs. einfache Algorithmen**: Mache klar, dass Bubble/Selection Sort zwar pädagogisch sinnvoll sind, aber in der Praxis oft effizientere Algorithmen eingesetzt werden (z.B. Merge Sort, Quick Sort). 