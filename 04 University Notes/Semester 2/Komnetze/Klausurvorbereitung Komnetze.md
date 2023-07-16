## Guidelines für die Seite:
- Oberen Links führen jeweils zur ausführlichen Wiederholungsfragen, i.d.R. >30 in der Anzahl
- Unten sind die wenigen Lernzielfragen der einzelnen Kapitel angefügt, die vermutlich 90% der Klausur fast sein werden, so wie ich ihn einschätze (Jan)

Kapitel der Vorlesung und Wiederholungsfragen:

1. [[Grundlagen von Kommunikationsnetzen]]
2. [[Anwendungsschicht]]
3. [[Transportschicht]]
4. [[Vermittlungsschicht]]
5. [[Sicherungsschicht]]



## Lernziele Kapitel 1: [[Grundlagen von Kommunikationsnetzen]]

###### Was ist ein [[Kommunikationsnetz]]?

Ein Kommunikationsnetz besteht aus Vermittlern, Endsystemen und Verbindungsstrecken.
Eine Anwendung am Endsystem nutzt das Kommunikationsnetz zur Nachrichtenübertragung.

###### Was ist ein [[Kommunikationsprotokoll]]?

Ein Kommunikationsprotokoll definiert einen festen Ablauf und festen Rahmen für die Kommunikation zwischen Endsystemen. Damit lässt sich eine einheitliche Interpretation übermittelter Nachrichten oder Daten sicherstellen.

- Protokolle bilden in der Regel internationale Standards.
- Jedes Protokoll kümmert sich möglichst nur um seine Aufgabe.


###### Grundlegende Systeme, Aufbau Netzzugang (Edge) und Netzkern (Core)
- Was ist der [[Netzzugang Edge]] und welche Aufgaben erfüllt er? Welchen Aufbau hat er?
	- Der Edge-Bereich bezeichnet den Bereich im Internet, in dem Endgeräte (Konsument ODER Data Center) angeschlossen werden.
	- ![[Netzzugang Edge#Aufbau]]
- Was ist der [[Netzkern Core]] und welche Aufgaben erfüllt er? Welchen Aufbau hat er?
	- ![[Netzkern Core]]
- Welche Lösungen gibt es für den **Internetzugang** in Heimnetzen?
	- [[DSL]]
	- [[Glasfaser]]
	- [[Kabel (Coaxial)]]
- Welche Komponenten werden in Heimnetzen benutzt?
	- [[Wlan-Router]]
	- [[Switch]] (vielleicht!)
	- [[Access Point]]
	- [[Was ist ein Repeater |Repeater]]
- Welche Komponenten kommen in Unternehmensnetzen hinzu?
	- Verwendung mehrerer [[Switch|Switches]] um Netz über mehrere Gebäude / Abteilungen aufzuteilen.
	- [[Server]]
	- (Redundante) [[Router]] für Internetzugang über [[ISP]]
- Welche [[Übertagungsmedien]] kennen Sie?
	- Leitungsgebundene Medien
		- [[Kupferkabel]]
		- [[Glasfaserkabel]]
		- [[Coaxialkabel]]
	- Leitungsungebundene Medien
		- Funk / Mobilfunk - [[LTE]] / [[5G]] / EDGE
		- [[WLAN]]
		- Radiowellen
		- Satelliten (GPS / Richtfunk / StarLink)
- Was bedeutet Paketvermittlung? Welche Vor- und Nachteile hat sie?
	- Paketvermittlung:
		- ![[Pasted image 20230716142839.png]]
- Was bedeutet [[WAN]], [[LAN]], [[MAN]] und wozu braucht man [[VPN]]?
	- LAN
		- ![[LAN#Definition]]
	- WAN
		- ![[WAN#Definition]]
	- MAN
		- ![[MAN#Definition]]
	- VPN
		- ![[VPN#Warum nutzt man VPN?]]
		- ![[VPN#Use-Cases]]
- Welche [[Netztopologien]] kennen Sie?
	- Stern
	- Ring
	- Linear
	- Tree
	- Mesh
	- Bus
- Woraus setzt sich das [[Internet]] zusammen?
	- Aus Netzen.
- Was sind [[Anforderungen an Computernetzwerke]] heutzutage?
	- ![[Anforderungen an Computernetzwerke]]
-  [[Schichtenmodell für Protokolle und Dienste]]  (Referenzmodelle)
	- Welche Schichtenmodelle kennen Sie?
	- ![[Schichtenmodell für Protokolle und Dienste]]
	- Was sind [[Header]] und was ist deren Inhalt?
	- Quell- und Zieladressen, für die Aufgaben der Schicht erforderliche Informationen
- Welche Standardisierungsgremien haben Einfluss auf Computernetzwerke?
	- IEEE
	- IETF
	- ITU-T
	- ETSI



## Lernziele Kapitel 2: [[Anwendungsschicht]]

- Konzept und Implementierung von [[Internetanwendungsprotokollen]]
- Welche Arten von [[Internetanwendungsprotokollen]] gibt es?
	- Verbindungslose Protokolle
	- Verbindungsorientierte Protokolle
	- Gemischte Protokolle
- [[Client-Server-Anwendungen]] vs [[Peer-to-Peer]]
- [[Servicemodelle]] und Anforderungen
- Was ist ein [[Socket]]?
	- Steckdose, die eindeutig identifiziert, welches Gerät und welcher Prozess es ist.
	- IP+Port
- Welche Anforderungen werden an ein [[Internetanwendungsprotokollen|Anwendungsprotokoll]] gestellt?
	- Paketverlust
	- Durchsatz
	- Delay
	- Verlässlichkeit
	- Sicherheit
- Welche Funktionen und Eigenschaften hat [[HTTP]]? 
	- Welchen groben Aufbau haben HTTP Requests und Responses? 
		- ![[HTTP#Aufbau]]
	- Wie können trotz Zustandslosigkeit von HTTP Sitzungen realisiert werden? 
		- Setzen von Cookies (Wird in Headern mitgegeben)
		- Problem: Datenschutz, Sicherheit
	- Welche Vorteile bietet HTTP/3 im Vergleich zu HTTP/1.1? 
		- Header Kompression
		- Parallele Streams
		- UDP als Transportprotokoll mit QUIC
	- Wie kann darüber hinaus die Antwortzeit beim Zugriff auf Web-Seiten bzw. Web-Anwendungen weiter reduziert werden?
		- Browser Cache
		- [[CDN]]
- Wie unterstützt [[DNS]] die Verwendung von Internetanwendungen? 
	- Keiner kann sich ne IP merken, ne Webadresse schon.
	- Wie ist der [[DNS]] Namensraum strukturiert? Was unterscheidet eine [[Domain]] von einer [[Zone]]?
		- Struktur:
			- Ist von rechts nach links zu lesen. (.de, .hs-fulda, informatik)
			- informatik.hs-fulda.de
			- Top Level Domain 
			- Second Level Domain
			- Subdomain
		- Unterschied [[Domain]] - [[Zone]]
			- Domain ist bspw. eine Spezifische Webseitenadresse: hs-fulda.de
			- Zone ist ein Bereich, in dem Domains liegen können.
			- Jede Zone hat einen Nameserver.
	- Wie wird die Ausfallsicherheit und Lastverteilung bei DNS realisiert?
		- Wird als verteilte hierarchische Datenbank realisiert.
		- 13 Rootserver mit vielen Kopien, Weiterleitungen und alternativen Wegen
	- Welche Resource Record Typen kennen Sie? 
		- A (Adress-Record)
		- AAAA(Adress-Record IPV6)
		- CNAME (Alias)
		- MX (MailExchange Server)
		- NS (NameServer)
		- PTR (Pointer, Reverse-Lookup)
	- Wie erfolgt eine rekursive Query?
		- Absetzen der Anfrage, erhalten der vollständigen Antwort
		- Kontrast zur iterativen Query (normal): Man sucht sich selbst den Weg durch viele Anfragen hintereinander
- Wie können Rechner automatisiert mit [[DHCP]] für die Verwendung von TCP/IP Netzen konfiguriert werden? 
	- ![[DHCP#Vorgehen]]


## Lernziele Kapitel 3: [[Transportschicht]]

- Aufgaben und Funktion der [[Transportschicht]]
- Eigenschaften von [[TCP]] und [[UDP]]
- Performance und Sicherheit auf der Transportschicht bewerten können
- Welche Aufgaben haben [[Verbindungslose Transportprotkolle]]?
- Welche Aufgaben haben [[Verbindungsorientierte Transportprotokolle]]?
- Wie wird bei [[TCP]] die Fehler-, Fluss- und Staukontrolle realisiert? 
- Welche aktuellen Performance- und Sicherheitsherausforderungen stellen sich für [[TCP]]/[[UDP]]?




## Lernziele Kapitel 5: [[Sicherungsschicht]] / Netzzugriff