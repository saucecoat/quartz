---
title: "Integration als Gegenteil der Differenzierung"
date: "2023-07-03"
tags: [alle, mathe, analysis, integral, integralrechnung, stammfunktion, differenzierung, differentialrechnung, steigung, steigungsdreieck]
---

## Integration

Der Prozess der <u>**Integration**</u> nimmt die Information der Steigungen und ermittelt daraus die zugrundeliegende Kurve.

Reiht man alle Steigungen $\frac{\mathrm{d}y}{\mathrm{d}x}$ einer Kurve hintereinander auf, so erhält man eine Reihe von Steigungsdreiecken ![[images/Integration_easy_Dreieck.png|50]].<br>
Zur Veranschaulichung gehen wir von endlichen $\mathrm{d}y$ und $\mathrm{d}x$ aus anstatt von unendlich kleinen. 

## Konstante Steigung

Die Steigung einer unbekannten Kurve $y$ lässt sich als durch die folgenden Steigungsdreiecke mit jeweils einer konstanten Steigung $\frac{\mathrm{d}y}{\mathrm{d}x}=a$ beschreiben:

![[images/Integration_easy_Dreiecke.png]]

>Wie sieht die Kurve aus, die durch die obigen Steigungen beschrieben wird?

> [!success]- Antwort
> 
>Setzen wir die Dreiecke passend aneinander, so ergibt sich eine Gerade, die durch die lineare Funktion $y=ax+b$ beschrieben wird. 
>
>![[images/Integration_easy_Gerade.png|300]]
>
>Da die Steigung an jeder Stelle gleich ist, ist es sogar egal, ob die Steigungsdreiecke nun endlich oder unendlich klein sind.
>
>Die Steigungsdreiecke geben jedoch keinen Aufschluss darüber, wo der $y$-Achsenabschnitt der Geraden liegen soll. Dieser ist in gewisser Weise beliebig, da wir nur Informationen über die Steigung haben und eine Änderung des $y$-Achsenabschnitts der Geraden nichts an der Steigung ändert.
>
>![[images/Integration_easy_Verschiebung.png|300]]
>
>Üblicherweise weist man auf diesen Umstand mit einer Konstanten $C$ hin:
>
>$$y=ax+C$$

## Nichtkonstante Steigung

Nehmen wir jetzt an, dass die Steigung einer uns unbekannten Kurve durch $\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{1}{5}x$ gegeben ist. 
An verschiedenen $x$-Werten ergeben sich nun folgende Steigungen:

![[images/Integration_easy_Steigungen.png|400]]

>Wie sieht die Kurve aus, die durch die obigen Steigungen beschrieben wird?

> [!success]- Antwort
>
>Setzt man die obigen Steigungsdreiecke aneinander, so ergibt sich folgende Kurve:
>
>![[images/Integration_easy_Parabel.png|400]]
>
>Dies ist zwar keine "glatte" Kurve, jedoch wird diese durch immer kleiner werdende $\mathrm{d}x$ und $\mathrm{d}y$ beliebig "glatt".

## Integralschreibweise

>Welche Gleichung beschreibt wohl den Verlauf dieser Kurve $y$?

Die Höhe $y$ an einer beliebigen Stelle ergibt sich durch die Summe aller kleinen $\mathrm{d}y$ bis zu dieser Stelle, also $$\int\mathrm{d}y=y.$$

Wegen 
$$\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{1}{5}x$$
$$\Rightarrow \mathrm{d}y=\frac{1}{5}x \cdot \mathrm{d}x$$

gilt:

$$y=\int \frac{1}{5}x~\mathrm{d}x.$$

Wir suchen also eine Funktion, deren Ableitung $\frac{1}{5}x$ ist. Nach ein wenig Tüfteln oder beim "Rückwärtsgehen" der Ableitungsregeln findet man:

$$y=\frac{1}{10}x^{2}.$$

Da abermals nichts über den $y$-Achsenabschnitt bekannt ist und dieser an den Steigungen nichts ändern würde, ergibt sich:

$$y=\frac{1}{10}x^{2}+C.$$



<u>**Quelle:**</u> [Calculus made easy (Silvanus Thompson)](https://www.gutenberg.org/ebooks/33283)