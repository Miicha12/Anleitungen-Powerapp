# **Workflow Tool Powerautomate für Coder**
## **Dokumentation**

### **Inhalt**

1. [Grundlagen Poweapps](#grundlagen-powerapps)
2. [Arbeiten mit Daten in Powerautomate](#arbeiten-mit-daten-in-powerautomate)


### **Grundlagen Powerapps**
In diesem Kapitel werden die relevantesten Funktionen von Powerapps und Powerautomate erklärt, die für die Entwicklung von Workflows und Automatisierungen in der Microsoft Power Platform verwendet werden.

#### **Grundfunktionen**

**`Condition`:**

<img src="img_55.png" alt="img_55.png" style="width:200px;"/>

Condition ist eine **Wenn-Bedingung**. Sie ermöglicht es, verschiedene Aktionen basierend auf bestimmten Bedingungen auszuführen.
> **z.B.** ìf()` in PowerApps.

Er bietet die Möglichkeit von zwei Pfaden, die ausgeführt werden, wenn die Bedingung erfüllt ist (True) oder nicht erfüllt ist (False).

**`Apply to each`:**

<img src="img_63.png" alt="img_63.png" style="width:200px;"/>

Apply to each ist eine **Schleife**, die es ermöglicht, eine Aktion für jedes Element in einer Sammlung auszuführen und diese auch zu wiederholen.

**`Initialize variable`:**

<img src="img_64.png" alt="img_64.png" style="width:200px;"/>

Initialize variable ist eine **Variable**, die in Power Automate verwendet wird, um Werte zu speichern und zu verwalten.
> **z.B.** `erstellt eine Variable mit dem Namen "myVariable" und dem Wert "Hello World"`.

**`Set variable`:**

<img src="img_65.png" alt="img_65.png" style="width:200px;"/>

Set variable ist eine **Variable**, die in Power Automate verwendet wird, um den Wert einer bereits initialisierten Variable zu ändern.
> **z.B.** `ändert den Wert der Variable "myVariable" auf "Goodbye World"`.

**`Append to array variable`:**

<img src="img_66.png" alt="img_66.png" style="width:200px;"/>

Append to array variable ist eine **Variable**, die in Power Automate verwendet wird, um einen Wert zu einem Array hinzuzufügen.
> **z.B.** `fügt den Wert "New Item" zum Array "myArray" hinzu`.

**`Send an email`:**

<img src="img_67.png" alt="img_67.png" style="width:200px;"/>

Send an E-Mail ist eine Aktion, die es ermöglicht, eine autmatische E-Mail zu senden.
> **z.B.** `sendet eine E-Mail an XY mit dem Betreff, dem Inhalt, den Variablen und den Anhängen`.

**`Get attachments`:**

<img src="img_68.png" alt="img_68.png" style="width:200px;"/>

Get atttachments ist eine Aktion, die es ermöglicht, Anhänge von einer Liste (**z.B von einem SharePoint-Element**) zu erhalten.

**`Get attachment content`:**

<img src="img_69.png" alt="img_69.png" style="width:200px;"/>

1. [ ] Get attachment content ist eine Aktion, die es ermöglicht, den Inhalt eines Anhangs zu erhalten.
> **z.B.** `erhält den Inhalt des Anhangs "myAttachment"`.

**`Respond to a PowerApp or flow`:**

<img src="img_70.png" alt="img_70.png" style="width:200px;"/>

Respond to a PowerApp or flow ist eine Aktion, die es ermöglicht, eine Antwort an eine PowerApp oder einen Flow zu senden.
> **z.B.** `sendet eine Antwort an die PowerApp mit dem Wert "Hello World"`.

**`Get items`:**

<img src="img_71.png" alt="img_71.png" style="width:200px;"/>

Get items ist eine Aktion, die es ermöglicht, Elemente und Datensetzte aus einer SharePoint-Liste zu erhalten.
> **z.B.** `erhält alle Elemente aus der SharePoint-Liste Bestellungen, Kunde, Aufgabe`.

**`Update item`:**

<img src="img_72.png" alt="img_72.png" style="width:200px;"/>

Update item ist eine Aktion, die es ermöglicht, ein Element in einer SharePoint-Liste zu aktualisieren.

**`Manually trigger a flow`:**

<img src="img_73.png" alt="img_73.png" style="width:200px;"/>

Manually trigger a flow ist eine Aktion, die es ermöglicht, einen Flow manuell auszulösen.
> **z.B.** `löst den Flow manuell aus, wenn der Button in PowerApps gedrückt wird`.

**`When a new email arrives`:**

<img src="img_74.png" alt="img_74.png" style="width:200px;"/>

When a new email arrives ist eine Aktion, die es ermöglicht, einen Flow auszulösen, wenn eine neue E-Mail eintrifft.

**`Recurrence`:**

<img src="img_75.png" alt="img_75.png" style="width:200px;"/>

Recurrence ist eine Aktion, die es ermöglicht, einen Flow in regelmäßigen Abständen auszuführen.
> **z.B.** `führt den Flow jeden Tag um 8 Uhr aus`.

<div style="page-break-before: always;"></div>

### **2. Arbeiten mit Daten in Powerautomate**

**Aktionen** sind vergefertigte Bausteine in Power Automate, die du per Klick in einen Flow einfügen kannst. Sie ermöglichen es dir, verschiedene Aufgaben auszuführen, wie z.B. das Senden von E-Mails, das Abrufen von Daten aus einer Datenbank oder das Aktualisieren von Datensätzen in einer SharePoint-Liste.

**Expressions** sind kleine Code-Funktionen, die innerhalb von Aktionen verwendet werden, um Werte zu berechnen, Daten zu Transformieren oder Bediengungen zu prüfen.
Sie beginnen immer mit einem `@`-Zeichen und werden direkt in Feldern der Aktionen geschrieben. Sie können in den meisten Aktionen verwendet werden, um dynamische Werte zu generieren oder zu verarbeiten.

**Wichtigste Aktionen und Expressions (kurz erklärt + Beispiel):**

**Aktionen (Low-Code):**

- `Filter Array`: Filtert ein Array basierend auf bestimmten Bedingungen.
  > **z.B.** `filtert alle Elemente, die größer als 10 sind`.
  > @equals(item()?['value'], 10)
  > @equals(item()?['status'], 'active')

- `Select`: Wählt bestimmte Eigenschaften aus einem Array aus.
  > **z.B.** `wählt nur die Eigenschaft "Name" aus jedem Element im Array aus`.
  > @item()?['Name']
  > ["Name": item()?['Kunde']]

- `Join`: Verbindet die Elemente eines Arrays zu einem String.
  > **z.B.** `verbindet die Elemente des Arrays mit einem Komma`.
  > @join(variables('myArray'), ', ')
  > @join(body('Filter_array')?['Kunde'], ', ')

- `Compose`: Erstellt eine neue Aktion, die einen Wert oder eine Berechnung enthält. Speichert oder formatiert Daten zwischendurch.
  > **z.B.** `erstellt eine Aktion, die den Wert "Hello World" enthält`.
  > @concat('Hello ', 'World')
  > @contact(item()?['Kunde'], '-', item()?['Auftrag'])

- `Create item`: Erstellt einen neuen Datenstatz in einer Datenquelle, z.B. in einer SharePoint-Liste.
  > **z.B.** `erstellt einen neuen Eintrag in der SharePoint-Liste "Bestellungen" mit den Werten "Kunde" und "Auftrag"`.
  > @item()?['Kunde']
  > @item()?['Auftrag']

- `Update item`: Aktualisiert einen bestehenden Datensatz in einer Datenquelle.
  > **z.B.** `aktualisiert den Eintrag in der SharePoint-Liste "Bestellungen" mit den Werten "Kunde" und "Auftrag"`.
  > @item()?['Kunde']
  > @item()?['Auftrag']

- `Delete item`: Löscht automatisch einen Datensatz aus einer Datenquelle.
  > **z.B.** `löscht den Eintrag in der SharePoint-Liste "Bestellungen" mit der ID 123`.
  > @item()?['ID']

- `Parse JSON`: Wandelt einen JSON-String in ein JSON-Objekt um, um auf die einzelnen Eigenschaften in Power Automate zugreifen zu können.
  > **z.B.** `wandelt den JSON-String '{"Name": "Max", "Alter": 30}' in ein JSON-Objekt um`.
  > @json('{"Name": "Max", "Alter": 30}')
  > body('Parse_JSON')?['Name'][Kunde']

**Expressions (Code):**

- `@equals()`: Vergleicht zwei Werte und gibt true oder false zurück.
  > **z.B.** `@equals(item()?['status'], 'active')` prüft, ob der Status eines Elements "active" ist.

- `@sort()`: Sortiert ein Array basierend auf einem bestimmten Kriterium.
  > **z.B.** `@sort(body('Filter_array')'Datum', 'asc')` sortiert die Elemente im Array "Datum" aufsteigend.

- `@union()`: Kombiniert zwei Arrays und entfernt Duplikate.
  > **z.B.** `@union(body('Liste1'), variables('Liste2'))` kombiniert die Arrays "Liste1" und "Liste2" und entfernt doppelte Einträge.

- `@join()`: Verbindet die Elemente eines Arrays zu einem String.
  > **z.B.** `@join(body('Filter_array')?['Kunde'], ', ')` verbindet die Werte des "Kunde"-Feldes im Array mit einem Komma.

- `@concat()`: Verbindet mehrere Strings zu einem neuen String.
  > **z.B.** `@concat('Bestellung ',item()?['ID'])` ergibt "Bestellung 123", wenn die ID 123 ist.

- `@length()`: Gibt die Länge eines Strings oder Arrays zurück.
  > **z.B.** `@length(body('Filter_array')?['Kunde'])` gibt die Anzahl der Elemente im "Kunde"-Array zurück.

- `@first()`: Gibt das erste Element eines Arrays zurück.
  > **z.B.** `@first(body('Filter_array')?['Kunde'])` gibt den ersten Kunden im Array zurück.

- `@last()`: Gibt das letzte Element eines Arrays zurück.
  > **z.B.** `@last(body('Filter_array')?['Kunde'])` gibt den letzten Kunden im Array zurück.

- `@addProperty()`: Fügt einem Objekt eine neue Eigenschaft hinzu.
  > **z.B.** `@addProperty(body('Filter_array'), 'Status', 'Aktiv')` fügt dem Objekt im Array die Eigenschaft "Status" mit dem Wert "Aktiv" hinzu.
  > **z.B.** `@addProperty(body('Objekt'), 'Summe', 100)` fügt dem Objekt die Eigenschaft "Summe" mit dem Wert 100 hinzu.

- `@addDays()`: Fügt einem Datum eine bestimmte Anzahl von Tagen hinzu.
  > **z.B.** `@addDays(utcNow(), 7)` gibt das Datum in 7 Tagen zurück.