- gesicherte Übertragung von Daten von einem physikalischen Netzknoten (NODE) zum nächsten
	- Zuverlässigkeit und Fehlererkennung
- Zugriffssteuerung auf Verbindungen (LINKS), Übertragungsmedium
	- shared vs. dedicated medium
	- optionale Fehler- und Flusskontroller auf einzelnem Link (nicht wie bei Transport End-to-End mehrere Links)
- Verkapselung der Daten höherer Schichten in Frames (Rahmen)
	- Synchronisation auf Medium, Hardware-Adressierung (MAC)
- Link- bzw. Netzzugriff über unterschiedliche Technologien möglichen:
	- LAN (Ethernet), WLAN, Power LAN, Mobilfunk, xDSL, Kabel, MPLS etc.
![[Pasted image 20230716105816.png]]
Link: Ein Link ist eine physische oder logische Verbindung zwischen zwei Netzwerkknoten, die es ermöglicht, Daten zu übertragen. Ein Link kann beispielsweise ein Ethernet-Kabel, eine WLAN-Verbindung oder eine serielle Verbindung sein.

Node: Ein Node ist ein Netzwerkknoten, der Daten sendet oder empfängt. Ein Node kann ein Computer, ein Router, ein Switch oder ein anderes Netzwerkgerät sein.

Frame: Ein Frame ist die Einheit, in der Daten auf dem Layer 2 übertragen werden. Ein Frame enthält normalerweise Header-Informationen (z. B. Quell- und Zieladresse) sowie Nutzdaten. Der Layer 2 fügt dem Frame Steuerinformationen hinzu, um die Übertragung und den Empfang der Daten zu ermöglichen.