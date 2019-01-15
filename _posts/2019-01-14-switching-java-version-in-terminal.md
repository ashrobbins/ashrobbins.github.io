---
title: 'Switching Java version in terminal '
date: 2019-01-15 00:00:00 +0000
tags:
- java

---
I was trying to run a maven command the other day and it kept failing due to my version of Java being too recent. You can quickly find out what version of Java you're using with the command `java -version`, which will give you an output like this...

{% highlight js %}
java version "10.0.2" 2018-07-17
{% endhighlight %}

As you can see above, we're using version 10.x.x. To switch to another installed version, simply run...

{% highlight js %}
export JAVA_HOME=`/usr/libexec/java_home -v 1.8`
{% endhighlight %}

...where `1.8` is the major release you're after.

There are more robust ways to set versioning on a global level, but if you're after a quick fix for your current terminal context, the above will do the job.