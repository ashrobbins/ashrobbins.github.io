---
title: SVG gradients in CSS
date: 2019-04-04T23:00:00.000+00:00
tags:
- css
- svg

---
[https://codepen.io/ashrobbins/pen/YMJEMX](https://codepen.io/ashrobbins/pen/YMJEMX "https://codepen.io/ashrobbins/pen/YMJEMX")

On a recent project we were building a new home page hero widget and the design called for the user to be able to select from a set of themes to decide what colour the hero should be.

They do this by assigning a 'Theme-xx' tag to the content item, and then we apply a class to the hero based on the theme tag used. Simple enough, we have a BEM modifier class that switches out colours based on the chosen tag.

One part of the design however is an SVG background graphic that has a gradient running left to right. Instead of having multiple SVGs in the page that get shown or hidden based on a class, I wanted to see if there was a cleverer way to do it.

<p class="codepen" data-height="265" data-theme-id="dark" data-default-tab="html,result" data-user="ashrobbins" data-slug-hash="YMJEMX" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="SVG Gradient Tags">

  <span>See the Pen <a href="[https://codepen.io/ashrobbins/pen/YMJEMX](https://codepen.io/ashrobbins/pen/YMJEMX "https://codepen.io/ashrobbins/pen/YMJEMX")">

  SVG Gradient Tags</a> by Ash Robbins (<a href="[https://codepen.io/ashrobbins](https://codepen.io/ashrobbins/pen/YMJEMX "https://codepen.io/ashrobbins/pen/YMJEMX")">@ashrobbins</a>)

  on <a href="[https://codepen.io](https://codepen.io/ashrobbins/pen/YMJEMX "https://codepen.io/ashrobbins/pen/YMJEMX")">CodePen</a>.</span></p>

<script async src="[https://static.codepen.io/assets/embed/ei.js](https://codepen.io/ashrobbins/pen/YMJEMX "https://codepen.io/ashrobbins/pen/YMJEMX")"></script>

As you can see in the pen above I've got a hidden svg which simply contains several `linearGradient` tags, each with an `id` and two or more `stop` tags within it. These are where the colours for the gradients are defined. We can then use css to update the `fill` property of the `path` element based on an id of one of the `linearGradient` tags, and the gradient used gets updated.