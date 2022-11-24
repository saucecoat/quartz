---
title: "Muster in Logartihmusfunktionen"
date: "2022-11-24"
tags: [alle, math, mathe, analysis, logarithmus, muster, pattern, ableitung, derivative, streckung, stauchung, verschiebung]
---

## Muster

Leitet man Funktionen der Form $\mathrm{log}(nx)$ mit $n \in \mathbb{R}$ ab, so findet man folgendes Muster:

$$\frac{\mathrm{d}}{\mathrm{d}x}\left(\mathrm{log}(x)\right)=\frac{1}{x}$$ 

$$\frac{\mathrm{d}}{\mathrm{d}x}\left(\mathrm{log}(2x)\right)=\frac{1}{x}$$ 

$$\frac{\mathrm{d}}{\mathrm{d}x}\left(\mathrm{log}(3x)\right)=\frac{1}{x}$$  

$$\frac{\mathrm{d}}{\mathrm{d}x}\left(\mathrm{log}(\pi x)\right)=\frac{1}{x}$$  

$$\vdots $$

$$\frac{\mathrm{d}}{\mathrm{d}x}\left(\mathrm{log}(nx)\right)=\frac{1}{x}$$  

Da $\mathrm{log}(nx)$ einer Streckung/Stauchung in $x$-Richtung entspricht, heißt das, dass das Strecken/Stauchen in $x$-Richtung die Steigung an keiner Stelle verändert.

## Erklärung 

Kramt man die [[Eine_Frage_des_Maßstabes_Mathewelten_ARTE|Logarithmus]]gesetze heraus, wird (zumindest algebraisch) schnell klar warum:

$$\mathrm{log}(nx)=\mathrm{log}(x)+\mathrm{log}(n)$$

Die Funktion $\mathrm{log}(nx)$ ist also bloß eine Verschiebung von $\mathrm{log}(x)$ in $y$-Richtung um $\mathrm{log}(n)$. Eine Verschiebung in $y$-Richtung verändert allerdings die Steigung nicht.

