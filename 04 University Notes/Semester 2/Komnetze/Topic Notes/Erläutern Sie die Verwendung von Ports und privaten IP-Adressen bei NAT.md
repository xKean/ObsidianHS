1. Bei der Netzwerkadressübersetzung (Network Address Translation, NAT) werden Ports und private IP-Adressen verwendet, um den Datenverkehr zwischen einem privaten Netzwerk und dem öffentlichen Internet zu verwalten.

Ports dienen zur Unterscheidung und Weiterleitung von Netzwerkdaten auf der Transportschicht (z.B. TCP oder UDP). Ein Port ist eine numerische Adresse innerhalb einer IP-Adresse, die den Zielprozess auf einem Gerät identifiziert. Durch die Verwendung von Ports kann NAT mehrere Geräte innerhalb eines privaten Netzwerks über eine einzige öffentliche IP-Adresse ansprechen.

Wenn Daten aus dem privaten Netzwerk an das Internet gesendet werden, ändert der NAT-Gerät (z.B. ein Router) die Quellportnummer jedes ausgehenden Pakets. Dadurch wird sichergestellt, dass die Antworten des Internetdienstes zum richtigen Gerät im privaten Netzwerk zurückgeleitet werden können.

Beim Empfang von Daten aus dem Internet analysiert das NAT-Gerät die Zielportnummer jedes eingehenden Pakets und leitet es an das entsprechende Gerät im privaten Netzwerk weiter, basierend auf den internen Portzuordnungen.

2. Wenn Geräte im privaten Netzwerk eine Verbindung zum Internet herstellen, verwendet NAT eine öffentliche IP-Adresse, um den gesamten ausgehenden Datenverkehr des privaten Netzwerks zu repräsentieren. Dabei erfolgt eine Übersetzung der privaten IP-Adressen in die öffentliche IP-Adresse.

Wenn eine Antwort aus dem Internet zurückkommt, übersetzt das NAT-Gerät die öffentliche IP-Adresse in die entsprechende private IP-Adresse und leitet die Daten an das entsprechende Gerät im privaten Netzwerk weiter.

Die Kombination aus Ports und privaten IP-Adressen ermöglicht es NAT, mehrere Geräte im privaten Netzwerk mit einer einzigen öffentlichen IP-Adresse zu verbinden und den Datenverkehr ordnungsgemäß weiterzuleiten. Dadurch wird die Anzahl der benötigten öffentlichen IP-Adressen reduziert und die Sicherheit und Effizienz des Netzwerks verbessert.