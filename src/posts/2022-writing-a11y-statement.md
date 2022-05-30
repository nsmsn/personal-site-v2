---
title: Adding an accessibility statement
description: An important new feature to this site.
date: 2022-05-30T11:23:57Z
tags:
  - redesign
layout: layouts/post.njk
---

With the latest deployment of this website, you should be able to see a link labeled “Accessibility” in the <code>footer</code>. This will take you to my [accessibility statement](/accessibility/).

Why publish an accessibility statement on a personal website? These things are far more common on government websites, or education institutions, and many large corporations. In many cases these organizations are leagally required to provide such a statement. 

Recently, I discovered [Ethan Marcotte’s blog post about his website accessibility statement](https://ethanmarcotte.com/wrote/an-accessibility-statement/). He quotes the [Web Accessibility Initiative](https://www.w3.org/WAI/planning/statements/) on why an accessibility statement is helpful: 

<blockquote>
Accessibility statements are important for several reasons:
<ul>
<li>Show your users that you care about accessibility and about them</li>
<li>Provide them with information about the accessibility of your content</li>
<li>Demonstrate commitment to accessibility, and to social responsibility</li>
</ul>
</blockquote>

When I set out to [redesign my site in December 2020](/posts/2020-newww-year/), providing an accessible experience was top of mind. With every new feature and page I add to my website, I consider accessibility and do my best to address it.

Often times this looks like running a URL through an automated accessibility checker. I personally love browser-based tools, and my longtime favorites are [WAVE](https://wave.webaim.org) and [Tenon](https://tenon.io/). These tools are good, and it’s fun or challenging to get a “score”. But they’re only capable of catching [30-50% of accessibility issues on a page](https://marcysutton.com/evinced-automated-accessibility-testing), so it’s important to do some manual checks.

I [fixed an issue](https://github.com/nsmsn/nicksimsondotcom/commit/929d7530e076763228f86a0775178f3b530688bb) recently on my [Library page](/library/), when I discovered redundant alt text on linked images. In this case, I had both a book cover image and book title linked and going to the same destination, and I was using the book title as the image’s <code>alt</code> attribute. I was trained to always use alt text on a linked image, but in this case if there is text in the link describing the link destination, it is OK to use an empty <code>alt=""</code>. [Pope Tech has a great blog post on this](https://blog.pope.tech/2020/03/13/linked-image-missing-alternative-text-example/), using an image card component as an example.

An accessibility statement is not going to prevent me from running into issues like this, but it does communicate my dedication to fixing these things as I discover them. I also included two ways my audience can report accessibility issues or barriers to me. Finally, I thought it was important to state that I am always learning new things about digital accessibility and will share what I learn. 

