---
title: "Osterdatum im Kopf berechnen"
date: "2025-04-20"
tags: 
  - alle
  - kalender
  - calendar
  - ostern
  - mond
  - mondphase
  - vollmond
  - datum
  - gregorianisch
---

> **HINWEIS:** Bitte die Seite <u>**ein zweites Mal laden**</u>. Die Animationen laden momentan leider noch nicht, wie sie sollen.

## Einleitung

Ostern ist ein beweglicher Feiertag. Das Osterfest scheint von Jahr zu Jahr recht zufällig hin und her zu springen. Zu erklären warum und wie man das Osterdatum im Kopf berechnen kann, ist das Ziel dieses Artikels. 

Zunächst werde ich im Theorieteil die historischen, mathematischen und astronomischen (Ostern hat schließlich etwas mit den Mondphasen zu tun) erklären. Anschließend werde ich die Rechenmethode vorstellen, welche zu großen Teilen auf der [Osterformel von Carl Friedrich Gauß](https://de.wikipedia.org/wiki/Gau%C3%9Fsche_Osterformel) fußt und abschließend folgen noch ein paar Rechenbeispiele samt Empfehlungen für weiterführende Literatur.

Im Kapitel der Rechenmethode wird die Herkunft der verwendeten Formel zwar nicht explizit erklärt, jedoch finden sich im Theorieteil einige unterstrichene Zahlen. Die Theorie hinter diesen Zahlen liefert eine Idee, warum die Formeln, die diese Zahlen enthalten, so sind wie sie sind. 

## Theorie

### Sonnen- und Mondkalender

Die Erde bewegt sich in rund 365,242 Tagen einmal um die Sonne — auch *tropisches Jahr* genannt.
Das *Kalenderjahr* hat jedoch nur 365 Tage und ist damit etwas zu kurz. Aus diesem Grund wurden schon in dem von Julius Caesar eingeführten julianischen Kalender gelegentlich Schalttage eingefügt, um die durchschnittliche Länge des Kalenders näher an den tatsächlichen Wert zu bringen. Jedes vierte Jahr wurde der 29. Februar eingefügt. Damit betrug die durchschnittliche Länge des Kalenderjahres 365,25 Tage, was 365,242 Tagen sehr nahe kommt.

Der Mond durchläuft von Neumond zu Neumond verschiedene Phasen. Ein solcher Durchgang — auch *Lunation* genannt — dauert durchschnittlich 29,53 Tage. Diese Dauer nennt man *synodischer Monat*, bzw. für unsere Zwecke einfach *Mondmonat*. Bei der Osterberechnung, für die Mondphasen entscheidend sind, wird mit der Näherung 29,5 Tage (gerundet <u>**30 Tage**</u>) gerechnet.

Es fällt auf, dass 12 Mondmonate kürzer sind als 12 Monate, nämlich nur rund 354 Tage lang und damit gut **<u>11 Tage</u>** kürzer als ein Kalenderjahr.
Ist also an einem bestimmten Datum Neumond, so ist im darauffolgenden Jahr 11 Kalendertage früher Neumond. Im Kalender gesehen wandert der Mond quasi jedes Jahr um 11 Tage nach vorne (Richtung Jahresbeginn).

Interessanterweise sind **<u>19 Kalenderjahre</u>** beinahe genau so lang sind wie 235 Mondmonate.

$$\begin{align*}
19 \cdot 365,25 &= 6939,75 \text{\quad(19 Kalenderjahre)}\\
235 \cdot 29,53 &= 6939,55  \text{\quad(235 Mondmonate)}\\
\end{align*}$$

Das bedeutet, dass sich die Mondphasen alle 19 Kalenderjahre wieder (mehr oder weniger) genau an derselben Stelle im Kalender befinden. 


### Gregorianische Kalenderreform

So genau die Längen von Kalenderjahr und tropischem Jahr sowie von 19 Kalenderjahren und 235 Mondmonaten zusammenliegen, so sind sie doch nicht genau gleich. Und über die Jahrhunderte wurde dies zu einem immer größer werdenden Problem. 
Da das Kalenderjahr etwas zu lang ist, lief der Kalender im Jahr 1582 dem tatsächlichen Lauf der Sonne um volle 10 Tage hinterher. Auch die berechneten Mondphasen lagen 3 Tage von der tatsächlichen Mondphase entfernt.

Die von Papst Gregor XIII. in diesem Jahre angestoßene Kalenderreform sollte dies beheben. Den entstandenen *gregorianische Kalender* benutzen wir in dieser Form noch heute. 
Zur Korrektur des Sonnenjahres wurden einmalig 10 Tage ausgelassen und es werden fortan innerhalb eines Zeitraums von **<u>400 Jahren</u>** immer jeweils 3 Schalttage ausgelassen (z.&nbsp;B. sind die Jahre 1700, 1800, 1900 nach der neuen Regel keine Schaltjahre mehr, das Jahr 2000 hingegen bleibt ein Schaltjahr). 
Zur Korrektur der Mondzyklen setzte man den errechneten Mond einmalig um drei Tage zurück, um fortan den errechneten Mond alle **<u>300 Jahre</u>** um einen Tag zurückzusetzen. [^1]

### Rechengrundlagen

Bei der Berechnung des Osterdatums werden wir ein wenig rechnen müssen, jedoch wird nichts schwierigeres als die Grundrechenarten nötig sein. Im Folgenden werden ein paar Hinweise zur Schreibweise und Tipps zum einfacheren Rechnen gegeben. 

#### Division mit Rest 

Bei der Division mit Rest schreibt man sowohl auf, wie oft eine Zahl in eine andere "passt" und wie viel als Rest übrig bleibt, z.&nbsp;B.:

$100 \div 7 = {\color{blue}{14}} \text{ Rest } {\color{red}{2}}$

Es gibt in der Mathematik zwei verschiedene Schreibweisen, um jeweils nur das maximal passende Vielfache bzw. nur den Rest zu betrachten:

$\lfloor \frac{100}{7} \rfloor = {\color{blue}{14}}$

$100 \pmod{7} = {\color{red}{2}}$

Die zweite Schreibweise für den Rest wird $\text{modulo}$ ausgesprochen und man kann sich vorstellen, dass man in unserem Beispiel so lange $7$ von der $100$ abzieht, bis man eine positive Zahl erreicht hat, die kleiner als $7$ ist.

Da wir das Rechnen $\text{modulo } 19$ brauchen werden, schauen wir uns dies kurz genauer an. 

##### Rechnen $\text{modulo } 19$ 

Wenn man bei einer Zahl $19$ abzieht, so hat diese immer noch denselben Rest beim Teilen durch $19$ wie zuvor. Ähnlich wie man beim Zurückdrehen einer Uhr um 12 Stunden, wieder auf derselben Zahl landet. 

Natürlich kann man auch Vielfache von $19$ abziehen. So haben z.&nbsp;B. $260$ und $260-19$ denselben Rest $\text{modulo } 19$, aber auch $260$ und $260-190$. 

Letzteres können wir auch wie folgt darstellen:

$$
\begin{matrix}
  & 2 & 6 & 0 \\ 
\- & 1 & 9 & 
\end{matrix}
$$

Im Kopf lässt sich $-19$ leichter als $-20$ und $+1$ rechnen:

$$
\begin{matrix}
  & 2 & 6 & 0 \\ 
\- & 2 & 0 &   \\ 
  & \+ & 1 & 
\end{matrix}
$$

Sprich man zieht an einer Stelle $2$ ab und addiert $1$ zur Stelle rechts daneben:

$$
\begin{matrix}
  & \phantom{-}2 & \phantom{+}6 & 0 \\ 
  & \-2 & \+1 & 
\end{matrix}
$$

Dieser Prozess lässt sich auch wie folgt beschreiben: 

Man zieht an einer Stelle $2$ ab, halbiert diese und addiert das Ergebnis zur Stelle rechts daneben.

{{< video src="/images/ostern_mod19_260.mp4" >}}

Es gilt also: $260 \pmod{19} = 70 \pmod{19}$, d.&nbsp;h. $260$ und $70$ haben beim Teilen durch $19$ den gleichen Rest. 

Da man beliebige Vielfache von $19$ abziehen kann, kann man auch $3 \cdot 19 = 57$ abziehen. 

$$
\begin{matrix}
  &  & 7 & 0 \\ 
  & \- & 5 & 7 
\end{matrix}
$$

Im Kopf leichter zu rechnen als:

$$
\begin{matrix}
  &  & 7 & 0 \\ 
  & \- & 6 & 0 \\ 
  &   & \+ & 3
\end{matrix}
$$

Oder auch:

$$
\begin{matrix}
  &  & \phantom{-}7 & \phantom{+}0 \\ 
  &  & \-6 & \+3 
\end{matrix}
$$

Dieser Prozess lässt sich abermals wie folgt beschreiben: 

Man zieht an einer Stelle $6$ ab, halbiert diese und addiert das Ergebnis zur Stelle rechts daneben.

Diese Vorgehensweise gilt jedoch nicht nur für $2$ und $6$, sondern ganz allgemein für jede beliebige gerade Zahl:

>Man zieht an einer Stelle eine gerade Zahl ab, halbiert diese und addiert das Ergebnis zur Stelle rechts daneben.

Ist die Stelle, bei der man die gerade Zahl abziehen will, eine ungerade Zahl, so bleibt $1$ als Rest stehen:

{{< video src="/images/ostern_mod19_70.mp4" >}}

Also ist $260 \pmod{19} = 13$. Das gleiche Ergebnis hätte man auch — und sogar schneller — erhalten, wenn man zu Beginn direkt die zweistellige Zahl $26$ abgezogen hätte:

{{< video src="/images/ostern_mod19_260_2.mp4" >}}

Hier ein Beispiel mit ungeraden zweistelligen Zahlen:

{{< video src="/images/ostern_mod19_1500.mp4" >}}

Also gilt: $1500 \pmod{19} = 18$.

 Begegnet man auf dem Weg des Kopfrechnens einer $19$ so kann man diese direkt durch Nullen ersetzen. Dies verkürzt oft die Rechnung. 
 Bleibt am Ende der Rechnung $19$ übrig, so **muss** man diese gar durch $0$ ersetzen, da das Rechnen $\text{modulo } 19$ immer eine positive Zahl zum Ergebnis hat, die kleiner als $19$ ist. Somit sind nur Zahlen von $0$ bis $18$ als Rest möglich.

{{< video src="/images/ostern_mod19_1995.mp4" >}}

#### Multiplikation mit 11

Die Multiplikation mit $11$ ist für Zahlen von $0$ und $18$ besonders einfach. 

**Einstellige Zahlen** werden schlicht verdoppelt:

$11 \cdot 4 = 44$<br>
$11 \cdot 7 = 77$<br>
etc.

Bei **zweistelligen Zahlen** bleiben die beiden Ziffern links und rechts stehen und zwischen diese schreibt man die Summe der beiden Ziffern:

$11 \cdot 13 = 1(1+3)3 = 143$<br>
$11 \cdot 15 = 1(1+5)5 = 165$<br>
$11 \cdot 17 = 1(1+7)7 = 187$<br>
etc.


### Die Wochentage auf der Hand

Mithilfe des Daumens können wir wie folgt die verschiedenen Wochentage darstellen: 

![[images/doomsday_wochentage.gif]]

Ist der aktuell mit dem Daumen festgehaltene Tag z. B. ein Donnerstag, dann liegt der Daumen auf dem oberen Knöchel des Ringfingers.
Will man den Wochentag 4 Tage später wissen, so geht man mit dem Daumen vier Knöchel weiter und landet beim Sonntag.

{{< video src="/images/ostern_tage_vor.mp4" >}}

Wenn wir mehr als 7 Tage vorwärts gehen müssen, dann können wir den Daumen dort lassen, wo er ist und solange Vielfache von 7 addieren, bis wir möglichst nah an der gewünschten Zahl sind — nach 7 Tagen kommen wir nämlich ohnehin wieder am selben Wochentag aus.<br> 
Wenn wir also z.&nbsp;B. 18 Tage vorwärts gehen müssen, dann sind wir nach 7 Tagen wieder beim selben Wochentag, nach 14 Tagen auch. Um nun zu den gewünschten 18 Tagen zu kommen, müssen wir nur noch 4 Tage vorwärts gehen. Also $18 \pmod{7} = 4$.

> Man nähert sich also einfach in 7er-Schritten der gewünschten Anzahl an Tagen und lässt den Daumen währenddessen, wo er ist. Die fehlenden Tag geht man dann in Einzelschritten weiter.

{{< video src="/images/ostern_tage_vor_modulo_7.mp4" >}}

Müssten wir 100 Tage vorwärts gehen, dann wären wir nach 7, 14, 21,..., 70, 77, 84, 91, 98 Tagen wieder am selben Wochentag. Wir müssen also insgesamt nur 2 Wochentage vorwärts gehen. Es ist also wie bereits oben gesehen, $100 \pmod{7} = 2$. 

## Osterberechnung

### Definition Osterdatum

Die Bestimmung des Osterdatums ist historisch sehr turbulent und wurde im [1. Konzil von Nicäa](https://de.wikipedia.org/wiki/Erstes_Konzil_von_Nic%C3%A4a) im Jahr 325 n.&nbsp;Chr. zum ersten Mal einheitlich definiert:

>Ostern fällt auf den ersten Sonntag nach dem Tag des ersten Vollmondes nach Frühlingsbeginn. [^2]

Um also das Osterdatum für ein Jahr berechnen zu können, müssen wir demnach zunächst herausfinden, an welchem Tag der Frühling beginnt. Anschließend müssen wir berechnen, an welchem Tag der nächstfolgende Vollmond stattfindet und zum Schluss den darauffolgenden Sonntag bestimmen.

Wichtig hierbei ist, dass es sich hierbei nicht um die tatsächlichen astronomischen Zeitpunkte von Frühlingsbeginn und Vollmond handelt.<br>
Als Frühlingsbeginn wurde fix der **21. März** gewählt — der tatsächliche Frühlingsbeginn ist teilweise auch 1 bis 2 Tage früher. 
Als Mond wird nicht der echte Himmelskörper zurate gezogen, sondern der eben beschriebene errechnete Mond.

Wir unterteilen das Finden des Osterdatums also in 3 Schritte:

>**Schritt 1:** Wochentag des Frühlingsbeginns bestimmen
>
>**Schritt 2:** Abstand zwischen Frühlingsbeginn und Vollmond berechnen
>
>**Schritt 3:** Datum des folgenden Sonntags bestimmen


### Schritt 1 - Wochentag des Frühlingsbeginns bestimmen

Das Datum des Frühlingsbeginns für die Osterberechnung ist der 21. März. Es bleibt also nur noch den Wochentag dieses Tages für ein bestimmtes Jahr herauszufinden.

Hier bedienen wir uns eines Verfahrens, das ich im Rahmen der [[Die_Doomsday-Methode|Doomsday-Methode]] entwickelt habe. Mit der Doomsday-Methode kann man den Wochentag eines beliebigen Datums bestimmen. Wen die Hintergründe interessieren, warum das gezeigte Verfahren den Wochentag des Frühlingsbeginns bestimmen kann, der liest am besten den Artikel zur Doomsday-Methode. So viel sei gesagt, der 21. März ist zufälligerweise genau ein Doomsday ;)

Im Folgenden werde ich lediglich das Verfahren ohne Erklärung geben.

Wir denken uns auf unserer Hand ein bei Dienstag beginnendes Häkchen ✔️.

![[images/doomsday_hand_haken.png]]

Wir gehen zunächst wie folgt vor:

>1. Wir setzen den Daumen auf **Dienstag** und denken uns die **ersten beiden Ziffern der gewünschten Jahreszahl**.
>
>2. Bei 0 beginnend **nähern wir uns nun dieser Zahl** in 1er-Schritten **entlang des Häkchens** gehen, bis zum nächsten **Vielfachen von 4**. 
>3. Dort bleibt der Daumen und wir denken uns die **letzten beiden Ziffern der gewünschten Jahreszahl**.
>
>4. Bei 0 beginnend **nähern wir uns nun dieser Zahl** so weit es geht in **12er-Schritten** und gehen pro 12er-Schritt mit dem Daumen um einen Knöchel vor.
>
>5. Wir schauen, **wie viel jetzt noch zur gewünschten Zahl fehlt**. Bei der 0 beginnend gehen wir so viele Male **1 Knöchel vorwärts**. **Bei der 4 und 8 jedoch gehen wir um 2 Knöchel** vorwärts.
>
>6. Der Wochentag auf dem der Daumen jetzt liegt ist, der Wochentag des 21.03.

#### Beispiel 2045

{{< video src="/images/ostern_fruehlingsbeginn_2045.mp4" >}}

#### Beispiel 1965

{{< video src="/images/ostern_fruehlingsbeginn_1965.mp4" >}}

#### Beispiel 1789

{{< video src="/images/ostern_fruehlingsbeginn_1789.mp4" >}}

### Schritt 2 - Abstand zwischen Frühlingsbeginn und Vollmond berechnen


Der schwierigste Schritt ist die Berechnung des Abstands zwischen dem Frühlingsbeginn und dem nächsten Vollmond zu berechnen. Wir führen hierfür zunächst zwei Schreibweisen ein:

$J$: Jahreszahl

$H$: vorderen beiden Ziffern des Jahres

Für das Jahr $2045$ wäre also $J = 2045$ und $H = 20$.

Für die Berechnung des Vollmondes müssen wir ein paar Zwischenergebnisse ausrechnen und diese jeweils weiterverarbeiten. Die Zwischenergebnisse $a$ und $b$ braucht man, um $c$ auszurechnen. 

Bei der Berechnung der Variablen $a$ und $b$ helfen uns unsere Rechentipps von oben.

>$a = J \pmod{19}$
>
>$b = 11a \pmod{30}$
>
>$c = D - b \pmod{30}$

Sollte bei der Berechnung von $c$ ein negatives Ergebnis auftauchen, addiert man einfach einmal $30$, damit man wieder eine positive Zahl erhält.

Die Variable $D$ ist für ein ganzes Jahrhundert immer gleich, sodass man sich dieses auch einfach merken kann. Für die Jahrhunderte, die an $1900$, $2000$ und $2100$ beginnen ist der Wert für $D = 24$. Für andere Jahrhunderte berechnet man $D$ wie folgt:

>$D = H - \lfloor \frac{H}{3} \rfloor - \lfloor \frac{H}{4} \rfloor +15$ [^3]

Der Wert für $D$ steigt also jedes Jahrhundert um $1$. Wenn das Jahrhundert bzw. die ersten beiden Ziffern des Jahres ($H$) durch $3$ oder $4$ teilbar sind, dann bleibt der Wert, wie er ist. Ist $H$ sogar durch $12$ teilbar, also sowohl durch $3$ und $4$ teilbar, dann verringert sich der Wert von $D$ sogar um $1$.

Hier ein paar Werte für $D$:

| **$H$** | **$D$** |
|:-------:|:-------:|
|  $15$   |  $22$   |
|  $16$   |  $22$   |
|  $17$   |  $23$   |
|  $18$   |  $23$   |
|  $19$   |  $24$   |
|  $20$   |  $24$   |
|  $21$   |  $24$   |
|  $22$   |  $25$   |
|  $23$   |  $26$   |
|  $24$   |  $25$   |
|  $25$   |  $26$   |
|  $26$   |  $27$   |
|  $27$   |  $27$   | 

>Vollmond ist dann $c$ Tage nach dem 21.03.


### Schritt 3 - Datum des folgenden Sonntags bestimmen

Wir wissen nun, an welchem Datum und Wochentag der Frühlingsbeginn (21.03.) stattfindet und wie viele Tage später der Vollmond stattfindet. Wir gehen nun also mit dem Daumen vom in Schritt 1 berechneten Wochentag des Frühlingsbeginns $c$ Tage nach vorne, um den Wochentag des Vollmondes zu erhalten.<br> 
Wie im obigen Kapitel *Die Wochentage auf der Hand* gesehen kann man hierbei auch in 7er-Schritten nähern. So finden wir schließlich den Wochentag des ersten Frühlingsvollmondes der $c$ Tage nach dem Frühlingsbeginn liegt. Den Abstand des darauffolgenden Sonntags zum 21.03. zu finden ist ein Leichtes. Wir gehen schlicht mit dem Daumen zum nächsten Sonntag und zählen dabei von $c$ beginnend immer um 1 Tag weiter. Ist der Vollmond an einem Sonntag, so gehen wir zum nächsten Sonntag. Nennen wir den Abstand von Frühlingsbeginn und dem Ostersonntag $d$.

Um zu wissen, welches Datum dieser Sonntag hat, können uns den folgenden Umstand zunutze machen: 

Ist $d$ nicht größer als $10$, so liegt das Osterdatum im März, ist $d$ größer als $10$, so liegt es im April. $11$ Tage nach dem 21.03. ist der 1. April. <br>
Wenn also $d>10$ ist, dann müssen wir von $d$ einfach $10$ abziehen und erhalten den Tag des Datums im April.

>Wenn $d \leq 10$, dann ist der Ostersonntag am ($21 + d$). März.
>
>Wenn $d > 10$, dann ist der Ostersonntag am ($d - 10)$. April.

**Beispiele:**

Ist $d = 4$, dann ist der Ostersonntag am 25.03. 

Ist $d = 10$, dann ist der Ostersonntag am 31.03.

Ist $d = 13$, dann ist der Ostersonntag am 03.04.

Ist $d = 21$, dann ist der Ostersonntag am 11.04.


Das war's :)
<br><br>
Nehmen an, dass der Frühlingsbeginn am Donnerstag liegt und $c = 19$:

{{< video src="/images/ostern_tage_vor_ostersonntag.mp4" >}}

### Zwei Ausnahmen

Keine Regel ohne Ausnahme, so auch bei der Osterberechnung. Vor der gregorianischen Kalenderreform war der 25.04. der letztmögliche Ostertermin. Dies sollte auch nach der Reform so bleiben, allerdings konnte es nun sein, dass Ostern nach den Berechnungsregeln in seltenen Fällen auch am 26.04. stattfinden hätte müssen. Dies sollte auf jeden Fall verhindert werden. Der Grund der zweiten Ausnahmeregel wird an dieser Stelle nicht erklärt. Hierfür wird auf eine [externe Quelle](http://nabkal.de/ostern.html) verwiesen. Die Ausnahmeregeln lauten:

- **Ausnahmeregel 1**: Fällt Ostern laut Berechnung auf den 26.04., so wird es stattdessen eine Woche nach hinten verschoben auf den 19.04.

- **Ausnahmeregel 2**: Fällt Ostern laut Berechnung auf den 25.04. **UND** ist der Vollmond an einem Sonntag **UND** ist $a > 10$, dann wird es stattdessen eine Woche nach hinten verschoben auf den 18.04. (Ist auch nur eine der 3 Bedingungen nicht erfüllt, so bleibt es bei dem errechneten Osterdatum.)

## Beispiele 

### Jahr 2045

#### Schritt 1

{{< video src="/images/ostern_fruehlingsbeginn_2045.mp4" >}}

#### Schritt 2

$a$ berechnen

{{< video src="/images/ostern_mod19_2045.mp4" >}}

$$\begin{align*}
a &= 2045 \pmod{19}\\
&= 12
\end{align*}$$

$b$ berechnen

$$\begin{align*}
b &= 1(1+2)2 \pmod{30}\\
&= 132 \pmod{30}\\
&= 12
\end{align*}$$

$c$ berechnen

$$\begin{align*}
c &= 24 - 12 \pmod{30}\\
&= 12 
\end{align*}$$

#### Schritt 3

{{< video src="/images/ostern_tage_vor_ostersonntag_2045.mp4" >}}

**<u>Ostersonntag 2045 ist also der 09.04.</u>**

### Jahr 1809

#### Schritt 1

{{< video src="/images/ostern_fruehlingsbeginn_1809.mp4" >}}

#### Schritt 2

$a$ berechnen

{{< video src="/images/ostern_mod19_1809.mp4" >}}

$$\begin{align*}
a &= 1809 \pmod{19}\\
&= 4
\end{align*}$$

$b$ berechnen

$$\begin{align*}
b &= 44 \pmod{30}\\
&= 14 
\end{align*}$$

$c$ berechnen

$$\begin{align*}
c &= 23 - 14 \pmod{30}\\
&= 9
\end{align*}$$

#### Schritt 3

{{< video src="/images/ostern_tage_vor_ostersonntag_1809.mp4" >}}

**<u>Ostersonntag 1809 ist also der 02.04.</u>**

### Jahr 1981

#### Schritt 1

{{< video src="/images/ostern_fruehlingsbeginn_1981.mp4" >}}

#### Schritt 2

$a$ berechnen

{{< video src="/images/ostern_mod19_1981.mp4" >}}

$$\begin{align*}
a &= 1981 \pmod{19}\\
&= 5
\end{align*}$$

$b$ berechnen

$$\begin{align*}
b &= 55 \pmod{30}\\
&= 25 \\
\end{align*}$$

$c$ berechnen

$$\begin{align*}
c &= 24 - 25 \pmod{30}\\
&= -1 \pmod{30}\\
&= 29
\end{align*}$$


#### Schritt 3

{{< video src="/images/ostern_tage_vor_ostersonntag_1981.mp4" >}}

Der errechnete Ostersonntag ist der 26.04.

**Ausnahmeregel 1**: Ostern fällt zurück auf den 19.04.

**<u>Ostersonntag 1981 ist also der 19.04.</u>**


### Jahr 2106

#### Schritt 1

{{< video src="/images/ostern_fruehlingsbeginn_2106.mp4" >}}

#### Schritt 2

$a$ berechnen

{{< video src="/images/ostern_mod19_2106.mp4" >}}

$$\begin{align*}
a &= 2106 \pmod{19}\\
&= 16
\end{align*}$$

$b$ berechnen

$$\begin{align*}
b &= 1(1+6)6 \pmod{30}\\
&= 176 \pmod{30}\\
&= 26
\end{align*}$$

$c$ berechnen

$$\begin{align*}
c &= 24 - 26 \pmod{30}\\
&= -2 \pmod{30}\\
&= 28
\end{align*}$$

#### Schritt 3

{{< video src="/images/ostern_tage_vor_ostersonntag_2106.mp4" >}}

Der errechnete Ostersonntag ist der 25.04.

**Ausnahmeregel 2**: Ostern fällt laut Berechnung auf den 25.04. **UND** der Vollmond ist an einem Sonntag **UND** $a > 10$. Ostern fällt also zurück auf den 18.04.

**<u>Ostersonntag 2106 ist also der 18.04.</u>**


## Weiterführende Literatur

### Internet
- [Youtube - Easter, Passover, and Astronomy: Why the different dates? Explained!](https://youtube.com/watch?v=aq_e3EkXFFM)
- [nabkal.de - Webseite mit umfassenden Informationen und Rechnern zu Kalender- und Osterthemen](http://nabkal.de/ostern.html)

### Bücher
- [Walther Jacobsthal (1917) - Mondphasen, Osterrechnung und Ewiger Kalender](https://link.springer.com/book/10.1007/978-3-642-47540-5)
- [Michael E. Klews (2008) - Die Herleitung der Osterformeln von Gauß, Butcher & Jones, Meeus sowie Knuth aus dem computus paschalis](https://www.logos-verlag.de/cgi-bin/buch/isbn/1923)



[^1]: Das stimmt nicht ganz. Genau genommen sollte der errechnete Mond ab dem Jahr 1800 siebenmal  jeweils alle 300 Jahre um einen Tag zurückgesetzt werden und danach einmal nach 400 Jahren. Dieser 2500 Jahre dauernde Zyklus wiederholt sich anschließend immer wieder. Unsere vereinfachte Regel von oben, weicht als von der tatsächlichen erst ab dem Jahr 4200 ab. Bis dahin soll diese Näherung genügen.

[^2]: Ist der Vollmond an einem Sonntag, so findet Ostern am darauffolgenden Sonntag statt. (siehe auch das Unterkapitel "Zwei Ausnahmen")

[^3]: Die 3 und die 4 in den Rechnungen kommen durch die Korrekturen in der gregorianischen Kalenderreform alle 300 bzw. 400 Jahre.<br>$-\lfloor \frac{H}{3} \rfloor$ ist die Korrektur für den Mond und $H - \lfloor \frac{H}{4} \rfloor$ für die Sonne.

