---
dg-publish: true
---
User Dataram Protocol

- Verbindungsloses Protokoll
- Daten werden ohne vorher eine virtuelle Verbindung aufzubauen übermittelt
- Keine Garantie für die korrekte Übermittlung der Daten
- Keine Fehlerkorrektur
- Keine Fluss- und Staukontrolle
- Gegenstück zu [[TCP]]


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


- Der Empfang der Daten wird nicht bestätigt



#### Warum nutzt man UDP wenn es "unzuverlässig" ist?
- Es ist schnell
- Die Anwendung kann dann im Zweifelsfall sebst entscheiden ob sie das Paket noch einmal benötigt.
- Beispiel: Video-Streaming / Low Latency gaming


#### Vorteile
- Keine Verbindung (geringes Delay)
- Einfache Implementierung
- Schlanker Header
- Keine Fehler- Fluss- und Staukontrolle (kann auch ein Nachteil sein)
- Besonders geeignet für Echtzeitübertragung