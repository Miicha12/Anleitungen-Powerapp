# **Workflow Tool Powerautomate für Coder**
## **Dokumentation**

### **Inhalt**

1. [Grundlagen Poweapps](#grundlagen-powerapps)


### **Grundlagen Powerapps**
In diesem Kapitel werden die relevantesten Funktionen von Powerapps und Powerautomate erklärt, die für die Entwicklung von Workflows und Automatisierungen in der Microsoft Power Platform verwendet werden.

#### **Grundfunktionen**

`Condition`:
![img_55.png](img_55.png)

Condition ist eine **Wenn-Bedingung**. Sie ermöglicht es, verschiedene Aktionen basierend auf bestimmten Bedingungen auszuführen.
> **z.B.** ìf()` in PowerApps.

Er bietet die Möglichkeit von zwei Pfaden, die ausgeführt werden, wenn die Bedingung erfüllt ist (True) oder nicht erfüllt ist (False).

`Apply to each`:
![img_63.png](img_63.png)

Apply to each ist eine **Schleife**, die es ermöglicht, eine Aktion für jedes Element in einer Sammlung auszuführen und diese auch zu wiederholen.

`Initialize variable`:
![img_64.png](img_64.png)

Initialize variable ist eine **Variable**, die in Power Automate verwendet wird, um Werte zu speichern und zu verwalten.
> **z.B.** `erstellt eine Variable mit dem Namen "myVariable" und dem Wert "Hello World"`.

`Set variable`:
![img_65.png](img_65.png)

Set variable ist eine **Variable**, die in Power Automate verwendet wird, um den Wert einer bereits initialisierten Variable zu ändern.
> **z.B.** `ändert den Wert der Variable "myVariable" auf "Goodbye World"`.

`Append to array variable`:
![img_66.png](img_66.png)

Append to array variable ist eine **Variable**, die in Power Automate verwendet wird, um einen Wert zu einem Array hinzuzufügen.
> **z.B.** `fügt den Wert "New Item" zum Array "myArray" hinzu`.

`Send an email`:
![img_67.png](img_67.png)

Send an E-Mail ist eine Aktion, die es ermöglicht, eine autmatische E-Mail zu senden.
> **z.B.** `sendet eine E-Mail an XY mit dem Betreff, dem Inhalt, den Variablen und den Anhängen`.

`Get attachments`:
![img_68.png](img_68.png)

Get atttachments ist eine Aktion, die es ermöglicht, Anhänge von einer Liste (**z.B von einem SharePoint-Element**) zu erhalten.
`Get attachment content`:
![img_69.png](img_69.png)

1. [ ] Get attachment content ist eine Aktion, die es ermöglicht, den Inhalt eines Anhangs zu erhalten.
> **z.B.** `erhält den Inhalt des Anhangs "myAttachment"`.

`Respond to a PowerApp or flow`:
![img_70.png](img_70.png)

Respond to a PowerApp or flow ist eine Aktion, die es ermöglicht, eine Antwort an eine PowerApp oder einen Flow zu senden.
> **z.B.** `sendet eine Antwort an die PowerApp mit dem Wert "Hello World"`.

`Get items`:
![img_71.png](img_71.png)

Get items ist eine Aktion, die es ermöglicht, Elemente und Datensetzte aus einer SharePoint-Liste zu erhalten.
> **z.B.** `erhält alle Elemente aus der SharePoint-Liste Bestellungen, Kunde, Aufgabe`.

`Update item`:
![img_72.png](img_72.png)

Update item ist eine Aktion, die es ermöglicht, ein Element in einer SharePoint-Liste zu aktualisieren.

`Manually trigger a flow`:
![img_73.png](img_73.png)

Manually trigger a flow ist eine Aktion, die es ermöglicht, einen Flow manuell auszulösen.
> **z.B.** `löst den Flow manuell aus, wenn der Button in PowerApps gedrückt wird`.

`When a new email arrives`:
![img_74.png](img_74.png)

When a new email arrives ist eine Aktion, die es ermöglicht, einen Flow auszulösen, wenn eine neue E-Mail eintrifft.

`Recurrence`:
![img_75.png](img_75.png)

Recurrence ist eine Aktion, die es ermöglicht, einen Flow in regelmäßigen Abständen auszuführen.
> **z.B.** `führt den Flow jeden Tag um 8 Uhr aus`.

