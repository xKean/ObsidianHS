
#### Vorlesungsdurchskipping und wichtige Sachen rauschreibing

- [[Express Architektur]] (Generell Webserver Architektur)
- [[MVC]]
- [[Formulare|Formulare - AUSDRÜCKLICH TEIL DER KLAUSUR]]
- [[Ablauf Express Server Erstellen]]
- [[Express - Basic Knowledge]]
- [[Anpassung des Ports]]
- [[Installation Nodemon]]
- [[Request(req) und Response(res)]]
- [[Javascript]]
- [[Express Routes]]
- [[HTTP-Methoden]]
- [[JSON in Js]]
- [[Dateien lesen und schreiben in Node.js]]
- [[Middleware]]
- [[EJS und Templates]]
- [[REST (Representational State Transfer)]]
- [[HTTP Status Codes]]
- [[Web APIs und Fetch]]
- [[Synchron vs Asynchron]]



#### Wichtige  Sachen aus Übungen
Alles vor Übung 5 ist nur Bootstrap, HTML und CSS. Sollte also nichts dran kommen

- Übung 5
	- Hier wird ein Express Server erstellt mithilfe [[Ablauf Express Server Erstellen|der Anleitung aus der Vorlesung]]
	- Änderung des Titels: Wo kann man den Titel der Webapplikation ändern?
		- Bei der generierten Express-Anwendung gibt es nur einen view, der Standardmäßig gerendert wird. Der Titel wird auf der ejs-Seite folgendermaßen verarbeitet:  `<title><%= title %></title>`
		- Was heißt das?
			- Der Title wird in der Route als Parameter übergeben und kann in der index-Route angepasst werden.
			- ![[Pasted image 20230724103016.png]]
	- Wie kann man weitere Parameter an den View übergeben und anzeigen?
		- Übergeben
			- Der Parameter kann einfach an die Liste angehängt werden ![[Pasted image 20230724103301.png]]
		- Anzeigen
			- Der Parameter kann durch die EJS-Syntax wie auch der Titel auf der Seite gerendert werden![[Pasted image 20230724103429.png]]
	- Views untereinander verlinken / neue Seite anlegen
		- Route
			- Neue Route anlegen
			- ![[Pasted image 20230724104134.png]]
		- View und Verlinkung
			- ![[Pasted image 20230724104231.png]]
- Zusammenfassung Übung 5
	- Titel kann durch den Title-Tag auf der Seite verändert werden
	- Parameter können über den Router eingespielt werden und via EJS (`<%= title %>`) genutzt werden
	- Verlinkungen unter HTML Seiten via Router-Routen und `<a href="/route" </a>`


- Übung 6: Formulare
	- [[Formular mit Labels anlegen]]:
	- Neue (post)Route anlegen
	- Ausgabe von Benutzer eingegebenen Parametern durch `console.log(req.body.geburtstag);`

- Übung 7: Routing
	- Nutzung einer Wildcard (id) in query
		- `req.params.id`
	- Definition eines Objekts
	  ```js
	  let post = {
	    title: req.body.titel,
	    user: req.body.benutzername,
	    date: req.body.datum,
	    text: req.body.text,
	  };
	```
	- Anhängen eines Objekts an ein Array via `posts.push(post)`


  - Übung 8: MVC Model
	  - Nutzung von JSON als Filestorage mit `fs.readFileSync(dir)` und `fs.writeFileSync(dir, data)`
	  - Nutzung von Pfeilfunktionen
	  - Nutzung von IDs im Datenmodell zum finden von Daten unabhängig von Erstellungsreihenfolge
		  - `let post = blog.find((p) => p.id === parseInt(req.params.postid));`
		  - [[Unterschied zwischen == und ===]]
	  - Fileupload (nicht Klausurrelevant?!)
	  - ![[Pasted image 20230724200604.png]]