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


## Lernziele Kapitel 4: [[Vermittlungsschicht]]
- Welche Anforderungen werden an Protokolle auf der Vermittlungsschicht gestellt? 
	- Pakete zwischen Sender und Empfänger vermitteln
	- Packen von Segmenten in IP-Pakete, entpacken beim Empfänger
	- Forwarding -> Eingangs- zu Ausgangsport
	- Routing: Nutzung von Routing-Algorithmen für Wegewahl
- Was ist das [[Internet]]? 
	- ![[Internet]]
- Wie wird gewährleistet, dass Pakete im Internet nicht unendlich zirkulieren? 
	- [[TTL]]
- Woraus besteht eine [[IP-Adresse]] und wie wird ein IP-[[Subnetz]] definiert? 
	- IP-Adresse
		- ![[IP-Adresse#IPV4]]
	- Subnetz
		- ![[Subnetz]]
- Welche Vorteile bietet das Classless Inter-Domain Routing? 
	- Alte Methode: Netzklassen
		- Bei Netzklassen wurde nur zwischen /8 (Klasse A), /16 (Klasse B), /24 (Klasse C) unterschieden. Da diese Netze für die meisten Usecases zu groß waren, wurden Adressen verschwendet.
	- Neue Methode: Classless Inter-Domain Routing
		- Subnetze können klassenlos spezifiziert werden.
		- Es ist egal ob ein /24, /23, /21 oder ein /17 Netz erstellt wird.
- Wie kann erkannt werden, ob die Ziel-IP-Adresse im gleichen [[Subnetz]] ist? 
	- Die Netz-ID wird bitweise mit logischem "UND" vergleicht
	- ![[Pasted image 20230717125503.png]]
	- Was passiert, wenn die Adresse im gleichen [[Subnetz]] ist? 
		- Das Paket wird direkt an den Zielrechner gesendet.
	- Was passiert, wenn sie in einem fremden [[Subnetz]] liegt? 
		- Das Paket wird an das Default-Gateway gesendet.
- Welche Vorteile bietet das [[Longest Prefix Matching]] für das [[Routing]]? 
	- Durch [[Route Aggregation]] können "kleinere" Routingtabellen ermöglicht werden
	- [[Longest Prefix Matching]] ermöglicht einfacheren Umzug zwischen ISPs
- Wie kann das Subnetz 176.16.128.0/17 in fünf neue Subnetze unterteilt werden? 
	- https://youtu.be/4RMb3eOuZsQ
- Erläutern Sie die Verwendung von Ports und privaten [[IP-Adresse]]n bei [[NAT]]. 
	- Im Heimnetz
		- Router hat <u>eine</u> öffentliche [[IP-Adresse]]
		- Server von außen möchte Gerät in meinem Heimnetz erreichen#
		- Server schickt anfrage mit IP (Router) + Port  => [[Socket]]
		- Router leitet Anfrage (durch Port) an Endgerät PC weiter.
		- Kommunikation funktioniert.
		- Somit muss nicht jeder PC eine eigene öffentliche IP haben, sondern nur der Router.
		- Im Heimnetz selbst werden private IP-Adressen zur Kommunikation benutzt. Diese sind obviously nicht öffentlich eindeutig
- Welche Vorteile bietet IPv6? Wie erfolgt die Migration von IPv4 nach IPv6? 
	- Vorteile
		- ViEl MeHr AdReSsEn (128 Bit statt 32)
		- Lokalisierung via "Vorwahlen"
			- Dadurch einfacheres, schnelleres Routing
	- Migration
		- Dual Stack oder Dual Stack Lite
			- Es werden gleichzeitig IPV4 und IPV6 vergeben
			- ![[Pasted image 20230717134534.png]]#
			- Problem: IPV4 ist überall verbaut.
- Wie wird die Privatsphäre bei der Verwendung von IPv6 geschützt?
	- Privacy Extensions
		- Der Rechner erhält zusätzlich eine zweite zufällig gewürfelte temporäre IPv6-Unicast-Adresse, die regelmäßig gewechselt und für ausgehende Verbindungen genutzt wird.
		- Weniger Tracking / Verfolgbarkeit
- Welche Aufgaben übernehmen [[Forwarding Plane]] und [[Control Plane]] bei Routern? 
	- Forwarding Plane
		- ![[Forwarding Plane]]
	- Control Plane
		- ![[Control Plane]]
- Was unterscheidet statisches/dynamisches Routing? Welche Typen kennen Sie? 
	- Statische Routen
		- Statische Routen sind sinnvoll, wenn sich (optimale) Routen fast nie ändern. Beispielsweise in einem Heimnetz oder in einem Subnetz muss auf einen Server mit <u>immer der gleiche IP</u> zugegriffen werden.
	- Dynamische Routen
		- Dynamische Routen lohnen sich (bspw. im Internet) wenn man sich nicht darauf verlassen kann, dass die Routen nicht ändern.
		- Distanz-Vektor (Wie das Internet funktioniert)
			- Router kennt Nachbar-Router und Link-Kosten 
			- Iterativer Austausch von Nachbar-Routern über Netz (auch von Fehlern!) 
			- Nachrichtenaustausch nur zwischen Nachbarn, dafür hohe Konvergenzzeit • Routing-Schleifen möglich (z.B. Problem „Count to infinity“)
		- Link-State Routing-Protokolle (Nur in privaten Netzen)
			- Alle Router kennen komplette Topologie und deren Zustand („Link State“: Link up/down, Verzögerung, Auslastung, Kosten/Gebühren, …)
			- Hohes Nachrichtenaufkommen im Gesamtnetz, dafür geringere Konvergenzzeit
			- Routing-Fehler durch oszillierende Routen möglich 
			- Fehlerhafte Link-Kosten haben im Gegensatz zu Distanz-Vektor nur lokale Auswirkung
- Welche Vorteile hat [[OSPF]]? 
	- Sicherheit (OSPF-Pakete können Authentifizierung beinhalten)
	- Lastverteilung über Pfade mit gleichen Kosten
	- „Quality of Service“ in Kosten abbildbar: Z.B. Links mit hoher Latenz
	- Integrierter Support für Multicast-Routing 
	- Hierarchisches OSPF-Routing für große Domains
- Wie werden bei [[BGP]] Prefixes für das Routing im Internet ausgetauscht? 
	- Router kommunizieren miteinander und updaten ihre Routing Tabellen aufgrund von Update-Nachrichten von anderen Routern.
- Warum ist bei [[BGP]] ein Policy-based Routing wichtig? 
	- Ggf. wegen politischen oder wirtschaftlichen Gründen
		- Routing durch Kriegsländer (kritische Informationen)
	- Somit können Informationen auf "sicheren" Wegen geleitet werden.
- Welche Funktionen übernimmt das Hilfsprotokoll [[ICMP]]? 
- Wofür wird [[ARP]] benötigt?
	- ARP wird genutzt um zu einer IP-Adresse eine MAC-Adresse zuzuordnen

## Lernziele Kapitel 5: [[Sicherungsschicht]] / Netzzugriff