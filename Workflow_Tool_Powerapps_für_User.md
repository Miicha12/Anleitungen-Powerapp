# **Workflow Tool Powerapps für User**
## **Dokumentation**

## Inhalt:

1. Zweck
2. Legende
3. StartScreen
4. Home-Screen
5. Auftrag-Screen
6. Signierung-Screen
7. Bemerkung-Screen
8. Materialbestellung-Screen
9. Archiv-Screen
10. Archivauftrag-Screen
11. Archivmaterialbestellung-Screen

### 1. Zweck

Powerapps ist ein Tool von Microsoft, welches verwendet wird um Inhouse-Tools bzw. Softwares zu erstellen. <p> Dafür braucht man keine umfangreiche Programmierkenntnisse und kann die Software benutzerdefiniert erstellen.

Die Siemens-Energy AG nutzt PowerApps für ihren Bestellworkflow. Dort kann jeder Mitarbeiter Bestellungen erfassen. Die Werkstudenten sind für das Codieren der Seite zuständig und ist immer in Austausche mit den Admins der App.

### 2. Legende

![img_7.png](img_7.png)

Anhand von der Legende kann man die verschiedenen Icons und deren Bedeutung erkennen. <p> Diese Icons sind auf den verschiedenen Screens zu finden und helfen bei der Navigation.

![img_16.png](img_16.png)

Erklärung:

- `WF angelegt`: Noch nicht zur Auftragserfassung gesendet
- `WF zur Bearbeitung`: In der Auftragserfassung
- `AEB gesendet`: Kundenauftrag im SAP angelegt
- `AB gesendet`: Lieferterminbestätigung erhalten
- `Abgeschlossen`: Fakturadatum erreicht, Weiterleitung zur Verrechnung
- `Faturierung`: Beim CPM zur Verrechnung
- `Archivierung`: Verrechnet, bereit zur Archivierung

![img_17.png](img_17.png)

Erklärung:

- `Materialbestellung angelegt`: Noch nicht zur Auftragserfassung gesendet
- `Workflow zur Bearbeitung`: In der Auftragserfassung
- `Bestellung angelegt`: Noch nicht an den Lieferanten gesendet
- `Bestellung an den Lieferanten gesendet`
- `Lieferantenbestätigung erhalten`: Lieferantenreferenz, Liefertermin

### 3. StartScreen

![img.png](img.png)

Im `Start-Screen` kann man sich zu folgenden Pages navigieren lassen:

- `Neuen Auftrag erfassen`: Hier gelangt man zum Auftrag-Screen
- `Übersicht`: Hier gelangt man zum Home-Screen
- `Archiv`: Hier gelangt man zum Archiv-Screen
- Mit den `Pfeiltasten` am Unteren Rand kann man sich durch einen kleinen Tutorial navigieren, der die wichtigsten Funktionen erklärt.

### 4. Home-Screen

![img_8.png](img_8.png)

Im `Home-Screen` sind alle Bestellungen ersichtlich. Durch die Filter Funktion kann man gezielt nach einem Auftrag suchen. <p> Durch die `+` - Taste kann man auch einen neuen Auftrag erfassen.

![img_2.png](img_2.png)

Auf diesen Screen kann man die vorhandenen Materialbestellungen, Transporte und auch Bemerkungen einsehen oder auch erstellen. <p> Dafür muss man in der jeweiligen Liste auf das Kreuz klicken und man gelangt in der entsprechende Seite.

### 5. Auftrag-Screen

![img_9.png](img_9.png)

Im `Auftrag-Screen` kann man einen neuen Auftrag erfassen. <p> Wichtig dabei ist, dass man hier die Felder mit den `*` markiert ausfüllen muss, damit der Auftrag auch gespeichert werden kann. <p> Sobald dieser gespeichert wurde, wird er im `Home-Screen` angezeigt und kann dort auch bearbeitet werden.

![img_4.png](img_4.png)
![img_1.png](img_1.png)

In diesem Screen sieht man ein Beispielauftrag, welcher bereits erfasst wurde und auch signiert ist. Ist das Faktura Plandatum erreicht wird eine Automatische E-Mail an den PM gesendet damit abgeklärt wird ob der Auftrag verrechnet werden kann. <p> Ist der Auftrag abgeschlossen kann der PM über den `Auftrag verrechnen`-Button den Auftrag abschliessen. <p> Der Auftrag wird dann im `Archiv-Screen` angezeigt und kann dort auch nicht mehr bearbeitet werden. <p> Sollte der Auftrag bis zum Faktura Plandatum nicht abgeschlossen sein, kann das Datum in die Zukunft verschoben werden und das Prozedere beginnt von vorne.

### 6. Signierung-Screen

![img_10.png](img_10.png)

Der `Signierung-Screen` ist dafür da, ein Projekt zu Unterschreiben und diesen als freigegeben zu deklarieren.


### 7. Bemerkung-Screen

![img_5.png](img_5.png)

Im `Bemerkung-Screen` werden die Bemerkungen zu einem Auftrag erfasst. <p> Zusätzlich kann man auch die dazugehörigen Anhänge mitversenden. Sobald die Bemerkung gespeichert wird, wird sie im `Home-Screen` angezeigt.

![img_11.png](img_11.png)

Auf diesem Screen sieht man wie es aussieht, wenn eine Bemerkung bereits erfasst wurde.

### 8. Materialbestellung-Screen

![img_12.png](img_12.png)

Im `Materialbestellung-Screen` werden die Bestellungen erfasst. Man trägt die Daten ein sowie auch die Termine wie beispielsweise `Lieferbestätigung bis` oder `PO Datum`. Damit hat man Deadlines. Ebenfalls kann man Anhänge oder Bemerkungen  hinzufügen <Bei Bemerkung erfasst man diese im `Bemerkung-Screen`>

### 9. Archiv-Screen

![img_13.png](img_13.png)

Im `Archiv-Screen` sieht man alle archivierten Bestellungen. Man kann in die einzelnen bestellungen auch klicken, jedoch sind diese unveränderbar, da sie schon abgeschlossen sind.

### 10. Archivauftrag-Screen

![img_14.png](img_14.png)

Der `Archivauftrag-Screen` ist dem `Archiv-Screen` unterstellt. Dieser zeigt den `Auftrag-Screen` des abgeschlossenen Auftrags vom `Archiv-Screen`.

### 11. Archivmaterialbestellung-Screen

![img_15.png](img_15.png)

Der `Archivmaterialbestellung-Screen` ist dem `Archiv-Screen` unterstellt. Dieser zeigt den `Materialbestellung-Screen` des abgeschlossenen Auftrags vom `Archiv-Screen`.


