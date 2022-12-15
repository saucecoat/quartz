---
title: "Drehungen mit Quaternionen"
date: "2022-12-15"
tags: [alle, math, mathe, quaternion, 3b1b, 3blue1brown, stereographische_projektion, drehung, 4d, 3d, 2d, komplexe_zahlen, complex_numbers, rotation]
---

## Dreidimensionale Zahlen gibt es nicht

Dreidimensionale Zahlen sind nicht möglich, da der Fakt, dass z. B. der Punkt $(1|0|0)$ zu $(0|1|0)$ gedreht wurde, die Drehung im Dreidimensionalen nicht eindeutig beschreibt. 
Es könnte z. B. eine Drehung um $\begin{pmatrix}0\\\\0\\\\1\end{pmatrix}$ um $90°$ gewesen sein oder eine Drehung um $\begin{pmatrix}1\\\\1\\\\0\end{pmatrix}$ um $180°$.

Im Gegenzug dazu beschreibt eine komplexe Zahl eindeutig einen Punkt sowie eine Drehung im Zweidimensionalen.

**Quellen:**
- https://old.reddit.com/r/math/comments/9urjyx/why_there_is_no_complex_numbers_in_3_dimension/e96j4lg/
- https://eater.net/quaternions/video/stereo3d (ab 4:00)

## Multiplikation von Quaternionen als Drehungen im Dreidimensionalen

[[Quaternionen_mithilfe_von_Vektoren_multiplizieren|Die Multiplikation von Quaternionen]] in 4D sieht aus wie [eine synchrone Drehung **zweier** zueinander senkrechter Kreise](https://eater.net/quaternions/video/rotation). Durch die Projektion von 4D zu 3D, kann einer dieser Kreise aussehen wie eine Gerade.

Eine Drehung in 3D sieht hingegen aus wie eine Drehung <u>**eines**</u> Kreises am Äquator der Einheitskugel, welcher senkrecht zur Drehachse liegt.

Wählt man nun die Drehachse sowie den Äquatorkreis in 3D als die beiden oben erwähnten senkrechten Kreise in 4D, so drehen sich diese bei einer Multiplikation von Quaternionen beide. Da man jedoch in 3D nur die Drehung um den Äquatorkreis haben möchte, muss man die Drehung der Drehachse wieder rückgängig machen. Dies wird erreicht durch die Multiplikation von links und von rechts. 

Möchte man in 3D den Äquatorkreis etwa um $90°$ um die Drehachse drehen, so dreht man in 4D die Drehachse zunächst um $45°$ durch eine Multiplikation von <u>**links**</u>. Hierdurch bewegt sich auch der gewünschte Äquatorkreis um $45°$ in die richtige Richtung. 
Anschließend dreht man durch eine Multiplikation von <u>**rechts**</u> die Drehachse um $-45°$ wieder zurück an die gewünschte Anfangsposition. Der Äquatorkreis dreht sich durch eine Multiplikation von rechts um $-45°$ jedoch weiterhin in die gewünschte Richtung, sodass er sich nach der Multiplikation von links und von rechts um insgesamt $90°$ gedreht hat.

## Drehung von $(1|0|0)$ um $180°$ um die Achse $\begin{pmatrix}1\\\\1\\\\0\end{pmatrix}$  

### Erläuterung

Der Punkt $(1|0|0)$ entspricht der Quaternion $i$.

Die Drehung um $180°$ entspricht der Multiplikation von links mit $\cos(90°)+\sin(90°)\cdot \left( ai+bj+ck\right)$ und der Multiplikation von rechts mit $\cos(-90°)+\sin(-90°)\cdot \left( ai+bj+ck\right)$.

Die (normierte) Drehachse entspricht dem Vektorteil $(a,b,c)$ der obigen Quaternionen. Für die Achse $\begin{pmatrix}1\\\\1\\\\0\end{pmatrix}$ ist dies $\frac{1}{\sqrt{2}}\cdot \left( 1i+1j+0k\right) = \frac{1}{\sqrt{2}}i+\frac{1}{\sqrt{2}}j$.

### Berechnung 

$\left(\cos\left( 90° \right)+ \sin( 90° )\cdot\left(\frac{1}{\sqrt{2}}i+\frac{1}{\sqrt{2}}j\right)\right)\cdot i \cdot \left(\cos\left( -90° \right)+ \sin( -90° )\cdot\left(\frac{1}{\sqrt{2}}i+\frac{1}{\sqrt{2}}j\right)\right)$

$= \left( \frac{1}{\sqrt{2}}i + \frac{1}{\sqrt{2}}j \right) \cdot i \cdot \left( -\frac{1}{\sqrt{2}}i-\frac{1}{\sqrt{2}}j \right)$

$= \left( \frac{1}{\sqrt{2}}i^{2} + \frac{1}{\sqrt{2}}ji \right) \cdot \left( -\frac{1}{\sqrt{2}}i-\frac{1}{\sqrt{2}}j \right)$

$= \left( -\frac{1}{\sqrt{2}}-\frac{1}{\sqrt{2}}k \right) \cdot \left( -\frac{1}{\sqrt{2}}i-\frac{1}{\sqrt{2}}j \right)$

$= \frac{1}{2}i + \frac{1}{2}j + \frac{1}{2}ki + \frac{1}{2}kj$

$= \frac{1}{2}i + \frac{1}{2}j + \frac{1}{2}j - \frac{1}{2}i$

$= j$

Das entspricht dem Punkt $(0|1|0)$.
