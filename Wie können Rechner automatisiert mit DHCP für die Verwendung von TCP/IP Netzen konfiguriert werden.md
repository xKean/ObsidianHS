Endsysteme, die DHCP verwenden, können durch dieses Protokoll automatisch IP-Adressen und andere Parameter für eine oder begrenzte Zeit zugewiesen bekommen. Sonst müssten IP-Konfigurationen (IP-Adresse, Gateway, DNS-Server) manuell eingetragen werden.

1. Der Client sendet **DHCP-Discover** in einem sogenannten IP-Broadcast Paket (Ziel-IP-Adresse = 255.255.255.255 (Broadcast an alle im Netz)) als Anforderung, um von einem Server die Konfigurationsparameter (IP-Adresse, Subnet Mask) zu bekommen.
2. Jeder DHCP-Server kann mit **DHCP-OFFER** dem Client sein Angebot zukommen lassen.
3. Der Client wählt z.B. das erste Angebot aus und sendet eine Broadcast Nachricht **DHCP-REQUEST**, um das ausgewählte Angebot anzufordern. der ausgewählte Server antwortet mit **DHCP-ACK**.