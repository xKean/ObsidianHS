#### Aufgaben
- Verschlüsselung von übertragenen Segmenten  (Vetraulichkeit)
- Integrität der Segmente durch Hashes (Prüfsummen)
- Endpunkt Authentifikation


##### Realisierung der Verschlüsselung
- Jeder Client mit TLS hat einen öffentlichen und privaten Schlüssel ![[Pasted image 20230716192146.png]]
- mit öffentlichem Schlüssel verschlüsselte Daten nur mit privatem Schlüssel entschlüsselbar
- Zertifikat beinhaltet digitale Signierung des öffentlichen Schlüssels durch vertrauenswürdigen Dritten
- Peter will Jan was schicken: 
	- Dafür nimmt er meinen öffentlichen Schlüssel und verschlüsselt die Nachricht mit diesem
	- Das sendet er mir und die Nachricht kann nur mit meinem privaten Schlüssel entschlüsselt werden

#### Wie sicher ist TLS?
- Basiert auf Geheimhaltung der Schlüssel und auf dem Vertrauen in Zertifizierungsstellen (wie Let's Encrypt)
- Verbesserung: Public Key Pinning, HTTP Strict Transport Security