---
title: "Ableitung √x mit Infinitesimalen und h-Methode"
date: "2023-07-04"
tags: [alle, mathe, analysis, infinitesimalrechnung, differentialrechnung, ableitung, differentialquotient, wurzel, grenzwert, h_methode]
---

>Bestimme die Ableitungsfunktion $f'$ von $f(x)=\sqrt{x}$.


## Infinitesimale

$$\sqrt{x} \cdot \sqrt{x} = x$$

Verändern wir $x$ und $\sqrt{x}$ infinitesimal, so ergibt sich:

$$
\begin{align*}
\left( \sqrt{x}+\mathrm{d}\sqrt{x} \right) \cdot \left( \sqrt{x}+\mathrm{d}\sqrt{x} \right) &= x+\mathrm{d}x\\
\left( \sqrt{x}+\mathrm{d}f \right) \cdot \left( \sqrt{x}+\mathrm{d}f \right) &= x+\mathrm{d}x\\
\sqrt{x} \cdot \sqrt{x} + \sqrt{x}~\mathrm{d}f + \sqrt{x}~\mathrm{d}f + \mathrm{d}f \cdot \mathrm{d}f &= x+\mathrm{d}x\\
x + 2 \sqrt{x} ~ \mathrm{d}f + \left( \mathrm{d}f \right)^{2} &= x+\mathrm{d}x\\
2 \sqrt{x} ~ \mathrm{d}f &= \mathrm{d}x
\end{align*}
$$

>$$\frac{\mathrm{d}f}{\mathrm{d}x}=\frac{1}{2\sqrt{x}}$$


## h-Methode

$$
\begin{align*}
\frac{f(x+h)-f(x)}{h}&=\frac{\sqrt{x+h}-\sqrt{x}}{h}\\
&=\frac{\sqrt{x+h}-\sqrt{x}}{h} \cdot \frac{\sqrt{x+h} + \sqrt{x}}{\sqrt{x+h} + \sqrt{x}}\\
&=\frac{\left( \sqrt{x+h} \right)^{2} - \left( \sqrt{x} \right)^{2}}{h \cdot \left( \sqrt{x+h} + \sqrt{x} \right)}\\
&=\frac{x+h-x}{h \cdot \left( \sqrt{x+h} + \sqrt{x} \right)}\\
&=\frac{1}{\sqrt{x+h} + \sqrt{x}}
\end{align*}
$$

Für $h \to 0$ gilt:

>$$f'(x)=\frac{1}{\sqrt{x}+\sqrt{x}}=\frac{1}{2\sqrt{x}}$$