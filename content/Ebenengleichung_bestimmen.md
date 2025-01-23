---
title: Ebenengleichung bestimmen
date: 2025-01-23
tags:
  - alle
  - mathe
  - lineare_algebra
  - analytische_geometrie
  - ebene
  - ebenengleichung
  - parameterform
  - parametergleichung
  - normalenform
  - koordinatenform
  - koordinatengleichung
  - hessesche_normalform
  - aufgabe
  - punkt
  - gerade
---


## Hinweise 

- Die folgenden Beispiele beziehen sich auf den Vektorraum $\mathbb{R}^{3}$.
- Im Folgenden bezeichnet $S_{g}$ den Stützvektor der Geraden $g$ und $\vec{r}\_{g}$ den Richtungsvektor der Geraden $g$.
- Ebenengleichungen sind in ihrer Darstellung nicht eindeutig. Man könnte jeweils auch eine andere Geradengleichung bestimmen, indem man z.&nbsp;B. einen anderen Stützvektor als den im Beispiel verwendeten wählt. 

--- 

## Die Schritte zum Bestimmen einer Ebenengleichung

Die grundsätzlichen Schritte zum Bestimmen einer Ebenengleichung sind stets dieselben:

>**Schritt 1:** Gegenseitige Lage der gegebenen Objekte bestimmen
>
>**Schritt 2:** Spannvektoren bestimmen
**Schritt 2b (nur bei Koordinaten- und Normalenform):** Normalenvektor bestimmen
>
>**Schritt 3:** Geradengleichung aufstellen

---

## Ebene aus drei Punkten

>**Fall ①: Die Punkte liegen nicht auf einer gemeinsamen Geraden**
>
>$\quad A(3|-2|0),~B(1|-1|2),~C(2|1|2)$
>
>**Fall ②: Die Punkte liegen auf einer gemeinsamen Geraden**
>
>$\quad A(1|2|-1),~B(2|3|-4),~C(-1|0|5)$



### **Schritt 1:** Gegenseitige Lage der gegebenen Objekte bestimmen

Überprüfen, ob die drei Punkte auf einer gemeinsamen Geraden liegen.

>**Fall ①: Die Punkte liegen nicht auf einer gemeinsamen Geraden**
>
>$$\vec{AB}=\begin{pmatrix}-2\\\\1\\\\2\end{pmatrix},~\vec{AC}=\begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$$
>
>Auf Kollinearität prüfen:
>
>$$k \cdot\begin{pmatrix}-2\\\\1\\\\2\end{pmatrix} = \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$$
>
>$$
>\begin{aligned}
>-2k &= -1 & \Rightarrow & \quad k = \frac{1}{2} \\\\
>\Rightarrow \qquad\quad k &= 3 & \Rightarrow & \quad k = 3 \\\\
>2k &= 2 & \Rightarrow & \quad k = 1 
>\end{aligned}
>$$
>$$\tag*{$\text{Widerspruch!}$}$$
><br><br>
>$\vec{AB}$ und $\vec{AC}$ sind nicht kollinear. Die Punkte $A$, $B$ & $C$ liegen damit nicht auf einer gemeinsamen Gerade. 
>$\vec{AB}$ und $\vec{AC}$ können also als Spannvektoren verwendet werden.

>**Fall ②: Die Punkte liegen auf einer gemeinsamen Geraden**
>
>$$\vec{AB}=\begin{pmatrix}1\\\\1\\\\-3\end{pmatrix},~\vec{AC}=\begin{pmatrix}-2\\\\-2\\\\6\end{pmatrix}$$
>
>Auf Kollinearität prüfen:
>
>$$k \cdot\begin{pmatrix}1\\\\1\\\\-3\end{pmatrix} = \begin{pmatrix}-2\\\\-2\\\\6\end{pmatrix}$$
>
>$$
>\begin{aligned}
>k &= -2 \\\\
>\Rightarrow \qquad\quad k &= -2  \\\\
>k &= -2  \\
>\end{aligned}
>$$
>
>$\vec{AB}$ und $\vec{AC}$ sind kollinear. Die Punkte $A$, $B$ & $C$ liegen damit auf einer gemeinsamen Gerade. 
>Somit können mit ihnen keine Spannvektoren bestimmt werden.

### **Schritt 2:** Spannvektoren bestimmen

>**Fall ①: Die Punkte liegen nicht auf einer gemeinsamen Geraden**
>
>Laut Schritt 1 können $\vec{AB}=\begin{pmatrix}-2\\\\1\\\\2\end{pmatrix},~\vec{AC}=\begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$ als Spannvektoren verwendet werden.

### **Schritt 2b (nur bei Koordinaten- und Normalenform):** Normalenvektor bestimmen

>**Fall ①: Die Punkte liegen nicht auf einer gemeinsamen Geraden**
>
>$$\begin{aligned}
\vec{n} &= \vec{AB} \times \vec{AC} \\\\
&= \begin{pmatrix}-2\\\\1\\\\2\end{pmatrix} \times \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}\\\\\\\\
&= \begin{pmatrix}-4\\\\2\\\\-5\end{pmatrix}
\end{aligned}$$

### **Schritt 3:** Geradengleichung aufstellen

>**Fall ①: Die Punkte liegen nicht auf einer gemeinsamen Geraden**
>
>**Parameterform:** $$E: X = A + s \cdot \vec{AB} + t \cdot \vec{AC}$$
$$\Rightarrow E: X=\begin{pmatrix}3\\\\-2\\\\0\end{pmatrix} + s \cdot \begin{pmatrix}-2\\\\1\\\\2\end{pmatrix} + t \cdot \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$$
>
>**Normalenform:** $$E: \vec{n} \cdot \left( X - A\right) = 0$$
$$\Rightarrow E: \begin{pmatrix}-4\\\\2\\\\-5\end{pmatrix} \cdot \left[X - \begin{pmatrix}-2\\\\1\\\\2\end{pmatrix}\right] = 0$$
>
>**Koordinatenform:** $$E: n_{1}x_{1} + n_{2}x_{2} + n_{3}x_{3} = \vec{n} \cdot A$$
$$\Rightarrow E: -4x_{1} + 2x_{2} - 5x_{3} = \begin{pmatrix}-4\\\\2\\\\-5\end{pmatrix} \cdot \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix}$$
$$\Rightarrow E: -4x_{1} + 2x_{2} - 5x_{3} = -16$$
>
>**Hessesche Normalform:** $$E: -4x_{1} + 2x_{2} - 5x_{3} = -16$$
>$$\Rightarrow E: 4x_{1} - 2x_{2} + 5x_{3} = 16$$
>$$\Rightarrow E: 4x_{1} - 2x_{2} + 5x_{3} - 16 = 0$$
>$$\Rightarrow E: \frac{1}{\sqrt{4^{2} + (-2)^{2} + 5^{2}}} \cdot (4x_{1} - 2x_{2} + 5x_{3} - 16) = 0$$
>$$\Rightarrow E: \frac{1}{\sqrt{45}} \cdot (4x_{1} - 2x_{2} + 5x_{3} - 16) = 0$$

---

## Ebene aus Punkt und Gerade

>**Fall ①: Punkt liegt nicht auf Gerade**
>
>$\quad B(1|-1|2),~~g: X = \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix} + p \cdot \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$
>
>**Fall ②: Punkt liegt auf Gerade**
>
>$\quad B(2|1|2),~~g: X = \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix} + p \cdot \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$

### **Schritt 1:** Gegenseitige Lage der gegebenen Objekte bestimmen

Überprüfen, ob der Punkt $B$ auf der Geraden $g$ liegt.

>**Fall ①: Punkt liegt nicht auf Gerade**
>
>$$\overrightarrow{S_{g}B} = \begin{pmatrix}1\\\\-1\\\\2\end{pmatrix} - \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix} = \begin{pmatrix}-2\\\\1\\\\2\end{pmatrix}$$
>$$\vec{r}\_{g} = \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$$
>
>Auf Kollinearität prüfen:
>
>$$k \cdot\begin{pmatrix}-2\\\\1\\\\2\end{pmatrix} = \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$$
>
>$$
>\begin{aligned}
>-2k &= -1 & \Rightarrow & \quad k = \frac{1}{2} \\\\
>\Rightarrow \qquad\quad k &= 3 & \Rightarrow & \quad k = 3 \\\\
>2k &= 2 & \Rightarrow & \quad k = 1 
>\end{aligned}
>$$
>$$\tag*{$\text{Widerspruch!}$}$$
><br><br>
>$\overrightarrow{S_{g}B}$ und $\vec{r}\_{g}$ sind nicht kollinear. Also können beide als Spannvektoren verwendet werden.
>An dieser Stelle wäre auch eine Punktprobe möglich gewesen, allerdings haben wir auf diese Weise bereits zwei Spannvektoren bestimmt.

>**Fall ②: Punkt liegt auf Gerade**
>
>$$\overrightarrow{S_{g}B} = \begin{pmatrix}2\\\\1\\\\2\end{pmatrix} - \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix} = \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$$
>$$\vec{r}\_{g} = \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$$
>
>$\overrightarrow{S_{g}B}$ und $\vec{r}\_{g}$ sind offensichtlich kollinear und damit liegt Punkt $B$ auf der Geraden $g$. Also können aus diesem Punkt und dieser Geraden keine Spannvektoren bestimmt werden.
>An dieser Stelle wäre auch eine Punktprobe möglich gewesen.

### **Schritt 2:** Spannvektoren bestimmen

>**Fall ①: Punkt $B$ liegt nicht auf Gerade $g$**
>
>Laut Schritt 1 können $\overrightarrow{S_{g}B}=\begin{pmatrix}-2\\\\1\\\\2\end{pmatrix},~\vec{r}\_{g}=\begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$ als Spannvektoren verwendet werden.

### **Schritt 2b (nur bei Koordinaten- und Normalenform):** Normalenvektor bestimmen

>**Fall ①: Punkt liegt nicht auf Gerade**
>
>$$\begin{aligned}
\vec{n} &= \overrightarrow{S_{g}B} \times \vec{r}\_{g}\\\\
&= \begin{pmatrix}-2\\\\1\\\\2\end{pmatrix} \times \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}\\\\\\\\
&= \begin{pmatrix}-4\\\\2\\\\-5\end{pmatrix}
\end{aligned}$$

### **Schritt 3:** Geradengleichung aufstellen

>**Fall ①: Punkt liegt nicht auf Gerade**
>
>**Parameterform:** $$E: X = B + s \cdot \overrightarrow{S_{g}B} + t \cdot \vec{r}\_{g}$$
$$\Rightarrow E: X=\begin{pmatrix}1\\\\-1\\\\2\end{pmatrix} + s \cdot \begin{pmatrix}-2\\\\1\\\\2\end{pmatrix} + t \cdot \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$$
>
>**Normalenform:** $$E: \vec{n} \cdot \left( X - B\right) = 0$$
$$\Rightarrow E: \begin{pmatrix}-4\\\\2\\\\-5\end{pmatrix} \cdot \left[X - \begin{pmatrix}1\\\\-1\\\\2\end{pmatrix}\right] = 0$$
>
>**Koordinatenform:** $$E: n_{1}x_{1} + n_{2}x_{2} + n_{3}x_{3} = \vec{n} \cdot B$$
$$\Rightarrow E: -4x_{1} + 2x_{2} - 5x_{3} = \begin{pmatrix}-4\\\\2\\\\-5\end{pmatrix} \cdot \begin{pmatrix}1\\\\-1\\\\2\end{pmatrix}$$
$$\Rightarrow E: -4x_{1} + 2x_{2} - 5x_{3} = -16$$
>
>**Hessesche Normalform:** $$E: -4x_{1} + 2x_{2} - 5x_{3} = -16$$
>$$\Rightarrow E: 4x_{1} - 2x_{2} + 5x_{3} = 16$$
>$$\Rightarrow E: 4x_{1} - 2x_{2} + 5x_{3} - 16 = 0$$
>$$\Rightarrow E: \frac{1}{\sqrt{4^{2} + (-2)^{2} + 5^{2}}} \cdot (4x_{1} - 2x_{2} + 5x_{3} - 16) = 0$$
>$$\Rightarrow E: \frac{1}{\sqrt{45}} \cdot (4x_{1} - 2x_{2} + 5x_{3} - 16) = 0$$

---

## Ebene aus Gerade und Gerade

>**Fall ①: Geraden parallel**
>
>$\quad g: X = \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix} + p \cdot \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix},~~h: X = \begin{pmatrix}1\\\\-1\\\\2\end{pmatrix} + q \cdot \begin{pmatrix}-2\\\\6\\\\4\end{pmatrix}$
>
>**Fall ②: Geraden schneiden sich**
>
>$\quad g: X = \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix} + p \cdot \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix},~~h: X = \begin{pmatrix}2\\\\1\\\\2\end{pmatrix} + q \cdot \begin{pmatrix}-2\\\\1\\\\2\end{pmatrix}$
>
>**Fall ③: Geraden identisch**
>
>$\quad g: X = \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix} + p \cdot \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix},~~h: X = \begin{pmatrix}2\\\\1\\\\2\end{pmatrix} + q \cdot \begin{pmatrix}-2\\\\6\\\\4\end{pmatrix}$
>
>**Fall ④: Geraden windschief**
>
>$\quad g: X = \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix} + p \cdot \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix},~~h: X = \begin{pmatrix}1\\\\-1\\\\2\end{pmatrix} + q \cdot \begin{pmatrix}2\\\\-1\\\\-2\end{pmatrix}$

### **Schritt 1:** Gegenseitige Lage der gegebenen Objekte bestimmen

Gegenseitige Lage der beiden jeweiligen Geraden bestimmen.

>**Fall ①: Geraden parallel**
>
>Die Lage der Geraden $g$ & $h$ wird wie gewohnt bestimmt. 
>
>Sind $g$ & $h$ parallel, so kann eine eindeutige Ebenengleichung bestimmt werden.

>**Fall ②: Geraden schneiden sich**
>
>Die Lage der Geraden $g$ & $h$ wird wie gewohnt bestimmt. 
>
>Schneiden sich $g$ & $h$, so kann eine eindeutige Ebenengleichung bestimmt werden.

>**Fall ③: Geraden identisch**
>
>Die Lage der Geraden $g$ & $h$ wird wie gewohnt bestimmt. 
>
>Sind $g$ & $h$ identisch, so kann <u>**keine**</u> eindeutige Ebenengleichung bestimmt werden.

>**Fall ④: Geraden windschief**
>
>Die Lage der Geraden $g$ & $h$ wird wie gewohnt bestimmt. 
>
>Sind $g$ & $h$ windschief, so liegen sie nicht auf einer gemeinsamen Geraden und es kann <u>**keine**</u> Ebenengleichung bestimmt werden.

### **Schritt 2:** Spannvektoren bestimmen

>**Fall ①: Geraden parallel**
>
>Da $g$ & $h$ parallel sind, können die Richtungsvektoren $\vec{r}\_{g}$ & $\vec{r}\_{h}$ nicht als Spannvektoren verwendet werden, da diese kollinear sind.
>Als zweiten Spannvektoren können wir allerdings einen Vektor nehmen, der von einem Punkt der Geraden $g$ zu einem Punkt der Geraden $h$ führt. Als Spannvektoren können wir z.&nbsp;B. $\vec{r}\_{g} = \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$ & $\overrightarrow{S_{g}S_{h}} = \begin{pmatrix}-2\\\\1\\\\2\end{pmatrix}$ auswählen.

>**Fall ②: Geraden schneiden sich**
>
>Da sich $g$ & $h$ schneiden, kann ein Stützvektor einer Geraden z.&nbsp;B. $S_{g} = \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix}$ als Stützvektor der Ebene gewählt werden und die beiden Richtungsvektoren $\vec{r}\_{g} = \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix}$ & $\vec{r}\_{h} = \begin{pmatrix}-2\\\\1\\\\2\end{pmatrix}$ als Spannvektoren.

### **Schritt 2b (nur bei Koordinaten- und Normalenform):** Normalenvektor bestimmen

>**Fall ①: Geraden parallel**
>
>$$\begin{aligned}
\vec{n} &= \vec{r}\_{g} \times \overrightarrow{S_{g}S_{h}}\\\\\\\\
&= \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix} \times \begin{pmatrix}-2\\\\1\\\\2\end{pmatrix}\\\\\\\\
&= \begin{pmatrix}-4\\\\2\\\\-5\end{pmatrix}
\end{aligned}$$

>**Fall ②: Geraden schneiden sich**
>
>$$\begin{aligned}
\vec{n} &= \vec{r}\_{g} \times \vec{r}\_{h}\\\\\\\\
&= \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix} \times \begin{pmatrix}-2\\\\1\\\\2\end{pmatrix}\\\\\\\\
&= \begin{pmatrix}-4\\\\2\\\\-5\end{pmatrix}
\end{aligned}$$

### **Schritt 3:** Geradengleichung aufstellen

>**Fall ①: Geraden parallel**
>
>**Parameterform:** $$E: X = S_{g} + s \cdot \vec{r}\_{g} + t \cdot \overrightarrow{S_{g}S_{h}}$$
$$\Rightarrow E: X = \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix} + s \cdot \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix} + t \cdot \begin{pmatrix}-2\\\\1\\\\2\end{pmatrix}$$
>
>**Normalenform:** $$E: \vec{n} \cdot \left( X - S_{g}\right) = 0$$
$$\Rightarrow E: \begin{pmatrix}-4\\\\2\\\\-5\end{pmatrix} \cdot \left[X - \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix}\right] = 0$$
>
>**Koordinatenform:** $$E: n_{1}x_{1} + n_{2}x_{2} + n_{3}x_{3} = \vec{n} \cdot S_{g}$$
$$\Rightarrow E: -4x_{1} + 2x_{2} - 5x_{3} = \begin{pmatrix}-4\\\\2\\\\-5\end{pmatrix} \cdot \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix}$$
$$\Rightarrow E: -4x_{1} + 2x_{2} - 5x_{3} = -16$$
>
>**Hessesche Normalform:** $$E: -4x_{1} + 2x_{2} - 5x_{3} = -16$$
>$$\Rightarrow E: 4x_{1} - 2x_{2} + 5x_{3} = 16$$
>$$\Rightarrow E: 4x_{1} - 2x_{2} + 5x_{3} - 16 = 0$$
>$$\Rightarrow E: \frac{1}{\sqrt{4^{2} + (-2)^{2} + 5^{2}}} \cdot (4x_{1} - 2x_{2} + 5x_{3} - 16) = 0$$
>$$\Rightarrow E: \frac{1}{\sqrt{45}} \cdot (4x_{1} - 2x_{2} + 5x_{3} - 16) = 0$$

>**Fall ②: Geraden schneiden sich**
>
>**Parameterform:** $$E: X = S_{g} + s \cdot \vec{r}\_{g} + t \cdot \vec{r}\_{h}$$
$$\Rightarrow E: X = \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix} + s \cdot \begin{pmatrix}-1\\\\3\\\\2\end{pmatrix} + t \cdot \begin{pmatrix}-2\\\\1\\\\2\end{pmatrix}$$
>
>**Normalenform:** $$E: \vec{n} \cdot \left( X - S_{g}\right) = 0$$
$$\Rightarrow E: \begin{pmatrix}-4\\\\2\\\\-5\end{pmatrix} \cdot \left[X - \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix}\right] = 0$$
>
>**Koordinatenform:** $$E: n_{1}x_{1} + n_{2}x_{2} + n_{3}x_{3} = \vec{n} \cdot S_{g}$$
$$\Rightarrow E: -4x_{1} + 2x_{2} - 5x_{3} = \begin{pmatrix}-4\\\\2\\\\-5\end{pmatrix} \cdot \begin{pmatrix}3\\\\-2\\\\0\end{pmatrix}$$
$$\Rightarrow E: -4x_{1} + 2x_{2} - 5x_{3} = -16$$
>
>**Hessesche Normalform:** $$E: -4x_{1} + 2x_{2} - 5x_{3} = -16$$
>$$\Rightarrow E: 4x_{1} - 2x_{2} + 5x_{3} = 16$$
>$$\Rightarrow E: 4x_{1} - 2x_{2} + 5x_{3} - 16 = 0$$
>$$\Rightarrow E: \frac{1}{\sqrt{4^{2} + (-2)^{2} + 5^{2}}} \cdot (4x_{1} - 2x_{2} + 5x_{3} - 16) = 0$$
>$$\Rightarrow E: \frac{1}{\sqrt{45}} \cdot (4x_{1} - 2x_{2} + 5x_{3} - 16) = 0$$

---

## Übungsaufgaben

Bestimmen Sie (falls möglich) jeweils die Ebenengleichungen in **Parameterform, Normalenform, Koordinatenform und Hesseschen Normalform** für die Ebene $E$, für die Folgendes gilt:

a) $E \text{ enthält } A(1|1|-2),~B(-2|1|0) \text{ und } C(0|1|2)$

b) $E \text{ enthält } A(1|-1|-4) \text{ und } g:X = \begin{pmatrix}12\\\\4\\\\0\end{pmatrix} + s \cdot \begin{pmatrix}1\\\\1\\\\-4\end{pmatrix}$

c) $E \text{ enthält } g:X = \begin{pmatrix}1\\\\0\\\\1\end{pmatrix} + s \cdot \begin{pmatrix}2\\\\-1\\\\3\end{pmatrix} \text{ und } h:X = t \cdot \begin{pmatrix}2\\\\-1\\\\3\end{pmatrix}$

d) $E \text{ enthält } g:X = \begin{pmatrix}1\\\\0\\\\1\end{pmatrix} + s \cdot\begin{pmatrix}2\\\\-1\\\\3\end{pmatrix} \text{ und } h:X = \begin{pmatrix}1\\\\0\\\\1\end{pmatrix} + t \cdot \begin{pmatrix}2\\\\-1\\\\3\end{pmatrix}$

e) $E \text{ enthält } A(1|-1|4) \text{ und steht senkrecht auf } g:X = \begin{pmatrix}12\\\\4\\\\0\end{pmatrix} + s \cdot \begin{pmatrix}1\\\\1\\\\-4\end{pmatrix}$

f) $E \text{ enthält } A(1|0|-3) \text{ und hat den Normalenvektor } \vec{n} = \begin{pmatrix}2\\\\-2\\\\3\end{pmatrix}$
