---
title: SVG gradients in CSS
date: 2019-04-04 23:00:00 +0000
tags:
- css
- svg

---
[https://codepen.io/ashrobbins/pen/YMJEMX](https://codepen.io/ashrobbins/pen/YMJEMX "https://codepen.io/ashrobbins/pen/YMJEMX")

On a recent project we were building a new home page hero widget and the design called for the user to be able to select from a set of themes to decide what colour the hero should be.

They do this by assigning a 'Theme-xx' tag to the content item, and then we apply a class to the hero based on the theme tag used. Simple enough, we have a BEM modifier class that switches out colours based on the chosen tag.

One part of the design however is an SVG background graphic that has a gradient running left to right. Instead of having multiple SVGs in the page that get shown or hidden based on a class, I wanted to see if there was a cleverer way to do it.

<iframe height="265" style="width: 100%;" scrolling="no" title="SVG Gradient Tags" src="https://codepen.io/ashrobbins/embed/YMJEMX?height=265&theme-id=dark&default-tab=html,result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/ashrobbins/pen/YMJEMX'>SVG Gradient Tags</a> by Ash Robbins
  (<a href='https://codepen.io/ashrobbins'>@ashrobbins</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

As you can see in the pen above I've got a hidden svg which simply contains several `linearGradient` tags, each with an `id` and two or more `stop` tags within it. These are where the colours for the gradients are defined. We can then use css to update the `fill` property of the `path` element based on an id of one of the `linearGradient` tags, and the gradient used gets updated.