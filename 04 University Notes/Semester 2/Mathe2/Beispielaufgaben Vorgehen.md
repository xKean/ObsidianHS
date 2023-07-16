Hier findet hier einmal meine Vorgehensbeschreibung zu den einzelnen Aufgaben aus den Beispielaufgaben. Die Lösungen hat Frau Radl hochgeladen, ich hab sie aber auch ins Obsidian hochgeladen und ganz unten auf dieser Seite verlinkt.
1. Aufgabe: Komplexe Zahlen
![[Pasted image 20230707174124.png]]
<details> <summary>Allgemeines Vorgehen</summary> <p>1. Normale Koordinatensystem mit zwei Achsen zeichnen. x-Achse ist der Re-Teil und y-Achse der Im-Teil der komplexen Zahl.</p>
<p>2. Die Mengen jeweils verstehen versuchen. Entweder mit konkreten Beispielen, wie: wie muss mein Im-Teil aussehen, wenn er immer größer als 1 sein soll etc. ODER rechnerisch umformen (z.B. den Betrag auflösen etc.)</p>
</details>
<details> <summary>Lösungsvorgehen bei der Beispielaufgabe</summary> <p>(i) Zunächst die Menge hinten umformen, sodass dort die Differenz von zwei komplexen Zahlen steht, das bedeutet steht der Abstand zwischen diesen beiden komplexen Zahlen. Dann steht dort der Abstand von unseren Zahlen zu der Zahl -1+i ist stets kleiner bzw. gleich 1 => Die Menge ist ein Kreis mit Radius 1, um den Mittelpunkt (-1|+1).</p>
<p>(ii) Der Re-Teil muss immer größer bzw. gleich sein als der Im-Teil: Wenn beide gleich wären, wäre dies genau die Winkelhalbierender zwischen x- und y-Achse. Da der Re-Teil aber größer oder gleich sein soll, ist es die gesamte Winkelhalbierende und alles rechts davon.</p>
</details>

![[Pasted image 20230707181148.png]]
<details> <summary>Allgemeines Vorgehen</summary> <p>1. Die Zahl mit dem komplex Konjugiertem der komplexen Zahl aus dem Nenner erweitern. </p>
<p> Danach solange umformen und auseinander ziehen, bis die Form a+bi erreicht ist. </p>
</details>

![[Pasted image 20230707181526.png]]
<details> <summary>Allgemeines Vorgehen</summary> <p>1. r bestimmen: r = |z|  </p>
<p> 2. φ bestimmen: s. Vorlesung für die Formel (auf das Blatt!)</p>
</details>


2. Aufgabe: Relationen
	![[Pasted image 20230707181830.png]]
<details> <summary>Allgemeines Vorgehen</summary>
<p> Sich überlegen, was die Relation macht. Bei der a) dann ein entsprechendes Beispiel sich ausdenken an Zahlen aus der Menge, auf der die Relation gelten soll (hier Natürliche Zahlen), die die Bedingung der Relation (hier a+b ungerade) erfüllen.</p>
<p> Bei den Eigenschaften die Definitionen der Eigenschaften durchgehen und prüfen, ob diese für diese Relation zutreffen. </p>
</details>

3. Aufgabe: Lineare Gleichungssysteme (LGS):
	![[Pasted image 20230707182038.png]]
<details> <summary>Allgemeines Vorgehen</summary>
<p>1. Das LGS als erweiterte Koeffizentenmatrix schreiben: (A|b), wobei b der Lösungsvektor, also hier (2,4) ist. </p>
<p> 2. Das LGS mit Gauß auf Zeilenstufenform bringen (Treppe)</p>
<p> 3. Das LGS mit Rückeinsetzen lösen (die Lösungen nach und nach ausrechnen) </p>
<p> Sonderfälle: Wenn das LGS unterbestimmt ist, also weniger Gleichungen als Unbekannte (hier 4 Unbekannte nur 2 Gleichungen), können die fehlenden Gleichungen als Nullzeilen gedacht werden. Nullzeilen bedeuten immer, dass für jede Nullzeile eine der Variablen frei gewählt werden kann, z.B. z = r, wobei r eine reelle Zahl ist -> immer mit angeben, was für eine Zahl r dann sein darf. Das LGS hat dann immer unendlich viele Lösungen. Zur Struktur der Lösungsmenge, siehe nächste Aufgabe.</p>
</details>

![[Pasted image 20230707182428.png]]

<details> <summary>Allgemeines Vorgehen</summary>
<p>1. Zunächst das LGS wieder als Matrix schreiben (A | b) und in Zeilenstufenform bringen (wenn nötig).</p>
<p> 2. Dann den Rang der Matrix A und den Rang der erweiterten Koeffizentenmatrix (A|b) ablesen. Der Rang ist hierbei die Anzahl Zeilen, in denen nicht alle Einträge 0 sind. Der Rang von (A|b) ist hier immer 3, da im Lösungsvektor nie eine 0 auftreten kann. </p>
<p> 3. Es gelten folgende Kriterien für die Lösbarkeit eines LGS der Struktur Ax = b (also wie hier): <br>
(i) Das LGS hat keine Lösung, wenn Rang (A) != Rang (A|b). <br>
(ii) Das LGS hat genau eine Lösung, wenn Rang (A) = Rang (A|b) und Rang(A) = Rang (A|b) = Anzahl Variablen/Unbekannte (hier 3). <br>
(iii) Das LGS hat unendlich viele Lösungen, wenn Rang (A) = Rang (A|b) und Rang (A) = Rang (A|b) kleiner Anzahl Variablen. </p>
<p>Mit diesem Wissen entsprechend die Möglichkeiten für die Ränge und in diesem Fall α durchgehen. </p>
</details> 




















5. Ist $B = \{b_1, b_2, b_3\}$ eine Basis vom $\mathbb{R}^3.$?
	1.  Lösung: Da Dim von $\mathbb{R}^3$  = 3, reicht zu zeigen, dass $b_1, b_2, b_3$ linear unabhängig sind. 
6. Sind $b_1,b_2,b_3$ linear unabhängig?
	1. Lösung: Die drei Vektoren als Matrix A schreiben. Wenn es eine quadratische Matrix ist: Determinante bestimmen. Ist die Determinante $\neq$ 0, sind die Vektoren linear unabhängig.
	2. Wenn es keine quadratische Matrix ist, löse das LGS (A|0).
7. Handelt es sich um bei f eine lineare Abbildung von $\mathbb{R}^3$ $->$ $\mathbb{R}^3$?
	1. Lösung: die zwei Eigenschaften einer linearen Abbildung überprüfen:
		1. Homogenität: $f(λx) = λf(x)$         λ $\in$ $\mathbb{R}$, x $\in$ $\mathbb{R}^3$
		2. Additivität: $f(x+y) = f(x) + f(y)$    x, y $\in$  $\mathbb{R}^3$
8. <details> <summary>Short Summary</summary> <p>text to hide</p> </details>
9. 