
### Verbindungsorientierte Protokolle
Protokolle bauen auf gesicherter Übertragung der Transportschicht auf. (TCP)

##### Beispiel Verbindungsorientierte Protokolle
- [[HTTP]]
- [[SMTP]]
- [[IMAP]]
- [[FTP]]



### Verbindungslose Protokolle
Protokolle erfordern keinen Aufbau einer gesicherten Übertragung auf der Transportschicht

##### Beispiel Verbindungslose Protokolle
- [[DHCP]]
- [[RTP]]
- [[SIP]]


### Gemischte Protokolle
Sowohl verbindungslose als auch verbindungsorientierte Kommunikation

##### Beispiel Gemischte Protokolle
- [[DNS]]



### Anforderungen an Anwendungsprotokolle
- <u>Paketverlust</u>: einige Anwendungen erfordern 100% Zuverlässigkeit, andere können einzelne Paketverluste tolerieren 
- <u>Durchsatz</u> (Bitrate): einige Anwendungen (Video) erfordern minimale Bitrate, andere nutzen die verfügbare Bitrate so gut es geht (sog. „best effort“) 
- <u>Delay</u> (Verzögerung, Latenz): einige Anwendungen (Internettelefonie, Gaming) erfordern geringes  Delay, Abweichung des Delays während der Übertragung (Jitter) 
- davon abhängig <u>Verlässlichkeit</u>: Auswahl des Transportprotokolls  
	- z.B. UDP im Gegensatz zu TCP: verbindungslos, kein Verbindungsaufbau (damit schnellerer Beginn der Datenübertragung), keine Fehler-/Flusskontrolle 
- <u>Sicherheit</u>: Verschlüsselung, Datensicherheit → SSL/TLS 

![[Pasted image 20230716153243.png]]

