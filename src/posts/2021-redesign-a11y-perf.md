---
title: Accessibility and Performance
description: A few handy code snippets and more. 
date: 2021-02-07
tags:
  - redesign
layout: layouts/post.njk
---

I have read and agree with Robin Rendle's sentiment: [accessibility and web performance are not features, they’re the baseline ](https://css-tricks.com/accessibility-and-web-performance-are-not-features-theyre-the-baseline/). 

That said, I want to spend a little bit of time highlighting some of the front end code I'm excited about that keeps my website fast and usable.

## Skip Link
If you inspect the markup of each page the very first link in the <code>body</code> of my website is a "Skip to Content Link", an anchor tag that links to the <code>main</code> element with an ID of "main-content". When you select the link the page will scroll down to the "main-content" ID applied to the <code>main</code> element, <em>skipping</em> all the navigation links on its way down.

When CSS is loaded, the skip link is visually hidden by the following CSS:

<pre>
<code>
  .skip-link:not(:focus) {
    border: 0;
    clip: rect(0 0 0 0);
    height: auto;
    margin: 0;
    overflow: hidden;
    padding: 0;
    position: absolute;
    width: 1px;
    white-space: nowrap;
  }
</code>
</pre>

This visually hidden code snippet can also be found on [Andy Bell's website](https://piccalil.li/quick-tip/visually-hidden)

Tabbing through the <code>header</code> element with a keyboard reveals the Skip to Content link, styled as a large button (you can't miss it):

<img src="/img/post-images/2021-skip-link.png" loading="lazy" alt="Light blue Skip to content link visible on Nick Simson dot com" width="603">

The styled link also has a hover style applied:

<img src="/img/post-images/2021-skip-link-hover.png" loading="lazy" alt="Navy blue Skip to content link with hover styles applied" width="603">

The following CSS gives a smooth-scrolling animation to all in-page links (as long as <a href="https://caniuse.com/css-scroll-behavior">the browser supports the <code>scroll-behavior</code> property</a>):

<pre>
<code>
html {
  scroll-behavior: smooth;
}
</code>
</pre>

If <code>scroll-behavior</code> is not supported, the link still works and will just jump to the section of the page. This will be the behavior if the visitor has disabled motion and animation in their browser preferences:

<pre>
<code>
/* Remove all animations and transitions for people that prefer not to see them */
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
</code>
</pre>

Again, these snippets are courtesy of Andy Bell, via his [modern CSS reset](https://piccalil.li/blog/a-modern-css-reset).

## Optional Web Fonts

This one may prove controversial. I am implementing the following in all @font-face declarations since I am using [three webfonts](/posts/2020-redesign-webfonts-html/): 

<pre>
<code>
 @font-face {
    font-display: optional;
  }
</code>
</pre>

If any of the fonts take longer than 100 milliseconds to render on the initial page load, the fallback font will display instead. The fonts will be visible on refresh, or the next page a visitor reaches. Since I picked typefaces that are close to the proportions of the system defaults, this isn't a huge deal to me, and I almost how many people will notice. But for the same reason, any Flash of Unstyled Text or layout shift in the design isn't a huge deal, and I could easily revert back to <code>font-display: swap</code>.

Since I am serving the fonts with Google's CDN, I am also using <code>link rel="preconnect"</code> before the font stylesheet to speed up the delivery of the fonts, which I'm treating as an enhancement to the page layout.

Simon Hearne has a big, long write-up on strategies to [avoid layout shifts caused by web fonts](https://simonhearne.com/2021/layout-shifts-webfonts/), if you're interested in more of this topic.

## Native Lazy Loading

Since this starting landing in web browsers in summer 2019, I'm getting in the habit of writing <code>loading="lazy"</code> as an attribute on my images in posts, and adding this to previous posts on this site. This is an instruction to the browser to wait to load the image until it is close to coming in frame of the viewpoert. Thankfully, I'm not using a lot of images on a single page, but this will be handy if/when I add a portfolio to this site.

[Web.dev](https://web.dev/browser-level-image-lazy-loading/) and [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/Performance/Lazy_loading) both have information on how this feature works.

## Wrapping Up

If I add more code that enhances accessibility or performance, I will either add to this post or include snippets in a future follow-up post. In the meantime, you can catch up on my other [posts tagged 'Redesign'](/tags/redesign/).