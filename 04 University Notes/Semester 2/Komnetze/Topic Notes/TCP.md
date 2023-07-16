
Transmission Control Protocol

- Verbindungsorientiertes Protokoll
- Wesentlicher Unterschied zu [[UDP]]: Alle Daten die Übertragen werden werden bestätigt.
- Für Jedes übertragene Segment gibt es eine Quittung

Bei TCP wird immer

- Quell-IP-Adresse
- Quell-Port
- Ziel-IP-Adresse
- Ziel-Port

übermittelt. Daraus lässt sich eine eindeutige Verbindung identifizieren.

#### Aufgaben
TCP ist ein Protokoll, das eine virtuelle Verbindung zwischen genau einem Quell- und genau einem Zielrechner in einem IP-Netz aufbaut. Über diese Verbindung werden die Daten in Form von festgelegten Dateneinheiten (Segmenten) ausgetauscht. Die Verbindung ist bidirektional (duplex).
- Bildung von TCP-Paketen
- (De)Multiplexen von Anwendungen
- Aufbau und Abbau von (virtuellen) TCP-Verbindungen
- Transport von TCP-Paketen über TCP-Verbindungen
- Fehlerkontrolle: Sicherung des Datentransports
- Flusskontrolle: Anpassung der Sendeseite an die Gegenseite
- Staukontrolle: Anpassung der Sendeseite an Netzauslastung

#### Sockets
- Sockets bei TCP werden durch die 4 Parameter eindeutig definiert: Quell-IP, Quell-Port, Ziel-IP, Ziel-Port
- Unterscheidet sich einer dieser 4 Werte, kann der Demultiplexer die eingehende Nachricht an einen anderen Anwendungsprozess leiten (abhängig von Quell-IP und Quell-Port)
- So wird eine feste Verbindung realisiert (nicht wie bei UDP)

#### Verbindungsablauf
1. 3-Wege-Handshake zum Verbindungsaufbau (inkl. erste Anfrage in letzter ACK-Message)
2. Zuverlässige Übertragung ist nun möglich
3. HTTP-Requests können übertragen werden (GET, POST, etc)
4. 4-Wege-Verbindungsabbau
![[Pasted image 20230716174603.png]]




#### Aufgaben von TCP bei Übermittlung von Segmenten
- Abstimmung maximale Länge von Segmenten
- Grantie der Korrekten Reihenfolge der Segmente
- Wiederherstellung von Daten im Zielrechner durch die zusammensetzung der empfangenen Segmente
- Anforderung von verlorengegangenen Datensegmenten


#### Byteweise Nummerierung von Daten
- Zufällige Anfangs-Sequenznummer
- Sequenznummer += Gesendete Bytes

#### Header
![[Pasted image 20230716175056.png]]
- Quell-Port: die Quelle xDXDXD
- Ziel-Port: das Ziel XDXDXD
- Sequenznummer: byteweise Nummerierung von zu sendenden Daten (das wievielte Paket ist das jetzt)
	- Bei TCP werden die zu sendenden Daten byteweise mit Hilfe einer Sequenznummer nummeriert. Beim Aufbau einer TCP-Verbindung generiert jedes TCP-Modul eine zufällige Anfangs-Sequenznummer. Diese Nummern werden ausgetauscht und gegenseitig bestätigt. Im Quellrechner wird die Sequenznummer jeweils um die Anzahl der bereits gesendeten Bytes erhöht.
- Quittungsnummer: für die byteweise Bestätigung empfangener Daten
- Window: Fenstergröße für die Flusskontrolle, gibt dem Sender an, wie viele Bytes gesendet werden können
- Control Flags: ACK, RST (Reset), SYN (Aufbau), FIN (Abbau)

#### Pipelining
- wenn immer nur ein Segment übertragen wird, dann dauerts lang, da ja Bestätigung zurückkommen muss
- mehrere Segmente (Windows) ohne Bestätigung schicken
- Anzahl wird durch Window Size angegeben
- Im Fehlerfall Segmente neu übertragen
	- Variante 1: "Go-Back-N": Übertrage alle Segmente ab letztem erfolgreich quizzierten neu
	- Variante 2: "Selective Repeat": Übertrage nur verlorene Segmente (mehr Aufwand, aber weniger Neuübertragungen)
	- Aktuelle üblich: Mischung aus 1 und 2

#### Flusskontrolle
- Abstimmung wieviel Übertragen wird nach Prinzip Sliding Window
- Window kann man als Sendefenster interpretieren. Bei jeder Bestätigung (ACK) wird das Sendefenster nach rechts verschoben (Sliding). Die Seq- und ACK-Nummern werden beim Aufbau der TCP-Verbindung zufällig gewählt und ausgetauscht sowie anschließend aufsteigend verwendet.
- Beispiel: Windowssize: 4. Pakete mit Nummern 20-23 werden geschickt. Erst wenn das ACK für Paket 20 zurückkommt, wird Paket 24 geschickt usw. ![[Pasted image 20230716180447.png]]

#### Timeout
- Wenn für ein abgesendetes TCP-Paket innerhalb eines bestimmten Zeitraums (maximale Wartezeit auf Quittung (Maximum Segment Lifetime)) keine Bestätigung eingeht, wird die Übertragung ab dem zuletzt erfolgreich quittierten TCP-Segment wiederholt. 
- Der Empfang der TCP-Segmente wird nur dann bestätigt, wenn ihre Reihenfolge vollständig ist.![[Pasted image 20230716181743.png]]
- Die maximale Wartezeit für die Quittungen wird bei TCP basierend auf RTT der Verbindung abgeschätzt (> RTT) 
	- erste Schätzung: Abstand zw. Segment und ACK (3-Way-Handshake)
	- Zu geringe Wartezeit: Zu viele unnötige erneute Übertragungen
	- Zu hohe Wartezeit: Langsame Reaktion auf Fehler
- Variiert über Laufzeit der Verbindung (schwankende Auslastung des Netzes), daher Glättung durch gewichteten Mittelwert:
	- $EstimatedRTT_n = (1-α)* EstimatedRTT_{n-1} + α*SampleRTT$
	- α typischerweise 0,125
	- Einfluss älterer Messwerte nimmt exponentiell ab
	- Timeout = EstimatedRTT + Sicherheitsabstand
	- $DevRTT = (1-\beta)*DevRTT + β*|SampleRTT-EstimatedRTT|$
	- β üblicherweise 0,25
	- TimeoutInterval = EstimatedRTT+ 4*DevRTT
	- Hohe Varianz der RTT-Werte → hoher Sicherheitsabstand -> Also hohes TimeoutIntervall

#### TripleDuplicate
- Timeout häufig groß -> Lange Wartezeit auf erneuten Transfer und dann wieder alle Pakete
- Paketverlust erkennen und reagieren -> Bescheid geben: "Hey du bist zu weit -> ich bin erst bei dem hier"
	- Wenn Sender drei doppelte ACKs empfängt -> sende Segment mit kleinster unbestätigter Sequenznummer erneut ohne Timeout zu warten
![[Pasted image 20230716183326.png]]

#### PerformanceImprovements
![[Pasted image 20230716183901.png]]

#### Staukontrolle
- Receive Windows (rwnd) und Congestion Window (cwnd) (startet bei 1) geben beide eine Anzahl an möglichen zu übermittelten Segmenten an
- Die kleinere Zahl bestimmt wieviele tatsächlich übermittelt werden, ohne auf ein ACK zu warten, das sonst ggf. die Netzknoten gar nicht so viele Segmente übertragen könnten, wie der Empfänger empfangen könnten
- Slow-Start:
	- Der Sender startet mit einer minimalen Anzahl und erhöht die Senderate bis zu einem Schwellwert (slow start) (exponentiell)
	- $Rate[Byte/s] = \frac{n*MSS[Bytes]}{RTT[s]}$
	- MSS -> Maximale Segment Größe (bei 3-Way-Handshake ausgehandelt)
- Tahoe Algorithmus:
	- Ab dem Erreichen des Slow-Start-Schwellwertes nun langsamer inkrementieren (linear) und bei Verlust reduzieren (congestion avoidance)
	- Bei einem Timeout eines ACK zurückfallen auf slow-start ![[Pasted image 20230716185105.png]]
- Reno Algorithmus (verbesserter Tahoe):
	- Bei „triple duplicate ACK“ wird nur das betroffene Segment erneut gesendet (sog. „fast retransmit“)
	- Da weniger Segmente erneut versendet werden müssen, kann cwnd weniger stark gedrosselt werden
	- cwnd wird nach triple duplicate ACK nur halbiert, kein slow-start, falsche Reihenfolge ist weniger schlimm als Timeout (fast recovery)![[Pasted image 20230716185237.png]]
- Sofern kein Timeout auftritt, läuft TCP congestion control in congestion avoidance, wird auch AIMD Phase genannt: Sägezahn – Additive Increase, Multiplicative Decrease, also wie Reno
	- maximale Übertragungsrate bei folgendem Beispiel: ![[Pasted image 20230716191105.png]]
	-  $Rate[Byte/s] = \frac{13*1460[Bytes]}{0,1[s]}$
	