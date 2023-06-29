---
dg-publish: true
---

### Definition

Mirror Ports oder Port Mirroring ist eine Funktion von Netzwerk-Switches, bei der der Datenverkehr, der über einen oder mehrere Ports läuft, kopiert und auf einen anderen, speziell dafür vorgesehenen Port (Mirror Port) weitergeleitet wird. Dies ermöglicht die Überwachung und Analyse des Netzwerkverkehrs, ohne den normalen Datenfluss zu stören.


Mirror-Ports müssen mindestens die Datenrate der gesamten gemonitorten Ports aufweisen. (duplex!)
Das bedeutet, dass man für das mirroring von einem 100 Mbit Port einen **200** Mbit Mirror-Port braucht. (Senden des Überwachten Ports = 100 Mbit + Empfangen des Überwachten Ports = 100 Mbit)