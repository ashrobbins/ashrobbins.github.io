---
title: Set multiple styles in JS with cssText
date: 2019-11-19 00:00:00 +0000
tags:
- css
- js

---
If you want to add multiple styles to an element via JavaScript, and you don't care about over-riding any existing style attribute it may have, you can use `cssText` to do that.

{% highlight js %}
element.style.cssText = 'height: 100px; opacity: 1;';  
{% endhighlight %}

This saves having to write two separate lines for each style update.