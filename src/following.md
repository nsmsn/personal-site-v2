---
layout: layouts/page.njk
title: Following
description: Links to people, studios, and organizations.
templateClass: tmpl-page
permalink: /following/
---

Here’s my attempt to create a directory of interesting people and collectives I follow via RSS, newsletters, social media, etc. 

In earlier days, this might have looked like a <em>[webring](https://indieweb.org/webring)</em> or <em>[blogroll](https://indieweb.org/blogroll)</em>. I call this my <em>affinity&nbsp;pool</em>.

<small>If you want your name and link removed for any reason, just [email me](mailto:nick@nicksimson.com) and I’ll take it down <abbr title="as soon as possible">ASAP</abbr>. Sorry for being&nbsp;weird.</small>

&nbsp;

## People

Artists, designers, developers, educators, illustrators, writers, and&nbsp;others.

<div>
<small><ul class="list-unstyled list-following">
  {% for item in people.items %}
  <li><a href="{{ item.url }}" target="_blank">{{ item.name }}</a> <span class="text-meta">{{ item.meta }}</span>
  </li>
  {% endfor %}
</ul></small>
</div>

&nbsp;

## Studios

Design studios creating interesting work.

<div>
<small><ul class="list-unstyled list-following">
  {% for item in studios.items %}
  <li><a href="{{ item.url }}" target="_blank">{{ item.name }}</a>
  </li>
  {% endfor %}
</ul></small>
</div>

&nbsp;

## Organizations

Nonprofits I actively support or donate to when I can.

<div>
<small><ul class="list-unstyled list-following">
  {% for item in orgs.items %}
  <li><a href="{{ item.url }}" target="_blank">{{ item.name }}</a> <span class="text-meta">{{ item.meta }}</span>
  </li>
  {% endfor %}
</ul></small>
</div>