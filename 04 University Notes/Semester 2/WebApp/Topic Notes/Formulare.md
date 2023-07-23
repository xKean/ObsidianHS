<u><center>**Ausdrücklich Teil der Klausur**</center></u>

### Definition
„Ein Webformular ist eine organisierte Sammlung von Elementen, die dem Anwender erlauben, Daten anzugeben, zu verändern, auszuwählen oder mit diesen zu interagieren.“


### Funktionen Webformular
↘Eingabe von Daten 
↘Veränderung von Daten 
↘Interaktion mit Webseite


↘Formulare sind für die Interaktion mit dem Benutzer essentiell 
↘Form-Element muss action und method definieren und ein Submit beinhalten 
↘Sinnvolle Beschreibung der Eingabemöglichkeiten



### Aufbau<u></u>


```html
<form action "/suchen" method = "get">
	<label for = "search" > Suchbegriff: </label>
	<input type = "text" id = "search" name = "searchVariableName" placeholder = "Suchtext" </input>
	<input type = "submit" value = "Finden">
</form>
```

### Mögliche Input-Types
```
<input type="button">
<input type="checkbox">
<input type="color">
<input type="date">
<input type="datetime-local">
<input type="email">
<input type="file">
<input type="hidden">
<input type="image">
<input type="month">
<input type="number">
<input type="password">
<input type="radio">
<input type="range">
<input type="reset">
<input type="search">
<input type="submit">
<input type="tel">
<input type="text">
<input type="time">
<input type="url">
<input type="week">
```


### Gegenstück in Routes
Zum Beispiel Oben:
![[Express Routes#Get]]


Für Post:

![[Express Routes#Post]]


### Get vs Post
- Get gibt Eingabeparameter in route / query mit
- Post nicht

![[Pasted image 20230723155437.png]]



### Additional Resources:
[HTML Input Types](https://www.w3schools.com/html/html_form_input_types.asp)
