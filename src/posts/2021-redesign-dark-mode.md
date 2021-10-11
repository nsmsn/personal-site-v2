---
title: Now with dark mode
description:  Adding a new feature to this site’s design.
date: 2021-10-10
tags:
  - redesign
layout: layouts/post.njk
---

If your device supports a dark mode, and you’ve set this as your preference, you can now view my website in a darker color scheme. I worked on it this weekend during an [IndieWeb Create Day](https://events.indieweb.org/2021/10/indieweb-create-day-ZKw5v2nFDu6f)&mdash;one day dedicated to working on our personal websites or various IndieWeb projects out in the open.

<figure>
    <img src="/img/post-images/2021-10-lightmode-darkmode.jpg" class="panel"
         alt="NickSimson dot com slash info" />
    <figcaption>My info page in both light mode and dark mode</figcaption>
</figure>

I launched my site with an off-white background, so the "light mode" design will be my default design. Adding dark mode support is pretty straightforward. There is a media query for dark color scheme preference:

<pre>

@media (prefers-color-scheme: dark) {
    
    */ Write your dark mode styles here /*

  }

</pre>

Within that rule you can write in any overrides you desire. The complexity is going to depend on how your CSS is structured. I’m using Sass on nicksimson.com, and I have several places where I am declaring colors. First, I have a <code>_config.scss</code> file where I have fonts, colors, and sizes declared as Sass variables. The colors are named things like <code>$darkblue</code> and <code>$lightyellow</code>. 

Throughout my various <code>.scss</code> files I have colors applied to the <code>body</code>, base elements like <code>h1</code>, and classes like <code>.post-tag</code>. 

To get started, I fired up Eleventy and localhost, set my OS preferences to dark mode, and created a new <code>_darkmode.scss</code> file. I started writing a few rules on <code>body</code> to see how the browser rendered my site. The easiest place for me to start was to swap the text color and background color:

<pre>

@media (prefers-color-scheme: dark) {
    
    body {
        background: $darkgray;
        color: $ivory;
    }

  }

</pre>

This base rule quickly shows how many places where you may need to adjust colors to fix contrast issues. My <code>$darkblue</code> hyperlinks for example, started to disappear into the background. I already have a [page that displays every html element](/html) so I used this to quicky diagnose other elements to override. My site is not minimal in that it uses white black and blue. I have supporting text in medium gray, I apply subtle background colors to elements like <code>pre</code> and <code>code</code>, not to mention classes like <code>.post-tag</code> and <code>.panel</code>. When you highlight text on my site, it applies a high contrast highlight color scheme, so another thing I needed to override too.

Remember how I said I had several classes in several <code>.scss</code> files applying color rules? For organizations sake it makes more sense to include the dark mode overrides in each file, rather than putting all these random elements and classes in one file. At the same time I didn't want to have to add the media query after every rule that apllied a color in the stylesheet.

## CSS variables to the rescue

From a couple dozen colors declared in my config file, I narrowed down the big five that make up my core color scheme. I wrote these values as CSS variables on the <code>root</code> element, named by purpose instead of color value. These are background color, text color, light text (heading levels 5 and 6 plus supporting text like <code>figcaption</code>), link color and link hover color.

<pre>

:root {
  --bg-color: #faf9f9;
  --text-color: #343434;
  --light-text: #676767;
  --link-color: #334492;
  --link-hover: #ee453b;
}

</pre>

This involved changing some rules from Sass variables to these new CSS variables, like on the body element for example:

<pre>

body {
  background-color: var(--bg-color);
  color: var(--text-color);
}

</pre>

Going back to my <code>_darkmode.scss</code> file, I erased my body rules and changed these root colors within the dark mode media query:

<pre>
@media (prefers-color-scheme: dark) {
    :root {
        --bg-color: #343434;
        --text-color: #faf9f9;
        --light-text: #c0c0c0;
        --link-color: #a4bfeb;
        --link-hover: #f18680;
      }
  }
</pre>

This covers most of my dark mode needs. Beyond these variables, I am still including dark mode overrides on other <code>.scss</code> files, at the end of each stylesheet. There are only a few of these, and again they are on files like <code>_panel.scss</code> and <code>_tags.scss</code>.

It only took a few hours and it was fun to share my work at the end of the day on Zoom with a few others in the IndieWeb community. Now I’m happy to share it with the world. 