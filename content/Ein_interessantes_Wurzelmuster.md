---
title: "Ein interessantes Wurzelmuster"
date: "2022-11-15"
tags: [alle, math, pattern, muster, square_root, root, wurzel]
---

Hier ist ein interssantes Muster, das ich beim Herumspielen mit Wurzeln entdeckt habe:

 $$\begin{aligned}0,5&=\sqrt{0,25}\\\\1,5&=\sqrt{2,25}\\\\2,5&=\sqrt{6,25}\\\\3,5&=\sqrt{12,25}\\\\4,5&=\sqrt{20,25}\\\\5,5&=\sqrt{30,25}\\\\6,5&=\sqrt{42,25}\end{aligned}$$    

Die Zahlen unter der Wurzel erhöhen sich bei jedem Schritt nach dem folgenen Muster: 
+2, +4, +6, +8, +10, +12, ...

Wenn man diese Zahlen bis zum $n$-ten Schritt aufaddiert, sieht man, dass das Ergebnis gleich dem Doppelten der $n$-ten Dreieckszahl ist. Also: $2 \cdot \frac{1}{2} \cdot n \cdot (n+1)$, 

Insgesamt ergibt sich also:
$$n+0,5=\sqrt{n \cdot (n+1) +0,25}$$

Es ist also z. B. $7,5=\sqrt{7 \cdot 8 +0,25}=\sqrt{56,25}$ oder $30,5=\sqrt{30 \cdot 31 +0,25}=\sqrt{930,25}$. Ziemlich nett.

Um zu sehen, warum dem so ist, müssen wir nur beide Seiten quadrieren und dann vereinfachen:

$$\begin{aligned}(n+0,5)^{2}&=n \cdot(n+1)+0,25\\\\\Leftrightarrow n^{2}+n+0,25&=n^{2}+n+0,25\end{aligned}$$

Dieses Resultat haut einen vielleicht nicht aus den Socken, aber ich liebe es, wenn man herausfindet, warum ein gefundenes Muster, so ist, wie es ist.

Etwas auf den ersten Blick Mysteriöses nur mithilfe von logischen Schlüssen in etwas Selbstverständliches zu verwandeln, ist einfach wunderschön.
