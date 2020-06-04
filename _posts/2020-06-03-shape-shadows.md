---
title: Shape shadows
date: 2020-06-03 23:00:00 +0000
tags: []

---
Something I just found out - you can have shadows that follow the outline of a shape within an image, by sticking it into a wrapper element that has a `filter` applied.

Say you've got a `png` image of a shirt with a transparent background. If you apply a normal `box-shadow` to it you'll get a shadow around the whole image, which would look a bit odd.

![](/uploads/screenshot-2020-06-04-at-09-58-26.png)

We can fix that by instead putting the `img` into a wrapping element:

{% highlight html %}  
<span>  
    <img src="/path/to/image.png" />  
</span>  
{% endhighlight %}

and then applying a css `filter` to that wrapping element:

{% highlight css %}  
span {  
    filter: drop-shadow(-1px 7px 4px rgba(0,0,0,.7));  
}  
{% endhighlight %}