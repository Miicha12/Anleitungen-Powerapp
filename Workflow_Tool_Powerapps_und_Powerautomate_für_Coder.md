# **Workflow Tool Powerapps und Powerautomate für Coder**
## **Dokumentation**

## **Inhalt:**
1. Grundlagen Powerapps
2. Grundlagen des Einfpgens von Elementen
3. Legende von Properties


## **1. Grundlagen Powerapps**

In diesem Kapitel werden die relevantesten Funktionen erläutert, die für die Entwicklung von Apps in Powerapps erforderlich sind.

### **Grundfunktionen**

- `If()`: Wenn etwas zutrifft, dann mach dies, sonst mach das.  
  > ***z. B.*** Wenn Alter über 18, dann "Erwachsen", sonst "Kind"
- `Switch()`: Für mehrere Bedingungen. ähnlich wie `If()`, aber für mehrere Fälle.  
  > ***z. B.*** Wenn Alter 0-12, dann "Kind", 13-19, dann "Teenager", sonst "Erwachsen"
- `Notify()`:Zeigt eine kleien Nachricht in der App an.  
  > ***z. B.*** "Daten erfolgreich gespeichert"
- `Navigate()`: Navigiert zu einem anderen Bildschirm in der App.  
  > ***z. B.*** `Navigate(Screen2, ScreenTransition.Fade)`
- `Back()`: Geht zum vorherigen Bildschirm zurück.  
  > ***z. B.*** `Back()`
- `Exit()`: Beendet die App.  
  > ***z. B.*** `Exit()`

### **Textfunktionen**
- `Text()`: Formatiert eine Zahl oder ein Datum als Text.  
  > ***z. B.*** `Text(1234.56, "[$-de-DE]#,##0.00")` formatiert die Zahl als deutschen Währungsbetrag.
- `Value()`: Konvertiert Text in eine Zahl.  
  > ***z. B.*** `Value("1234.56")` gibt die Zahl 1234.56 zurück.
- `Len()`: Gibt die Länge eines Textes zurück.  
  > ***z. B.*** `Len("Hallo")` gibt 5 zurück.
- `Left()`, `Right()`, `Mid()`: Extrahieren Teile eines Textes.
    > ***z. B.*** `Left("Hallo", 2)` gibt "Ha" zurück, `Right("Hallo", 2)` gibt "lo" zurück, `Mid("Hallo", 2, 3)` gibt "all" zurück.
- `Upper()`, `Lower()`: Wandeln Text in Groß- oder Kleinschreibung um.
    > ***z. B.*** `Upper("Hallo")` gibt "HALLO" zurück, `Lower("HALLO")` gibt "hallo" zurück.
`Trim()`: Entfernt Leerzeichen am Anfang und Ende eines Textes.  
  > ***z. B.*** `Trim("  Hallo  ")` gibt "Hallo" zurück.

### **Mathematikfunktionen**
- `Round()`: Rundet eine Zahl auf eine bestimmte Anzahl von Dezimalstellen.  
  > ***z. B.*** `Round(123.456, 2)` gibt 123.46 zurück.
- `Abs()`: Gibt den Absolutwert einer Zahl zurück.  
  > ***z. B.*** `Abs(-5)` gibt 5 zurück.
- `Sqrt()`: Gibt die Quadratwurzel einer Zahl zurück.  
  > ***z. B.*** `Sqrt(16)` gibt 4 zurück.
- `Rand()`: Gibt eine Zufallszahl zwischen 0 und 1 zurück.  
  > ***z. B.*** `Rand()` gibt eine Zufallszahl wie 0.123456 zurück.
- `Mod()`: Gibt den Rest einer Division zurück.  
  > ***z. B.*** `Mod(10, 3)` gibt 1 zurück, da 10 geteilt durch 3 einen Rest von 1 hat.
  > 

### **Logikfunktionen**
- `And()`, `Or()`, `Not()`: Logische Operatoren für Bedingungen.  
  > ***z. B.*** `If(And(Age > 18, IsStudent), "Erwachsen und Student", "Nicht erwachsen oder kein Student")`
  > `If(Or(Age < 18, IsStudent), "Kind oder Student", "Erwachsen und kein Student")`
- `IsBlank()`: Überprüft, ob ein Wert leer ist.  
  > ***z. B.*** `If(IsBlank(TextInput1.Text), "Feld ist leer", "Feld hat Inhalt")`
- `IsEmpty()`: Überprüft, ob eine Sammlung, Liste ider Tabelle leer ist.  
  > ***z. B.*** `If(IsEmpty(MyCollection), "Sammlung ist leer", "Sammlung hat Elemente")`
- `IsNumeric()`: Überprüft, ob ein Wert numerisch ist.  
  > ***z. B.*** `If(IsNumeric(TextInput1.Text), "Ist eine Zahl", "Ist keine Zahl")`
- `IsError()`: Überprüft, ob ein Ausdruck einen Fehler zurückgibt.  
  > ***z. B.*** `If(IsError(LookUp(MyTable, ID = 1)), "Fehler beim Suchen", "Suche erfolgreich")`

### **Datum- und Zeitfunktionen**
- `Now()`: Gibt das aktuelle Datum und die aktuelle Uhrzeit zurück.  
  > ***z. B.*** `Now()` gibt etwas wie "2023-10-01 12:34:56" zurück.
- `Today()`: Gibt das aktuelle Datum zurück (ohne Uhrzeit).  
  > ***z. B.*** `Today()` gibt "2023-10-01" zurück.
- `Date()`: Erstellt ein Datum aus Jahr, Monat und Tag.  
  > ***z. B.*** `Date(2023, 10, 1)` gibt "2023-10-01" zurück.
- `DateAdd()`: Fügt einem Datum eine bestimmte Anzahl von Tagen, Monaten oder Jahren hinzu.  
  > ***z. B.*** `DateAdd(Today(), 7, Days)` gibt das Datum in 7 Tagen zurück.
- `DateDiff()`: Berechnet die Differenz zwischen zwei Daten in Tagen, Monaten oder Jahren.  
  > ***z. B.*** `DateDiff(Today(), Date(2023, 12, 31), Days)` gibt die Anzahl der Tage bis zum 31. Dezember 2023 zurück.
- `Year()`, `Month()`, `Day()`: Extrahieren Jahr, Monat oder Tag aus einem Datum.  
  > ***z. B.*** `Year(Today())` gibt das aktuelle Jahr zurück, `Month(Today())` den aktuellen Monat, `Day(Today())` den aktuellen Tag.
- `Weekday()`: Gibt den Wochentag eines Datums zurück (1 = Sonntag, 2 = Montag, ...).  
  > ***z. B.*** `Weekday(Today())` gibt den aktuellen Wochentag zurück.
- `FormatDateTime()`: Formatiert ein Datum als Text.  
  > ***z. B.*** `FormatDateTime(Today(), DateTimeFormat.LongDate)` gibt das Datum im langen Format zurück, z. B. "1. Oktober 2023".

### **Listen und Daten**
- `Collect()`: Fügt Elemente zu einer Sammlung hinzu.  
  > ***z. B.*** `Collect(MyCollection, {Name: "Max", Age: 30})` fügt ein Objekt mit Name und Alter zur Sammlung hinzu.
- `Clear()`: Löscht alle Elemente aus einer Sammlung.  
  > ***z. B.*** `Clear(MyCollection)` entfernt alle Elemente aus der Sammlung.
- `ClearCollect()`: Löscht eine Sammlung und fügt dann neue Elemente hinzu.  
  > ***z. B.*** `ClearCollect(MyCollection, {Name: "Max", Age: 30})` löscht die Sammlung und fügt ein neues Objekt hinzu.
- `Remove()`: Entfernt ein bestimmtes Element aus einer Sammlung.  
  > ***z. B.*** `Remove(MyCollection, {Name: "Max", Age: 30})` entfernt das Objekt mit Name "Max" und Alter 30 aus der Sammlung.
- `RemoveIf()`: Entfernt Elemente aus einer Sammlung, die eine bestimmte Bedingung erfüllen.  
  > ***z. B.*** `RemoveIf(MyCollection, Age < 18)` entfernt alle Objekte aus der Sammlung, bei denen das Alter unter 18 ist.
- `Patch()`: Aktualisiert oder fügt ein Element in einer Sammlung hinzu.  
  > ***z. B.*** `Patch(MyCollection, {Name: "Max"}, {Age: 31})` aktualisiert das Alter des Objekts mit Name "Max" auf 31.
- `Sort()`: Sortiert eine Sammlung nach einem bestimmten Feld.  
  > ***z. B.*** `Sort(MyCollection, Age, Ascending)` sortiert die Sammlung nach dem Alter in aufsteigender Reihenfolge.
- `SortByColumns()`: Sortiert eine Sammlung nach mehreren Spalten.  
  > ***z. B.*** `SortByColumns(MyCollection, "Name", Ascending, "Age", Descending)` sortiert zuerst nach Name aufsteigend und dann nach Alter absteigend.
- `Filter()`: Filtert eine Sammlung nach einer Bedingung.  
  > ***z. B.*** `Filter(MyCollection, Age > 18)` gibt alle Objekte zurück, bei denen das Alter über 18 ist.

### **Suchen und Filtern**
- `LookUp()`: Sucht ein einzelnes Element in einer Sammlung, das eine bestimmte Bedingung erfüllt.  
  > ***z. B.*** `LookUp(MyCollection, Name = "Max")` gibt das Objekt mit Name "Max" zurück.
- `Search()`: Sucht nach einem Text in einer Sammlung.  
  > ***z. B.*** `Search(MyCollection, "Max", "Name")` gibt alle Objekte zurück, bei denen der Name "Max" enthält.
- `First()`, `Last()`: Gibt das erste oder letzte Element einer Sammlung zurück.  
  > ***z. B.*** `First(MyCollection)` gibt das erste Objekt in der Sammlung zurück, `Last(MyCollection)` das letzte.
- `FirstN()`, `LastN()`: Gibt die ersten oder letzten N Elemente einer Sammlung zurück.  
  > ***z. B.*** `FirstN(MyCollection, 3)` gibt die ersten 3 Objekte zurück, `LastN(MyCollection, 2)` die letzten 2.
- `Distinct()`: Gibt eine Sammlung von eindeutigen Werten aus einer bestimmten Spalte zurück.  
  > ***z. B.*** `Distinct(MyCollection, Name)` gibt eine Liste aller eindeutigen Namen in der Sammlung zurück.
- `StartsWith()`, `EndsWith()`: Überprüfen, ob ein Text mit einem bestimmten Präfix oder Suffix beginnt oder endet.  
  > ***z. B.*** `StartsWith("Hallo", "Ha")` gibt `true` zurück, `EndsWith("Hallo", "lo")` gibt ebenfalls `true` zurück.


## **2. Grundlagen des Einfügens von Elementen**

In diesem Kapitel werden die Grundlagen des Einfügens von Elementen in Powerapps erläutert, einschliesslich der Verwendung von Steuerelementen und deren Eigenschaften.

Damit man ein Element in Powerapps einfügen kann, muss man im Sharepoint das Element speichern. Für Powerapps ist Sharepoint eine Datenbank und dort wird alles gespeichert.

- Dafür gehst du auf der RC-CH-Workflow

![alt text](image.png)

- Bei der gelben Markierung findest du alle Sharepoint-Listen, die du für deine App verwenden kannst.  
  > ***z. B.*** `RC-CH.Workflow` ist eine Liste, in der du deine Workflows speichern kannst.

![alt text](image-1.png)

- Ganz rechts auf `Add Column` erstellt man eine Spalte nach Wunsch / Vorgabe. Danach wird dies gespeichert.

![alt text](image-2.png)

- Ganz wichtig: Auf der Powerapps-Seite musst du die Liste `refreshen`, da diese ergänzt wurde.

![alt text](image-3.png)

- Unter `Properties` &rarr; `Display` &rarr; `Edit fields` &rarr; `Add fields` findest du ein erstelltes Feld
- Wichtig zu beachten ist, dass du unter Data Source die richtige Sharepoint Liste anwählst und auf den Screen in die Form (Quadrat mit Violetter Umrandung) anklickst.

### **Gängige Feldtypen in PowerApps (basierend auf der Benutzeroberfläche)**

PowerApps bietet verschiedene Steuerelemente für due Dateneingabe und Navigation. Hier sind due wichtigsten Typen und ihre Anwendungen:

1. **`Textfelder`**
   - Einzeiliges Textfeld `TextInput`: Zum Eingeben kurzer Texte wie "Projektname" oder "Bestellnummer".
   - Mehrzeiliges Textfeld `TextArea`: Für längere Eingaben wie "Bemerkung zu Bestellung" oder "Notizen zum Kunden".

2. **`Auswahlfelder`**
   - Dropdown `DropDown` / Kombobox `ComboBox`: Ermöglicht die Auswahl einer Option aus einer Liste, <p>
   > ***z.B.*** "Lieferantentyp" oder "Status".

3. **`Datumauswahl`**
   - Date Picker `DatePicker`: Auswahl eines Datums, <p>
   > ***z.B.*** "Lieferdatum" oder "Projektstart"

4. **`Umschalter` für Ja/Nein-Entscheidungen**
   - Toggle `Toggle`: Schieberegler für Ein/Aus-Aktionen wie (Neuer Lieferant: `On/Off`)

5. **`Schaltflächen` für `Aktionen`**
   - Button `Button`: Führ eine aktion aus, <p>
   > ***z.B*** "Bestellung erfassen" oder "Dokument öffnen"

6. **`Navigation` und `Aktionsleisten`**
   - Diese Steuerelemente dienen dazu, die Benutzer durch die App zu führen oder zusätzlliche Funktionen bereizusellen:
     - `Navigationsleisten`: Ermöglichen den Wechsel zwischen verschiedenen Ansichten oder Seiten der App. <p> 
     > ***z.B.*** Eine leiste am oberen Bildschirmrand mit `Startseite`, `Bestellungen` und `Einstellungen`.
     - `Aktionsleiste`: Bieten Schnellzugriffe auf wichtige Funktionen. <p>
     > ***z.B*** Ein `+` Symbol zum Hinzufügen neuer Daten oder ein `Anhang-Button`zum hochladen von Dokumenten.

Diese Feldtypen sind essenziell für die Dateneingabe und Steuerung in PowerApps. Eine sinnvolle Platzierung und Verwendung verbessert die Benutzerfreundlichkeit erheblich.

## **3. Legende von Properties**

![img_18.png](img_18.png)

`Properties` bestimmen, **wie ein Element aussieht und funktioniert** also
> ***z.B.*** die Farbe, Grösse, Sichtbarkeit und Verhalten eines Steuerelements.

Damit legt man fest, **was der Nutzer sieht und wie er mit dem Element interagieren kann.**

In PowerApps gibt es **zwei Arten con eigenschaften**, die man einstellen kann:
- `Display` enthält die sichtbaren Grundeinstellungen <p></p>
> ***z.B.*** die Farbe, Grösse oder Sichtbakeit.
- `Advanced` zeigt **erweiterte Einstellungen** an:
> ***z.B.*** wie das Element auf Klicks reagiert oder mit Daten verbunden ist.

So kann man einfach steuern, **wie ein `Button` aussieht und wofür er zuständig ist** von einfach bis komplexen Funktionen.

### **Display-Eigenschaften**
- **`Text`**: Der Text, der im `Element` oder `Button` angezeigt wird.  
  > ***z. B.*** "Bestellung abschliessen"
- **`DisplayMode`**: Legt fest, ob das Element `Bearbeitbar`, `Nur-Lesen` oder `Deaktiviert` ist.  
  > ***z. B.*** `DisplayMode.Edit` für ein bearbeitbares Textfeld.
- **`Visible`**: Bestimmt, ob das Element sichtbar ist oder nicht.  
  > ***z. B.*** `true` für sichtbar, `false` für unsichtbar.
- `Position (X/Y)`: Legt die Position des Elements auf dem Bildschirm fest.  
  > ***z. B.*** `X = 100`, `Y = 200` für eine Position 100 Pixel von links und 200 Pixel von oben.
- **`Size (Width(Height)`**: Bestimmt die Grösse des Elements.  
  > ***z. B.*** `Width = 200`, `Height = 50` für eine Breite von 200 Pixeln und eine Höhe von 50 Pixeln.
- **`Padding`**: Fügt Abstand um das Element herum hinzu.  
  > ***z. B.*** `Padding = 10` für einen Abstand von 10 Pixeln auf allen Seiten.
  - **`Allignment`**: Legt die Ausrichtung des Textes im Element fest.  
  >   ***z. B.*** `Alignment = Center` für zentrierten Text. `Alignment = Left` für linksbündigen Text. `Alignment = Right` für rechtsbündigen Text. `Alignment = Justify` für Blocksatz. `Alignment = Top` für Text am oberen Rand. `Alignment = Bottom` für Text am unteren Rand.
- **`VerticalAlign`**: Bestimmt die vertikale Ausrichtung des Textes im Element.  
  > ***z. B.*** `VerticalAlign = Top` für Text am oberen Rand, `VerticalAlign = Bottom` für Text am unteren Rand.
- **`Font, FontSize, FontWeight`**: Legt die Schriftart, Schriftgrösse und Schriftstärke fest.  
  > ***z. B.*** `Font = "Arial"`, `FontSize = 14`, `FontWeight = Bold` für eine fette Schriftart in Arial mit einer Grösse von 14.
- **`Color`**: Bestimmt die Textfarbe des Elements.  
  > ***z. B.*** `Color = RGBA(0, 0, 0, 1)` für schwarzen Text.
  > [Color Enumeration](https://learn.microsoft.com/en-us/power-platform/power-fx/reference/function-colors)
- **`Fill`**: Legt die Hintergrundfarbe des Elements fest.  
  > ***z. B.*** `Fill = RGBA(255, 255, 255, 1)` für einen weissen Hintergrund.
- **`BorderColor` / `BorderThikness` / `Radius`**: Bestimmt die Farbe des Rahmens, die Dicke des Rahmens und die Eckenradien des Elements.  
  > ***z. B.*** `BorderColor = RGBA(0, 0, 0, 1)`, `BorderThickness = 2`, `Radius = 5` für einen schwarzen Rahmen mit einer Dicke von 2 Pixeln und abgerundeten Ecken von 5 Pixeln.
- **`HoverFill` / `PressedFill`/ `DisabledFill`**: Legt die Hintergrundfarbe des Elements fest, wenn der Mauszeiger darüber schwebt, wenn es gedrückt wird oder wenn es deaktiviert ist.  
  > ***z. B.*** `HoverFill = RGBA(200, 200, 200, 1)` für eine hellgraue Farbe beim Hover-Effekt. <p></p>
  > ***z. B.*** `PressedFill = RGBA(150, 150, 150, 1)` für eine dunklere Farbe beim Drücken des Elements.
  > ***z. B.*** `DisabledFill = RGBA(220, 220, 220, 1)` für eine hellere Farbe, wenn das Element deaktiviert ist.

### **Advanced-Eigenschaften**

