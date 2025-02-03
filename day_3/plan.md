## **Tag 3: Angewandte OOP und Design Patterns**
**Ziel:**  
- Vertiefung der **objektorientierten Programmierung (OOP)** durch **praxisnahe Anwendungen**.  
- Einführung in einfache **Design Patterns**, aber mit Schwerpunkt auf **praktische Umsetzung**.  

---

### **Tagesablauf**
| **Uhrzeit**   | **Thema**                                      | **Beschreibung** |
|--------------|-----------------------------------------------|-----------------|
| **09:00 - 09:15** | **Begrüßung & Recap von Tag 2**             | Wiederholung der wichtigsten OOP-Konzepte. |
| **09:15 - 10:15** | **Erweiterung von OOP: Zusammensetzung (Composition)** | Praktischer Einsatz von Objekten in anderen Objekten. |
| **10:15 - 10:30** | **Kurze Einführung in einfache Design Patterns** | Factory Method, Singleton (nur Konzept, wenig Theorie). |
| **10:30 - 11:00** | **Pause** | |
| **11:00 - 12:00** | **Mini-Projekt: Modellierung eines realen Systems** | Studierende erstellen eine Anwendung mit mehreren Klassen. |
| **12:00 - 12:30** | **Code-Verbesserung & Debugging-Techniken** | Gemeinsame Analyse des Codes, Verbesserung der Struktur. |
| **12:30 - 13:00** | **Reflexion & Q&A** | Fragen der Studierenden beantworten, mögliche Erweiterungen diskutieren. |

---

## **Detaillierter Ablauf**

### **09:00 - 09:15: Begrüßung & Recap von Tag 2**
- **Ziel:** Wiederholung der Kernkonzepte aus Tag 2 (Klassen, Vererbung, Kapselung, abstrakte Klassen, statische Methoden).  
- **Aktivität:**  
  - Dozent stellt **3 Fragen** zur Wiederholung:
    - Was ist der Unterschied zwischen **Kapselung** und **Vererbung**?
    - Warum nutzen wir **private Attribute (`__attribut`)**?
    - Wozu dienen **statische Methoden (`@staticmethod`)**?
  - Ein Studierender demonstriert eine einfache Klasse mit **Vererbung**.  

---

### **09:15 - 10:15: Zusammensetzung (Composition) – Objekte in Objekten**
- **Theorie (kurz, ca. 10 Minuten)**  
  - **Warum brauchen wir Composition?**  
    - Alternative zu Vererbung → Bessere Flexibilität.  
    - Ein **Objekt kann mehrere andere Objekte enthalten** (z. B. ein Auto hat einen Motor und Reifen).  

- **Code-Beispiel:**  
  ```python
  class Motor:
      def __init__(self, leistung):
          self.leistung = leistung

  class Auto:
      def __init__(self, marke, modell, motor):
          self.marke = marke
          self.modell = modell
          self.motor = motor  # Objekt innerhalb eines anderen Objekts

      def anzeigen(self):
          print(f"{self.marke} {self.modell} mit {self.motor.leistung} PS")

  # Motor-Objekt erstellen
  motor1 = Motor(150)

  # Auto-Objekt mit Motor erstellen
  auto1 = Auto("BMW", "X3", motor1)
  auto1.anzeigen()
  ```

- **Übung:**  
  - Studierende erstellen eine `Bibliothek`-Klasse, die mehrere `Bücher` enthält.  
  - `Buch` hat Attribute `titel` und `autor`.  
  - `Bibliothek` speichert eine Liste von Büchern und kann sie anzeigen.

---

### **10:15 - 10:30: Einführung in einfache Design Patterns**
- **Theorie (sehr kurz, kein tiefes Verständnis erforderlich):**  
  - **Factory Method:** Erzeugt Objekte, ohne die exakte Klasse anzugeben.  
  - **Singleton:** Erlaubt nur eine einzige Instanz einer Klasse.  

- **Factory Method Beispiel:**  
  ```python
  class Fahrzeug:
      def __init__(self, typ):
          self.typ = typ

      def fahren(self):
          print(f"Das {self.typ} fährt los!")

  class FahrzeugFabrik:
      @staticmethod
      def erstellen(typ):
          return Fahrzeug(typ)

  # Fahrzeuge mit Factory erstellen
  auto = FahrzeugFabrik.erstellen("Auto")
  fahrrad = FahrzeugFabrik.erstellen("Fahrrad")

  auto.fahren()
  fahrrad.fahren()
  ```

- **Frage:**  
  - Warum ist die `FahrzeugFabrik`-Klasse nützlich?

- **Übung:**  
  - Studierende erstellen eine einfache `MitarbeiterFabrik`, die `Mitarbeiter`-Objekte mit bestimmten Rollen erzeugt.

---

### **10:30 - 11:00: Pause** 😃  

---

### **11:00 - 12:00: Mini-Projekt – Modellierung eines realen Systems**
- **Aufgabe:**  
  - Studierende modellieren eine **Bestellung in einem Online-Shop**.  
  - Sie definieren folgende Klassen:
    - `Produkt` (Name, Preis)
    - `Kunde` (Name, E-Mail)
    - `Bestellung` (enthält `Produkte` und `Kunde`)

- **Beispiel:**  
  ```python
  class Produkt:
      def __init__(self, name, preis):
          self.name = name
          self.preis = preis

  class Kunde:
      def __init__(self, name, email):
          self.name = name
          self.email = email

  class Bestellung:
      def __init__(self, kunde):
          self.kunde = kunde
          self.produkte = []

      def produkt_hinzufuegen(self, produkt):
          self.produkte.append(produkt)

      def anzeigen(self):
          print(f"Bestellung für {self.kunde.name}:")
          for p in self.produkte:
              print(f"- {p.name} ({p.preis} €)")

  # Testen
  kunde1 = Kunde("Max Mustermann", "max@example.com")
  bestellung1 = Bestellung(kunde1)

  produkt1 = Produkt("Laptop", 1200)
  produkt2 = Produkt("Maus", 30)

  bestellung1.produkt_hinzufuegen(produkt1)
  bestellung1.produkt_hinzufuegen(produkt2)

  bestellung1.anzeigen()
  ```

- **Ziel:**  
  - Studierende erweitern das Modell, indem sie **mehr Funktionen hinzufügen** (z. B. Gesamtpreis berechnen).  

---

### **12:00 - 12:30: Code-Verbesserung & Debugging-Techniken**
- **Debugging-Methoden:**  
  - **`print()` für schnelle Fehleranalyse.**  
  - **Breakpoints in VS Code oder PyCharm setzen.**  
  - **`pdb`-Modul für Debugging in Python nutzen.**  

- **Übung:**  
  - Studierende verbessern ihren `Bestellung`-Code:
    - Berechnung des **Gesamtpreises**.
    - Neue Methode `bestellung_anzeigen()` debuggen.

---

### **12:30 - 13:00: Reflexion & Q&A**
- **Offene Fragen klären.**  
- **Zusammenfassung des Tages:**  
  - **Zusammensetzung vs. Vererbung:** Wann sollte man was nutzen?  
  - **Wie Factory Patterns in großen Projekten helfen können.**  

- **Hausaufgabe:**  
  - Studierende erstellen eine `Restaurant`-Klasse mit `Tischen`, die `Bestellungen` enthalten.

---

## **Zusammenfassung**
✅ **Praktische OOP-Konzepte mit realistischen Beispielen**  
✅ **Minimaler Design-Pattern-Fokus, aber nützliche Einführung**  
✅ **Viel Praxis: Eigenständiges Programmieren steht im Fokus**  
