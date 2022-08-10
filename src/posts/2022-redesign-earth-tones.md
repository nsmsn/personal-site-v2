---
title: Earth tones
description: A new color scheme and a little CSS refactor spurred on by using dark mode. 
date: 2022-08-09T23:37:55Z
tags:
  - redesign
layout: layouts/post.njk
---

Nope, it is not déjà vu. I revised my website colors again. This time, if you are viewing my website in in light mode, you are seeing a rich brown text on a creamy, ivory-colored background. In dark mode, you are likely seeing light text on a rich chocolatey dark brown background. 

<figure>
    <img src="/img/post-images/2022-08-lightmode-darkmode.jpg" class="panel"
         alt="NickSimson dot com slash info" />
    <figcaption>My info page in both light mode and dark mode</figcaption>
</figure>

You can go ahead and read my post from October 2021 [detailing how I originally shipped a dark mode on this site](/posts/2021-redesign-dark-mode/) to see a screenshot of the previous implementation. Not much has changed on the technical front. After a few months of using my own site, I decided to change the color scheme with these warmer, earthier colors, because the blue links left me feeling a bit cold, especially in dark mode.

<figure>
<img class="panel" src="/img/post-images/2022-harvest-neil-young.jpg" alt="Cover of Neil Young's 1972 album Harvest" width="497" height="487" loading="lazy"/>
<figcaption>This album cover may or may not have influenced my website’s current color scheme.</figcaption>
</figure>

Not much else to say design-wise. I have been using the Instapaper app for over a decade, as well as the reader view in Firefox (my main web browser of choice these days). Both of these reading apps support a “sepia” background option. Sometime last year, I stumbled across the [Wikipedia entry for cosmic latte](https://en.wikipedia.org/wiki/Cosmic_latte), the alleged average color of the universe, represented by hex triplet <code>#FFF8E7</code>. In addition to being a bit of trivia or a miserable inside joke, this particular shade of beige is pretty easy on the eyes for longform reading.

<img src="/img/post-images/2022-color-blender-earthtones.png" alt="Gradiation of beige to chocolate on Eric Meyer's color blender" width="506" height="494" loading="lazy" />

I used a shade that is just a bit lighter, and instead of charcoal or black I paired this with a color that reminded me of dark chocolate. I found I love my [type choices](/type/) even more in this understated palette. To get a few midpoints (colors for card components, supporting text, etc.) I used a classic web design tool, [Eric Meyer's Color Blender](https://meyerweb.com/eric/tools/color-blend/). Link color matches text color this time, except links will always be underlined.

With almost all blues eliminated in this new minimal palette, I thought it would be a good time to take stock of any CSS declarations I no longer needed and remove them. I used [cssstats.com](https://cssstats.com/) to audit these styles. 

<figure>
<a href="http://web.archive.org/web/20220807202952/https://cssstats.com/stats/?url=nicksimson.com"><img src="/img/post-images/2022-css-color-stats.png" alt="screenshot of CSS stats dot com"  loading="lazy"/></a>
<figcaption>50 unique colors. 84 total color declarations. 44 unique background colors. 60 total background colors. (According to <a href="http://web.archive.org/web/20220807202952/https://cssstats.com/stats/?url=nicksimson.com">cssstats.com</a>)</figcaption>
</figure>

Wow, that’s a lot of color. When I started working on this site in 2020, I grabbed the whole [tachyons palette](http://tachyons.io/docs/themes/skins/). I’m not sure what I was thinking at the time, perhaps I might be a little ambitious with a rainbow of different colors throughout my site. That didn’t really pan out, and so I was able to get rid of a big chunk of my <code>_config.scss</code> file, plus a bunch of color utility classes it turns out I wasn’t using at all. 

With my earlier implementation of dark mode, I also struggled a bit with how other user interface (UI) components should translate from light to dark. Should a card component be lighter or darker than the background color? What about <code>code</code> and <code>pre</code> elements? Does this relationship switch from one mode to another? 

Accessibility, as always is a primary concern. To get a range of values that are interoperable in both light and dark modes, I put some of [my color values from color blender](https://meyerweb.com/eric/tools/color-blend/#F9F4EB:231C13:10:hex) into EightShapes’ [Contrast Grid tool](https://contrast-grid.eightshapes.com/?version=1.1.0&background-colors=&foreground-colors=%23ffffff%2C%20White%0D%0A%23f9f4eb%2C%20Ivory%0D%0A%23e6e0d7%2C%20LightGray%0D%0A%23aba59c%2C%20Gray%0D%0A%235d574e%2C%20MedGray%0D%0A%23433c33%2C%20DarkGray%0D%0A%23231c13%2C%20Black%0D%0A%23c11b11%2C%20DarkRed%0D%0A%23ee453b%2C%20BrandRed%0D%0A%23f18680%2C%20LightRed%0D%0A%23fac1bf%2C%20LightestRed&es-color-form__tile-size=compact&es-color-form__show-contrast=aaa&es-color-form__show-contrast=aa&es-color-form__show-contrast=aa18). I also added shades and tints of my red brand color, since I want a link style to stand out for certain links, like my [post tags](/tags/). The contrast grid tool is one of my favorites. It allows you to test many foreground and background colors at once in compliances with WCAG 2.0’s minimum contrast requirements.  

<figure>
<a href="https://contrast-grid.eightshapes.com/?version=1.1.0&background-colors=&foreground-colors=%23ffffff%2C%20White%0D%0A%23f9f4eb%2C%20Ivory%0D%0A%23e6e0d7%2C%20LightGray%0D%0A%23aba59c%2C%20Gray%0D%0A%235d574e%2C%20MedGray%0D%0A%23433c33%2C%20DarkGray%0D%0A%23231c13%2C%20Black%0D%0A%23c11b11%2C%20DarkRed%0D%0A%23ee453b%2C%20BrandRed%0D%0A%23f18680%2C%20LightRed%0D%0A%23fac1bf%2C%20LightestRed&es-color-form__tile-size=compact&es-color-form__show-contrast=aaa&es-color-form__show-contrast=aa&es-color-form__show-contrast=aa18"><img src="/img/post-images/2022-contrastgrid-earthtones.png" alt="screenshot of accessible color combos in beige, brown and red"  loading="lazy"/></a>
<figcaption>My latest color scheme, using EightShapes’ Contrast Grid</figcaption>
</figure>

I wanted to make it easier on myself this time, using CSS variables again, and making the little UI decisions less <em>variable</em> themselves. In light mode, the “card” background will be a bit darker than the background color, and in dark mode, the “card” will be a bit lighter. In my current case, “card” styles are <code>div</code>s with a <code>.panel</code> class applied, plus the <code>blockquote</code>, <code>code</code> and <code>pre</code> elements. I am applying a strict rule to my internal brand guidelines not to mix these up too much. When I do (putting code samples in a blockquote for example), hopefully my type system sorts these out perceptively. Minimalism is harder than it looks!

So to review, that’s six different values: a <code>body</code> background color, a “card” background color, a text color, a supporting (light) text color, a default link color (same as text color), and a hovered link color. Here’s those variables in action:

<pre>

:root {
  --bg-color: #faf6ef;
  --bg-card: #e6e0d7;
  --text-color: #433c33;
  --light-text: #5d574e;
  --link-color: #433c33;
  --link-hover: #ee453b;
}

</pre>

And the colors for dark mode:

<pre>
@media (prefers-color-scheme: dark) {
    :root {
        --bg-color: #231c13;
        --bg-card: #433c33;
        --text-color: #f9f4eb;
        --light-text: #e6e0d7;
        --link-color: #f9f4eb;
        --link-hover: #f18680;
      }
}
</pre>

I’ve found lately when working with CSS variables, and dark mode especially, that it is better to name classes and variables with the purpose of the color, rather than the color’s name. Now that I’m going down this road, there is probably a lot more in my stylesheets I can refactor, maybe embracing more repeatable utility classes for the different components that make up my site. It is always a work in progress. 

I hope you like the new color scheme as much as I do.