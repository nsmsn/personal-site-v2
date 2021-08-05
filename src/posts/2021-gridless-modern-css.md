---
title: Gridlessness and modern CSS
description: There’s never been a better time to learn (or re-learn) CSS.
date: 2021-07-21
tags:
  - learning
layout: layouts/post.njk
---

I just finished reading [gridless.design](https://gridless.design/), Donnie D’Amato’s thesis (in the form of a website) for doing away with the <i>n</i>-column grid or the <i>n</i>-pixel grid in the web design process. [Go read it](https://gridless.design/), if you haven’t already.

I’m convinced by his argument, being someone who has designed and implemented designs from both sides of the fence. I’ve reached for frameworks like the [960 grid system](https://960.gs/) or [Bootstrap's 12-column grid](https://getbootstrap.com/docs/5.0/layout/grid/) in the past. I’m not going to come down as hard on Donnie on these kinds of tools&ndash;I still think they have their place. You can build a serviceable website with a ready to go UI quickly and cheaply. This very website uses the flexbox-based grid from Chris Ferdinandi’s [Kraken project](https://cferdinandi.github.io/kraken/components.html) in places, because sometimes frankly, you need to split up a <code>.container</code> class into halves, or thirds, or fourths.

The Bootstrap 12-column grid, like all frameworks, was a product of a specific time and place. The best practical argument against reaching for these kinds of things today is that we just have better, more powerful tools for layout that can accomplish much more (in fewer lines of code).

One of my new favorite websites (and newsletters) to learn from is [ModernCSS.dev](https://moderncss.dev/) by Stephanie Eckles. Newer CSS features and properties are making me re-think the number of <code>@media</code> queries and breakpoints I am writing, even in responsive designs. The best advice on breakpoints I’ve found is to write them when your design is breaking. Thanks to relative units, tools like <code>clamp</code>, you can design layouts with fluid typography that don’t break often, if at all.

Stephanie’s [many other projects](https://thinkdobecreate.com/links/) are worth checking out; I’m particularly a fan of [11ty Rocks!](https://11ty.rocks/) as well as [SmolCSS](https://smolcss.dev/).

Another great resource for learning modern CSS was written by Andy Bell, commissioned by Google, at the enviable URL [web.dev/learn/css/](https://web.dev/learn/css/). Each lesson in this course is self-contained, meaning you don’t need to move from the course from start to finish. And it is not just layout, either. There’s an entire lesson on CSS animation, and an entire lesson on gradients, for example.

There’s never been a better time to learn CSS than now. It’s also a good time to time to re-learn CSS, especially if you are like me: tired of doing old hacks, and craving more elegant code.
