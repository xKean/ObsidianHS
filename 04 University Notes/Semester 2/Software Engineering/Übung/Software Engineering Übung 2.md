---
dg-publish: true
---

Tandem: Jan Niklas Witzel, Maximilian Hickisch, Peter Braun

### Aufgabe 1 : Projekt Papierflieger

#### V-Modell:
![[Pasted image 20230427140207.png]]

#### Liste der Anforderungen:
- geradeaus gleiten
- Stabiler Flug

#### Testspezifikation des Systems:
- Wir benutzen eine Abschusskonstruktion für den Papierflieger. Dies hilft dabei, Anwenderfehler zu vermeiden.

#### Systemarchitektur:
- Gerade Faltlinien
- Symmetrische Faltungen
- Gerade schnitte

#### Testspezifikationen der Module:
- Saubere Schnittkante prüfen, Scharfe Schere
- Spiegelt sich meine Faltung? Ist sie symmetrisch und liegen die Kanten aufeinander?
- Gibt es Überstände ?

#### Abnahme Report
- Der Papierflieger fliegt gut und erfüllt die Anforderungen.


### Aufgabe 2

a. Inkrementelle Entwicklung ist für Geschäftssysteme effektiv, weil sie Flexibilität bietet, Risiken mindert, schnelleren Return on Investment ermöglicht und die Qualitätssicherung verbessert. Außerdem können bei der Programmierung kosten gespart werden, da man nicht an einer fertigen Software gearbeitet wird, sondern man dauerhaft im Entwicklungsprozess ist.

b. Das inkrementelle Modell ist für Echtzeitsysteme weniger geeignet, da es strikte Anforderungen, Integrität, Konsistenz und den höheren Test- und Validierungsaufwand nicht optimal berücksichtigt.
Ein Echtzeitsystem muss bei der ersten Auslieferung bereits bestimmte Anforderungen erfüllen, da die Funktionalität sonst nicht gewährleistet werden kann.

Beispiel Motorsteuerung Auto:
- Die Software muss den Motor vollkommen steuern können, nicht nur den Start.


### Aufgabe 3 
Die Notwendigkeit für die zwei Aktivitäten ergibt sich daraus, dass auf ein bereits vorhandenes System zurückgegriffen wird. Zunächst muss also der Status qou analysiert werden und entschieden werden welche Teile dieser Software recycelt werden können. Anschließend muss untersucht werden, inwieweit die Anforderung  an die vorgefundenen Funktionalitäten dieser Software angepasst werden müssen.