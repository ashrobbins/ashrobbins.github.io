---
title: SVG gradients in CSS
date: 2019-04-04T23:00:00.000+00:00
tags:
- css
- svg

---
Morning gang. As requested in the check-in yesterday I've knocked up a stripped back demo of how we're using svg gradient tags in the visual refresh for PL.

[https://codepen.io/ashrobbins/pen/YMJEMX](https://codepen.io/ashrobbins/pen/YMJEMX "https://codepen.io/ashrobbins/pen/YMJEMX")

The context for this is that we want to give editors the choice of colour theme for any article, video or gallery they use on the home page hero. They do this by assigning a 'Theme-xx' tag to the content item, and then we apply a class to the hero based on the theme tag used.

We've got a hidden svg which simply contains several `linearGradient` tags, each with an id and two or more `stop` tags within them. These are where the colours for the gradients are defined.We can then use css to update the `fill` property of the `path` element based on an id of one of the `linearGradient` tags, and the gradient used gets updated.