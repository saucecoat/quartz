---
title: "Geradengleichung mit und ohne Vektoren"
date: "2022-10-30"
tags: [alle, mathe, analytische_geometrie, gerade, geradengleichung, vektor]
---
Geraden können im Zweidimensionalen sowohl mithilfe der Geradengleichung $y=mx+b$ (mit der Steigung $m$ und dem y-Achsenabschnitt $b$) als auch mithilfe von Vektoren dargestellt werden.

Die Darstellung ohne Vektoren beschreibt vor allem einen funktionalen Zusammenhang zwischen zwei Größen.

Die Darstellung mit Vektoren hingegen beschreibt eine geradlinige Bewegung im Raum ausgehend von einem Startpunkt. Diese Darstellung bietet den Vorteil, sich auf höherdimensionale Räume verallgemeinern zu lassen.

# Umwandlung ohne Vektoren $\rightarrow$ mit Vektoren (im $\mathbb{R}^{2}$)
Sei die Gerade $y=-2x+7$ gegeben. 

Also Stützvektor kann $\begin{pmatrix}0\\\\7\end{pmatrix}$ genommen werden, welche dem y-Achsenabschnitt $b$ entspricht.

Die Steigung $m=-2$ gibt uns einen möglichen Richtungsvektor $\begin{pmatrix}1\\\\-2\end{pmatrix}$ an. Auch möglich wäre z. B. $\begin{pmatrix}-1\\\\2\end{pmatrix}$.

Die gegebene Gerade kann als durch die folgende Geradengleichung mit Vektoren beschrieben werden: $$X=\begin{pmatrix}0 \\\\ 7\end{pmatrix}+t \cdot \begin{pmatrix}1\\\\-2\end{pmatrix}$$

# Umwandlung mit Vektoren $\rightarrow$ ohne Vektoren (im $\mathbb{R}^{2}$)
Sei die Geradengleichung $X=\begin{pmatrix}2\\\\3\end{pmatrix}+t \cdot \begin{pmatrix}1\\\\-2\end{pmatrix}$ gegeben. Gesucht ist die Geradengleichung $y=mx+b$, die dieselbe Gerade beschriebt. 

Die Steigung lässt sich direkt aus dem Richtungsvektor $\begin{pmatrix}1\\\\-2\end{pmatrix}$ ablesen, nämlich $m=-2$.

Zur Bestimmung des y-Achsenabschnitts $b$ müssen wir denjenigen Punkt auf der Geraden finden, für den $x=0$ gilt. Wir suchen also den Parameter $t$, sodass die $x$-Koordinate $0$ wird: $$2+t \cdot 1=0.$$
Daraus folgt, dass $t=-2$. Durch Einsetzen von $t=\textcolor{red}{-2}$ ergibt sich die gesuchte $y$-Koordinate:
$$3+\textcolor{red}{(-2)}\cdot (-2)=7.$$
Der y-Achsenabschnitt ist also $b=7$.

Die gegebene Gerade kann also durch die folgende Geradengleichung ohne Vektoren beschrieben werden: $$y=-2x+7$$


