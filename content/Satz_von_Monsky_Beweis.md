---
title: "Satz von Monsky - Teilung eines Quadrats in eine ungerade Zahl von Dreiecken"
date: "2022-11-03"
tags: [alle, math, mathe, p-adic_numbers, p-adische_zahlen, aigner, beweis, dreieck, quadrat, aufteilen, flächeninhalt, metric, metrik, sperners_lemma, math_stackexchange, farbe, monsky]
---

### Satz von Monsky

>Ein Quadrat lässt sich nicht in eine ungerade Anzahl an Dreiecken mit gleichem Flächeninhalt zerlegen.

### Vollständiger Beweis 

- Anschauliche Version des Beweises: [Aigner - Das Buch der Beweise Kap. 20 Ein Quadrat und viele Dreiecke](https://link.springer.com/chapter/10.1007/978-3-642-02259-3_20)
- Originalbeweis von Monsky: [Monsky - On Dividing a Square Into Triangles](https://www.jstor.org/stable/2317329)
- Präsentation zum Beweis: [Schmitt - Über die Zerlegung eines Quadrats in Dreiecke gleicher Fläche](https://page.math.tu-berlin.de/~felsner/Lehre/TilingSlides/schmitt_100130_1.pdf)

### Skizzierung Beweisidee

>1. Mithilfe der 2-adischen Metrik $|\cdot|_{2}$ wird das Einheitsquadrat auf eine ganz spezielle Weise mit 3 Farben eingefärbt. 
>- Die 2-adische Metrik wird jedoch nicht auf $\mathbb{Q}_{2}$ angewendet, sondern auf das Einheitsquadrat $[0;1]^2\subset \mathbb{R}^2$.
>- Erklärung, wie $|\cdot|_{2}$ auf $\mathbb{R}$ übertragen werden kann auf [Math Stackexchange](https://math.stackexchange.com/questions/1348581/extending-2-adic-valuation-to-real-numbers), im [Aigner - Das Buch der Beweise, S. 156 ff.](https://link.springer.com/chapter/10.1007/978-3-642-02259-3_20) und bei [Schmitt](https://page.math.tu-berlin.de/~felsner/Lehre/TilingSlides/schmitt_100130_1.pdf#page=17).

>2. Mithilfe eines Arguments ähnlich [Sperners Lemma](https://yewtu.be/watch?v=7s-YM-kcKME) wird gezeigt, dass bei **jeder** Zerlegung des Einheitsquadrats in beliebige (nicht einmal notwendigerweise gleich große) Dreiecke, immer mindestens ein Dreieck mit drei verschiedenfarbigen Eckpunkten ("Regenbogendreieck") entsteht.[^1]

>3. Mithilfe der Determinante wird gezeigt, dass ein "Regenbogendreieck" bei ungeradem $n$ weder den Flächeninhalt $0$ noch den Flächeninhalt $\frac{1}{n}$ haben kann.
>- Jede Zerlegung, die ein "Regenbogendreieck" beinhaltet, kann also keine gewünschte Zerlegung darstellen, da diese Zerlegung aus $n$ Dreiecken mit einem Flächeninhalt von je $\frac{1}{n}$ bestehen muss.

[^1]: In der Veranschaulichung von Aigner (siehe oben) werden Punkt 2 & 3 in umgekehrter Reihenfolge behandelt.
