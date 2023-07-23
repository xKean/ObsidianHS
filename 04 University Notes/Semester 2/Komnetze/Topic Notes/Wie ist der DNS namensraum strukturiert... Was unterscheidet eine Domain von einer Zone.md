Bei DNS handelt es sich um eine baumförmige weltweite Vernetzung von einzelnen Name-Servern, die eine weltweit verteilte **DNS-Datenbank** bilden. Jedes Datenelement in der DS-Datenbank ist über einen **Namen** indiziert. **Diese Namen sind im Grunde genommen nur Pfade** in einem großen Baum. Dieser Baum besitzt oben eine einzige Wurzel (Root).

Jeder **Knoten** repräsentiert eine **Domain (Domäne)** und stellt einen Teil der gesamten Datenbank dar, vgl. mit einem Verzeichnis eines Dateisystems. Jede Domain kann in weitere Teile untergliedert werden. der vollständige Domain-Name im Baum besteht aus den Namen der einzelnen Knoten bis zur Root. Dies bedeutet, dass sich der Name eines Knotens aus den Namen im Pfad zusammensetzt, wobei diese Namen durch einen Punkt voneinander getrennt werden. Zum Beispiel setzt sich der Domain-Name **hs-fulda.de** aus den Namensbestandteilen **hs-fulda** und **de** zusammen. 

Ein Name-Server stellt einen dedizierten Rechner dar, in dem die Informationen (als **Ressource Records**) über den Domain-Namensraum gespeichert werden.
![[Pasted image 20230712135450.png]]

Name-Server verwalten den Namensraum innerhalb einer Domain (als **Ressource Records**). Zusammengesetzt ergeben die Resource Records der Domains den eindeutigen "**Fully Qualified Domain Name**" (FQDN) eines Hosts z.B. sonne.informatik.hs-fulda.de.

Das Aufteilen einer Domain in Zonen und Subdomains hat den Vorteil, Verwaltungsaufgaben verschiedenen organisatorischen Gruppen zuordnen zu können. Z.B. übergibt die Organisation HS Fulda die Verantwortung für die e der Subdomain informatik.hs-fulda.de an den Fachbereich AI. Der Name-Server der Zone hs-fulda.de enthält Verweise auf entsprechende Namen und Daten in den einzelnen Subdomains.

Je Zone existiert mindestens ein [[autorativer Name-Server]], der nach Namen in dieser Domain gefragt werden darf. Mehrere Server pro Zone sind möglich.