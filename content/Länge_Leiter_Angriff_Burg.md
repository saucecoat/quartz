---
title: "Optimale Länge einer Leiter für einen Angriff auf eine Burg"
date: "2022-11-02"
tags: [math, mathe, podcast, length, länge, leiter, ladder, attack, burg, mittelalter, pythagoras, trigonometry, trigonometrie, dreieck, verhältnis, proportion]
---
## Quelle
[Podcast *Opinionated History of Mathematics* (2022-10-11)](https://intellectualmathematics.com/blog/review-of-netzs-new-history-of-greek-mathematics/)

## Question 
Let’s start by attacking a city. The enemies are hunkering down behind their city walls. We are going to have to scale the walls with ladders. How long should we make the ladders? The ancient historian Polybius has the answer:

## Answer
> “The method of discovering the right length for ladders is as follows. … If the height of the wall be, let us say, ten of a given measure, the length of the ladders must be a good twelve. 
> ==**The distance from the wall at which the ladder is planted must**==, in order to suit the convenience of those mounting, ==**be half the length of the ladder**==, for if they are placed farther off they are apt to break when crowded and if set up nearer to the perpendicular are very insecure for the scalers. … So here again it is evident that those who aim at success in military plans and surprises of towns must have studied geometry.”

Great stuff. But Netz gets it wrong, in my opinion. Here is how he concludes:

## Pythagoras not efficient
“And then, of course, we are supposed to apply – Polybius leaves this implicit – Pythagoras’s theorem.” (223)

I don’t think so. I don’t think that’s what Polybius intended.

==**Sure enough, you can solve for the length of the ladder using the Pythagorean Theorem, but that is a clumsy and inefficient way to do it.**== If you did this the modern way you would need to do some algebra followed by some calculation involving a square root. They didn’t have calculators on their phones back then, you know. Do you expect carpenters in the military to be able to calculate square roots by hand?

## More efficient way
In fact, Polybius has already told you everything you need to know with his numerical example. If the wall is 10, the ladder should be 12, he says. But it scales! ==**So what Polybius is really saying is that, whatever the height of the wall is, the ladder is always 20% longer than that. That’s all you need to know. No Pythagorean Theorem needed.**==

Those numbers are a rule of thumb. You can also do it more exactly if you want, according to Polybius’s more theoretical characterization of the optimal length. But you don’t need the Pythagorean Theorem for that either. There’s a much better way, that you can easily teach to an illiterate carpenter in five minutes.

## Geometric way
==**Draw an equilateral triangle**==, just as Euclid does in Proposition 1 of the Elements. ==**Cut it down the middle. Now you have a right-angled triangle, where the base is exactly half of the hypothenuse.**== This corresponds precisely to Polybius’s rule: the distance along the ground is half the length of the ladder.

So now we have a scale model of what we want. The height down the middle of the equilateral triangle represents the city wall; the side of the equilateral triangle represents the ladder, and it is precisely half its own length from the foot of the wall, exactly as Polybius says it should be for optimal stability.

So if we are given that the height of the wall is for example 10 meters, then we divide the height of the triangle into ten equal parts. We take a blank ruler and mark those ten marks on it. Then we take this ruler, with this length unit, and measure the hypothenuse of the triangle. However many marks long it is, that’s how many meters our ladder needs to be.

Piece of cake. Easy to improvise in the field without any specialized knowledge or tools. While Netz is busy trying to teach his carpenters the algebra of quadratic expressions and how to extract square roots, I have already scaled his walls using my much quicker methods.



 