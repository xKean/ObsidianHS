![[Pasted image 20230716165856.png]]

Um eine Ausfallsicherheit zu realisieren, sollte JEDER Server ca. 75% der für das eigene Subnetz bestimmten IP-Adressen verfügen. Jeder Server sollte über 25% der für das Subnetz bestimmten IP-Adressen verfügen.

**DHCP LEASE**
Der Zeitraum einer dynamischen IP Zuweisung nennt man LEASE.
Alle Clients versuchen nach der halben abgelaufenen Zeit ihren Lease zu erneuern. Dafür sendet der Client eine eine REQUEST and den Server und diese wird wieder über ACK akzeptiert und aktualisiert.