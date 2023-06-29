---
dg-publish: true
---


## Komplexe Zahlen
### Komplex Konjugiert
#### Notation:

$\overline {z_1}$

Hier wird  ""+ und - zwischen Realteil und Imaginärteil umgedreht.

#### Beispiel
$2^{3} \sqrt3$
$z_1 = \sqrt3 − i$
$\overline z_{1}= \sqrt3 + i$

### Betrag
Bei
$z = x + yi$
$|z|  = \sqrt {x^{2}+ y^{2}}$

### Multiplizieren
Es wird alles mit allem multipliziert wie bei normalen Zahlen. (Klammern ausmultiplizieren)
Dabei ist darauf zu achten, dass $i^{2} = -1$

### Umgang mit i
$i^{2}= -1$
$i^{3}= -i$
$i^{4}= 1$
$i^{5}= i$



## Binäre Relationen
Bei einer Relation $R \subseteq A \times B$
### Linkstotal
Jedes Element aus $A$ hat <u>mindestens einen</u> Partner in $B$.
### Rechtstotal
Jedes Element aus $B$ hat <u>mindestens einen</u> Partner in $A$.
### Linkseindeutig
Jedes Element aus $B$ hat <u>höchstens einen</u> Partner in $A$.
### Rechtseindeutig
Jedes Element aus $A$ hat <u>höchstens einen</u> Partner in $B$
## Definition Funktion
Bei einer Relation $R \subseteq A \times B$
Es ist eine "Abbildung" oder "Funktion" wenn die Relation [[Formelsammlung Mathe 2#Linkstotal|Linkstotal]] <u>und</u> [[Formelsammlung Mathe 2#Rechtseindeutig|Rechtseindeutig]] ist. Das heißt: "Jedem Element in A wird genau einem Element in B zugeordnet".


## Eigenschaften von Relationen
### Reflexiv
Wenn für alle $x \in M$ gilt: $x \sim_R x$ .
Das heißt: Jedes Element steht in Relation zu sich selbst.

#### Beispiel Vereinfacht:
- $a = a$ Gleichheitsrelation gilt immer
- Ich bin ich!

#### Beispiel:
- Die Kleiner-Gleich-Relation $\leq$  auf den reellen Zahlen ist reflexiv, da stets $x\leq x$ gilt. Sie ist darüber hinaus eine Totalordnung. Gleiches gilt für die Relation $\geq$.
- Die gewöhnliche Gleichheit $=$  auf den reellen Zahlen ist reflexiv, da stets $x=x$ gilt. Sie ist darüber hinaus eine Äquivalenzrelation.
- Die Teilmengenbeziehung $\subseteq$  zwischen Mengen ist reflexiv, da stets $A\subseteq A$ gilt.

### Irreflexiv
Wenn für alle $x \in M$ gilt: $x \nsim_R x$ .
Das heißt: Kein Element steht in Relation zu sich selbst.

#### Beispiel Vereinfacht:
- $\neg(a < a)$ Kleiner-Relation gilt nie.
- Es gibt keinen Sohn, der sein Vater ist.

#### Beispiel:
- Die Kleiner-Relation $<$  auf den reellen Zahlen ist irreflexiv, da nie $x<x$ gilt. Sie ist darüber hinaus eine strenge Totalordnung. Gleiches gilt für die Relation $>$ .
- Die Ungleichheit $\neq$  auf den reellen Zahlen ist irreflexiv, da nie $x\neq x$ gilt.
- Die echte Teilmengenbeziehung $\subset$  zwischen Mengen ist irreflexiv, da nie $A\subset A$ gilt. 

### Symmetrisch
Wenn für alle $x, y \in M$ gilt: Wenn $x \sim_R y$ gilt, dann gilt auch $y \sim_R x$
Das heißt: Wenn das eine Element zum anderen eine Relation hat, hat auch das andere zum einen eine Relation.

#### Beispiel Vereinfacht:
- $a = b ⇒ b = a$
- Ich bin Sohn von Paul. ⇒ Paul ist mein Vater.

#### Beispiel:
- Die gewöhnliche Gleichheit = auf den reellen Zahlen ist symmetrisch, denn aus $x=y$ folgt $y=x$. Sie ist darüber hinaus eine Äquivalenzrelation.

- Die Ungleichheitsrelation $\neq$  auf den reellen Zahlen ist zwar keine Äquivalenzrelation, aber ebenfalls symmetrisch, denn aus $x\neq y$ folgt $y\neq x$.

### Asymmetrisch
Wenn für alle $x, y \in M$ gilt: Aus $x \sim_R y$ folgt $y \nsim_R x$
Das heißt: Es gibt in der Relation kein Paar $x,y$ für das auch die Umkehrung gilt.
Jede Asymmetrische Funktion ist auch [[Formelsammlung Mathe 2#Antisymmetrisch|Antisymmetrisch]].

#### Beispiel Vereinfacht:
- $a > b ⇒ b > a$ ⚡
- Ich bin Sohn meines Vaters. ⇒ Mein Vater mein Sohn. ⚡

#### Beispiel
- Die Relation $<$ „ist (echt) kleiner als“ auf den reellen Zahlen, die darüber hinaus eine strenge Totalordnung ist. Gleiches gilt für die Relation $>$  „ist (echt) größer als“.
- Die Relation $\subset$  „ist echte Teilmenge von“ und ebenfalls die Relation $\supset$  „ist echte Obermenge von“ als Beziehungen zwischen Mengen. Sie sind in einem System von Mengen oder von Teilmengen einer gegebenen Menge darüber hinaus eine strenge Halbordnung.

### Transitiv
Wenn für alle $x,y,z \in M$ gilt: Wenn $x \sim_R y$ und $y \sim_{R}z$ gilt, dann gilt auch $x \sim_R z$ 

#### Beispiel Vereinfacht:
- $(a > b) ∧ (b > c) ⇒ a > c$
- Paul ist Vorfahre von Peter und Peter ist Vorfahre von Ernst. ⇒ Paul ist Vorfahre von Ernst.

#### Beispiel:
- Die gewöhnliche Gleichheit $=$  auf den reellen Zahlen ist transitiv, denn aus$ x=y$ und $y=z$ folgt $x=z$. Sie ist darüber hinaus eine Äquivalenzrelation.
- Die Ungleichheitsrelation $\neq$  auf den reellen Zahlen ist hingegen nicht transitiv: $3\neq 5$ und $5\neq 3$, aber $3\neq 3$ gilt natürlich nicht ⚡.

### Antisymmetrisch
Wenn für alle $x,y \in M$ gilt: Aus $x \sim_R y$ und $y \sim_{R}x$ folgt $x=y$
Das heißt: Wenn X eine Relation zu Y hat und Y eine Relation zu X hat, dann ist $x = y$

#### Beispiel Vereinfacht:
- $a ≥ b ∧ b ≥ a ⇒ a = b$

#### Beispiel:
- Antisymmetrisch sind die Relationen $\leq$  und $\geq$  auf den reellen Zahlen. Aus $x\leq y$ und $y \le x$ folgt $x=y$. Das Gleiche gilt für $x\geq y$ und $y\geq x$.

- Auch die Teilbarkeitsrelation $\mid$ für natürliche Zahlen ist antisymmetrisch, denn aus $a\mid b$ und $b\mid a$ folgt $a=b$. Die Teilbarkeit auf den ganzen Zahlen ist hingegen nicht antisymmetrisch, weil beispielsweise $3\mid -3$ und $-3\mid 3$ gilt, obwohl $-3\neq 3$.


### Websites die hier gut geholfen haben:
[Reflexive Relation](https://www.biancahoegel.de/mathe/relation/relation_reflexiv.html und weitere Unterseiten

[Eigenschaften von Relationen - Matheretter](https://www.matheretter.de/wiki/eigenschaften-relationen) - Einfache Beispiele, gut verständlich