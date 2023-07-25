### Definition
Middleware ist ein ( lose definierter) Begriff für jede Software oder Service, die es den Teilen eines
Systems ermöglicht, miteinander zu kommunizieren und Daten zu verwalten. Es ist die Software, die
die Kommunikation zwischen den Komponenten und die Ein- und Ausgabe handhabt, so dass sich
die Entwickler auf den spezifischen Zweck ihrer Anwendung konzentrieren können.
In server-seitigen Webanwendungs-Frameworks wird der Begriff oft spezifischer verwendet, um sich
auf vorgefertigte Softwarekomponenten zu beziehen, die der Anfrage/Antwort-
Verarbeitungspipeline des Frameworks hinzugefügt werden können, um Aufgaben wie den
Datenbankzugriff zu erledigen.

### Warum benutzt man middleware?
- Meistens vorgefertigte Softwarekomponenten 
- Können einfach dem Projekt hinzugefügt werden 
- Erweitern die Funktionalität der Anwendung 
- Ermöglichen Fokussierung auf die eigentliche Anwendung
- Middleware erweitert die Funktionalität von Software indem es (meist vorgefertigte) zusätzliche Komponenten einbindet.


### Wichtige Syntax
- Es ist wichtig, dass die Middlewarefunktion mit `next();` endet.!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

### Beispiel Logging

![[Pasted image 20230723161942.png]]
![[Pasted image 20230723161949.png]]



### Beispiel nutzung Middleware in der Route

![[Pasted image 20230723164106.png]]

oder

```js
// Einfache Middleware-Funktion
const simpleLoggerMiddleware = (req, res, next) => {
  console.log(`Anfrage an ${req.method} ${req.url} von ${req.ip}`);
  next(); // Die next()-Funktion wird aufgerufen, um die Kontrolle an die nächste Middleware oder Route zu übergeben
};

// Beispielroute mit Middleware
app.get('/example', simpleLoggerMiddleware, (req, res) => {
  res.send('Hallo, dies ist eine Beispielroute!');
});
```


### Nutzung der Middleware für alle zukünftigen routen ab Erstellung
```js
// Einfache Middleware-Funktion
const simpleLoggerMiddleware = (req, res, next) => {
  console.log(`Anfrage an ${req.method} ${req.url} von ${req.ip}`);
  next(); // Die next()-Funktion wird aufgerufen, um die Kontrolle an die nächste Middleware oder Route zu übergeben
};

// Middleware der Express-App hinzufügen (bevor die Routen definiert werden)
app.use(simpleLoggerMiddleware);

// Beispielroute
app.get('/', (req, res) => {
  res.send('Hallo, dies ist eine Beispielroute!');
});
```


### Nutzung von Middleware die nicht zentral definiert wurde

```js
function isAuthenticated(req, res, next) {
  // Ein einfaches Beispiel, wie Sie prüfen könnten, ob ein Benutzer authentifiziert ist
  if (req.isAuthenticated()) {  // 'isAuthenticated' könnte eine Funktion sein, die Sie definieren, oder von einem Modul wie 'passport' stammen
    next(); // Wenn der Benutzer authentifiziert ist, rufen Sie die nächste Middleware-Funktion in der Kette auf.
  } else {
    res.status(403).send("Nicht autorisiert"); // Wenn der Benutzer nicht authentifiziert ist, senden Sie eine 403-Antwort.
  }
}

router
  .route("/")
  .get(isAuthenticated, blogController.getAllPosts) // Hier fügen Sie 'isAuthenticated' als Middleware vor 'getAllPosts' hinzu
  .post(blogController.createPost);

```
