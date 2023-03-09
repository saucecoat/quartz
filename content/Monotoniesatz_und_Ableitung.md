---
title: "Monotoniesatz und Ableitung"
date: "2023-02-12"
tags: [alle, mathe, unterricht , analysis, ableitung, monotonie, streng_monoton, klammer]
---

## Monotoniesatz

Der Monotoniesatz gilt <u>**nur**</u> in eine Richtung:

> Wenn $f'(x)>0$ in einem Intervall $I$, dann ist $f$ dort *streng monoton steigend*.

Das heißt jedoch <u>**nicht**</u>, dass $f$ nicht streng monoton steigend sein kann, wenn $f'(x)=0$ in $I$. 

So ist z. B. $f(x)=x^{3}$ <u>auf ganz $\mathbb{R}$ streng monoton steigend</u>, obwohl an der Stelle $x_{0}=0$ die Ableitung verschwindet. 
Da für alle $x<x_{0}$ gilt, dass $f(x)<f(x_{0})$ und für alle $x>x_{0}$, dass $f(x)>f(x_{0})$, ist $f$ trotzdem streng monoton steigend.

## Monotonie ganzrationaler Funktionen 

Eine Funktion ist also auf einem Intervall, auf dem sie mit Ausnahme von einzelnen isolierten $x$-Werten steigt, streng monoton steigend. Hat sie für mehr als einen $x$-Wert "hintereinander" die Ableitung $0$, so ist sie nicht streng monoton steigend. 

Dieser Fall kommt bei ganzrationalen Funktionen (welche heutzutage in der Schule leider den einzig tiefer thematisierten Funktionstyp darstellt) allerdings nicht vor und ist deswegen in der heutigen Schulmathematik praktisch irrelevant. 
Ein Beispiel zur Besprechung des Unterschieds findet sich [[Diskussion_strenge_Monotonie|hier]].

In der Schule ist es daher heutzutage eigentlich egal, ob man bei der Angabe von Monotonieintervallen runde oder eckige Klammern verwendet. Der Einfachheit halber kann man sich also auf den Gebrauch von runden Klammern beschränken, da diese auch im Fall $\pm \infty$ verwendet werden.

## Monotonieintervalle mithilfe der Ableitung bestimmen

Das Ablesen von Intervallgrenzen kann trügerisch sein, da das Ablesen ungenau ist und eventuelle Grenzen übersehen werden können, wie z. B. bei $f(x)=-0,01x^{4}+x^{3}$.

Es braucht also eine rechnerische Methode zur Bestimmung der Intervallgrenzen.

Aus dem Mittelwertsatz folgt für ganzrationale Funktionen:

> Wenn an der Stelle $x_{0}$ ein Wechsel des Monotonieverhaltens vorliegt, dann gilt $f'(x_{0})=0$.

Das Verschwinden der Ableitung ist also ein notwendiges Kriterium für einen Monotoniewechsel, jedoch wie oben gesehen kein hinreichendes.

Die Lösungen der Gleichung $f'(x)=0$ können demnach herangezogen werden, um potentielle Intervallgrenzen zu bestimmen.

 