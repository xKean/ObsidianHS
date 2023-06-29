---
dg-publish: true
---
Express setup in Vorlesungsfolien



### Dateien

#### bin/www
Globale Einstellungen


#### app.js
Routen setzen, views, imports mit `app.use`


#### routes/name.js
Hier wird definiert was der router actually holt, request params, Titel

Routing wird immer in Reihenfolge von Einbindung druchgeführt. Erster "treffer" führt zur Antwort für den User. Beispiel mit `/users` - Controller und `/users` - Route.

Routing wird immer durchgeführt von `localhost/routername/command`


#### views/name.ejs
Basically superpowered html