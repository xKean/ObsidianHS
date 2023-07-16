Diese Schicht übernimmt die Fehler-/Flusskontrolle sowie die logische Verbindungskontrolle. 

Ausführlich:
1. Logische Verbindungskontrolle: Die LLC-Schicht ermöglicht die Einrichtung, Aufrechterhaltung und Beendigung logischer Verbindungen zwischen Endpunkten im Netzwerk. Dies umfasst die Identifizierung und Adressierung von Endpunkten, die Synchronisierung des Datenflusses und die Verwaltung von Verbindungsstatusinformationen.
    
2. Rahmenkapselung: Die LLC-Schicht nimmt die Daten von der darüber liegenden Schicht, dem Network Layer, entgegen und verpackt sie in Frames für die Übertragung über das physische Medium. Sie fügt dem Frame Header-Informationen hinzu, z. B. Kontrollbits, Quell- und Zieladressen sowie Prüfsummen zur Fehlererkennung.
    
3. Fehlerkontrolle: Die LLC-Schicht stellt sicher, dass die übertragenen Frames fehlerfrei sind. Hierzu verwendet sie Fehlererkennungstechniken wie CRC (Cyclic Redundancy Check), um die Integrität der Daten zu überprüfen. Bei Erkennung von Fehlern können entsprechende Maßnahmen ergriffen werden, z. B. die Anforderung einer erneuten Übertragung des fehlerhaften Frames.
    
4. Flusskontrolle: Die LLC-Schicht unterstützt die Flusskontrolle, um sicherzustellen, dass der Datenverkehr zwischen Sender und Empfänger ausgeglichen ist. Durch die Verwendung von Kontrollsignalen oder -mechanismen kann die LLC-Schicht sicherstellen, dass der Sender die Daten nicht schneller sendet, als der Empfänger sie verarbeiten kann, um einen Pufferüberlauf zu vermeiden.