---
title: "Alternative Dartellung Drehmatrix"
date: "2022-12-08"
tags: [alle, math, mastodon, matrix, rotation, drehmatrix, drehung, lineare_algebra, analytische_geometrie]
---


## Übliche Darstellung

Die übliche Darstellung einer Drehmatrix ist: 

$$\begin{bmatrix}\cos\theta & -\sin \theta \\\\ \sin \theta & \cos \theta \end{bmatrix}$$

Die damit verbundene Vorstellung ist, dass der Einheitsvektor $\begin{pmatrix}1\\\\0\end{pmatrix}$ um den Winkel $\theta$ auf den Vektor $\begin{pmatrix}\cos\theta \\\\ \sin\theta\end{pmatrix}$ gedreht wird und der Einheitsvektor $\begin{pmatrix}0\\\\1\end{pmatrix}$ um den Winkel $\theta$ auf den Vektor $\begin{pmatrix}-\sin \theta \\\\ \cos \theta\end{pmatrix}$.

## Alternative Darstellung

Patrick Honner schlägt in [diesem Post](https://mathstodon.xyz/@phonner/109477904103810149) vor, stattdessen die folgende Darstellung für eine Drehmatrix zu wählen:

$$\begin{bmatrix}\cos(\theta) & \cos (\theta + \frac{\pi}{2})\\\\ \sin(\theta) & \sin (\theta + \frac{\pi}{2}) \end{bmatrix}$$

Die mit dieser Darstellung verbundene Vorstellung unterscheidet sich in der Interpretation der zweiten Spalte. 
Anstatt einer Drehung des Einheitsvektors $\begin{pmatrix}0\\\\1\end{pmatrix}$ um den Winkel $\theta$, stellt man sich erneut eine Drehung des Einheitsvektors $\begin{pmatrix}1\\\\0\end{pmatrix}$ vor, jedoch um den Winkel $\theta + \frac{\pi}{2}$, also um $90°$ mehr.
Man dreht sich sozusagen um $90°$ um dort anzukommen, wo der Einheitsvektor $\begin{pmatrix}0\\\\1\end{pmatrix}$ sich befindet, um anschließend die Drehung um $\theta$ zu vollziehen.

Durch diese Darstellung wird laut Honner besser ersichtlich, dass die Orientierung und der Winkel zwischen den Einheitsvektoren durch eine Drehung erhalten bleibt.
 