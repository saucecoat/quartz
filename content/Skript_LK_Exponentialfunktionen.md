---
title: Skript Leistungskurs Exponentialfunktionen
date: 2024-09-12
tags:
  - alle
  - mathe
  - unterricht
  - leistungskurs
  - exponentialfunktion
  - logarithmus
  - definition
  - satz
  - beweis
---


> [!note] Definition Exponentialfunktion
> 
>Eine Funktion $f(x)$ ist eine <u>**Exponentialfunktion**</u>, wenn sie folgende Form erfüllt:
>
>$$f(x)=c \cdot a^{x},$$
>
>mit $c$, $a \in \mathbb{R}\setminus\{0\}$ und $a\neq 1$.
>
>$c$ wird auch <u>**Startwert**</u> genannt und $a$ die <u>**Zuwachsrate**</u> oder <u>**Wachstumsfaktor**</u>.


> [!tip] Satz 1
> 
> Es sei $f(x)=a^{x}$ mit $a>0$ eine beliebige Exponentialfunktion, dann gilt:
>
>$$f'(x)=f(x) \cdot f'(0)$$

> [!success]- Beweis Satz 1
> 
>Sei $f(x)=a^x$ mit $a>0$.
>
>Für eine beliebige Stelle $x_{0}$ gilt allgemein:
>
>$$f'(x_{0}) = \lim_{h\to 0} \frac{f(x_{0}+h)-f(x_{0})}{h}$$
>
>Mit der gegebenen Exponentialfunktion ergibt sich:
>
>$$= \lim_{h\to 0} \frac{a^{x_{0}+h}-a^{x_{0}}}{h}$$
>
>Nach Potenzgesetzen gilt:
>
>$$= \lim_{h\to 0} \frac{a^{x_{0}} \cdot a^{h}-a^{x_{0}}}{h}$$
>
>Ausklammern liefert:
>
>$$= \lim_{h\to 0} \frac{a^{x_{0}} \cdot \left(a^{h}-1\right)}{h}$$
>
>Da $a^{x_{0}}$ unabhängig von $h$ ist, gilt:
>
>$$= a^{x_{0}} \cdot \lim_{h \to 0} \frac{a^{h}-1}{h}$$
>
>Dieser Grenzwert ist genau der Differentialquotient an der Stelle $0$. Dies ist leichter zu sehen, wenn wir den Quotienten leicht umschreiben:
>
>$$\begin{aligned}
>&= a^{x_{0}} \cdot \lim_{h \to 0} \frac{a^{0+h}-a^{0}}{h}\\\\\\
>&= a^{x_{0}} \cdot \lim_{h \to 0} \frac{f(0+h)-f(0)}{h}\\\\\\
>&=a^{x_{0}} \cdot f'(0)
>\end{aligned}$$
>
>$$\tag*{$\square$}$$
>&nbsp;


> [!note] Definition Eulersche Zahl $e$
> 
>Die <u>**Eulersche Zahl $e$**</u> ist eine irrationale Zahl mit dem Wert 
>
>$$e=2,71828182845\ldots$$
>
>Stellt $e$ die Basis einer Exponentialfunktion dar, so nennt man die Funktion $f(x)=e^{x}$ auch die <u>**natürliche Exponentialfunktion**</u> oder einfach <u>**$e$-Funktion**</u>. Für diese gilt $f'(x)=e^{x}$, da für die Zahl $e$ genau gilt, dass $f'(0)=1$.
>
>Ein bekannter Grenzwert für die Eulersche Zahl ist:
>
>
>$$e=\lim_{n \to \infty} \left(1 + \frac{1}{n} \right)^{n}$$



> [!note] Definition Logarithmus
> 
>Die Lösung der Exponentialgleichung
>
>$$a^{x}=b, \qquad \text{mit } a,b>0$$
>
>wird bezeichnet als <u>**Logarithmus**</u> $\log_{a}(b)$ bezeichnet.
>Gesprochen: "Logarithmus zur Basis $a$ von $b$".



> [!note] Definition Natürlicher Logarithmus
> 
>Den Logarithmus zur Basis $e$ nennt man den <u>**natürlichen Logarithmus**</u> (*logarithmus naturalis*). 
>Man schreibt statt $\log_{e}(x)$ schlicht:
>
>$$\ln(x)$$



> [!tip] Satz 2
> 
> Es sei $f(x)=e^{k \cdot x}$ mit $k \neq 0$. Dann gilt:
>
>$$f'(x)=k \cdot e^{k \cdot x}$$

> [!success]- Beweis Satz 2
> 
> Sei $g(x)=e^{x}$ die gewöhnliche $e$-Funktion und $f(x)=e^{k \cdot x}$ unsere gegebene Exponentialfunktion.
> Wir stellen fest, dass die Funktion $f(x)$ eine Streckung der $e$-Funktion $g(x)$ in $x$-Richtung um den Faktor $\frac{1}{k}$.
> 
> Per Definition wissen wir, dass $g'(0)=1$, das heißt, dass das Steigungsdreieck an der Tangente bei $x_{0}=0$ eine Steigung von $1$ hat. 
> 
> Für $g(x)=e^{x}$ gilt also: 
> 
> $$g'(0)= m_{g} = \frac{\Delta y}{\Delta x} = 1$$
> 
> Bei der Streckung in $x$-Richtung wird auch das Steigungsdreieck um denselben Faktor $\frac{1}{k}$ gestreckt. Für das Steigungsdreieck von $f(x)$ gilt also:
>
>$$\begin{aligned}
>f'(0) = m_{f} &= \frac{\Delta y}{\frac{1}{k} \cdot \Delta x}\\\\\\
>&= \frac{k \cdot \Delta y}{\Delta x}\\\\\\
>&= k \cdot \frac{\Delta y}{\Delta x}\\\\\\
>&= k \cdot g'(0)\\
>&= k \cdot 1\\
>&= k
>\end{aligned}$$
>
>Nach Satz 1 gilt:
>
>$$\begin{aligned}
>f'(x) &= f(x) \cdot f'(0)\\
>&= e^{k \cdot x} \cdot k
>\end{aligned}$$
>$$\tag*{$\square$}$$
>&nbsp;


> [!summary] Satz 2.2
> 
> Es sei $f(x)=e^{kx}$ mit $k \neq 0$. Dann gilt:
>
>$$F(x)=\frac{1}{k} \cdot e^{kx}+c, \quad \text{mit } c\in\mathbb{R}$$ 

> [!success]- Beweis
> 
> Nach Faktorregel und Satz 2 gilt:
> 
> $$\begin{aligned}
> F'(x)&=\frac{1}{k} \cdot k \cdot e^{kx}\\\\
> &=e^{kx}
> \end{aligned}$$
> 
> $$\tag*{$\square$}$$
> &nbsp;


> [!tip] Satz 3
> 
> Es sei $f(x)=a^{x}$ mit $a>0$ eine beliebige Exponentialfunktion. Dann gilt:
>
>$$f'(x)=\ln(a) \cdot a^{x}$$

> [!success]- Beweis Satz 3
> 
> Es sei $f(x)=a^{x}$ mit $a>0$ eine beliebige Exponentialfunktion. Nach der Definition des (natürlichen) Logarithmus gilt:
> 
> $$f(x)=a^{x}=e^{\ln(a) \cdot x}$$
> 
> Nach Satz 2 gilt:
> 
> $$f'(x)=\ln(a) \cdot e^{\ln(a) \cdot x}$$
> 
> Nach Definition des (natürlichen) Logarithmus gilt schließlich:
> 
> $$f'(x) = \ln(a) \cdot a^{x}$$
> $$\tag*{$\square$}$$
> &nbsp;


> [!summary] Satz 3.2
> 
> Es sei $f(x)=a^{x}$ mit $a>0$ eine beliebige Exponentialfunktion. Dann gilt:
>
>$$F(x)=\frac{1}{\ln(a)} \cdot a^{x}+c, \quad \text{mit } c\in\mathbb{R}$$ 

> [!success]- Beweis
> 
> Nach Faktorregel und Satz 3 gilt:
> 
> $$\begin{aligned}
> F'(x)&=\frac{1}{\ln(a)} \cdot \ln(a) \cdot a^{x}\\\\
> &=a^{x}
> \end{aligned}$$
> 
> $$\tag*{$\square$}$$
> &nbsp;
