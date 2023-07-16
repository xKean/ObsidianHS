1. Adressanfrage: Wenn ein Gerät Daten an eine IP-Adresse senden möchte, aber die zugehörige MAC-Adresse nicht kennt, sendet es eine ARP-Anfrage (ARP Request) als Broadcast-Paket an das lokale Netzwerk. Die ARP-Anfrage enthält die IP-Adresse des Zielgeräts.

2. Adressauflösung: Die ARP-Anfrage wird von allen Geräten im Netzwerk empfangen. Das Gerät mit der angefragten IP-Adresse erkennt die Anfrage und sendet eine ARP-Antwort (ARP Reply) an den Absender. Die ARP-Antwort enthält die MAC-Adresse des Geräts.

3. Aktualisierung der ARP-Tabelle: Nach Erhalt der ARP-Antwort aktualisiert das sendende Gerät seine ARP-Tabelle, in der die Zuordnung von IP-Adressen zu MAC-Adressen gespeichert ist. Dadurch wird zukünftig eine direkte Kommunikation mit dem Zielgerät ermöglicht, da die MAC-Adresse bekannt ist.

4. Cache für Adressauflösung: Um die Effizienz zu steigern, speichert jedes Gerät eine ARP-Tabelle mit den IP- und MAC-Adressen von kürzlich aufgelösten Geräten. Dadurch müssen nicht bei jeder Kommunikation ARP-Anfragen gesendet werden, sondern die Tabelle kann für die Adressauflösung genutzt werden.

5. Aktualisierung und Ablauf der Einträge: Die Einträge in der ARP-Tabelle werden regelmäßig aktualisiert, um sicherzustellen, dass die IP-MAC-Zuordnungen korrekt sind. Einträge können auch ablaufen, wenn sie längere Zeit nicht genutzt wurden oder wenn die Netzwerkverbindung geändert wurde.