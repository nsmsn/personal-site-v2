---
layout: layouts/page.njk
title: Following
description: Links to people, studios, and organizations.
templateClass: tmpl-page
permalink: /following/
---

I’m spending less and less time on Corporate Social Media™ these days, preferring RSS (wherever applicable). Here’s my attempt to create a directory of interesting people and collectives I follow via RSS or would be following on Twitter, Instagram, etc. 

In earlier days, this might have looked like a <em>[webring](https://indieweb.org/webring)</em> or <em>[blogroll](https://indieweb.org/blogroll)</em>. I call this my <em>affinity&nbsp;pool</em>.

&nbsp;

## People

Artists, designers, developers, educators, illustrators, writers, and others.

<small><ul class="list-unstyled list-multi-col">
  {% for item in people.items %}
  <li><a class="h-card" href="{{ item.url }}" target="_blank">{{ item.name }}</a> <span class="text-meta">{{ item.meta }}</span>
  </li>
  {% endfor %}
</ul></small>

&nbsp;

## Studios

Design studios creating interesting work.

<small><ul class="list-unstyled list-multi-col">
  {% for item in studios.items %}
  <li><a href="{{ item.url }}" target="_blank">{{ item.name }}</a> <span class="text-meta">{{ item.meta }}</span>
  </li>
  {% endfor %}
</ul></small>

&nbsp;

## Organizations

Nonprofits I actively support or donate to when I can.

<small><ul class="list-unstyled list-multi-col">
  {% for item in orgs.items %}
  <li><a href="{{ item.url }}" target="_blank">{{ item.name }}</a> <span class="text-meta">{{ item.meta }}</span>
  </li>
  {% endfor %}
</ul></small>