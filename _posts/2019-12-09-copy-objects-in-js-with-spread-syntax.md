---
layout: post
title: Copy objects in JS with spread syntax
date: 2019-12-09 00:00:00 +0000
tags:
- js

---
Let's say in your code you have an object:

{% highlight js %}
const object = {
    name: 'Ash',
    color: 'red',
    age: 100
};
{% endhighlight %}

If you want to copy that object to a new object you can do that like...

{% highlight js %}
const newObject = { ...object };
{% endhighlight %}

If you wanted to copy that object but also update one of the values, you could do that like...

{% highlight js %}
const newObject = {
    ...object,
    color: 'purple'
};
{% endhighlight %}
