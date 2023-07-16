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
###### Was sind [[Anforderungen an Computernetzwerke]] heutzutage?

![[Anforderungen an Computernetzwerke]]
###### [[Schichtenmodell für Protokolle und Dienste]]  (Referenzmodelle)
- Welche Schichtenmodelle kennen Sie?
	- ![[Schichtenmodell für Protokolle und Dienste]]
- Was sind [[Header]] und was ist deren Inhalt?
	- Quell- und Zieladressen, für die Aufgaben der Schicht erforderliche Informationen










###### Welche Standardisierungsgremien haben Einfluss auf Computernetzwerke?
- IEEE
- IETF
- ITU-T
- ETSI










## Lernziele Kapitel 2: [[Anwendungsschicht]]

- Konzept und Implementierung von [[Internetanwendungsprotokollen]]
- [[Client-Server-Anwendungen]] vs [[Peer-to-Peer]]
- [[Servicemodelle]] und Anforderungen
- Welche Aufgaben hat ein typisches [[Anwendungsprotokoll]] einer Internetanwendung? 
- Welche Funktionen und Eigenschaften hat [[HTTP]]? 
- Wie unterstützt [[DNS]] die Verwendung von Internetanwendungen? 
- Wie können Rechner automatisiert mit [[DHCP]] für die Verwendung von TCP/IPNetzen konfiguriert werden?


## Lernziele Kapitel 3: [[Transportschicht]]

- Aufgaben und Funktion der [[Transportschicht]]
- Eigenschaften von [[TCP]] und [[UDP]]
- Performance und Sicherheit auf der Transportschicht bewerten können
- Welche Aufgaben haben [[Verbindungslose Transportprotkolle]]?
- Welche Aufgaben haben [[Verbindungsorientierte Transportprotokolle]]?
- Wie wird bei [[TCP]] die Fehler-, Fluss- und Staukontrolle realisiert? 
- Welche aktuellen Performance- und Sicherheitsherausforderungen stellen sich für [[TCP]]/[[UDP]]?




## Lernziele Kapitel 5: [[Sicherungsschicht]] / Netzzugriff