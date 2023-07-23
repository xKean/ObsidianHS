![[Pasted image 20230716112920.png]]
- hat KEINE Längenangabe und keine Unterstützung der LLC-Schicht
- stattdessen Typ-Feld für eine Protokoll ID des Protokolls in der Nutzlast (entspricht teilweise der LLC-Schicht)
- i.d.R. transportiert Ethernet max. 1500 Byte Nutzlast (optional bis max 9000 Bytes (Jumbo-Frames) möglich)
- 4 Byte große Feld FCS beinhaltet die Frame-Prüfsequenz, die mittels zyklischem Kodierungsverfahren (CRC) gebildet wird. 
	- Damit werden Adressen, Länge, Füllzeichen abgesichtert
	- FCS und PA ermöglichen Synchronisation bzw. Erkennung des Frames auf dem Übertragungsmedium