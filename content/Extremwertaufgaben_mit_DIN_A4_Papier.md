---
title: "Extremwertaufgaben mit DIN A4-Papier"
date: "2023-03-12"
tags: [alle, mathe, analysis, extremstelle, extremwertaufgabe, randwert, definitionsbereich, papier, box, rechteck, flächeninhalt, maximieren, minimieren, ableitung]
---

# Box basteln 

## Aufgabe

Es soll aus einem Blatt DIN A4-Papier durch das Herausschneiden eines Quadrats an jeder Ecke, sowie das anschließende Hochklappen der Seiten eine möglichst große Box gebastelt werden.

![[images/Extremwert_DINA4_Box_1.png]]

> Wie groß müssen die Quadrate sein, damit das Volumen der Box möglichst groß ist?

<u>**Hinweis:**</u> Im Folgenden wird der Einfachheit halber mit den Seitenlängen $21$ und $30$ gerechnet.

## Lösung

> [!success]- Lösung
> Bezeichnen wir die Länge des Quadrats mit $x$ so ergibt sich folgendes Bild:
> 
> ![[images/Extremwert_DINA4_Box_2.png]]
> 
> Wir können nun eine Funktion $V$ angeben, die das Volumen in Abhängigkeit zur Seitenlänge $x$ des Quadrats angibt:
> 
> $$\begin{aligned}
V(x) &= x \cdot (21-2x) \cdot (30-2x)\\\\
&= 4x^{3}-102x^{2}+630x
\end{aligned}$$
>
> Es ist wichtig zu beachten, dass für den <u>Definitionsbereich</u> von $V$ gilt, dass $x \in [0;~10,5]$, da die kürzere Seitenlänge des Blattes $21~cm$ beträgt.
> 
> Mithilfe der ersten Ableitung $V'(x)=12x^{2}-204x+630$ die lokalen Extrema:
>  
> $$\begin{aligned}
V'(x) &= 0\\\\
\Rightarrow x_{1} \approx 4,06&;~~x_{2} \approx 12,94
\end{aligned}$$
>
>Aufgrund des eingeschränkten Definitionsbereichs kommt nur $x_{1}$ als Lösung infrage. 
>Mithilfe der hinreichenden Bedingung zeigt sich, dass sich bei $x_{1}$ in der Tat ein lokaler Hochpunkt befindet.
>
>Nun müssen noch die <u>Randwerte</u> betrachtet werden, die zeigen, dass sich bei $x_{1}$ auch der globale Hochpunkt befindet. 
>
>Wenn einem noch kein Beispiel begegnet ist, bei dem die globalen Extrema an den Rändern liegen, wird man den letzten Schritt (Betrachtung der Randwerte) vermutlich nicht durchführen.
>Das folgende Beispiel dient zur Bewusstmachung, dass die Extrema auch an den Rändern liegen können.


# Kleinstes Rechteck finden

## Aufgabe

Aus einem DIN A4-Blatt wird eine Ecke von je $15~cm$ auf beiden Seiten abgeschnitten.

![[images/Extremwert_DINA4_Kleinstes_Rechteck_1.png]]

Es soll nun mit zwei Schnitten, welche parallel zu den jeweiligen Seiten verlaufen, ein neues Rechteck entstehen:

![[images/Extremwert_DINA4_Kleinstes_Rechteck_2.png]]

> Wo müssen sich die beiden Schnitte treffen, damit das entstehende Rechteck möglichst <u>klein</u> ist?

## Lösung 

> [!success]- Lösung
> 
> Wir bezeichnen die Seitenlängen des entstehenden Rechtecks wie folgt:
> 
> ![[images/Extremwert_DINA4_Kleinstes_Rechteck_3.png]]
> 
> Für den Flächeninhalt $A$ des Rechtecks gilt dann:
> 
> $$\begin{aligned}
A(x) &= (6+x)(30-x)\\\\
&= -x^{2}+24x+180
\end{aligned}$$
> 
> Es ist abermals wichtig zu beachten, dass der <u>Definitionsbereich</u> von $A$ eingeschränkt ist. Es gilt, dass $x \in [0;~15]$.
> 
> Mithilfe der ersten Ableitung $A'(x)=-2x+24$ die lokalen Extrema:
>  
> $$\begin{aligned}
A'(x) &= 0\\\\
\Rightarrow x &= 12
\end{aligned}$$
>
>Mithilfe der hinreichenden Bedingung zeigt sich, dass sich bei $x=12$ tatsächlich ein lokaler Hochpunkt befindet.
>
> Da wir allerdings nach einem Tiefpunkt suchen, bringt uns diese Entdeckung nicht weiter. Ein Blick auf den Graphen von $A$ zeigt uns, dass der kleinste Wert im Definitionsbereich $[0;~15]$ sich am linken Rand bei $x=0$ befindet.
> 
> ![[images/Extremwert_DINA4_Kleinstes_Rechteck_4.png]]
> 
> Das globale Minimum befindet sich an der Stelle $x=0$.
> 
> <u>Weiterführende Frage:</u> Warum kann ein globales Extremum nur an den lokalen Extrema oder an den Rändern auftreten? 