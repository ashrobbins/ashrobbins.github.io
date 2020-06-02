---
layout: post
title: Create multiple vars from object keys
date: 2019-12-09 00:00:00 +0000
tags:
- js

---
Let's say you have an object that looks like this...

{% highlight js %}
const object = {
    name: 'Ash',
    color: 'red',
    age: 100
};
{% endhighlight %}

And for some reason maybe you need to create some local variables within a function based on the values of the keys in that object. You can do that like this...

{% highlight js %}
const { name, color, age } = object;
{% endhighlight %}

As long as each variable name you supply maps to the name of a key in the object, you're good to go.
