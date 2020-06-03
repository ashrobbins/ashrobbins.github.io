---
layout: post
title: Fixing an issue with scroll-snap on iOS
date: 2019-11-06T00:00:00.000+00:00
tags:
- css

---
On one of our sites we have a grid of article thumbnails that becomes horizontally scrollable on mobile, and we've used `scroll-snap` on the container element to give a more carousel-like feel and make sure that the list always snaps to the edge of one of the items.

Our QA team raised a bug on certain iOS devices where the list would always snap back to the first item and not scroll through as the user expected.

![](https://media.giphy.com/media/ZdNd2oQCV3yrMrfpZs/giphy.gif)

After a fair amount of head scrartching this was fixed by adding

{% highlight css %}
-webkit-overflow-scrolling: touch;
{% endhighlight %}

to the container element.

![](https://media.giphy.com/media/d7BjVQoKpG0WhxchJY/giphy.gif)