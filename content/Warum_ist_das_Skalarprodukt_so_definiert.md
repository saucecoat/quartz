---
title: "Warum ist das Skalarprodukt so definiert?"
date: "2022-10-30"
tags: [math, mathe, lineare_algebra, analytische_geometrie, skalarprodukt, dot_product, definition, reddit, wikipedia]
---
- Weder die geometrische Definition noch die Definition in kartesischen Koordinaten ist willkürlich. Beide folgen aus der geometrisch motivierten Forderung, dass das Skalarprodukt eines Vektors mit sich selbst das Quadrat seiner Länge ist, und der algebraisch motivierten Forderung, dass das Skalarprodukt die obigen Eigenschaften 1–3 erfüllt. (Quelle: https://de.wikipedia.org/wiki/Skalarprodukt#Eigenschaften)
- It's defined like that because it's a useful definition. The dot product allows you to recover all geometric properties of vectors:
**Lengths**: $$|\vec{a}| = \sqrt{\vec{a}\cdot \vec{a}}$$
**Angles**: $$\theta = \text{arccos}\left(\frac{\vec{a}\cdot \vec{b}}{|\vec{a}||\vec{b}|}\right)=\text{arccos}\left( \frac{\vec{a}\cdot \vec{b}}{\sqrt{\vec{a}\cdot \vec{a}}\cdot\sqrt{\vec{b}\cdot \vec{b}}} \right)$$
**Projections**: $$\vec{a} \text{ projected onto } \vec{b} = \left(\frac{\vec{a}\cdot \vec{b}}{|\vec{b}|^2}\right)\cdot\vec{b}=\left(\frac{\vec{a}\cdot \vec{b}}{\vec{b}\cdot\vec{b}}\right)\cdot\vec{b}$$
This is extremely useful for more advanced purposes, where one turns this around and uses these formulas to define the geometry of a space using an inner product (e. g. [movie recommendation system (Netflix) where the angle between higher-dimensional vectors is calculated](https://towardsdatascience.com/using-cosine-similarity-to-build-a-movie-recommendation-system-ae7f20842599
)). For example, the local angles and distances on a complicated surface in $\mathbb{R}^3$ are obtained by restricting the dot product of the ambient Euclidean space to the different tangent planes of the surface. (Quelle: https://www.reddit.com/r/askmath/comments/jneuch/why_the_dot_product_is_defined_like_that/)
