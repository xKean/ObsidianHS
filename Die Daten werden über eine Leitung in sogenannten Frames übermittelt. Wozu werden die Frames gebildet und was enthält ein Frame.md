![[Pasted image 20230716105911.png]]

- Jede Schicht hat einen Header, wobei Header + Nutzdaten = Protokolldateneinheit. 
- Jede Schicht betrachtet nur ihren Header, der Rest sind Nutzdaten
- IP-Pakete nicht auf Leitung versendbar
	- Fehlende Regelung für Synchro
- Also Einbettung der IP-Pakete in Data Link Frames
- Header + Trailer für Synchro von Sender und Empfänger (Medienzugriff), in Header zusätzlich Adressen
- Der Header enthält Steuerinformationen
- Der Trailer ist der Abschlussteil des Frames und enthält einen Prüfwert zur Fehlererkennung