
User Datagram Protocol

- Verbindungsloses Protokoll
- Daten werden ohne vorher eine virtuelle Verbindung aufzubauen übermittelt
- Keine Garantie für die korrekte Übermittlung der Daten
- Keine Fehlerkorrektur
- Keine Fluss- und Staukontrolle
- Gegenstück zu [[TCP]]


#### Header
```
  0      7 8     15 16    23 24    31
 +--------+--------+--------+--------+
 |     Source      |   Destination   |
 |      Port       |      Port       |
 +--------+--------+--------+--------+
 |                 |                 |
 |     Length      |    Checksum     |
 +--------+--------+--------+--------+
 |
 |          data octets ...
 +---------------- ...

	  User Datagram Header Format
```


#### Aufgaben
- Bildung und Transport von UDP - Paketen
- (De)Multiplexen von Anwendungen ![[Pasted image 20230716173002.png]]


#### Sockets
- Sockets (definiert durch: IP-Adresse + Port) stellen die Endpunkte des Transports von Nachrichten dar. UDP Sockets werden direkt für fortlaufende Übertragung genutzt, keine Verbindung, kein Verbindungsauf-/-abbau, keine Fehler- /Flusskontrolle etc. 
- Eingehende UDP-Nachrichten mit der gleichen Ziel-IP-Adresse und gleichem Ziel-Port gehen unabhängig von der Quell-IP-Adresse und dem Quell-Port immer an das gleiche Socket (und damit den gleichen Anwendungsprozess). Bei TCP sind alle 4 Parameter wichtig, nicht nur Ziel-Socket.

#### Warum nutzt man UDP wenn es "unzuverlässig" ist?
- Es ist schnell
- Die Anwendung kann dann im Zweifelsfall sebst entscheiden ob sie das Paket noch einmal benötigt.
- Beispiel: Video-Streaming / Low Latency gaming


#### Vorteile
- Keine Verbindung (geringes Delay)
- Einfache Implementierung
- Schlanker Header
- Keine Fehler- Fluss- und Staukontrolle (kann auch ein Nachteil sein)
	- Vorteil, da: QUIC möglich, so schnell wie möglich gesendet
- Besonders geeignet für Echtzeitübertragung