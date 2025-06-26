# Workflow Tool Powerapps und Powerautomate für Coder
## Dokumentation

## Inhalt:
1. Grundlagen Powerapps
2. Grundlagen des Einfpgens von Elementen


## 1. Grundlagen Powerapps

In diesem Kapitel werden die relevantesten Funktionen erläutert, die für die Entwicklung von Apps in Powerapps erforderlich sind.

### Grundfunktionen

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

### Textfunktionen
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

### Mathematikfunktionen
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

### Logikfunktionen
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

### Datum- und Zeitfunktionen
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

### Listen und Daten
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

### Suchen und Filtern
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


## 2. Grundlagen des Einfügens von Elementen

In diesem Kapitel werden die Grundlagen des Einfügens von Elementen in Powerapps erläutert, einschließlich der Verwendung von Steuerelementen und deren Eigenschaften.

Damit man eine Element in Powerapps einfügen kann, muss man im Sharepoint das Element speichern. Für Powerapps ist Sharepoint eine Datenbank und dort wird alles gespeichert.

- Dafür gehst du auf der RC-CH.Workflow

![Sharepoint-bild-1.png](src/main/recources/graphic/Sharepoint-bild-1.png)

- Bei der gelben Markierung findest du alle Sharepoint-Listen, die du für deine App verwenden kannst.  
  > ***z. B.*** `RC-CH.Workflow` ist eine Liste, in der du deine Workflows speichern kannst.
  > 
> 
> 
> 
> 