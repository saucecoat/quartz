---
title: Übungsaufgaben Extremstellen berechnen
date: 2026-02-03
tags:
  - alle
  - mathe
  - schule
  - analysis
  - kurvendiskussion
  - extremstelle
  - sattelpunkt
  - ganzrationale_funktion
  - aufgabe
  - python 
---


## Anmerkungen 

$a, b, c$ geben die Nullstellen der Ableitungsfunktion $f'(x)=m \cdot \left( a^{n}(x-b)(x-c) + K \right)$ an, d.&nbsp;h. die Sattel- bzw. Extremstellen von $f(x)$.<br>
(Hierbei gilt $a \in [-1, 1]\cap\mathbb{Z}$, $n \in \{1,2,3,4\}$, $b,c \in [-4,4]\cap\mathbb{Z}$, $K \in [-10,10]\cap\mathbb{Z}$ und $m \in \{\pm 1, \pm 2, \pm 3\}$. Diese Werte lassen sich im unten aufgeführten Python-Code beliebig anpassen).

Die Exponenten geben die Vielfachheit der Nullstellen an.<br>
Falls Exponent vorhanden $\rightarrow$ VZW-Kriterium nötig.<br>
Gerader Exponent $\rightarrow$ Sattelpunkt.<br>
Ungerader Exponent $\rightarrow$ Extrempunkt.


## Aufgaben

**Kategorie 1: Potenzfunktion**

1. $f(x) = \frac{3}{5}x^5 + 15$ (a=0^4)
2. $f(x) = - \frac{1}{5}x^5 + 4$ (a=0^4)
3. $f(x) = - \frac{1}{4}x^4 - 2$ (a=0^3)
4. $f(x) = - \frac{1}{2}x^6 + 21$ (a=0^5)
5. $f(x) = - \frac{1}{4}x^4 - 2$ (a=0^3)
6. $f(x) = x^3 - 12$ (a=0)
7. $f(x) = - \frac{1}{2}x^4 + 4$ (a=0^3)
8. $f(x) = - \frac{1}{3}x^3 + 6$ (a=0)
9. $f(x) = - \frac{1}{2}x^6 - 3$ (a=0^5)
10. $f(x) = \frac{1}{5}x^5 - 1$ (a=0^4)
11. $f(x) = - \frac{2}{3}x^3 - 4$ (a=0)
12. $f(x) = - \frac{1}{2}x^4 - 6$ (a=0^3)
13. $f(x) = x^3 - 21$ (a=0)
14. $f(x) = - \frac{1}{7}x^7 + 7$ (a=0^6)
15. $f(x) = - \frac{2}{3}x^3 - 20$ (a=0)
16. $f(x) = \frac{3}{4}x^4 + 12$ (a=0^3)
17. $f(x) = x^3 - 18$ (a=0)
18. $f(x) = - \frac{1}{3}x^3 - 2$ (a=0)
19. $f(x) = \frac{3}{7}x^7 - 15$ (a=0^6)
20. $f(x) = - \frac{1}{7}x^7 - 10$ (a=0^6)
21. $f(x) = \frac{1}{6}x^6 - 6$ (a=0^5)
22. $f(x) = \frac{2}{5}x^5 - 18$ (a=0^4)
23. $f(x) = - x^3 + 15$ (a=0)
24. $f(x) = \frac{3}{5}x^5 + 21$ (a=0^4)
25. $f(x) = - \frac{1}{3}x^3 - 3$ (a=0)
26. $f(x) = - \frac{2}{7}x^7 + 8$ (a=0^6)
27. $f(x) = - \frac{1}{3}x^3 - 9$ (a=0)
28. $f(x) = - \frac{1}{7}x^7 + 5$ (a=0^6)
29. $f(x) = - \frac{3}{4}x^4 - 9$ (a=0^3)
30. $f(x) = - \frac{2}{5}x^5 - 8$ (a=0^4)

**Kategorie 2: Zwei Extremstellen, nur Ausklammern nötig**

1. $f(x) = \frac{2}{3}x^3 + x^2 + 10$ (a=0, b=-1)
2. $f(x) = \frac{2}{3}x^3 - 3x^2 + 8$ (a=0, c=3)
3. $f(x) = - \frac{2}{3}x^3 - x^2 + 6$ (a=0, c=-1)
4. $f(x) = - x^3 - \frac{9}{2}x^2$ (a=0, c=-3)
5. $f(x) = - \frac{1}{3}x^3 - \frac{1}{2}x^2 + 5$ (a=0, b=-1)
6. $f(x) = \frac{2}{3}x^3 + 2x^2$ (a=0, b=-2)
7. $f(x) = - \frac{1}{3}x^3 + x^2 + 8$ (a=0, b=2)
8. $f(x) = \frac{1}{3}x^3 - x^2$ (a=0, c=2)
9. $f(x) = \frac{1}{3}x^3 + x^2 + 4$ (a=0, c=-2)
10. $f(x) = - \frac{1}{3}x^3 + 2x^2 + 1$ (a=0, b=4)
11. $f(x) = \frac{2}{3}x^3 + 4x^2 - 8$ (a=0, c=-4)
12. $f(x) = \frac{2}{3}x^3 + 3x^2$ (a=0, c=-3)
13. $f(x) = - x^3 - 3x^2 + 30$ (a=0, b=-2)
14. $f(x) = \frac{1}{3}x^3 - x^2 - 3$ (a=0, b=2)
15. $f(x) = x^3 + \frac{3}{2}x^2 - 24$ (a=0, c=-1)
16. $f(x) = x^3 - \frac{3}{2}x^2 - 30$ (a=0, c=1)
17. $f(x) = - \frac{2}{3}x^3 - 3x^2 + 16$ (a=0, b=-3)
18. $f(x) = \frac{1}{3}x^3 - \frac{3}{2}x^2 + 8$ (a=0, c=3)
19. $f(x) = x^3 - \frac{9}{2}x^2 - 3$ (a=0, c=3)
20. $f(x) = - \frac{1}{3}x^3 - \frac{1}{2}x^2 - 10$ (a=0, c=-1)
21. $f(x) = \frac{1}{3}x^3 - x^2 - 6$ (a=0, b=2)
22. $f(x) = - \frac{1}{3}x^3 - x^2 - 2$ (a=0, b=-2)
23. $f(x) = \frac{2}{3}x^3 - 2x^2 - 10$ (a=0, b=2)
24. $f(x) = - \frac{2}{3}x^3 + 3x^2 + 8$ (a=0, c=3)
25. $f(x) = \frac{2}{3}x^3 - 2x^2 - 6$ (a=0, b=2)
26. $f(x) = - \frac{1}{3}x^3 - x^2 + 10$ (a=0, c=-2)
27. $f(x) = \frac{1}{3}x^3 + 2x^2 + 7$ (a=0, c=-4)
28. $f(x) = \frac{1}{3}x^3 + \frac{3}{2}x^2 + 8$ (a=0, c=-3)
29. $f(x) = \frac{2}{3}x^3 + 3x^2 - 14$ (a=0, b=-3)
30. $f(x) = - x^3 - \frac{3}{2}x^2 + 27$ (a=0, b=-1)

**Kategorie 3: Zwei Extremstellen, quadratische Gleichung**

1. $f(x) = x^3 - 3x^2 - 24x + 30$ (b=-2, c=4)
2. $f(x) = - \frac{2}{3}x^3 - 2x^2 + 6x + 2$ (b=-3, c=1)
3. $f(x) = - x^3 - 3x^2 + 9x - 30$ (b=-3, c=1)
4. $f(x) = - x^3 + \frac{15}{2}x^2 - 12x - 6$ (b=1, c=4)
5. $f(x) = - \frac{1}{3}x^3 + 2x^2 - 3x + 2$ (b=3, c=1)
6. $f(x) = - x^3 - \frac{15}{2}x^2 - 18x - 6$ (b=-2, c=-3)
7. $f(x) = \frac{2}{3}x^3 - 3x^2 - 8x$ (b=-1, c=4)
8. $f(x) = - \frac{1}{3}x^3 + \frac{1}{2}x^2 + 6x - 5$ (b=3, c=-2)
9. $f(x) = - \frac{2}{3}x^3 + 8x - 10$ (b=2, c=-2)
10. $f(x) = \frac{2}{3}x^3 + 3x^2 - 8x + 16$ (b=1, c=-4)
11. $f(x) = \frac{2}{3}x^3 - 4x^2 + 6x + 14$ (b=1, c=3)
12. $f(x) = - \frac{2}{3}x^3 + 2x^2 + 6x - 2$ (b=-1, c=3)
13. $f(x) = - x^3 + \frac{3}{2}x^2 + 6x + 30$ (b=-1, c=2)
14. $f(x) = - x^3 - 3x^2 + 24x - 6$ (b=-4, c=2)
15. $f(x) = - x^3 + \frac{9}{2}x^2 + 12x - 15$ (b=-1, c=4)
16. $f(x) = - \frac{1}{3}x^3 - x^2 + 8x - 8$ (b=-4, c=2)
17. $f(x) = \frac{2}{3}x^3 + 2x^2 - 6x - 4$ (b=1, c=-3)
18. $f(x) = x^3 - 3x - 30$ (b=1, c=-1)
19. $f(x) = - \frac{1}{3}x^3 + \frac{5}{2}x^2 - 6x - 5$ (b=2, c=3)
20. $f(x) = - \frac{1}{3}x^3 + x^2 + 8x - 7$ (b=4, c=-2)
21. $f(x) = \frac{2}{3}x^3 + x^2 - 4x - 6$ (b=-2, c=1)
22. $f(x) = x^3 - 3x^2 - 24x$ (b=-2, c=4)
23. $f(x) = \frac{1}{3}x^3 + 3x^2 + 8x - 4$ (b=-2, c=-4)
24. $f(x) = - x^3 + \frac{3}{2}x^2 + 18x$ (b=-2, c=3)
25. $f(x) = - \frac{2}{3}x^3 + 2x^2 + 6x$ (b=-1, c=3)
26. $f(x) = - \frac{2}{3}x^3 - x^2 + 12x$ (b=2, c=-3)
27. $f(x) = - \frac{2}{3}x^3 + 7x^2 - 24x - 6$ (b=4, c=3)
28. $f(x) = - \frac{1}{3}x^3 + \frac{5}{2}x^2 - 4x + 6$ (b=4, c=1)
29. $f(x) = - x^3 - \frac{21}{2}x^2 - 36x + 6$ (b=-4, c=-3)
30. $f(x) = - x^3 + \frac{3}{2}x^2 + 18x - 30$ (b=3, c=-2)

**Kategorie 4: Ein Sattelpunkt, VZW-Kriterium, quadratische Gleichung**

1. $f(x) = - \frac{2}{3}x^3 + 2x^2 - 2x + 6$ (b=1^2)
2. $f(x) = - x^3 - 9x^2 - 27x - 3$ (b=-3^2)
3. $f(x) = \frac{2}{3}x^3 - 6x^2 + 18x - 18$ (b=3^2)
4. $f(x) = x^3 - 12x^2 + 48x - 9$ (b=4^2)
5. $f(x) = - \frac{2}{3}x^3 - 4x^2 - 8x + 14$ (b=-2^2)
6. $f(x) = \frac{2}{3}x^3 - 8x^2 + 32x + 8$ (b=4^2)
7. $f(x) = \frac{1}{3}x^3 - x^2 + x - 10$ (b=1^2)
8. $f(x) = - \frac{2}{3}x^3 - 8x^2 - 32x - 10$ (b=-4^2)
9. $f(x) = - \frac{1}{3}x^3 - 2x^2 - 4x - 10$ (b=-2^2)
10. $f(x) = - \frac{2}{3}x^3 + 8x^2 - 32x + 18$ (b=4^2)
11. $f(x) = x^3 - 6x^2 + 12x + 24$ (b=2^2)
12. $f(x) = - x^3 + 3x^2 - 3x + 27$ (b=1^2)
13. $f(x) = - \frac{2}{3}x^3 + 8x^2 - 32x + 14$ (b=4^2)
14. $f(x) = - \frac{2}{3}x^3 - 4x^2 - 8x + 4$ (b=-2^2)
15. $f(x) = x^3 + 3x^2 + 3x + 12$ (b=-1^2)
16. $f(x) = \frac{1}{3}x^3 - 3x^2 + 9x - 2$ (b=3^2)
17. $f(x) = - \frac{2}{3}x^3 + 8x^2 - 32x$ (b=4^2)
18. $f(x) = - x^3 - 3x^2 - 3x + 18$ (b=-1^2)
19. $f(x) = - \frac{1}{3}x^3 + 2x^2 - 4x + 9$ (b=2^2)
20. $f(x) = - \frac{1}{3}x^3 - 4x^2 - 16x - 5$ (b=-4^2)
21. $f(x) = \frac{2}{3}x^3 + 4x^2 + 8x - 10$ (b=-2^2)
22. $f(x) = - x^3 + 6x^2 - 12x + 21$ (b=2^2)
23. $f(x) = - \frac{1}{3}x^3 + x^2 - x - 7$ (b=1^2)
24. $f(x) = - \frac{1}{3}x^3 - 3x^2 - 9x - 8$ (b=-3^2)
25. $f(x) = \frac{2}{3}x^3 - 8x^2 + 32x + 2$ (b=4^2)
26. $f(x) = x^3 + 9x^2 + 27x - 15$ (b=-3^2)
27. $f(x) = \frac{2}{3}x^3 - 2x^2 + 2x - 20$ (b=1^2)
28. $f(x) = x^3 + 9x^2 + 27x - 12$ (b=-3^2)
29. $f(x) = \frac{1}{3}x^3 - 3x^2 + 9x - 3$ (b=3^2)
30. $f(x) = \frac{1}{3}x^3 + x^2 + x - 2$ (b=-1^2)

**Kategorie 5: Eine Extremstelle & eine Sattel-/Extremstelle, VZW-Kriterium, nur Ausklammern nötig**

1. $f(x) = \frac{1}{4}x^4 + x^3 - 8$ (a=0^2, c=-3)
2. $f(x) = - \frac{3}{7}x^7 - 2x^6 - 30$ (a=0^5, b=-4)
3. $f(x) = - \frac{1}{4}x^4 + \frac{2}{3}x^3 - 7$ (a=0^2, b=2)
4. $f(x) = - \frac{1}{2}x^6 + \frac{6}{5}x^5 - 27$ (a=0^4, c=2)
5. $f(x) = - \frac{3}{4}x^4 - 2x^3 - 15$ (a=0^2, c=-2)
6. $f(x) = - \frac{1}{2}x^6 + \frac{9}{5}x^5 + 3$ (a=0^4, c=3)
7. $f(x) = \frac{3}{5}x^5 - 3x^4 - 27$ (a=0^3, c=4)
8. $f(x) = - \frac{1}{6}x^6 - \frac{2}{5}x^5 - 4$ (a=0^4, b=-2)
9. $f(x) = - \frac{1}{7}x^7 - \frac{1}{3}x^6 - 6$ (a=0^5, b=-2)
10. $f(x) = \frac{1}{3}x^6 - \frac{6}{5}x^5 - 18$ (a=0^4, b=3)
11. $f(x) = \frac{3}{7}x^7 - 2x^6$ (a=0^5, c=4)
12. $f(x) = - \frac{1}{2}x^4 + 2x^3 - 4$ (a=0^2, b=3)
13. $f(x) = - \frac{1}{4}x^4 - \frac{4}{3}x^3 + 5$ (a=0^2, b=-4)
14. $f(x) = - \frac{1}{2}x^6 + \frac{6}{5}x^5 - 30$ (a=0^4, c=2)
15. $f(x) = \frac{1}{5}x^5 - x^4 - 2$ (a=0^3, c=4)
16. $f(x) = \frac{1}{7}x^7 + \frac{1}{2}x^6 + 8$ (a=0^5, c=-3)
17. $f(x) = - \frac{1}{7}x^7 + \frac{2}{3}x^6 + 1$ (a=0^5, b=4)
18. $f(x) = - \frac{3}{4}x^4 + 2x^3 + 3$ (a=0^2, b=2)
19. $f(x) = \frac{1}{2}x^6 + \frac{12}{5}x^5 + 15$ (a=0^4, c=-4)
20. $f(x) = - \frac{3}{4}x^4 + 2x^3 - 3$ (a=0^2, b=2)
21. $f(x) = \frac{1}{2}x^6 - \frac{12}{5}x^5 + 24$ (a=0^4, c=4)
22. $f(x) = \frac{1}{2}x^4 + \frac{4}{3}x^3 + 20$ (a=0^2, c=-2)
23. $f(x) = \frac{1}{4}x^4 - \frac{2}{3}x^3 + 8$ (a=0^2, c=2)
24. $f(x) = \frac{1}{2}x^4 - \frac{4}{3}x^3 + 16$ (a=0^2, b=2)
25. $f(x) = - \frac{1}{4}x^4 - x^3 - 9$ (a=0^2, c=-3)
26. $f(x) = - \frac{3}{5}x^5 + 3x^4 + 24$ (a=0^3, b=4)
27. $f(x) = - \frac{1}{6}x^6 + \frac{2}{5}x^5 + 5$ (a=0^4, b=2)
28. $f(x) = \frac{3}{5}x^5 + 3x^4 + 3$ (a=0^3, b=-4)
29. $f(x) = \frac{3}{5}x^5 + \frac{3}{2}x^4 - 3$ (a=0^3, c=-2)
30. $f(x) = - \frac{3}{4}x^4 + 3x^3 + 30$ (a=0^2, b=3)

**Kategorie 6: Zwei bis drei Sattel-/Extremstellen, VZW-Kriterium, quadratische Gleichung**

1. $f(x) = - \frac{2}{5}x^5 - \frac{5}{2}x^4 - \frac{8}{3}x^3 - 20$ (a=0^2, b=-4, c=-1)
2. $f(x) = \frac{3}{5}x^5 + \frac{15}{4}x^4 + 6x^3 - 27$ (a=0^2, b=-3, c=-2)
3. $f(x) = - \frac{1}{2}x^6 - \frac{6}{5}x^5 + \frac{9}{4}x^4 - 18$ (a=0^3, b=-3, c=1)
4. $f(x) = \frac{1}{6}x^6 - \frac{3}{5}x^5 + \frac{1}{2}x^4 + 4$ (a=0^3, b=1, c=2)
5. $f(x) = - \frac{3}{5}x^5 + 4x^3 + 15$ (a=0^2, b=2, c=-2)
6. $f(x) = - \frac{3}{7}x^7 - \frac{3}{2}x^6 - \frac{6}{5}x^5 - 21$ (a=0^4, b=-1, c=-2)
7. $f(x) = - \frac{3}{5}x^5 - \frac{9}{4}x^4 + 4x^3 + 9$ (a=0^2, b=-4, c=1)
8. $f(x) = - \frac{1}{3}x^6 + \frac{1}{2}x^4 + 12$ (a=0^3, b=-1, c=1)
9. $f(x) = \frac{1}{6}x^6 - \frac{1}{5}x^5 - 3x^4 - 3$ (a=0^3, b=4, c=-3)
10. $f(x) = \frac{3}{7}x^7 - x^6 - \frac{9}{5}x^5 + 9$ (a=0^4, b=3, c=-1)
11. $f(x) = - \frac{1}{5}x^5 + \frac{16}{3}x^3 - 5$ (a=0^2, b=-4, c=4)
12. $f(x) = \frac{1}{2}x^6 + \frac{9}{5}x^5 + \frac{3}{2}x^4 + 3$ (a=0^3, b=-2, c=-1)
13. $f(x) = - \frac{1}{6}x^6 - \frac{4}{5}x^5 - \frac{3}{4}x^4 + 1$ (a=0^3, b=-3, c=-1)
14. $f(x) = \frac{3}{5}x^5 - 9x^3 - 18$ (a=0^2, b=-3, c=3)
15. $f(x) = \frac{1}{6}x^6 + \frac{6}{5}x^5 + \frac{9}{4}x^4 + 3$ (a=0^3, b=-3^2)
16. $f(x) = - \frac{2}{7}x^7 - \frac{5}{3}x^6 - \frac{12}{5}x^5 + 18$ (a=0^4, b=-3, c=-2)
17. $f(x) = \frac{1}{7}x^7 - x^6 + \frac{8}{5}x^5 + 9$ (a=0^4, b=2, c=4)
18. $f(x) = - \frac{1}{7}x^7 - \frac{1}{3}x^6 + \frac{3}{5}x^5 + 7$ (a=0^4, b=1, c=-3)
19. $f(x) = - \frac{3}{7}x^7 + \frac{27}{5}x^5 - 12$ (a=0^4, b=3, c=-3)
20. $f(x) = - \frac{1}{5}x^5 - \frac{5}{4}x^4 - \frac{4}{3}x^3 + 10$ (a=0^2, b=-1, c=-4)
21. $f(x) = - \frac{3}{7}x^7 + \frac{3}{2}x^6 + \frac{12}{5}x^5 + 6$ (a=0^4, b=4, c=-1)
22. $f(x) = \frac{3}{7}x^7 - \frac{3}{2}x^6 - \frac{12}{5}x^5 - 12$ (a=0^4, b=4, c=-1)
23. $f(x) = - \frac{1}{5}x^5 + \frac{16}{3}x^3 + 10$ (a=0^2, b=4, c=-4)
24. $f(x) = \frac{1}{2}x^6 - \frac{3}{4}x^4 - 21$ (a=0^3, b=1, c=-1)
25. $f(x) = - \frac{2}{5}x^5 - 3x^4 - 6x^3 + 16$ (a=0^2, b=-3^2)
26. $f(x) = - \frac{3}{5}x^5 - \frac{3}{2}x^4 + 3x^3 - 6$ (a=0^2, b=1, c=-3)
27. $f(x) = \frac{2}{7}x^7 + \frac{5}{3}x^6 + \frac{12}{5}x^5 + 10$ (a=0^4, b=-3, c=-2)
28. $f(x) = \frac{1}{2}x^6 - \frac{3}{5}x^5 - 9x^4 + 12$ (a=0^3, b=4, c=-3)
29. $f(x) = \frac{1}{7}x^7 - \frac{1}{5}x^5 - 2$ (a=0^4, b=-1, c=1)
30. $f(x) = \frac{3}{7}x^7 - \frac{3}{5}x^5 + 3$ (a=0^4, b=-1, c=1)

## Python-Code


```python
import random
from fractions import Fraction

# ---------------- Hilfsfunktionen ----------------

def term_to_latex(coeff, power):
    if coeff == 0:
        return ""

    sign = "-" if coeff < 0 else "+"
    coeff = abs(coeff)

    if coeff.denominator == 1:
        coeff_str = f"{coeff.numerator}"
    else:
        coeff_str = f"\\frac{{{coeff.numerator}}}{{{coeff.denominator}}}"

    if power == 0:
        term = coeff_str
    elif power == 1:
        term = "x" if coeff == 1 else f"{coeff_str}x"
    else:
        term = f"x^{power}" if coeff == 1 else f"{coeff_str}x^{power}"

    return f" {sign} {term}"

def build_latex(terms, K):
    latex = "".join(terms).strip()
    if latex.startswith("+"):
        latex = latex[2:]
    if K != 0:
        sign = "+" if K > 0 else "-"
        latex += f" {sign} {abs(K)}"
    return latex

# ---------------- Kategorie-Logik ----------------

def get_category(bracket):
    has_a = "a=" in bracket
    has_b = "b=" in bracket
    has_c = "c=" in bracket

    a_pow = "a=0^" in bracket
    b_pow = has_b and "^" in bracket.split("b=")[1]
    c_pow = has_c and "^" in bracket.split("c=")[1]

    var_count = sum([has_a, has_b, has_c])

    if has_a and not has_b and not has_c:
        return 1

    if has_a and (has_b ^ has_c) and not a_pow and not b_pow and not c_pow:
        return 2

    if not has_a and has_b and has_c and not b_pow and not c_pow:
        return 3

    if not has_a and (b_pow or c_pow):
        return 4

    if var_count == 2 and has_a:
        if has_b and a_pow and not b_pow:
            return 5
        if has_c and a_pow and not c_pow:
            return 5

    if has_a and a_pow:
        if (has_b and b_pow) or (has_c and c_pow):
            return 6
        if has_b and has_c and not b_pow and not c_pow:
            return 6

    return None

# ---------------- Generierung ----------------

tasks_per_category = 30

excluded_combinations = [(0,1), (0,-1), (1,0), (-1,0), (1,1), (-1,-1)]
categories = {i: [] for i in range(1, 7)}

while any(len(categories[i]) < tasks_per_category for i in categories):

    a = random.randint(-1, 1)
    b = random.randint(-4, 4)
    c = random.randint(-4, 4)
    K = random.randint(-10, 10)
    exp = random.randint(1, 4)

    if a != 0 and (b, c) in excluded_combinations:
        continue

    m = random.choice([1, 2, 3, -1, -2, -3])

    terms = []

   
  #  --------- Fall a = 0 ---------
    if a == 0:
        A = Fraction(1, 3) * m
        B = Fraction(b + c, 2) * m
        C = Fraction(b * c, 1) * m
        K *= m

        terms.append(term_to_latex(A, 3))
        terms.append(term_to_latex(B, 2))
        terms.append(term_to_latex(C, 1))

        parts = [] if not (b == 0 or c == 0) else ["a=0"]

        if b != 0 and b == c:
            parts.append(f"b={-b}^2")
        else:
            if b != 0:
                parts.append(f"b={-b}")
            if c != 0 and c != b:
                parts.append(f"c={-c}")

   
  #  --------- Fall a ≠ 0 ---------
    else:
        zero_count = (b == 0) + (c == 0)
        n_final = exp + zero_count

        A = Fraction(a, exp + 3) * m
        B = Fraction(a * (b + c), exp + 2) * m
        C = Fraction(a * b * c, exp + 1) * m
        K *= m

        terms.append(term_to_latex(A, exp + 3))
        terms.append(term_to_latex(B, exp + 2))
        terms.append(term_to_latex(C, exp + 1))

        a_str = "a=0" if n_final == 1 else f"a=0^{n_final}"
        parts = [a_str]

        if b != 0 and b == c:
            parts.append(f"b={-b}^2")
        else:
            if b != 0:
                parts.append(f"b={-b}")
            if c != 0 and c != b:
                parts.append(f"c={-c}")

    bracket_str = ", ".join(parts)
    latex_function = build_latex(terms, K)
    output = f"$f(x) = {latex_function}$ ({bracket_str})"

    cat = get_category(bracket_str)
    if cat and len(categories[cat]) < tasks_per_category:
        categories[cat].append(output)

# ---------------- Ausgabe ----------------

for cat in range(1, 7):
    print(f"\n**Kategorie {cat}**\n")
    for i, task in enumerate(categories[cat], 1):
        print(f"{i}. {task}")
```

