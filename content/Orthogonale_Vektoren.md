---
title: Orthogonale Vektoren
date: 2023-10-19
tags:
  - alle
  - mathe
  - analytische_geometrie
  - skalarprodukt
  - orthogonal
  - senkrecht
  - rechter_winkel
  - pythagoras
  - vektor
---


Zwei Vektoren $\vec{a}$, $\vec{b}$ stehen **orthogonal** aufeinander, wenn sie in einem rechten Winkel zueinander liegen. Man schreibt dann: $\vec{a}\perp\vec{b}$.

Die Orthogonalität kann man mithilfe der Koordinaten der Vektoren bestimmen. Bei der Herleitung hilft uns der Satz des Pythagoras.

Gegeben seien zwei Vektoren $\vec{a}=\begin{pmatrix}a_{1} \\ a_{2}\end{pmatrix}$ und $\vec{b}=\begin{pmatrix}b_{1} \\ b_{2}\end{pmatrix}$ aus dem $\mathbb{R}^{2}$, d.&nbsp;h. aus dem Zweidimensionalen.

![[images/Orthogonale_Vektoren_1.png]]

Wie kann der rote Vektor auf der Hypotenuse mithilfe der anderen beiden Vektoren beschreiben?

>[!success]- Antwort
>
>![[images/Orthogonale_Vektoren_2.png]]

Für die Länge des Vektors $\vec{a}$ gilt: $|\vec{a}|=\sqrt{a_{1}^{2}+a_{2}^{2}}$. Also gilt auch für die quadrierte Länge: $|\vec{a}|^{2}=a_{1}^{2}+a_{2}^{2}$.

Mithilfe der Längen der drei obigen Vektoren können wir den Satz des Pythagoras anwenden. 
>
>[!success]- Antwort
>
>$|\vec{a}-\vec{b}|^{2} = |\vec{a}|^{2}+|\vec{b}|^{2}$.

Wir berechnen nun die quadrierte Länge der linken Seite:

>[!success]- Antwort
>
>$|\vec{a}-\vec{b}|^{2} = (a_{1}-b_{1})^{2} + (a_{2}-b_{2})^{2}$
>
>Binomische Formel anwenden:
>>
>>[!success]- Antwort
>>
>>$\begin{aligned}
(a_{1}-b_{1})^{2} + (a_{2}-b_{2})^{2} &= \left(a_{1}^{2}-2a_{1}b_{1}+b_{2}^{2}\right) + \left(a_{2}^{2}-2a_{2}b_{2}+b_{2}^{2}\right)\\\\\\ &= a_{1}^{2}+a_{2}^{2}+b_{1}^{2}+b_{2}^{2}-2(a_{1}b_{1}+a_{2}b_{2})
\end{aligned}$ 


Nun berechnen wir die quadrierte Länge der rechten Seite:

>[!success]- Antwort
>
>$|\vec{a}|^{2}+|\vec{b}|^{2} = a_{1}^{2}+a_{2}^{2}+ b_{1}^{2}+b_{2}^{2}$
>

Setzen wir beide Seiten in die Gleichung ein, so ergibt sich:

>[!success]- Antwort
>
>$a_{1}^{2}+a_{2}^{2}+b_{1}^{2}+b_{2}^{2}-2(a_{1}b_{1}+a_{2}b_{2}) = a_{1}^{2}+a_{2}^{2}+ b_{1}^{2}+b_{2}^{2}$


Vereinfachen liefert:

>[!success]- Antwort
>
>$-2(a_{1}b_{1}+a_{2}b_{2}) = 0 \Leftrightarrow a_{1}b_{1}+a_{2}b_{2} = 0$


Zwei Vektoren $\vec{a}$, $\vec{b}$ stehen also genau dann orthogonal zueinander, wenn:

>[!success]- 
>
>$$a_{1}b_{1}+a_{2}b_{2} = 0$$ 
