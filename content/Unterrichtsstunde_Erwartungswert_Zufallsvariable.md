---
title: "Unterrichtsstunde Erwartungswert & Zufallsvariable"
date: "2023-04-25"
tags: [alle, mathe, unterricht, stochastik, erwartungswert, zufallsvariable, fair, glücksrad, einführung, arithmetisches_mittel]
---


## Warm-Up

- Vorentlastung: Berechnung des *arithmetischen Mittels*

| Klassenspiegel      |                |                |                |                |                |                |
| ------------------- |:--------------:|:--------------:|:--------------:|:--------------:|:--------------:|:--------------:|
| Note                |       1        |       2        |       3        |       4        |       5        |       6        |
| abs. Häufigkeit $H$ |       3        |       8        |       7        |       5        |       2        |       0        |
| rel. Häufigkeit $h$ | $\frac{3}{25}$ | $\frac{8}{25}$ | $\frac{7}{25}$ | $\frac{5}{25}$ | $\frac{2}{25}$ | $\frac{0}{25}$ |

$$\bar{x} = \frac{3}{25} \cdot 1 + \frac{8}{25} \cdot 2 + \frac{7}{25} \cdot 3 + \frac{5}{25} \cdot 4 + \frac{2}{25} \cdot 5 + \frac{0}{25} \cdot 6 = 2,8$$


## Beschreibung & Durchführung Glücksspiel

- Folgendes Glücksspiel wird vorgestellt
	- Der Spieler bekommt zu Beginn $20$ Spielchips
	- Ein Spiel kostet $2$ Spielechips
	- Der Spieler dreht das Rad und erhält den angezeigten Betrag ausgezahlt
	- Der Spieler spielt mindestens $10$-mal
- Erwartungen für das Spiel werden festgehalten
- Spiel wird mit einem Schüler vor der Klasse gespielt



<iframe scrolling="no" title="Glücksrad" src="https://www.geogebra.org/material/iframe/id/s22d7ssf/width/700/height/700/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/true/rc/false/ld/true/sdz/false/ctl/false" width="500px" height="500px" style="border:0px;"> </iframe>

**Quelle:** https://www.geogebra.org/m/s22d7ssf

## Ergebnismenge & Zufallsvariable

- Schüler sollen Ergebnismenge für das einmalige Drehen des Glücksrads aufschreiben
- Viele Schüler werden die folgende Ergebnismenge aufschreiben: <br> $\Omega = \\{ 0~€, 1~€, 2~€, 6~€ \\}$
- Folgende Ergebnismenge wird an die Tafel geschrieben: <br> $\Omega = \\{ -2~€, -1~€, 0~€, 4~€ \\}$
- Beide Ergebnismengen sind richtig, beziehen sich allerdings auf unterschiedliche **<u>Zufallsvariablen</u>**

### Definition Zufallsvariable

>Eine Zufallsvariable ist eine Größe, die vom Zufall abhängt. 
>
>Je nach Wahl der Zufallsvariable verändert sich auch die zugehörige Ergebnismenge. 

Die Ergebnismenge besteht dabei immer aus reellen Zahlen. Das bedeutet, dass z.&nbsp;B. die Farbe keine Zufallsvariable sein kann.

### Bestimmung am Beispiel Glücksrad

- Aus obigem Glücksspiel kann man z.&nbsp;B. folgende zwei Zufallsvariablen betrachten:
	- $X = \text{Auszahlung}$
	- $Y = \text{Gewinn}$

- Diesen lassen sich folgende Ergebnismengen zuordnen:
	- $\Omega_{X} = \\{ 0~€, 1~€, 2~€, 6~€ \\}$
	- $\Omega_{Y} = \\{ -2~€, -1~€, 0~€, 4~€ \\}$

## Erwartungswert

### Definition Erwartungswert

>Der Erwartungswert ist eine Schätzung des arithmetischen Mittels bei hinreichend großer Versuchsanzahl.
>
>Er gibt an, welcher Wert im Durchschnitt zu erwarten ist.
>
>Je nach Wahl der Zufallsvariable verändert sich auch der zugehörige Erwartungswert.


### Berechnung am Beispiel Glücksrad

| Glücksrad              |               |               |               |               |
| ---------------------- |:-------------:|:-------------:|:-------------:|:-------------:|
| $X$=Auszahlung         |     $0~€$     |     $1~€$     |     $2~€$     |     $6~€$     |
| $Y$=Gewinn             |    $-2~€$     |    $-1~€$     |     $0~€$     |     $4~€$     |
| Wahrscheinlichkeit $p$ | $\frac{1}{2}$ | $\frac{1}{4}$ | $\frac{1}{8}$ | $\frac{1}{8}$ |

- Berechnung Erwartungswerte:
	$$\mu_{X} = \frac{1}{2} \cdot 0~€ + \frac{1}{4} \cdot 1~€ + \frac{1}{8} \cdot 2~€ + \frac{1}{8} \cdot 6~€ = 1,25~€$$
	-  Es ist demnach eine Auszahlung von durchschnittlich $1,25~€$ pro Spiel zu erwarten. 
	
	$$\mu_{Y} = \frac{1}{2} \cdot \left( -2~€ \right) + \frac{1}{4} \cdot \left( -1~€ \right) + \frac{1}{8} \cdot 0~€ + \frac{1}{8} \cdot 4~€ = -0,75~€$$
	- Es ist demnach ein Gewinn von durchschnittlich $-0,75~€$ pro Spiel zu erwarten. Man verliert also auf lange Sicht jede Runde $0,75~€$.

## Faire Spiele

### Definition faires Spiel

>Ein Spiel wird als fair bezeichnet, wenn der zu erwartende <u>**Gewinn**</u> genau $0$ beträgt. Es gilt also:
>
>$$\text{Das Spiel ist fair.} \quad \Leftrightarrow \quad \mu_{\text{Gewinn}}=0$$

### Aufgabe

Wie muss die Zahl auf dem roten Feld des Glücksrads verändert werden, damit das Glücksspiel fair ist?

--- 
## Gegenüberstellung Grundbegriffe Stochastik

| Empirische Daten<br><br>("Experiment wurde durchgeführt") | Schätzungen für große Versuchsanzahlen<br><br>("Experiment wurde (noch) nicht durchgeführt") |
|:---------------------------------------------------------:|:--------------------------------------------------------------------------------------------:|
|                                                           |                                                                                              |
|                  relative Häufigkeit $h$                  |                                    Wahrscheinlichkeit $p$                                    |
|              arithmetisches Mittel $\bar{x}$              |                                     Erwartungswert $\mu$                                     |

## Weiterführendes Projekt

Ein weiterführendes Projekt, das viel Raum zum Erforschen und Experimentieren ermöglicht, bietet die [[Cereal_Box_Problem_Thinking_Task|Cereal Box-Aufgabe]].