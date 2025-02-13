# **📌 Detaillierter Plan für Tag 5: Datenanalyse mit NumPy & Pandas (Teil 1)**  
**Ziel:**  
- Einführung in die **Datenverarbeitung mit Python**.  
- Verwendung von **NumPy für numerische Berechnungen** und **Pandas für Datenanalyse**.  
- Erste Schritte mit **Datenimport, -manipulation und -visualisierung**.

---

## **📅 Tagesablauf**
| **Zeit**   | **Thema**                                      | **Beschreibung** |
|------------|-----------------------------------------------|-----------------|
| **09:00 - 09:30** | **Einführung in Datenanalyse mit Python** | Warum sind NumPy & Pandas wichtig? Überblick über Datenverarbeitung. |
| **09:30 - 10:15** | **Grundlagen von NumPy: Arrays & Operationen** | Arbeiten mit Arrays, grundlegende Berechnungen, Indexierung. |
| **10:15 - 10:30** | **Pause** | - |
| **10:30 - 11:15** | **Fortgeschrittene NumPy-Funktionen** | Broadcasting, mathematische Funktionen, Performance-Vergleiche. |
| **11:15 - 12:00** | **Grundlagen von Pandas: DataFrames & Series** | Daten laden, grundlegende Operationen, Zugriff auf Daten. |
| **12:00 - 12:30** | **Datenmanipulation in Pandas** | Sortieren, Filtern, Berechnungen mit Pandas. |
| **12:30 - 13:00** | **Reflexion & Q&A** | Fragen und Diskussionen, Zusammenfassung des Tages. |

---

## **📌 9:00 - 09:30: Einführung in Datenanalyse mit Python**
> **Warum brauchen wir NumPy & Pandas?**  
- **NumPy:**  
  - Schnelle **numerische Berechnungen** mit Arrays und Matrizen.  
  - **Viel schneller als normale Python-Listen**.  
- **Pandas:**  
  - **Tabellenartige Datenstrukturen (DataFrames)** für einfache Analyse.  
  - **Effiziente Datenverarbeitung & -bereinigung**.

**Beispiel: Warum ist NumPy schneller als Listen?**
```python
import numpy as np
import time

groesse = 1000000
liste = list(range(groesse))
array = np.arange(groesse)

start = time.time()
sum(liste)
print("Listen-Summe:", time.time() - start)

start = time.time()
np.sum(array)
print("NumPy-Summe:", time.time() - start)
```
> **Diskussion:**  
- Wann brauchen wir **NumPy** und wann **Pandas**?  
- Welche Probleme lösen diese Bibliotheken?  

---

## **📌 9:30 - 10:15: Grundlagen von NumPy: Arrays & Operationen**
> **Ziel:** Verstehen, wie NumPy Arrays funktionieren und warum sie effizient sind.

### **1️⃣ Erstellen von NumPy Arrays**
```python
import numpy as np

# Array aus einer Liste
a = np.array([1, 2, 3, 4, 5])

# Array mit Nullen oder Einsen
b = np.zeros((3,3))  # 3x3 Null-Matrix
c = np.ones((2,2))   # 2x2 Einsen-Matrix

# Gleichmäßige Werte erzeugen
d = np.arange(0, 10, 2)  # [0, 2, 4, 6, 8]
e = np.linspace(0, 1, 5)  # [0, 0.25, 0.5, 0.75, 1]
```

### **2️⃣ Indexierung & Slicing**
```python
arr = np.array([10, 20, 30, 40, 50])
print(arr[1])      # 20
print(arr[1:4])    # [20, 30, 40]
print(arr[::-1])   # [50, 40, 30, 20, 10]
```

> **Praxis:**  
1. Erstelle verschiedene **NumPy-Arrays** und teste **Indexierung & Slicing**.  
2. Wandle eine **Liste in ein NumPy-Array** um und vergleiche Performance.  

---

## **📌 10:30 - 11:15: Fortgeschrittene NumPy-Funktionen**
> **Ziel:** NumPy-Operationen für mathematische Berechnungen & schnelle Berechnungen nutzen.

### **1️⃣ Mathematische Operationen**
```python
arr = np.array([1, 2, 3, 4, 5])
print(np.sum(arr))      # 15
print(np.mean(arr))     # 3.0 (Mittelwert)
print(np.std(arr))      # 1.41 (Standardabweichung)
print(np.max(arr))      # 5 (Maximum)
print(np.min(arr))      # 1 (Minimum)
```

### **2️⃣ Broadcasting & Elementweise Operationen**
```python
arr = np.array([1, 2, 3, 4])
print(arr * 2)       # [2, 4, 6, 8]
print(arr + 10)      # [11, 12, 13, 14]

# Elementweise Multiplikation
arr2 = np.array([2, 4, 6, 8])
print(arr * arr2)    # [2, 8, 18, 32]
```

> **Praxis:**  
1. Berechne **Mittelwert, Summe und Standardabweichung** eines Arrays.  
2. Erstelle **zwei Arrays** und wende **elementweise Operationen** an.  

---

## **📌 11:15 - 12:00: Grundlagen von Pandas: DataFrames & Series**
> **Ziel:** Einführung in **DataFrames**, die leistungsfähige Datenstruktur von Pandas.

### **1️⃣ DataFrames erstellen & importieren**
```python
import pandas as pd

# Erstellen eines DataFrames aus einem Dictionary
daten = {'Name': ['Anna', 'Ben', 'Chris'],
         'Alter': [25, 30, 35],
         'Gehalt': [50000, 55000, 60000]}

df = pd.DataFrame(daten)
print(df)
```

### **2️⃣ Zugriff auf Daten**
```python
print(df['Name'])   # Zugriff auf eine Spalte
print(df.iloc[1])   # Zugriff auf eine Zeile nach Index
print(df.loc[1])    # Zugriff auf eine Zeile mit Label
```

> **Praxis:**  
1. Erstelle ein **DataFrame aus einer CSV-Datei**.  
2. Nutze **`.iloc[]` und `.loc[]`**, um Daten auszuwählen.  

---

## **📌 12:00 - 12:30: Datenmanipulation in Pandas**
> **Ziel:** Lernen, wie man **Daten filtert, sortiert und berechnet**.

### **1️⃣ Daten sortieren & filtern**
```python
# Sortieren nach Alter
df.sort_values(by='Alter', ascending=False)

# Filtern nach Gehalt
print(df[df['Gehalt'] > 52000])
```

### **2️⃣ Berechnungen mit Pandas**
```python
# Neue Spalte hinzufügen
df['Bonus'] = df['Gehalt'] * 0.1

# Durchschnittsgehalt berechnen
print(df['Gehalt'].mean())  # 55000
```

> **Praxis:**  
1. Sortiere ein DataFrame nach verschiedenen Spalten.  
2. Füge eine neue Spalte hinzu und berechne einen **Bonus** für Mitarbeiter.  

---

## **📌 12:30 - 13:00: Reflexion & Q&A**
> **Diskussion:**  
- **Wann sollten wir NumPy vs. Pandas verwenden?**  
- **Welcher Teil war heute am herausforderndsten?**  
- **Wichtige Konzepte noch einmal erklären.**

> **Hausaufgabe:**  
1. Lade einen **CSV-Datensatz** in Pandas.  
2. **Sortiere & filtere die Daten** basierend auf einer Bedingung.  
3. Erstelle eine neue **berechnete Spalte**.

---

✅ **Tag 5 erfolgreich abgeschlossen!** 🎉  
Möchtest du eine **Präsentation oder ein Jupyter Notebook für diesen Tag**? 🚀