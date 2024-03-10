---
title: Unterrichtsstunde Gabriels Horn
date: 2024-03-10
tags:
  - alle
  - mathe
  - unterricht
  - schule
  - lk
  - uneigentliches_integral
  - rotation
  - rotationskörper
  - analysis
  - integral
  - unendlichkeit
  - unendliche_summen
  - harmonische_reihe
  - harmonic_series
  - geometrische_reihe
  - riemannscher_umordnungssatz
  - riemann_rearrangement_theorem
  - gabriels_horn
  - paradox 
---


# Was bisher geschah

- Unter- und Obersummen
- Hauptsatz der Differential- und Integralrechnung
	- inkl. intuitiver Vorstellung des Hauptsatzes mittels infinitesimaler Größen ($\mathrm{d}x$)
- [[Pi_ist_4|"Beweis"]] $\pi=4$
- uneigentliche Integrale
- Rotationskörper
	- inkl. intuitiver Vorstellung von "unendlich feinen" Zylindern mit der Höhe $\mathrm{d}x$

# Unterrichtsverlauf

## Integral $\int_{1}^{\infty} \frac{1}{x}~\mathrm{d}x$

Schüler sollen das Integral $\int_{1}^{\infty} \frac{1}{x}~\mathrm{d}x$ bestimmen. Die Grundidee ist wieder eine Abschätzung. Es wird zunächst nach unten abgeschätzt.

In der folgenden Geogebra-Datei wird das gesuchte Integral $a$ und eine Untersumme $b$ präsentiert. 

<iframe scrolling="no" title="Integral 1/x & harmonische Reihe" src="https://www.geogebra.org/material/iframe/id/sqecsr7r/width/800/height/500/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/true/ctl/false" width="800px" height="500px" style="border:0px;"> </iframe>

Die Schüler sollen nun die Größe der einzelnen Rechtecke bestimmen und summieren. Es ergibt sich die harmonische Reihe: 

$$\int_{1}^{\infty} \frac{1}{x}~\mathrm{d}x > \frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \frac{1}{5} + \frac{1}{6} + \ldots$$

Es ist nicht ersichtlich, ob die resultierende Reihe konvergiert oder divergiert. Es wird erneut nach unten abgeschätzt. In der Geogebra-Datei wird die Untersumme $c$ gezeigt. Abermals sollen die Schüler die Größe der einzelnen Rechtecke bestimmen und summieren:

$$\begin{aligned}
\int_{1}^{\infty} \frac{1}{x}~\mathrm{d}x &> \frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \frac{1}{5} + \frac{1}{6} + \ldots\\
&> \frac{1}{2} + \frac{1}{2} + \frac{1}{2} + \frac{1}{2} + \frac{1}{2} + \dots
\end{aligned}$$

Diese Summe divergiert offensichtlich, ist also gewissermaßen "$= \infty$":

$$\begin{aligned}
\int_{1}^{\infty} \frac{1}{x}~\mathrm{d}x &> \frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \frac{1}{5} + \frac{1}{6} + \ldots\\
&> \frac{1}{2} + \frac{1}{2} + \frac{1}{2} + \frac{1}{2} + \frac{1}{2} + \dots\\
&= \infty
\end{aligned}$$

Wenn die Untersumme bereits divergiert, dann muss auch unser ursprüngliches Integral divergieren.

## Harmonische vs. geometrische Reihe

Es wird anschließend die obige harmonische Reihe $\frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \frac{1}{5} + \frac{1}{6} + \ldots$ mit der geometrischen Reihe $\frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \frac{1}{16} + \frac{1}{32} + \ldots$ kontrastiert.

Anschaulich wird gezeigt, dass die obige geometrische Reihe gegen $1$ geht. 

Wenn die Frage nicht von selbst aufgeworfen wird, wird diskutiert, warum die eine unendliche Summe divergiert, die andere wiederum konvergiert.


## Exkurs: Die alternierende harmonische Reihe

Als Exkurs kann auch die alternierende harmonische Reihe $1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \frac{1}{5} - \frac{1}{6} + \ldots$ erwähnt werden. Der [Beweis ohne Worte](https://maa.org/sites/default/files/Hudleson-MMz-201007804.pdf), der zeigt, dass diese Reihe gegen $\log(2)$ konvergiert, wird als Angebot für einen Kurzvortrag in der folgenden Stunde ausgegeben.

Spaßeshalber kann noch erwähnt werden, dass die alternierende harmonische Reihe wegen des [[Riemannscher Umordnungssatz|Riemannschen Umordnungssatzes]] durch Vertauschen der Summanden jeden beliebigen Wert annehmen kann.


## Volumen Gabriels Horn

Nun drehen wir unser Integral $\int_{1}^{\infty} \frac{1}{x}~\mathrm{d}x$ um die $x$-Achse und die Schüler sollen in 3er-Gruppen das Volumen des resultierenden Rotationskörpers (auch *Gabriels Horn* genannt) berechnen.

Es müssen hierbei die Erkenntnisse über uneigentliche Integrale und Rotationskörper zusammengefügt werden.

$$\begin{aligned}
V_{Horn} &= \int\_{1}^{\infty} V_{Zylinder}\\\\
&= \int\_{1}^{\infty}\pi \cdot r^{2}  \cdot h\\\\
&= \int\_{1}^{\infty}\pi \cdot (f(x))^{2}~\mathrm{d}x\\\\
&= \pi \cdot \lim\_{a\to\infty} \int\_{1}^{a} (f(x))^{2}~\mathrm{d}x\\\\
&= \pi \cdot \lim\_{a\to\infty} \int\_{1}^{a} \frac{1}{x^{2}} ~\mathrm{d}x\\\\
&= \pi \cdot \lim\_{a\to\infty} \left[-\frac{1}{x}\right]\_{1}^{a}\\\\
&= \pi \cdot \lim\_{a\to\infty} \left(-\frac{1}{a}+1\right)\\\\
&= \pi
\end{aligned}$$

Gabriels Horn, das aus der Rotation einer unendlichen Fläche entsteht, besitzt also ein endliches Volumen von $\pi$.

"Man könnte also das ursprüngliche Integral niemals mit Farbe ausmalen, da man dafür unendlich viel Farbe bräuchte. Rotiert man das Integral jedoch, so kann man den resultierenden Körper mit $\pi$ Litern Farbe komplett füllen."

Dieses Paradoxon wird den Schülern als philosophische Denkaufgabe gestellt.

## Oberfläche Gabriels Horn

Die Schüler bekommen nun die Aufgabe die Oberfläche des Horns zu bestimmen. Hierzu sollen sie die Vorstellung der "unendlich feinen" Zylinder benutzen, die sie bereits von der Herleitung des Volumens von Rotationskörpern kennen. Allerdings müssen sie nun nicht mehr die Volumina der einzelnen Zylinder summieren, sondern deren Mantelflächen.

$$\int_{1}^{\infty} M_{Zylinder} = \int_{1}^{\infty} 2\pi \cdot r \cdot h$$

Hierbei ist Vorsicht geboten, den das entstehende Integral nähert sich zwar der gesuchten Oberfläche an, erreicht diese jedoch nicht genau. Man kann also sagen, dass

$$\begin{aligned}
O_{Horn} &\geq \int_{1}^{\infty} M_{Zylinder}\\\\
&= \int_{1}^{\infty} 2\pi \cdot r  \cdot h\\\\
&= \int_{1}^{\infty} 2\pi \cdot f(x)~\mathrm{d}x\\\\
&= 2\pi \cdot\int_{1}^{\infty} \frac{1}{x}~\mathrm{d}x
\end{aligned}$$

Aus dem Einstieg wissen wir allerdings bereits, dass dieses Integral divergiert. Die Oberfläche des Horn ist demnach ebenfalls unendlich groß. 

"Man könnte also das Horn mit $\pi$ Litern Farbe komplett füllen, jedoch würde man dabei die innere Wand des Horns nie komplett mit Farbe bedecken können."

Dieses Paradoxon wird den Schülern als philosophische Denkaufgabe gestellt.

## Philosophie Schlussdiskussion

Zum Abschluss wird mit den Schülern über mögliche Lösungen der aufgeworfenen Paradoxa gesprochen.

Die Studie von Wijeratne & Zazkis mit dem Namen [On Painter’s Paradox: Contextual and Mathematical Approaches to Infinity](https://link.springer.com/content/pdf/10.1007/s40753-015-0004-z.pdf) bietet hierfür gute Impulse. 

So sollte der Fallstrick besprochen werden, Vorstellungen über reale Objekte eins zu eins auf imaginäre, mathematische Objekte übertragen zu wollen. 
Auch die bei der Einführung uneigentlicher Integrale vollzogene Abstraktion der Definition eines Integrals sollte besprochen werden. Hier findet nämlich ein für die Mathematik typischer Schritt der Erweiterung einer Definition durch Abstraktion statt. Die intuitiv logische Definition des Integrals als Grenzwert der Unter- und Obersummen wird hier einfach auf unendliche Objekte erweitert. Denn in der Mathematik muss man sich nicht an die lästigen Beschränkungen der realen Welt halten ;)
