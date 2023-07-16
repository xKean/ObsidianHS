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

- Welche Protokolle realisieren die Transportschicht in TCP/IP-Netzen?
	- [[TCP]] (Verbindungsorientiert Transmission Control Protocol) und [[UDP]] (Verbindungslos User Datagram Protocol)
- Wie unterscheiden sich logische Verbindungen auf der Transport- und auf der Vermittlungsschicht?
	- Vermittlungsprotokolle werden über viele Layer3-Vermittler ausgeführt und regelt die Wegewahl für logische Verbindung der Endsysteme
	- Transportprotokolle werden auf den Endsystemen ausgeführt
		- Quell-Socket teilt Nachrichten in Segmente/Datagramme auf und gibt diese an Vermittlungsschicht weiter
		- Ziel-Socket fügt die Segmente/Datagramme wieder zusammen und gibt Nachricht an Anwendung weiter
	- ![[Pasted image 20230716171624.png]]	
- Welche Unterschiede weisen verbindungslose und verbindungsorientierte Transportprotokolle auf?
	- Die Verbindung xDXDXDXDXD
	- Verbindungsorientierte Protokolle gewährleisten:
		- Zuverlässigkeit des Datentransports:
			- Aufbau einer virtuellen Verbindung
		- Fehlerkontrolle (Flow Control)
		- Staukontrolle (Congestion Control)
- Wie hängen Segmentierung, Multiplexing und Demultiplexing auf der Transportschicht mit der Anwendungsschicht zusammen?
	- Anwendungen laufen in unterschiedlichen Prozessen des Betriebssystems: IP-Adresse (Layer 3) + Port (Layer 4) des Endsystems = Endpunktadresse / Socket des Prozesses
- Was wird durch Transportprotokolle definiert?
	- Multiplexing und Segmentierung von Daten mehrerer Anwendungsprozesse
	- Nachrichtensemantik und - syntax
	- Zuverlässigkeit des Datentransports (Verbindungsaufbau, Gewährleistung des korrekten Reihenfolge der Segmente, Berücksichtigung maximaler Segmentgrößen, KEINE Garantien für Delay, Bitrate)
	- Flusskontrolle (Flow Control)
	- Staukontrolle (Congestion Control)
- Wofür werden „well-known“ und „dynamic ports“ verwendet?
	- "well known ports" von IANA fest vergeben(<1024): 80 für HTTP, 53 für DNS, 443 HTTPS etc.
	- "user ports": 1024-49151, für alle Benutzer frei verwendbar, Registrierung bei IANA möglich
	- "private / dynamic ports": 49152-65535, frei verwendbar
- Welche Aufgaben hat [[UDP]]?
	- Der Empfang der Nachricht wird nicht bestätigt!
	- ![[UDP#Aufgaben]]
	- Wie werden Sockets bei UDP verwendet?
		- ![[UDP#Sockets]]
	- Welche Funktion haben Source und Destination Port im UDP-Header?
		- Quell- und Zielport werden da angegeben
		- ![[UDP#Header]]
	- Welche Vorteile hat UDP gegenüber TCP?
		- ![[UDP#Vorteile]]
- Welche Aufgaben hat [[TCP]]?
	- ![[TCP#Aufgaben]]
	- Wie werden Sockets bei TCP verwendet?
		- ![[TCP#Sockets]]
	- Wie erfolgt der Verbindungsauf- und -abbau bei TCP?
		- ![[TCP#Verbindungsablauf]]
	- Wie kann ein Web-Server eingehende Pakete den richtigen Prozessen zuordnen?
		- Durch Quell-IP und Quell-Port![[Pasted image 20230716174822.png]]
	- Welche Aufgabe haben Source/Destination Port, Sequence/Acknowledgement Number, Window und die Control Flags im TCP-Header?
		- ![[TCP#Header]]
	- Warum ist bei TCP ein Pipelining von Segmenten erforderlich?
		- Sonst pain, weil lange
		- ![[TCP#Pipelining]]
	- Was bedeutet Sliding Window bei TCP in Bezug auf Fehler- und Flusskontrolle?
		- ![[TCP#Flusskontrolle]]
	- Woran orientiert sich der Timeout für die Übertragung von TCP-Segmenten?
		- ![[TCP#Timeout]]
	- Welche Bedeutung haben Triple Duplicate ACKs bei TCP?
		- ![[TCP#TripleDuplicate]]
	- Was bedeuten Slow Start, AIMD und „fast recovery“ für die Staukontrolle bei TCP?
		- ![[TCP#Staukontrolle]]
	- Performance-Erweiterung?
		- ![[TCP#PerformanceImprovements]]
- Weitere Verbesserungen für TCP?
	- Congestion Control weiter verbessern: Erweiterungen für Unterscheidung von Paketverlust durch Timeout und Paketverlust durch Bitfehler (z.B. im WLAN)
	- Multipath TCP -> mehrere Verbindungen über eine Link Layer Verbindungen oder mehrere: parallele Übertragungspfade
	- Jumbo Pakete?
- Welche Aufgabe hat [[TLS]] und wie wird die Sicherheit hierbei realisiert?
	- Anforderungen an Netzsicherheit: 
		- Vertraulichkeit (Abhörsicherheit - Verschlüsslung)
		- Integrität (Übertragungssicherheit -> keine Manipulation, Hash)
		- Verbindlichkeit (digitale Signaturen - ist wirklich von dem und dem)
		- Authentizität (Identitätsprüfung -> Passwort, Zertifikate)
		- Verfügbarkeit (Unterbrechungsfrei -> Firewall, Intrusion Detection)
	- Sicherheit auf Transportschicht!
	- ![[TLS#Aufgaben]]
- Welche Vorteile und Funktionen bietet [[QUIC]] für HTTP/3?
	- ![[QUIC]]


## Lernziele Kapitel 4: Vermittlungsschicht


## Lernziele Kapitel 5: [[Sicherungsschicht]] / Netzzugriff