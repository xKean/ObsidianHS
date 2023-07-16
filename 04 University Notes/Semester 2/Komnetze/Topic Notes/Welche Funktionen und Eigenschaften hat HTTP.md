- Unterstützung der Applikationen: Web Browser, Web-Server
- Abruf & Verwendung von Web-Seiten/ -Anwendungen
	- Gerüst der Webseite in HyperText Markup Language (HTML)
	- Adressierung/ Verlinkung aller Inhalte: Uniform Resource Locator (URL)
	- **Hyper Media** --> mehrere Medien
	- **HyperText** --> Links
	
- HTTP ist standardisiert in RFC9114 (ich denke nicht, dass wir hier wissen müssen welches RFC, wofür auch immer das steht.)
	- HTTP/2
	- HTTP/3
	- HTTP/1.1
	
- Neben OSI Schicht 7 umfasst HTTP auch Aufgaben der OSI Schicht 6
	- Layer 6: Presentation Layer: Content-Type (Image, Text, HTML), Content Language
	- Layer 5: Session Layer: Cookies, [[persistente]] (TCP-)Verbindungen, ...
	
- HTTP Methoden:
	- GET
		- Abruf von Web-Seiten bzw. -Ressourcen
		- Übergabe von Parametern in URL z.B.: hhtp://www.hs-fulda.de/index.php **?id=182** 
		- also ab ? ist Parameter, aber ich denke ihr Brains habt das auch ohne diese überflüssige Klammer schon geschnallt, naja - je voller die Seite desto besser fühle ich mich weil ich ja was arbeite, Gaslighting ist also nicht nur Moritz's Hobby)
	- POST
		- Übertragung von Daten an den Web-Server (z.B. Formulare)
	- PUT
		- Hochladen von Ressourcen (Dateien) auf den Web-Server
	- DELETE
		- Löschen von Dateien auf dem Web-Server
