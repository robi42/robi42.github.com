---
layout: post
title: "Play 2 Boilerplate"
date: 2012-09-21 23:43
comments: true
categories: Code Web
---

A little project aimed at getting one up and running quickly with building a
contemporary web app using [Play 2](http://www.playframework.org/) framework.

Contains a bunch of current web dev **best practices** and niceties, from latest
Twitter Bootstrap (LESS) & Backbone.js to CoffeeScript with CommonJS modules
support & proper JS bundling.

Here're a couple of exemplary code snippets to whet one's appetite:

{% codeblock main.coffee lang:coffeescript %}
{log} = require './utilities'

$(document).ready ->
  window.app = {}
  log 'Hello, world!'
  return
{% endcodeblock %}

{% codeblock Application.scala lang:scala %}
object Application extends Controller {

  def index = Action {
    Ok(views.html.index(Messages("app.name")))
  }

}
{% endcodeblock %}

[Get it on GitHub](https://github.com/robi42/play2-boilerplate) while it's hot.
