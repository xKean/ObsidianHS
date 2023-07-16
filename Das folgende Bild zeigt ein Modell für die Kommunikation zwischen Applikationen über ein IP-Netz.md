![[Pasted image 20230716154924.png]]

- F1: Erläutern Sie die wichtigsten Prinzipien der Datenübermittlung zwischen X und Y
 - ???
- F2: Erläutern Sie die Prinzipien der Kommunikation zwischen den beiden Applikationen,
falls UDP als Transportprotokoll eingesetzt wird.
 - Eine Transport-Instanz (T-Instanz) mit UDP sendet eine Nachricht an ihre Partner-T-Instanz, ohne vorher eine Beziehung (Verbindung) zu ihr aufzubauen. Der Empfang der Nachricht wird nicht bestätigt. Es handelt sich hierbei um eine ungesicherte Übermittlung von Nachrichten.
- F3: Erläutern Sie die Prinzipien der Kommunikation zwischen den beiden Applikationen,
falls TCP als Transportprotokoll eingesetzt wird.
 - Eine T-Instanz mit TCP baut zuerst eine Beziehung (Verbindung) zu ihrer Partner-T-Instanz auf und sendet erst danach an diese Daten. Der Empfang der Daten wird bestätigt. Es handelt sich hierbei um eine gesicherte Übermittlung von Daten.