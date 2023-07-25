![[Pasted image 20230723160921.png]]

### Definition

Das Model-View-Controller (MVC)-Muster ist ein architektonisches Entwurfsmuster, das verwendet wird, um die Struktur von Softwareanwendungen zu organisieren. Es wurde entwickelt, um die Trennung der Geschäftslogik (Model), der Benutzeroberfläche (View) und der Benutzerinteraktion (Controller) zu fördern.

Model (Modell): Das Modell repräsentiert die Geschäftslogik und die Daten der Anwendung. Es enthält die Datenstrukturen und die Regeln, die auf die Daten angewendet werden. Das Modell ist unabhängig von der Benutzeroberfläche und der Interaktion.

View (Ansicht): Die View ist für die Darstellung der Daten verantwortlich, die vom Modell bereitgestellt werden. Es handelt sich um die Benutzeroberfläche der Anwendung. Die View zeigt die Daten dem Benutzer an und ist normalerweise passiv, da sie keine Geschäftslogik enthalten soll.

Controller (Steuerung): Der Controller verarbeitet die Benutzerinteraktionen und aktualisiert das Modell entsprechend. Er ist für die Entgegennahme von Benutzereingaben zuständig, wie beispielsweise Klicks oder Tastatureingaben, und leitet die entsprechenden Anweisungen an das Modell weiter. Der Controller aktualisiert auch die View, wenn sich der Zustand des Modells ändert, damit die Benutzeroberfläche korrekt aktualisiert wird.

Der Hauptvorteil von MVC besteht darin, dass es die Anwendung in drei unabhängige Komponenten aufteilt, was die Wartung und Erweiterung erleichtert. Es ermöglicht auch eine klare Trennung der Zuständigkeiten, was die Code-Qualität und die Wiederverwendbarkeit verbessert.

MVC ist weit verbreitet und wird in vielen Frameworks und Technologien verwendet, wie beispielsweise in der Webentwicklung (z. B. ASP.NET MVC, Ruby on Rails), der Desktop-Entwicklung und mobilen Anwendungen.

### Vorteile
Model-View-Controller erhöht die Wiederverwendbarkeit von Software
- Trennung von M/V/C
- 

### 3 Bestandteile:
[[MVC Model]]
[[MVC Controller]]
[[MVC View]]


### Struktur
Ordner mit Controllern, Model, Routen

![[Pasted image 20230723161517.png]]

### Funktionsweise
- Routen binden Controller ein und leiten Anfragen an diesen weiter
- Model enthält Daten 
- View enthält Darstellung