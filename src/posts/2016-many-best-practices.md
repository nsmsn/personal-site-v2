---
title: Many best practices
description: There’s more than one way to skin a website.
date: 2016-06-11
tags:
  - design
layout: layouts/post.njk
---

I recently stumbled across a website called [Web Field Manual](http://webfieldmanual.com/), a directory of resources "focused on documenting only the best knowledge for designing experiences and interfaces on the web."

The directory features a ton of links to information sources on relevant front-end web design topics: design process, style guide documentation, grids and typography, accessibility, and specific web technologies. Many of the articles and projects linked here I was familiar with, but several are new to me as well. 

No single link or author is the authoritative end-point for a particular subject. Combined, all these approaches make up a useful body of knowledge. Here are a few recent things I've discovered that are currently influencing or changing my web design approach:

## [ITCSS](http://itcss.io)
Short for *Inverted Triangle Cascading Stylesheets*, an approach to CSS architecture coined by Harry Roberts that is more strategy than strict methodology. ITCSS is primarily concerned with avoiding a needless complexity throughout the cascade by keeping the broadest, most reusable rules at the beginning of the file and finishes with the most specific rules (style overrides) at the end. 

[Jordan Koschei wrote an informative article](https://medium.com/@jordankoschei/how-i-shrank-my-css-by-84kb-by-refactoring-with-itcss-2e8dafee123a#.es1uf4lio) detailing how he refactored his own website styles using ITCSS, and how this shrank the file size of his final stylesheet and boosted his web performance. The [Xfive blog also recently published a helpful overview](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/). The ITCSS strategy can be easily combined with other CSS architecture approaches, such as SMACSS, OOCSS, or BEM. I'm currently applying the ITCSS approach on a side project, and have already found it both useful and efficient for naming and organizing my CSS files.

## [Fluid, Mathematical Web Typography](https://jxnblk.com/blog/mathematical-web-typography/)
[This post by Brent Jackson](https://jxnblk.com/blog/mathematical-web-typography/) builds upon previous writing on [modular scale typesetting](http://typecast.com/blog/a-more-modern-scale-for-web-typography) by others, proposing a simple set of rules to make type on the web infinitely scaleable and fluid, instead of relying on context-driven "magic numbers". A potentially infinite canvas throws a wrench into the historic conventions of typesetting, where rules have been built on fixed dimensions for centuries. 

Michael Riethmuller wrote more recently on [fluid typography with viewport units](https://www.smashingmagazine.com/2016/05/fluid-typography/). In this instance, "fluid" web type also means that there is no maximum <code>font-size</code> property, but the font system is sized in relationship to the overall canvas size. Responsive web design (largely) solved the designer dilemma for the mass adoption of smaller screens, but the [increasing support](http://caniuse.com/#feat=viewport-units) of viewport units and a typescale that increases exponentially could better [optimize our designs for larger screens](https://css-tricks.com/optimizing-large-scale-displays/).


## [Progressive Enhancement Everywhere](https://www.nngroup.com/articles/enhancement/)
The term *progressive enhancement*, coined around 2003, is not new, but I think its adoption and popularity will only trend upward. Voice-based user interfaces and artificial intelligence  I've become more fully aware of the concept by following the work of Jeremy Keith and Aaron Gustafson. I'm currently reading and enjoying Gustafson's [*Adaptive Web Design* book](http://adaptivewebdesign.info/), in which he describes interaction design as a series of enhancement layers built on top of a foundation of raw content and information: 

1. Markup (HTML, WAI-ARIA) is an enhancement layer, giving semantic structure to the content elements and exposing meaning to assistive technologies; 
2. Visual Design (Images, CSS, animations) is an enhancement layer, guiding the audience with visual prompts, identity, and delight; 
3. Interaction (Javascript) is the final enhancement layer, esablishing a baseline experience and fallbacks for interactions in which none, or only some of the programming is executed. 

Developing with this approach means that your content, service, and intention reaches the widest possible audience and accepts a broad and ever-increasing spectrum of input types and device capabilities&mdash;an exetension of the diversity of the human population itself and the human experience in the information age.