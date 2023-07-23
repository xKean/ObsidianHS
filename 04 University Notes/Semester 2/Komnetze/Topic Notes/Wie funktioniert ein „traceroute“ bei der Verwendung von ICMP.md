1. Der "traceroute"-Befehl wird gestartet und das Zielziel (Host oder IP-Adresse) wird angegeben.

2. Der Ausgangsrechner sendet ein ICMP Echo Request-Paket mit einer Time-to-Live (TTL) von 1 an das Zielziel. Die TTL gibt an, wie viele Netzwerkhops das Paket passieren kann, bevor es verworfen wird.

3. Das erste Router-Gateway auf dem Weg zum Zielziel empfängt das ICMP-Paket. Da die TTL auf 1 eingestellt ist und das Paket den Router erreicht hat, wird die TTL um 1 verringert, und der Router sendet ein ICMP Time Exceeded-Paket zurück an den Ausgangsrechner.

4. Der Ausgangsrechner erhält das ICMP Time Exceeded-Paket und erkennt den Router, von dem das Paket stammt. Die Zeit für die Runde-Reise (Round-Trip Time, RTT) wird ebenfalls gemessen und angezeigt.

5. Der "traceroute" erhöht die TTL um 1 und sendet ein neues ICMP Echo Request-Paket mit der erhöhten TTL. Dadurch wird das nächste Hop auf dem Weg zum Zielziel erreicht.

6. Schritte 3 bis 5 werden wiederholt, bis das ICMP Echo Request-Paket das Zielziel erreicht und eine ICMP Echo Reply-Nachricht zurückgesendet wird.

7. Der "traceroute" zeigt die Liste der Router (Hops) entlang des Pfades zum Zielziel an, basierend auf den empfangenen ICMP Time Exceeded-Nachrichten. Die RTT-Werte für jede Hops werden ebenfalls angezeigt.