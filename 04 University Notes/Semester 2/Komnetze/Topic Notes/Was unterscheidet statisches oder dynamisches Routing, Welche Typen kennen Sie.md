1. Statisches Routing: Manuelle Konfiguration der Routing-Tabellen durch den Administrator, geeignet für kleine Netzwerke mit einfacher Topologie und geringer Anzahl von Routern, weniger Bandbreiten- und Rechenleistungsanforderungen, bietet volle Kontrolle, aber erfordert manuelle Aktualisierung.

Dynamisches Routing: Automatische Berechnung und Aktualisierung der Routing-Tabellen durch Routerprotokolle, geeignet für komplexe Netzwerke, gute Anpassungsfähigkeit an Netzwerkänderungen, höhere Bandbreiten- und Rechenleistungsanforderungen, bietet Flexibilität, aber kann zu Konvergenzproblemen führen.

2. Distanz-Vektor (sowie Distanz-Pfad)

- Router kennt Nachbar-Router und Link-Kosten

- Iterativer Austausch von Nachbar-Routern über Netz (auch von Fehlern!)

- Nachrichtenaustausch nur zwischen Nachbarn, dafür hohe Konvergenzzeit

- Routing-Schleifen möglich (z.B. Problem „Count to infinity“)

Link-State Routing-Protokolle

- Alle Router kennen komplette Topologie und deren Zustand („Link State“: Link up/down, Verzögerung, Auslastung, Kosten/Gebühren, …)

- Hohes Nachrichtenaufkommen im Gesamtnetz, dafür geringere Konvergenzzeit

- Routing-Fehler durch oszillierende Routen möglich

- Fehlerhafte Link-Kosten haben im Gegensatz zu Distanz-Vektor nur lokale Auswirkung