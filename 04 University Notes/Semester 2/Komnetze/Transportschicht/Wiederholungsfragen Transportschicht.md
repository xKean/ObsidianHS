
## 3.1 TCP/IP-Anwendungsprotokolle und Anforderungen

**3.1.1 Welche Protokolle realisieren die Transportschicht in TCP/IP Netzen?**
- Die Transportschicht in TCP/IP Netzen wird realisiert durch UDP (User Datagram Protocol) und TCP (Transmission Control Protocol)

**3.1.2 Welche Unterschiede weisen verbindungslose und verbindungsorientierte
Transportprotokolle auf?**
- das verbindungslose Transportprotokoll UDP übermittelt Daten verbindungslos, d.h. ohne vorher eine virtuelle Verbindung aufzubauen. Keine Garantie für die korrekte Übermittlung der Daten
- das verbindungsorientierte Transportprotokoll TCP ermöglicht es, virtuelle Verbindungen zwischen den kommunizierenden Rechnern auf- und abzubauen. Durch Fehler- und Flusskontrolle wird dabei eine sichere Datenübermittlung gewährleistet (Ende-zu-Ende Fehler- und Flusskontrolle über mehrere Vermittler hinweg).

**3.1.3 Nennen Sie Einsatzgebiete von TCP und UDP jeweils am Beispiel eines darauf
basierenden Anwendungsprotokolls**
- TCP wird unter anderem für das HTTP Protokoll benutzt
- UDP wird bei der IP-Vergabe mithilfe von DHCP eingesetzt

**3.1.4 Wie unterscheiden sich logische Verbindungen auf der Transport- und auf der
Vermittlungsschicht**
- ???

**3.1.5 Wie hängen Segmentierung, Multiplexing und Demultiplexing auf der Transportschicht
mit der Anwendungsschicht zusammen?**
- TCP/IP-Stack im Betriebssystem muss eingehende Daten dem richtigen Anwendungsprozess zuordnen können. D.h. das jeder Anwendungsprozess von der Transportschicht einen neuen eindeutigen Quell-Port zugewiesen bekommt 

**3.1.6 Was wird durch Transportprotokolle definiert?**
- ???

**3.1.7 Was unterscheidet „well-known“ von „dynamic ports“ und wofür werden sie
verwendet?**
- Ports < 1024 bezeichnet man als **„system“** oder **„well known ports“**, Nutzung erfordert Admin-Rechte, Antrag für Vergabe der Nummern bei IANA erforderlich
- Ports 49152-65535 bezeichnet man als **„private“** oder **„dynamic ports“**, frei verwendbar

**3.1.8 Wieviel Ports können bei TCP und UDP unterschieden werden?**
- 16 Bit für Port-Nummer im Header (2^16=65535 Ports, 0 ist reserviert)

**3.1.9 Das folgende Bild zeigt ein Modell für die Kommunikation zwischen Applikationen
Über ein IP-Netz.**
- F1: Erläutern Sie die wichtigsten Prinzipien der Datenübermittlung zwischen X und Y
 - ???
- F2: Erläutern Sie die Prinzipien der Kommunikation zwischen den beiden Applikationen,
falls UDP als Transportprotokoll eingesetzt wird.
 - Eine Transport-Instanz (T-Instanz) mit UDP sendet eine Nachricht an ihre Partner-T-Instanz, ohne vorher eine Beziehung (Verbindung) zu ihr aufzubauen. Der Empfang der Nachricht wird nicht bestätigt. Es handelt sich hierbei um eine ungesicherte Übermittlung von Nachrichten.
- F3: Erläutern Sie die Prinzipien der Kommunikation zwischen den beiden Applikationen,
falls TCP als Transportprotokoll eingesetzt wird.
 - Eine T-Instanz mit TCP baut zuerst eine Beziehung (Verbindung) zu ihrer Partner-T-Instanz auf und sendet erst danach an diese Daten. Der Empfang der Daten wird bestätigt. Es handelt sich hierbei um eine gesicherte Übermittlung von Daten.

## 3.2 User Datagram Protocol

**3.2.1 Welche Aufgaben hat UDP?**
- Bildung und Transport von UDP-Paketen, (De)Multiplexen von Anwendungen

**3.2.2 Wie werden Sockets bei UDP verwendet?** 
- Sockets (definiert durch: IP-Adresse + Port) stellen die Endpunkte des Transports von Nachrichten dar. UDP Sockets werden direkt für fortlaufende Übertragung genutzt, keine Verbindung, kein Verbindungsauf-/-abbau, keine Fehler-/Flusskontrolle etc.

**3.2.3 Welche Funktion haben Source und Destination Port im UDP Header?**
- Source und Destination Port (je 16 Bit) geben Quell- und Ziel-Port (Layer 4 Adresse) an

**3.2.4 Welche Vorteile hat UDP gegenüber TCP?**
- Kein Verbindungsaufbau und damit geringeres Delay (Daten können sofort übermittelt werden)
- Schlanker Header, verringert Delay zusätzlich
- Keine Fehler-/Fluss-/Staukontrolle
 -  UDP-Daten können einfach gesendet werden und nutzen „best effort“ Dienst von IP (Internet) so gut wie möglich, keine Reduzierung der Bitrate etc., Daten werden so schnell gesendet, wie es über das Netz möglich ist und sie von der Anwendung kommen.
 - Eine Behandlung von Übertragungsfehlern, Flusskontrolle, Stau etc. müsste somit wenn von der Anwendung (in höherer Schicht) erbracht werden. (siehe HTTP/3 w/ QUIC)

## 3.3 Transmission Control Protocol

**3.3.1 Welche Aufgaben hat TCP?**
- Bildung von TCP-Paketen, (De)Multiplexen von Anwendungen
- Aufbau und Abbau von (virtuellen) TCP-Verbindungen
- Transport von TCP-Paketen über TCP-Verbindungen
- Fehlerkontrolle : Sicherung des Datentransports
- Flusskontrolle : Anpassung der Sendeseite an die Gegenseite
- Staukontrolle : Anpassung der Sendeseite an Netzauslastung

**3.3.2 Wie werden Sockets bei TCP verwendet?**
- Sockets stellen die Endpunkte des Transports von Nachrichten dar.

**3.3.3 Wodurch wird eine TCP-Verbindung eindeutig definiert?**
- Eine TCP-Verbindung wird eindeutig durch folgendes 4-Tupel definiert: (Quell-IP-Adresse, Quell-Port, Ziel-IP-Adresse, Ziel-Port) -> unterscheidet sich nur ein einziger dieser Parameter, kann der Demultiplexer die eingehende TCP-Nachricht an einen anderen Anwendungsprozess weiterleiten (abhängig von Quell-IP-Adresse/-Port). So wird bei TCP im Gegensatz zu UDP eine feste Verbindung realisiert.

**3.3.4 Wie erfolgt der Verbindungsauf- und -abbau bei TCP?**
- 3-Wege-Handshake Verbindungsaufbau bei TCP (HTTP):
 - Client schickt Sychronisierungsanfrage (SYN) an Server
 -  Server bestätigt dies mit Acknowledge (ACK) und sendet seinerseits Synchronisierungsanfrage zurück (ergibt: SYN,ACK)
 - Client bestätigt final mit ACK, Verbindung ist damit aufgebaut, daher können in diesem TCP-Segment bereits Nutzdaten (z.B. HTTP-Anfrage) enthalten sein
- 4-Wege-Verbindungsabbau bei TCP (HTTP): 
 -  FINish wird von beiden Seiten gesendet und gegenseitig bestätigt

**3.3.5 Wie kann ein Web-Server eingehende Pakete den richtigen Prozessen zuordnen?**
- Für HTTP ist der Port 80 und somit das Server Socket immer 80, da der Server die Verbindungen von TCP anhand von Client-IP/-Port differenzieren kann.

**3.3.6 Welche Aufgaben haben folgende Angaben im TCP-Header?**
- **Source Port (Quell-Port)**: Portnummer des Anwendungsprotokolls (der Applikation) im Quellrechner, das die Daten sendet.
- **Destination Port (Ziel-Port)**: Portnummer des Anwendungsprotokolls im Zielrechner, an die die Daten adressiert sind.
- **Sequence Number (Sequenznummer)** für die byteweise Nummerierung von zu sendenden Daten
- **Acknowledgement Number (Quittungsnummer)** für die byteweise Bestätigung empfangener Daten
- **(Receive) Window (Fenstergröße)** dient der Flusskontrolle und gibt dem Sender an, wie viele Bytes – beginnend ab der letzten Quittungsnummer – der Empfänger (Zielrechner) in seinem Aufnahme-Puffer noch aufnehmen kann.
- **Control Flags (Kontroll-Flags)** legen die Bedeutung des TCP-Segments fest. Dieses 6-Bit Feld hat folgende Struktur: URG, ACK, PSH, RST, SYN, FIN. Ist das entsprechende Bit gesetzt, gilt Folgendes:
 - URG (Urgent): Segment enthält dringliche Daten (selten verwendet) (nicht klausurrelevant)
 - ACK (Acknowledgement): Quittungsnummer wird übermittelt
 - PSH (Push): Daten sofort an die nächsthöhere Schicht übergeben (selten verwendet, z.B. für interaktive Anwendungen) (nicht klausurrelevant)
 - RST (Reset): TCP-Verbindung soll zurückgesetzt werden
 - SYN (Synchronization): Aufbau einer TCP-Verbindung
 - FIN (Finish): Abbau einer TCP-Verbindung
- **Options (variable Länge)**: TCP ermöglicht es, weitere Optionen anzugeben. Als eine Option kann z.B. Maximum Segment Size angegeben werden.

**3.3.7 Warum ist bei TCP ein Pipelining von Segmenten erforderlich?**
- Würde nur ein Segment übertragen und dann gewartet, würden lange Laufzeiten (Delays) Bitrate stark einschränken.
- Daher werden bei TCP mehrere Segmente versendet ohne auf eine Bestätigung zu warten

**3.3.8 Was bedeutet Sliding Window bei TCP in Bezug auf Fehler- und Flusskontrolle?**
- Window kann man als Sendefenster interpretieren. Bei jeder Bestätigung (ACK) wird das Sendefenster nach rechts verschoben (Sliding). Die Seq- und ACK-Nummern werden beim Aufbau der TCP-Verbindung zufällig gewählt und ausgetauscht sowie anschließend aufsteigend verwendet.

**3.3.9 Unter welchen Umständen kann bei TCP eine Sendeblockade entstehen?**
- ???

**3.3.11 Wo beginnt der Sender bei TCP nach dem Verlust eines Segments (Timeout) erneut
mit der Übertragung?**
- Wenn für ein abgesendetes TCP-Paket innerhalb eines bestimmten Zeitraums (maximale Wartezeit auf Quittung (Maximum Segment Lifetime) ) keine Bestätigung eingeht, wird die Übertragung ab dem zuletzt erfolgreich quittierten TCP-Segment wiederholt.

**3.3.12 Woran orientiert sich der Timeout für die Übertragung von TCP Segmenten?**
- Die maximale Wartezeit für die Quittungen wird bei TCP basierend auf RTT der Verbindung abgeschätzt (> RoundTripTime)

**3.3.13 Was wird durch die folgenden Formeln erreicht?**
- (keine ahnung wie ich die Formeln hier reinkriegen soll)
- Die erste Formel besagt, dass der Einfluss älterer Messwerte exponentiell abnimmt, typischerweise Alpha = 0,125
- Die zweite Formel besagt, Timeout = EstimatedRTT + Sicherheitsabstand
 - Hohe Varianz der RTT-Werte → hoher Sicherheitsabstand 
 - Beta = 0,25 typischer Wert 

## 3.4 Staukontrolle bei TCP

**3.4.1 Was bedeutet „slow start“ bei TCP?**
- Der Sender startet mit einer minimalen Anzahl für n, und erhöht die Senderate bis zu einem Schwellwert, z.B. n = 1:
 - 1 MSS/1 RTT = z.B. 1460 Bytes/0,2s = 7,3 kByte/s

**3.4.2 Welche Aufgabe hat das Congestion Window bei TCP, und wie wird es zusammen mit
der Window Angabe im TCP Header verwendet?**
- Empfänger signalisiert Sender durch das (Receive) Window (rwnd) die Menge an Daten, die er (noch) in seinem Puffer speichern kann
- Es wird ein weiteres Window eingeführt -> Congestion Window (cwnd), welches die Stau-/Flusskontrolle verwirklicht.
- Das jeweils „kleinere“ der beiden Fenster bestimmt die tatsächlich zulässige Anzahl von n übermittelten Segmenten, bevor der Sender auf ein ACK wartet.

**3.4.3 Was bedeutet AIMD bei der Staukontrolle von TCP?**
- Ab dem Erreichen des Slow-Start-Schwellwerts (Slow-Start Threshold) Größe des Congestion Windows (nun langsamer) inkrementieren und bei Verlust reduzieren (congestion avoidance)
- Sofern kein Timeout auftritt, läuft TCP congestion control in congestion avoidance, wird auch **AIMD Phase** genannt:
 - Additive Increase, Multiplicative Decrease
 - Dies wird auch "Sägezahn" von TCP genannt
- So wird ein Herantasten an die maximal verfügbare Übertragungsrate möglich
- Funktioniert auch für die Anpassung mehrerer Sender, z.B. für zwei Sender jeweils halbe max. Bitrate (faire Bitratenaufteilung)

## 3.5 Aktuelle Anforderungen an die Performance von TCP/UDP

**3.5.1 Nennen Sie ein Beispiel für eine Verbesserung der TCP congestion control**
- Erweiterungen für Unterscheidung von Paketverlust durch Timeout und Paketverlust durch Bitfehler (z.B. im WLAN)

**3.5.2 Welche Vorteile bietet Multipath TCP?**
- Mehrere TCP Verbindungen über eine Link Layer Verbindung
- Mehrere TCP Verbindungen über mehrere Link Layer Verbindungen

## 3.6 Sicherheit für Transportprotokolle (TLS/SSL

**3.6.1 Welche Anforderungen an die Netzwerksicherheit kennen Sie?**
- **Vertraulichkeit** -> Übertragung soll nicht von Dritten abgehört werden (Verschlüsselung)
- **Integrität** -> Übertragung soll nicht unterwegs von Dritten manipuliert werden können (Prüfsummen, Hash, digitale Signaturen) 
- **Verbindlichkeit** -> Absender soll nicht abstreiten können, dass übermittelte Daten von ihm stammen (digitale Signaturen)
- **Authentizität** -> Identitätsprüfung, Zuordnung von realer zu digitaler Identität (Passwort, Zertifikate)
- **Verfügbarkeit** -> Systeme, Anwendungen und Dienste im Netz sollen unterbrechungsfrei zur Verfügung stehen und Dienst erfüllen (Firewall, Intrusion Detection Systeme)

**3.6.2 Welche Schutzmaßnahmen realisiert TLS?**
- Verschlüsselung von übertragenen Segmenten
- Gewährleistung der Integrität der Segmente durch Hashes (Prüfsummen)
- Endpunktauthentifizierung
- Daten werden so verschlüsselt, dass nur Endpunkte sie entschlüsseln können (Übertragung von Daten über unsicheres Netz)
- -> Ermöglicht über **hybride Verschlüsselung**
 - Asymmetrische Verschlüsselung für Schlüsselaustausch (öffentlicher (public) und privater (private) Key des Servers)
 - Symmetrischer Schlüssel für transportierte Daten


