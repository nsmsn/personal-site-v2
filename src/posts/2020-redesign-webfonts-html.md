---
title: Web fonts and base HTML
description: My rationale for these new fonts, plus a poor man’s style guide. 
date: 2020-12-19
tags:
  - redesign
layout: layouts/post.njk
---


<figure>
    <img src="/img/post-images/2020-12-webfonts.png" class="photo-border"
         alt="NickSimson dot com homepage" />
    <figcaption>The current homepage with web fonts enabled</figcaption>
</figure>

If you are reading this post, it is likely you are viewing this with the webfonts. In my last [redesign post](/posts/newww-year/), I loosely mapped out some goals, including beauty, performance, accessibility, and celebrating open source.

In that spirit, I picked out three new typefaces to use on my site.

## Why Three?
While there are several ways to classify type, there are three major fallbacks you can tell a browser to use at the end of a CSS font stack: <code>serif</code>, <code>sans-serif</code>, and <code>monospace</code>. What these fallbacks actually are largely depends on your browser or operating system. 

<figure>
    <img src="/img/post-images/2020-12-fallbackfonts.png" class="photo-border"
         alt="NickSimson dot com homepage" />
    <figcaption>The current homepage with web fonts disabled and the fallback type displayed</figcaption>
</figure>

Using CSS custom properties, I can set simple variables at the <code>:root</code> for each font type. This will make it easy to remember a variable rather than a whole font stack

<pre><code>
:root {
    --sans: 'Epilogue', 'Segoe UI', Roboto, "Helvetica Neue", Helvetica, Arial, sans-serif;
    --serif: 'Literata', Georgia, serif;
    --mono:  'IBM Plex Mono', Consolas, Menlo, Monaco, "Andale Mono", "Lucida Console", "Courier New", Courier, monospace;
  }
</code></pre>

I build websites with [progressive enhancement](https://developer.mozilla.org/en-US/docs/Glossary/Progressive_Enhancement) in mind, so I use a pretty robust fontstack in my CSS, declaring common fallbacks available to different devices. For these three categories, I selected fonts that have proportions roughly equivalent to my default fallbacks. Right now I am not using a dramatic font loading strategy (more about that later), relying on a 'flash of unstyled text' or FOUT, if the network can't load my custom fonts.

## Character Traits
I did not pick three typefaces at random. My last design used a bookish serif called [Chaparral Pro](https://fontsinuse.com/typefaces/28/chaparral), designed by [Carol Twombly](http://www.alphabettes.org/review-carol-twombly-her-brief-but-brilliant-career-in-type-design/). This was one of the first webfonts available a decade ago when Typekit (now Adobe Fonts) launched and true web typography first became a thing. I still adore Chaparral, but it doesn't quite meet my criteria for my new site. The webfont version is a bit heavier than most of the other serifs on Adobe Fonts, the design itself is a bit of a hybrid between a humanist serif and a slab serif, with proportions that don't map close (or close enough for my discerning eye) to common fallbacks like Georgia and Times New Roman.

I chose [Literata](https://www.type-together.com/literata-3) instead, designed by Type Together (Veronika Burian and José Scaglione) and originally commissioned for Google Books in 2014. Since this design was made for reading devices, it certainly fits the "bookish" look I'm going for, and to the untrained eye, looks similar in proportion and style to Matthew Carter's [Georgia](https://fontsinuse.com/typefaces/70/georgia), another type designed for the screen first that has wide support on operating systems and browsers. Literata's killer feature for me, though is the <i>upright italics</i>, which are unusual to see in contemporary designs, and first caught my eye in 2014 when I saw it online.

It also helps that the redesigned and open-sourced Literata is available as a [variable font](https://web.dev/variable-fonts/), which means I can use one file to achieve a wide variety of weights and display styles. I want to set my block quotes with a little more <em>oomph</em>, without making my visitors download an extra resource.

For the sans-serif design, I wanted something that would work well for headlines, and be a distinct contrast from Literata. I've always been drawn to chunky nineteenth century grotesques, but I didn't want a revival typeface so much. I thought it would be a good idea to pick another variable font for versatility&mdash;an interface type for the header, navigation, and footer as well as headlines. I could a chunkier weight as a drop-cap on fancier, long posts down the road, or a lighter weight at smaller sizes for various [microcopy](https://www.uxbooth.com/articles/getting-ux-writing-right-with-microcopy/) instances.

Looking at the other open source variable fonts from Google, I discovered [Epilogue](https://www.etceteratype.co/epilogue) by Tyler Finck, another design introduced to the font service in 2020. I like the uppercase letters and how they almost appear condensed, but not quite as condensed as [Stratos](https://www.productiontype.com/family/stratos). I dig the slight curved edge of the lowercase <b>t</b> as well as the open loop tail on the two-story <b>g</b>, as well as the numbers. The name <em>Epilogue</em> fits in so nicely with <em>Literata</em>, continuing with that bookish theme. It doesn't hurt that Finck's Etcetera Type Company is based in Upstate New York, the region I grew up in.

Being a designer who codes, I also needed a monospace&mdash;not just for code but stylistically for things like timestamps on my posts and even the <code>figcaption</code> element. Again, continuing with the theme, I wanted a monospace in that sweet spot between a terminal font and a typewriter font. The [Plex family from IBM](https://www.ibm.com/plex/) just so happens to be open source, and the old IBM Selectric typewriter happens to be in [Plex Mono's DNA](https://www.ibm.com/plex/plexness/#mono-for-coding). Some of those rounded edges, distinct monospaced italics, and the two-story <b>g</b> all seem to compliment Epilogue and Literata. At the time of this writing, Plex Mono is not a variable font, so I will limit myself to a couple styles and a couple weights.

I'm happy with the harmony of these three distinct voices. Its a little idiosyncratic, but not too weird, which suits me. Because this is my first time using variable fonts, I'm going to use Google's CDN and fonts API to serve my type for now. Down the road I may want to self-host for added performance and possibly revisit my font loading strategy. But I have other fish to fry.

## Back to Base-ics

Now I have a lovely font stack I'm quite happy with. How do I put it all together? I want to revisit my base styles. I have a very simple style.css file inspired by [Andy Bell's helpful post on resets](https://piccalil.li/blog/a-modern-css-reset/), now enhanced with a more idiosyncratic typographic palette. I want to see quickly how all my basic HTML elements (with no classes applied) look. I need a [poor man's style guide](https://poormansstyleguide.com/).

I created a new page at [nicksimson.com/html](/html/) where you can see each markup element:

&nbsp;

<img src="/img/post-images/2020-12-headings.png"  class="photo-border"
         alt="H1 through H6 styles" />
At a cursory glance, my headings need a little work.

<img src="/img/post-images/2020-12-blockquote-figcaption.png" class="photo-border"
         alt="blockquote and figcaption styles" />
Not sure about the blockquote yet, but I like the figcaption now.

<img src="/img/post-images/2020-12-dl-tables.png" class="photo-border"
         alt="definition list and table styles" />
This area needs some work.

It might seem controversial to stop here and make a commit, but I want to step back and think about the CSS structure I'll need before I write any more. I'd like to break up my CSS into smaller files, and think about the elements I'm using now and what I will need in the future. 

Plus, I have that disclaimer about stuff looking wonky on the top of each page. That should buy me some time. I'll come back later when I've cleaned up this mess. In the meantime, you can view the other tagged posts in the ['Redesign' series](/tags/redesign/).