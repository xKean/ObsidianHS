Flooding & Filtering

Die folgende Abbildung zeigt die Layer-2-Weiterleitungstabellen mehrerer Switches.
	1. Fügen Sie die Einträge in den im Bild genannten Tabellen ein, die beim Versand eines Frames von Client A an Client B hinzukommen.
	2. An welchen Port übermittelt Switch 3 das Frame?
	4. Welchen Teil der Kommunikation zwischen A und B bekommt der Router C ebenfalls zugesendet, und welchen nicht?
	5. Nennen Sie Beispiele für weitere Spalten einer L2-Weiterleitungstabelle und deren Aufgaben.
	![[Pasted image 20230705125809.png]]

Client A übertragt an Client B. Das hört der Switch 1 and Port 1. Da er aber nicht weiß, wo die Adresse bb liegt, flooded er alle seine Ports mit dem Frame. Gleichzeitig trägt er in seine Tabelle folgende Zeile ein: MAC: aa, Port: 1.
Nun erhält Switch 2 das Frame auf Port 6 und fügt in seiner Tabelle ein: MAC: aa, Port: 6. Da er aber widerrum die MAC bb nicht kennt, flooded auch er seine Ports (hier 1 und 7) mit der Adresse. Hier hört also insbesondere auch der Router die Kommunikation. 
Nun erhält Switch 3 das Frame auf Port 3 und fügt in seiner Tablle eine: MAC: aa, Port: 3. Er kennt widerrum bb nicht, also flooded er seine Ports. 
Sollte bb nun eine Antwort an aa schicken, würde die Switches filtern, da sie alle aa kennen.

Weitere Spalten wären z.B. die Spalte Timeout (Überlebenslänge der Tabellenzeile) oder FLAGS (für z.B. VLANs etc.)

Weitere Beispiele: ![[Pasted image 20230716121952.png]]
![[Pasted image 20230716122013.png]]
