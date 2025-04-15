---
title: Den Wochentag jedes beliebigen Datums bestimmen — Die Doomsday-Methode
date: 2025-04-14
tags:
  - alle
  - kalender
  - calendar
  - doomsday
  - wochentag
  - conway
  - lewis_carroll
  - schaltjahr
  - gregorianisch
  - julianisch
---

> **HINWEIS:** Bitte die Seite <u>**ein zweites Mal laden**</u>. Die Animationen laden momentan leider noch nicht, wie sie sollen.


## Einleitung

In diesem Artikel stelle ich die aus meiner Sicht einfachste Methode vor, den Wochentag eines beliebigen Datums zu ermitteln.

Diese Methode entspricht im Großen und Ganzen der [Doomsday-Methode](https://web.archive.org/web/20240907031643/https://www.archim.org.uk/eureka/archive/Eureka-36.pdf#page=31) ([Wikipedia](https://en.wikipedia.org/wiki/Doomsday_rule)) des großartigen Mathematikers *John Horton Conway*, welcher seine Arbeit auf der des Mathematikers und Autoren der beiden *Alice*-Bücher [Lewis Carroll](https://www.nature.com/articles/035517a0) aufgebaut hat.

An dieser Stelle seien auch die Erkenntnisse aus Arbeiten von [Chamberlain Fong](https://arxiv.org/abs/1006.3913), [Dr. YingKing Yu](http://improvedddabyykyu.blogspot.com//2010/09/perpetual-calendar-in-your-head-by-dr.htm?m=0), [Mike Walters](https://easydoomsday.blogspot.com/2008/04/improved-doomsday-algorithm.html?m=1) (siehe auch [Fong & Walters](https://arxiv.org/abs/1010.0765)) erwähnt, die vor allem der Beschleunigung oben genannter Methode dienen.

Der Grund für die Annahme, dass die hier vorgestellte Herangehensweise besonders einfach ist, liegt nicht darin, dass ich irgendwelche neuen Zusammenhänge in Bezug auf die Doomsday-Methode entdeckt habe. Vielmehr rührt sie daher, dass die sonst in [Youtube-](https://youtube.com/watch?v=z2x3SSBVGJU)[Videos](https://youtube.com/watch?v=714LTMNJy5M) oder [Artikeln](http://rudy.ca/doomsday.html) gezeigten Variationen der Doomsday-Methode oft mit Rechnungen arbeiten, bei denen man zumeist mehrere Zahlen im Kopf behalten muss, nur um diese anschließend zu addieren, zu dividieren und Reste aus diesen Divisionen weiterzuverarbeiten. 
Dieser Ansatz ist meiner Meinung nach recht fehleranfällig und kompliziert. Er kann jedoch mit einem kleinen Hilfsmittel soweit vereinfacht werden, dass all diese Rechnungen auf bloßes Zählen reduziert werden und alle Memorisierungen von Zahlen als Zwischenschritte gänzlich wegfallen. Dieses Hilfsmittel ist die 🖐️. 

Dieser Artikel ist in drei Kapitel unterteilt. Nach dem ersten Kapitel wird man den Wochentag jeden Datums innerhalb eines Jahres bestimmen können. Kapitel 2 zeigt, wie man den Wochentag jeden Datums des 21. Jahrhunderts bestimmt und nach Kapitel 3 ist man in der Lage, von jedem beliebigen Datum den Wochentag zu bestimmen.

Bevor wir uns allergins mit der Bestimmung von Daten beschäftigen, sollte ein wichtiger Aspekt unseres Kalenders kurz genauer beleuchtet werden — die Schaltjahre.

### Schaltjahre 

#### Gregorianischer Kalender

Beim erstmals 1582 von Papst Gregor XIII. eingeführten und heute immer noch gebräuchlichen gregorianischen Kalender werden in regelmäßigen Abständen Schalttage eingefügt, um ihn möglichst genau mit dem tatsächlichen Lauf der Sonne zu synchronisieren. Eine Umrundung der Erde um die Sonne ist nämlich etwas länger als 365 Tage und darum erhalten manche Jahre einen extra Tag am Ende des Februars, um diesen Rückstand wieder aufzuholen. Diese Schaltjahre haben dann 366 Tage. Wann ein Jahr ein Schaltjahr ist, lässt dich durch folgende Regel ermitteln:

*Ist das Jahr durch 4 teilbar, ist es ein Schaltjahr. Ist das Jahr jedoch zusätzlich durch 100 teilbar, so ist es kein Schaltjahr, es sei denn es ist auch durch 400 teilbar.*

Diese zugegebenermaßen recht komplizierte Regel kann einfacher formuliert werden als:

> [!note] Schaltregel (greg.)
> 
>*Sind die letzten beiden Ziffern durch 4 teilbar, so ist das Jahr ein Schaltjahr. 
>Sind die letzten beiden Ziffern jedoch 00, so betrachte man stattdessen die beiden Ziffern links daneben.*

**Beispiele:**

1862: Kein Schaltjahr, da 62 nicht durch 4 teilbar ist.<br>
1900: Kein Schaltjahr, da 19 nicht durch 4 teilbar ist.<br>
2000: Schaltjahr, da 20 durch 4 teilbar ist.<br>
2012: Schaltjahr, da 12 durch 4 teilbar ist.

#### Julianischer Kalender


Der von Julius Caesar eingeführte julianische Kalender, der die Basis des gregorianischen Kalenders darstellt, ist mit diesem komplett identisch, bis auf die Regel für die Bestimmung der Schaltjahre. Diese lautet:

> [!note] Schaltregel (jul.)
> 
>*Ist das Jahr durch 4 teilbar, ist es ein Schaltjahr.*

Diese Regel ist zwar deutlich einfacher, jedoch auch viel schlechter darin, die reale Umlaufzeit der Erde um die Sonne abzubilden. Nach rund 1500 Jahre der Verwendung hinkte der Kalender dem wirklichen Lauf der Sonne um gut 10 Tage hinterher. Eine Reform musste her und der gregorianische Kalender war geboren.

**Beispiele:**

1262: Kein Schaltjahr, da 62 nicht durch 4 teilbar ist.<br>
1500: Schaltjahr, da 00 durch 4 teilbar ist.<br>
1600: Schaltjahr, da 00 durch 4 teilbar ist.<br>
1612: Schaltjahr, da 12 durch 4 teilbar ist.

## Kapitel 1 — Wochentage aller Daten eines Jahres bestimmen

### Die Wochentage auf der Hand

Mithilfe des Daumens können wir wie folgt die verschiedenen Wochentage darstellen: 

![[images/doomsday_wochentage.gif]]

Ist der aktuell mit dem Daumen festgehaltene Tag z. B. ein Donnerstag, dann liegt der Daumen auf dem oberen Knöchel des Ringfingers.
Will man den Wochentag 3 Tage später wissen, so geht man mit dem Daumen drei Knöchel weiter und landet beim Sonntag.

Kennt man also den Wochentag eines Tages, so kann man durch Vor- bzw. Zurückgehen den Wochentag jedes anderen Tages herausfinden.

{{< video src="/images/doomsday_tage_vor.mp4"  >}}

{{< video src="/images/doomsday_tage_zurueck.mp4"  >}}

Je weiter jedoch der Tag, dessen Wochentag man kennt und der gesuchte Tag auseinanderliegen, umso umständlicher wird das Ermitteln. Kennt man bspw. den Wochentag des 01.01. und möchte den Wochentag des 11.11. wissen, so müsste man sehr viele Tage durchgehen. 
Abhilfe schafft das Konzept der *Doomsdays*.

### Doomsday

#### Was ist ein Doomsday?

Das Konzept des *Doomsdays* geht auf den bereits erwähnten Mathematiker [John Conway](https://de.wikipedia.org/wiki/John_Horton_Conway) zurück. Jedes Jahr hat **einen** Doomsday. 

> [!note] Definition
> 
>Der Doomsday eines Jahres ist per Definition der Wochentag des letzten Februartages. 

Nehmen wir für ein Jahr an, dass der letzte Februartag — und damit der Doomsday — für dieses Jahr ein *Mittwoch* ist. Dann fallen auch alle folgenden Daten dieses Jahres auf einen Mittwoch. [^1]

![[images/doomsday_kalender_mittwoch.png]]

Der 21.03. z.&nbsp;B. ist ein Mittwoch, der 16.05. ist ein Mittwoch, der 08.08., der 26.09., der 26.12. etc. Alles Mittwoche.
Ist der Doomsday eines Jahres hingegen ein *Donnerstag*, so fallen alle diese Daten auch auf einen Donnerstag. Der 21.03. z.&nbsp;B. ist ein Donnerstag, der 16.05. ist ein Donnerstag, der 08.08., der 26.09., der 26.12. etc. Alles Donnerstage.

#### Ein Datum pro Monat reicht

Wie bereits gesehen, reicht es im Grunde aus, lediglich ein solches Datum pro Jahr zu kennen, da man von diesem ausgehend einfach zum gewünschten Datum vor- oder zurückgehen kann. Da die Wege wie gesehen dann allerdings recht lang werden können, ist es sinnvoller, **ein Datum pro Monat** zu kennen, das auf den Doomsday fällt.
Conway hat die folgenden Daten als besonders einprägsam erachtet. [^2] Die Daten im Januar und Februar in hellrot gelten nur für Schaltjahre. Was es mit dem März auf sich hat, wird weiter unten erklärt werden.

![[images/doomsday_kalender_rot.png]]

Trennt man diese Daten in gerade und ungerade Monate auf, so lassen sich ein paar Muster erkennen, die das Merken erleichtern. 

|  Ungerader<br>Monat  |   Gerader<br>Monat   |
|:--------------------:|:--------------------:|
| 03.01.<br>(*04.01.*) | 28.02.<br>(*29.02.*) | 
|        00.03.        |        04.04.        |
|        09.05.        |        06.06.        |
|        11.07.        |        08.08.        |
|        05.09.        |        10.10.        |
|        07.11.        |        12.12.        |

#### Gerade Monate

Die **geraden Monate ab April** sind sehr einfach zu merken: 04.04., 06.06., 08.08., 10.10. und 12.12.

Der letzte **Februar**tag ist per Definition ohnehin ein Doomsday.

#### Ungerade Monate

Die **ungeraden Monate** sind ein bisschen trickier, aber mit einem kleinen englischen Merksatz hat man direkt vier der sechs Monate abgedeckt (und zwar **Mai**, **Juli**, **September** und **November**):

>'I work from **9 to 5** at the **7-11**'.

Zu Deutsch '*Ich arbeite von 9 bis 5 im 7-11*', wobei [7-11](https://de.wikipedia.org/wiki/7-Eleven) eine US-amerikanische Ladenkette ist. Aus dem Merksatz gehen die Daten 09.05. & 05.09. sowie 07.11. & 11.07. hervor. 

Der **März** hat quasi kein eigenes Datum, da der letzte Februartag auch als der 00.03. angesehen werden kann. Wem das zu komisch vorkommt, merkt sich wahlweise einen der anderen roten Märztage: 07.03., 14.03., 21.03. oder 28.03.

Der **Januar** hat seinen Doomsday immer **3** Jahre lang am **03**.01., jedoch im **4.** Jahr (Schaltjahr) am **04**.01.

#### Beispiele

In den folgenden Beispielen gehen wir wie im obigen Kalender vom Doomsday *Mittwoch* aus.
Wir werden den Wochentag für verschiedene Daten bestimmen, indem wir vom jeweiligen Doomsday des entsprechenden Monats (siehe Tabelle oben) zum gewünschten Datum vor- bzw. zurückgehen. Auf diese Weise können wir den Wochentag jedes beliebigen Tages des obigen Kalenders bestimmen.

##### 10.04.

{{< video src="/images/doomsday_bsp_april.mp4"  >}}

##### 27.07.

{{< video src="/images/doomsday_bsp_juli.mp4"  >}}

##### 14.02. (Valentinstag)

{{< video src="/images/doomsday_bsp_februar.mp4"  >}}

Kennt man also den Doomsday eines Jahres, so kann man den Wochentag jedes beliebigen Tages in diesem Jahr bestimmen. Die Frage ist nun, wie man den Doomsday eines beliebigen Jahres bestimmt.

## Kapitel 2 — Wochentag aller Daten eines Jahrhunderts bestimmen

### Doomsday eines Jahres bestimmen

#### Doomsday von Jahr zu Jahr

Schauen wir uns den Doomsday für ein paar aufeinanderfolgende Jahre einmal an:

|  Jahr  | Doomsday |
|:------:|:--------:|
|  2018  |    Mi    |
|  2019  |    Do    |
| *2020* |   *Sa*   |
|  2021  |    So    |
|  2022  |    Mo    |
|  2023  |    Di    |
| *2024* |   *Do*   |
|  2025  |    Fr    |
|  2026  |    Sa    |
|  2027  |    So    |
| *2028* |   *Di*   |
|  2029  |    Mi    |
|  2030  |    Do    | 

> [!success] Erkenntnis
> 
>Der Doomsday springt **jedes Jahr um 1 Tag nach vorne**; wohingegen er an **Schaltjahren um 2 Tage nach vorne** springt. 

Das liegt daran, dass ein normales Kalenderjahr aus genau 52 Wochen und 1 Tag besteht — ein Schaltjahr hingegen aus 52 Wochen und 2 Tagen.

Sehen wir uns alle Doomsdays von 2000 bis 2099 auf einen Blick an. Die Schaltjahre sind orange eingefärbt.

![[images/doomsday_kalender_2000er.png]]

Wie oben gesehen, springt der Doomsday jedes Jahr um 1 Tag vor, bei den Schaltjahren um 2 Tage. Wenn wir also beim Jahr 2000 mit dem Doomsday Dienstag anfangen, können wir den Doomsday aller anderen Jahre des Jahrhunderts bestimmen, indem wir den Daumen immer die entsprechende Anzahl nach vorne bewegen. Den Doomsday 2030 ermitteln wir demnach wie folgt:

{{< video src="/images/doomsday_kal_2030.mp4"  >}}

Man achte darauf, dass man bei jedem Schaltjahr mit dem Daumen um 2 vorangeht.

Je weiter das gewünschte Jahr allerdings im Jahrhundert liegt, umso lästiger ist es, auf diese Weise den Doomsday zu bestimmen. Der Doomsday von 2095 wäre so definitiv kein Spaß.
Wir können uns jedoch ein Muster zunutze machen, durch das wir den ganzen Prozess beschleunigen können. 

#### Doomsday schneller finden

Sieht man sich die Doomsday-Tabelle länger an, so fällt auf, dass wenn man die Jahre von links nach rechts liest — also in 12er-Schritten — der Doomsday immer genau um einen Tag voranschreitet.

![[images/doomsday_kalender_2000er.png]]

> [!success] Erkenntnis
> 
>**Alle 12 Jahre** springt der Doomsday um **1 Tag nach vorne**.

Wir können uns also unserem gewünschten Datum erst in 12er-Schritten nähern, um anschließend wie vorhin in Einzeljahren voranzuschreiten. 

Den Doomsday von 2030 können wir so wesentlich schneller ermitteln als zuvor:

{{< video src="/images/doomsday_kal_24_30.mp4"  >}}

#### Zusammenfassung

> [!example] Vorgehensweise
> 
>1. Man **startet beim ersten Doomsday des Jahrhunderts**. In unserem Beispiel ist das Dienstag für das Jahr 2000.
>2. Man nähert sich dem gewünschten Jahr so weit es geht in **12er-Schritten** und geht dabei mit dem Daumen je **um 1 vorwärts**.
>3. Für die **restlichen Jahre** geht man mit dem Daumen je **um 1 vorwärts**; an **Schaltjahren um 2**. 

Hat man sich dem Jahr so weit es geht in 12er-Schritten genähert, so muss man danach nur beim 4. und 8. Jahr darauf achten, um 2 Tage vorwärts zu gehen. Dies lässt sich sehr gut im untenstehenden Beispiel für das Jahr 2095 erkennen. 

#### Beispiele

##### Doomsday 2030

{{< video src="/images/doomsday_bsp_2030.mp4"  >}}

##### Doomsday 2050

{{< video src="/images/doomsday_bsp_2050.mp4"  >}}

##### Doomsday 2084

{{< video src="/images/doomsday_bsp_2084.mp4"  >}}

##### Doomsday 2095

{{< video src="/images/doomsday_bsp_2095.mp4"  >}}

### Den Wochentag eines beliebigen Datums bestimmen

#### Wochentage im 21. Jahrhundert bestimmen

Wir können also jetzt den Doomsday eines beliebigen Jahres von 2000 bis 2099 bestimmen und wir können den Wochentag jedes beliebigen Tages innerhalb eines Jahres berechnen, indem wir vom jeweiligen Doomsday des Monats ausgehen. 

Führen wir beides zusammen, so können wir tatsächlich den Wochentag jedes beliebigen Tages von 2000 bis 2099 ermitteln.

#### Beispiele 

##### 03.09.2081

Die nächste totale Sonnenfinsternis, die man zumindest von Teilen Deutschlands aus beobachten kann, findet am 03.09.2081 statt. Welcher Wochentag ist das?

{{< video src="/images/doomsday_bsp_20810903.mp4"  >}}

##### 18.02.2021

Der Mars-Rover [*Perseverance*](https://de.wikipedia.org/wiki/Mars_2020) ist am 18.02.2021 auf dem Mars gelandet. Welcher Wochentag ist das?

{{< video src="/images/doomsday_bsp_20210218.mp4"  >}}

Wollen wir Daten in einem anderen Jahrhundert bestimmen, so brauchen wir lediglich den Doomsday des ersten Jahres dieses Jahrhunderts, z.&nbsp;B. 1900. Diesen nehmen wir dann als Start-Doomsday und machen dann alles weitere wie oben beschrieben. 

Für das Jahrhundert, das mit 2000 startet, ist der Start-Doomsday ein *Dienstag*.
Für das Jahrhundert, das mit 1900 startet. ist der Start-Doomsday ein *Mittwoch*.

Wie bestimmt den Start-Doomsday eines beliebigen Jahrhunderts?

## Kapitel 3 — Wochentag eines beliebigen Datums bestimmen

### Den Start-Doomsday eines Jahrhunderts bestimmen

Für die Bestimmung der Wochentage des 21. Jahrhunderts haben wir immer mit dem Dienstag gestartet. Für andere Jahrhunderte muss man jedoch mit anderen Wochentagen starten. Dieses letzte fehlende Puzzlestück beim Bestimmen von Wochentagen beliebigen Daten lernen wir nun kennen. 

#### Gregorianischer Kalender

Aufgrund der Schaltjahrregel im gregorianischen Kalender wiederholen sich die Start-Doomsdays alle 400 Jahre. Es gibt als nur vier mögliche Start-Doomsdays: *Dienstag*, *Mittwoch*, *Freitag* und *Sonntag*. [^3]

Schaut man sich diese auf der Hand an, so ergeben sie die Form eines Häkchens ✔️.

![[images/doomsday_hand_haken.png]]

Um den Doomsday eines beliebigen Jahrhunderts (im gregorianischen Kalender) zu bestimmen, geht man wie folgt vor:

> [!example] Vorgehensweise (greg.)
> 
>1. Start **mit dem gewünschten Jahrhundert** am **Dienstag**.
>2. In 100er-Schritten **entlang des Häkchens** gehen, bis zum nächsten **Vielfachen von 400**. Jeder 100er-Schritt ist dabei je ein Knöchel vorwärts.
>3. Der jetzt berührte Tag ist der **Start-Doomsday**

#### Beispiele 

##### Doomsday 1800

{{< video src="/images/doomsday_bsp_1800.mp4"  >}}

##### Doomsday 1900

{{< video src="/images/doomsday_bsp_1900.mp4"  >}}

##### Doomsday 2400

{{< video src="/images/doomsday_bsp_2400.mp4"  >}}

##### Doomsday 2500

{{< video src="/images/doomsday_bsp_2500.mp4"  >}}

#### Julianischer Kalender

Im julianischen Kalender hat aufgrund der Schaltjahrregel jedes Jahrhundert immer gleich viele Tage, und zwar 36.525 an der Zahl. Da 36.525 Tage genau ein Tag weniger sind als 5.218 Wochen, rückt der Start-Doomsday hier mit jedem Jahrhundert um einen Tag zurück:

*700* $\rightarrow$ *Sonntag*<br>
*800* $\rightarrow$ *Samstag*<br>
*900* $\rightarrow$ *Freitag*<br>
*1000* $\rightarrow$ *Donnerstag*<br>
*1100* $\rightarrow$ *Mittwoch*<br>
etc.

Die Doomsdays wiederholen sich also alle 700 Jahre. 

Um den Doomsday eines Jahrhunderts im julianischen Kalender zu bestimmen, geht man fast analog zum gregorianischen Kalender vor:

> [!example] Vorgehensweise (jul.)
> 
>1. Start **mit dem gewünschten Jahrhundert** am **Sonntag**.
>2. In 100er-Schritten tageweise vorangehen, bis zum nächsten **Vielfachen von 700**. Jeder 100er-Schritt ist dabei je ein Knöchel vorwärts.
>3. Der jetzt berührte Tag ist der **Start-Doomsday**.

#### Beispiele

##### Doomsday 200

{{< video src="/images/doomsday_bsp_200.mp4"  >}}

##### Doomsday 700

{{< video src="/images/doomsday_bsp_700.mp4"  >}}

##### Doomsday 1500

{{< video src="/images/doomsday_bsp_1500.mp4"  >}}

### Zusammenfassung

Zur Bestimmung des Wochentags eines beliebigen Datums muss man die in den Kapiteln vorgestellten Schritte in umgekehrter Reihenfolge durchlaufen. 

> [!example] Vorgehensweise
> 
>1. Erst bestimmt man den *Start-Doomsday* des Jahrhunderts
>2. Dann den *Doomsday* des gewünschten Jahres.
>3. Mit dessen Hilfe man dann zum gewünschten Datum vor- bzw. zurückgeht.

|                                    Schritt                                    |            Beispiel 23.09.1846           |
|:-----------------------------------------------------------------------------:|:------------------------------:|
| <u>**Start-Doomsday**</u> für das gewünschte <u>**Jahrhundert**</u> bestimmen | {{< video src="/images/doomsday_bsp_neptun_1.mp4"  >}} |
|       <u>**Doomsday**</u> für das gewünschte <u>**Jahr**</u> bestimmen        | {{< video src="/images/doomsday_bsp_neptun_2.mp4"  >}} |
|        Vom Doomsday des Monats <u>**zum gewünschten Datum gehen**</u>         | {{< video src="/images/doomsday_bsp_neptun_3.mp4"  >}} |

#### Beispiel 14.07.1789

An welchem Wochentag fand der Sturm auf die Bastille statt?

{{< video src="/images/doomsday_bsp_17890714.mp4"  >}}


#### Beispiel 20.07.1969

An welchem Wochentag landete Apollo 11 auf dem Mond?

{{< video src="/images/doomsday_bsp_19690720.mp4"  >}}


#### Beispiel 01.01.2000

An welchem Wochentag begann das neue Millenium?

{{< video src="/images/doomsday_bsp_20000101.mp4"  >}}

#### Beispiel 27.12.1571 (jul.)

An welchem Wochentag wurde Johannes Kepler geboren?

{{< video src="/images/doomsday_bsp_15711227_jul.mp4"  >}}




[^1]: In einem Schaltjahr sind die Tage im Januar und Februar jeweils um eins höher, da der letzte Februartag der 29. ist und nicht der 28. wie in einem "gewöhnlichen" Jahr.
[^2]: Man könnte auch andere Daten nehmen, die oben in rot eingezeichnet sind. Die hier gezeigten sind jedoch die gebräuchlichsten.
[^3]: Wegen der Schaltregel haben drei von vier hintereinanderfolgenden Jahrhunderten je 24 Schaltjahre und eines 25. Die Jahrhunderte bestehen also dreimal aus 5.217 Wochen + 5 Tagen und einmal aus 5.217 Wochen + 6 Tagen. Zusammen also: 20.868 Wochen + 21 Tage bzw. genau 20.871 Wochen.<br>Nach 4 Jahrhunderten hat man also eine ganzzahlige Anzahl an Wochen durchlaufen und demnach wieder den gleichen Wochentag.