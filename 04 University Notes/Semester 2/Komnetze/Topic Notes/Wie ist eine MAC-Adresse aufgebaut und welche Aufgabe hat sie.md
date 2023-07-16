![[Pasted image 20230716113311.png]]
- Jeder Ethernet hat eigene physikalische MAC-Adresse
- Oktetts 1-3 bilden OUI (organizationally unique Identifier): verwaltet durch IEEE - eindeutige ID des Herstellers (z.B.: 00:10:f6 für Cisco)
- Restlichen Oktetts (4-6) bilden Seriennummer (Ethernet-Adapter-ID)
- Adapter empfängt nur Frames für eigene Adresse oder für den Gruppenboradcast (ff:ff:ff:ff:ff:ff), AUSSER er ist im "promiscuous mode"
- MAC-Adresse kann sogar vom Betriebssystem temporär geändert werden
- MAC-Adressen bilden eine weltweit einheitliche flache Adressierung (kein hierarchischer Adressraum)
	- Extended Unique Identifiert (EUI-4)