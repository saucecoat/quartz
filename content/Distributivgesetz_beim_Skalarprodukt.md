---
title: "Distributivgesetz beim Skalarprodukt"
date: "2022-10-30"
tags: [math, mathe, skalarprodukt, dot_product, distributivgesetz, vector, vektor, lineare_algebra, analytische_geometrie, projektion, projection]
---
The geometric definition gives us the dot product as the magnitude of $\vec{a}$ multiplied by the scalar projection of $\vec{b}$ onto $\vec{a}$. This is given for any $\vec{a}$, $\vec{b}$ in n-space.

$$\vec{a}\cdot\vec{b}=|\vec{a}|\cdot|\vec{b}|\cdot cos(\vartheta)=|\vec{a}|\cdot|\vec{b}_{\vec{a}}|$$

The dot product of $\vec{a}$ with $\vec{b}+\vec{c}$ is just the magnitude of $\vec{a}$ times the scalar projection of $\vec{b}+\vec{c}$ onto $\vec{a}$. But that can be broken up into components, after which normal distribution takes over.

$$\begin{align*}\vec{a}\cdot\left(\vec{b}+\vec{c}\right)&=|\vec{a}|\cdot\left|\left(\vec{b}+\vec{c}\right)_{\vec{a}}\right|\\\\&=|\vec{a}|\cdot\left(|\vec{b}_\vec{a}|+|\vec{c}_\vec{a}|\right)\\\\&=|\vec{a}|\cdot|\vec{b}_\vec{a}|+|\vec{a}|\cdot|\vec{c}_\vec{a}|\\\\&=\vec{a}\cdot\vec{b}+\vec{a}\cdot\vec{c}\end{align*}$$

Quelle: https://math.stackexchange.com/questions/1215063/prove-the-distributive-property-of-the-dot-product-using-its-geometric-definitio
 