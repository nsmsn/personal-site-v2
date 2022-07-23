---
layout: layouts/page.njk
title: Following
description: Links to people, studios, and organizations.
templateClass: tmpl-page
permalink: /following/
---

I am on Corporate Social Media™ less and less these days, preferring RSS (wherever applicable). This is my attempt to create a directory of interesting people and collectives I follow via RSS or would be following on Twitter, Instagram, etc. In earlier days, this might have looked like a [webring](https://indieweb.org/webring) or [blogroll](https://indieweb.org/blogroll). I call this my <em>affinity&nbsp;pool</em>.

&nbsp;

## People

People who have informed, influenced, or inspired me in some way. Some of these people I know, a few I have met (virtually or in person).

<small><ul class="list-unstyled list-multi-col">
  {% for item in people.items %}
  <li><a class="h-card" href="{{ item.url }}" target="_blank">{{ item.name }}</a>
  </li>
  {% endfor %}
</ul></small>

&nbsp;

## Studios

Design studios who consistently put out interesting work.

<small><ul class="list-unstyled list-multi-col">
  {% for item in studios.items %}
  <li><a href="{{ item.url }}" target="_blank">{{ item.name }}</a>
  </li>
  {% endfor %}
</ul></small>

&nbsp;

## Organizations

Nonprofits I actively support or donate toward when I can.

<small><ul class="list-unstyled list-multi-col">
  {% for item in orgs.items %}
  <li><a href="{{ item.url }}" target="_blank">{{ item.name }}</a>
  </li>
  {% endfor %}
</ul></small>