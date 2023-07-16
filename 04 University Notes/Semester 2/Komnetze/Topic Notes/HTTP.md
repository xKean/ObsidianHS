Das Hypertext Transfer Protocol (HTTP) lässt Clients mit Web-Browsern über das [[Konzept des Internets|Internet]] mit Web-Servern kommunizieren und somit Daten abrufen und Services nutzen.

### Nutzung
Abruf von Webseiten und den Ressourcen (Bilder, Text etc.). Nutzt Port 80.
Wird nicht nur auf Schicht 7, sondern auch 5 und 6 genutzt.
- Layer 6: Presentation Layer: Content-Type (Image, Text, HTML), Content-Language
- Layer 5: Session Layer: Cookies, persistente (TCP-)Verbindungen

Layer 7: Abruf mit Get / actual Anzeige
Layer 6: Wie wird es angezeigt?
Layer 5: Verbindung aktiv halten, Cookies


### Versionen
- HTTP 1.1 (1999)
- HTTP 2 (2015)
- HTTP 3 (2022)
	- Header Kompression
	- Parallele Streams
	- UDP als Transportprotokoll mit QUIC

### Aufbau
- Request Header
	- ![[Pasted image 20230716154611.png]]
	- HTTP Methode
	- HTTP Version
	- HTTP Header (Browser, Browserversion, Sprache, Host, )
- Response
	- ![[Pasted image 20230716154623.png]]
	- HTTP Status
	- Server Info
	- Cookie Info

