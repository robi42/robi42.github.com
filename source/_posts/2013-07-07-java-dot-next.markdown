---
layout: post
title: "Java.next?"
date: 2013-07-07 00:17
comments: true
categories: Programming Code
---

After several years of programming Java while always keeping an eye on alternatives around, I've recently come to the conclusion: 

Actually, there are just a few things missing in the language by now which would make me a *happy camper*&#8482; indeed (enjoying its mature ecosystem of libraries and tools).

Especially, since [Lombok](http://projectlombok.org/) takes a lot of the general boilerplate code PITA away here (with useful features like convenient property accessors, `hashCode/equals/toString` impl., logging facility injection, ...).

Also, [Guava](https://code.google.com/p/guava-libraries/wiki/GuavaExplained) does a truly good job in enabling one to write more concise and robust code.

Plus, Java 7 brought at least some nice, welcome improvements in<br>
&rarr; `try-with-resources`, exceptions `multi-catch`, etc.

Finally, modern DI with Spring 3+ (or Guice) using `javax.inject.*` frees one from most needs for XML config and, after all, there still has to come a build system beating Maven.

So namely, here's a **personal wish list FTW**:

 * Pretty much everything [coming up in Java 8](http://www.techempower.com/blog/2013/03/26/everything-about-java-8/) (sooner than later, hopefully) -- particularly **lambdas** (at last...)
 * More **type inference** (which the JVM is totally capable of); Java 7's diamond operator's definetely a good start there but, please, let me write `val foos = ...` (like in Scala...)
 * **Collection literals** a lá Python or C#, something like this would be really sweet:

{% codeblock lang:java %}
     // Possibly, even without explicit generics declaration ;)
     val foo = new LiteralHashMap<String, String>{"bar": "baz"};
     foo["bar"] = "qux";
{% endcodeblock %}

Pretty please. :)

PS: literal multi-line strings, and so on and so forth, could be nice (but I can live without).
