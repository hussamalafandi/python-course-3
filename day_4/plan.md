# **📌 Detaillierter Plan für Tag 4: Computational Thinking, Algorithmeneffizienz & Rekursion**  
**Ziel:**  
- Entwicklung des algorithmischen Denkens und der Fähigkeit, Probleme strukturiert zu lösen.  
- Einführung in **Such- & Sortieralgorithmen** sowie deren Effizienzbewertung.  
- Verständnis und Anwendung von **Rekursion**, um komplexe Probleme zu lösen.

---

## **📅 Tagesablauf**
| **Zeit**   | **Thema**                                      | **Beschreibung** |
|------------|-----------------------------------------------|-----------------|
| **09:00 - 09:30** | **Einführung in Computational Thinking** | Zerlegen von Problemen, Mustererkennung, Abstraktion, Algorithmendesign. |
| **09:30 - 10:15** | **Suchalgorithmen (Linear & Binärsuche)** | Implementieren & Vergleichen von Suchalgorithmen. |
| **10:15 - 10:30** | **Pause** | - |
| **10:30 - 11:15** | **Sortieralgorithmen & Effizienz (Big O Notation)** | Implementierung von Bubble Sort & Quick Sort, Einführung in Big O. |
| **11:15 - 12:00** | **Einführung in Rekursion** | Was ist Rekursion? Einfaches Beispiel (Fakultät, Fibonacci). |
| **12:00 - 12:30** | **Rekursive Problemlösung** | Klassische Probleme (Summierung, Türme von Hanoi, Listen-Summen). |
| **12:30 - 13:00** | **Reflexion & Q&A** | Besprechung von Schwierigkeiten & Fragen. |

---

## **📌 9:00 - 09:30: Einführung in Computational Thinking**
> **Warum ist Computational Thinking wichtig?**  
Computational Thinking ist eine **Methode zur Problemlösung**, die hilft, komplexe Probleme in logische Schritte zu zerlegen.

- **Die 4 Prinzipien:**
  1. **Zerlegung (Decomposition)**  
     → Zerlege ein Problem in kleinere, leichter lösbare Teile.  
  2. **Mustererkennung (Pattern Recognition)**  
     → Gibt es Ähnlichkeiten zu bekannten Problemen?  
  3. **Abstraktion (Abstraction)**  
     → Was sind die wichtigsten Merkmale? Was kann ignoriert werden?  
  4. **Algorithmendesign (Algorithm Design)**  
     → Entwickle eine schrittweise Lösung (Algorithmus).

> **Praxis:**
- Beispiel: **Wie kann man den Prozess „Kaffee kochen“ in logische Schritte unterteilen?**
- **Diskussion:** Wann nutzen wir Computational Thinking im Alltag?

---

## **📌 9:30 - 10:15: Suchalgorithmen (Linear & Binärsuche)**
> **Ziel:** Implementieren und vergleichen von **Linearer Suche & Binärer Suche**.

### **1️⃣ Lineare Suche**
**Eigenschaften:**
- Einfach, aber langsam (`O(n)`)
- Funktioniert auf unsortierten Listen

**Python-Code:**
```python
def lineare_suche(liste, ziel):
    for index, wert in enumerate(liste):
        if wert == ziel:
            return index  # Element gefunden
    return -1  # Element nicht gefunden

zahlen = [3, 1, 4, 6, 9, 2]
print(lineare_suche(zahlen, 6))  # Ausgabe: 3
```

### **2️⃣ Binäre Suche**
**Eigenschaften:**
- Funktioniert nur auf **sortierten** Listen (`O(log n)`)
- Halbiert die Suchmenge mit jedem Schritt

**Python-Code:**
```python
def binaere_suche(liste, ziel):
    links, rechts = 0, len(liste) - 1
    while links <= rechts:
        mitte = (links + rechts) // 2
        if liste[mitte] == ziel:
            return mitte
        elif liste[mitte] < ziel:
            links = mitte + 1
        else:
            rechts = mitte - 1
    return -1  # Element nicht gefunden

zahlen_sortiert = [1, 2, 3, 4, 6, 9]
print(binaere_suche(zahlen_sortiert, 6))  # Ausgabe: 4
```

> **Praxis:**  
1. **Vergleich der beiden Algorithmen:**  
   - Testen mit verschiedenen Listengrößen.  
2. **Wann ist Binärsuche schneller als Linearsuche?**

---

## **📌 10:30 - 11:15: Sortieralgorithmen & Algorithmeneffizienz**
> **Ziel:** Implementierung von Sortieralgorithmen & Einführung in die **Big O Notation**.

### **1️⃣ Bubble Sort (Langsam, aber leicht verständlich)**
```python
def bubble_sort(liste):
    n = len(liste)
    for i in range(n):
        for j in range(n - i - 1):
            if liste[j] > liste[j + 1]:
                liste[j], liste[j + 1] = liste[j + 1], liste[j]

zahlen = [64, 34, 25, 12, 22, 11, 90]
bubble_sort(zahlen)
print(zahlen)
```
⏳ **Laufzeit:** `O(n^2)`

---

### **2️⃣ Quick Sort (Effizienter, wird in der Praxis häufig genutzt)**
```python
def quick_sort(liste):
    if len(liste) <= 1:
        return liste
    pivot = liste[len(liste) // 2]
    links = [x for x in liste if x < pivot]
    mitte = [x for x in liste if x == pivot]
    rechts = [x for x in liste if x > pivot]
    return quick_sort(links) + mitte + quick_sort(rechts)

zahlen = [64, 34, 25, 12, 22, 11, 90]
print(quick_sort(zahlen))
```
⚡ **Laufzeit:** `O(n log n)`

> **Praxis:**
1. **Vergleich der Sortiermethoden** mit unterschiedlich großen Listen.  
2. **Big O Notation erklären** (Verständnis für Laufzeiten entwickeln).

---

## **📌 11:15 - 12:00: Einführung in Rekursion**
> **Ziel:** Verstehen, wie eine Funktion sich selbst aufrufen kann.

### **Beispiel: Fakultät (5! = 5 × 4 × 3 × 2 × 1)**
```python
def fakultaet(n):
    if n == 0:
        return 1  # Basisfall
    return n * fakultaet(n - 1)  # Rekursiver Aufruf

print(fakultaet(5))  # Ausgabe: 120
```

### **2️⃣ Fibonacci-Folge (1, 1, 2, 3, 5, 8, …)**
```python
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n - 1) + fibonacci(n - 2)

print(fibonacci(5))  # Ausgabe: 5
```

> **Praxis:**  
1. **Wann ist Rekursion nützlich?**  
2. **Wieso sind zu viele rekursive Aufrufe ineffizient?**  
3. **Implementiere eine eigene rekursive Funktion!**

---

## **📌 12:00 - 12:30: Rekursive Problemlösung**
> **Ziel:** Lösen von **klassischen rekursiven Problemen**.

- **1️⃣ Summieren einer Liste mit Rekursion**
```python
def summe_liste(liste):
    if len(liste) == 0:
        return 0
    return liste[0] + summe_liste(liste[1:])

print(summe_liste([1, 2, 3, 4, 5]))  # Ausgabe: 15
```

- **2️⃣ Türme von Hanoi (Visualisierung eines berühmten Rekursionsproblems)**
```python
def hanoi(n, start, ziel, hilfe):
    if n == 1:
        print(f"Bewege Scheibe von {start} nach {ziel}")
        return
    hanoi(n - 1, start, hilfe, ziel)
    print(f"Bewege Scheibe von {start} nach {ziel}")
    hanoi(n - 1, hilfe, ziel, start)

hanoi(3, 'A', 'C', 'B')
```

---

## **📌 12:30 - 13:00: Reflexion & Q&A**
- **Diskussion:**  
  - Wann sollte man **Rekursion statt Schleifen** verwenden?
  - Welche Konzepte waren heute **am schwierigsten**?
- **Hausaufgabe:**  
  - Implementiere eine **rekursive Potenzfunktion (x^n)**.