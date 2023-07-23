↘Safe 
	↘Der Aufruf dieser Operation hat keine Nebenwirkungen. 
	↘Ressource erfährt durch den Abruf keine Änderung 

↘Idempotent 
	↘Das mehrfache Aufrufen dieser Operation liefert immer das gleiche Ergebnis.



↘GET 
	↘Anforderung einer Ressource 
	↘Webservice liefert die Repräsentation einer Ressource 
	↘Ist safe und idempotent 
	
↘POST 
	↘Erzeugt eine oder mehrere Ressourcen deren URIs noch nicht bekannt sind. 
	↘Bietet die meiste Flexibilität, da sie weder safe noch idempotent ist 
	
↘Daneben gibt es noch: 
	↘HEAD, PUT, DELETE, CONNECT, OPTIONS, TRACE und PATCH



↘PUT 
	↘Aktualisierung einer Ressource 
	↘Sollte die Ressource nicht existieren, wird sie unter der URI angelegt 
	↘Die Ressource wird vom Consumer in einer gültigen Repräsentation gesendet und ersetzt die bestehende Ressource 
	↘Ist idempotent 
	
↘PATCH 
	↘Modifiziert nur einen Teil der angegebenen Ressource 
	↘Gegenüber der HTTP Methode PUT wird die Ressource nicht komplett überschrieben 
	↘Ist weder safe noch idempotent


↘DELETE 
	↘Löschen einer Ressource 
	↘Falls die Ressource nicht existiert, wird kein Fehler ausgelöst, da das gewünschte Ergebnis schon erreicht ist. 
	↘Die Ressource darf nicht mehr unter der ursprünglichen URI geliefert werden. 
	↘Das mehrfache Löschen darf keinen Fehler liefern. 
	↘Ist idempotent 
	
↘HEAD 
	↘Fragt den HTTP-Header zu einer identifizierten Ressource ab. 
	↘Liefert den gleichen Header, wie die HTTP Methode GET, nur ohne Daten. 
	↘Ist safe und idempotent

↘OPTIONS 
	↘Liefert die HTTP Methoden, welche auf der identifizierten Ressource zur Verfügung stehen. 
	↘Ist idempotent 
	
↘TRACE 
	↘Liefert die Anfrage so zurück, wie der Server sie empfangen hat. So kann überprüft werden, ob und wie die Anfrage auf dem Weg zum Server verändert worden ist. 
	↘Liefert den gleichen Header, wie die HTTP Methode GET, nur ohne Daten. 
	↘Ist idempotent