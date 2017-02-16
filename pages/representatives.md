---
layout: page
title: "Our Representatives"
---

Getting in touch with our representatives is pretty easy.
You should never hesitate to do so.

We recommend putting their phone numbers in your contact list.
That way calling them becomes as easy as picking up the phone.

If you ever find any of this information to be out of date, or want to add anything, contact us: [hi@take-action-alaska.org](mailto:hi@take-action-alaska.org)

## Why you should call

> But a large volume of calls on an issue could bring an office to a halt, sometimes spurring the legislator to put out a statement on his or her position, Ms. Ellsworth said. [source: NY Times](https://www.nytimes.com/2016/11/22/us/politics/heres-why-you-should-call-not-email-your-legislators.html)

## On this page:
<ul class="toc">
{% for representative in site.representatives %}
  <li><a href="#{{representative.slug}}">{{ representative.role }} {{ representative.name }}</a></li>
{% endfor %}
</ul>

## Your Representatives:

{% for rep in site.representatives %}
<h3 id="{{representative.slug}}">{{ rep.role }} {{ rep.name }}</h3>
<div class="contact">
<ul class="address">
{% for line in rep.address %}
  <li>{{ line[1] }}</li>
{% endfor %}
</ul>
<ul class="phone-numbers">
{% for number in rep.phone_numbers %}
<li>{{ number[0] }}: {{ number[1] }}</li>
{% endfor %}
</ul>
</div>
{{ rep.content }}
{% endfor %}
