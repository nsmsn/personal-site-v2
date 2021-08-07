---
title: My six favorite utility classes 
description: Bits of CSS I re-use in almost every project.
date: 2021-08-07
tags:
  - redesign
layout: layouts/post.njk
---

My approach to writing CSS these days lays somewhere in between Andy Bell’s [CUBE CSS](https://cube.fyi/) and Harry Roberts’ [ITCSS](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/). I prefer Andy’s definition of a utility class from the CUBE CSS docs:

<blockquote>
A utility, in the context of CUBE CSS, is a CSS class that does one job and does that one job well.
</blockquote>

I’m writing this post to keep track of all of my favorite utilities&ndash;things I find myself reusing in almost every project.

## Visually Hidden 

<pre>
<code>
.vis-hidden {
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

If you ever used Bootstrap, you may recognize this as the <code>sr-only</code> class&mdash;in which sr stands for screen reader. I learned something from [Melanie Richards’ recent learning log](https://melanie-richards.com/blog/learning-log-2106/) and am using the <code>vis-hidden</code> class name from now on:

<blockquote>
This content is visually hidden; screen readers are not the only assistive tech that can access the hidden text on behalf of the user.
</blockquote>


## Uppercase Text
<pre>
<code>
.text-uppercase {
    text-transform: uppercase;
    letter-spacing: 1px;
}
</code>
</pre>

When you want something displayed in all capital letters, but you need [assistive technology to read it predictably](https://blogs.lanecc.edu/webteam/2017/03/07/using-all-capital-letters/). Adding in a little bit of letter spacing makes it a little easier to read a word set in all caps.

## Circular Images

<pre>
<code>
.img-circle {
    border-radius: 50%;
}
</code>
</pre>

This is great, whether you need a circular image for a user's avatar or in an "art-directed" post.


## Flex Objects

<pre>
<code>
.flexo {
    display: flex;
    flex-wrap: wrap;
    margin: -0.5em;
  }
  
  .flexo > * {
    flex: 1 0 18em;
    margin: 0.75em;
  }
</code>
</pre>

A G-rated version of Heydon Pickering’s "[Fukol Grid](https://github.com/Heydon/fukol-grids)". Turns anything nested in a <code>div</code> with a class of <code>flexo</code> into a flexible object ([View demo](https://codepen.io/nsmsn/pen/yodeeo)).


## Unstyled List

<pre>
<code>
.list-unstyled {
    list-style: none;
    padding: 0;
  }
</code>
</pre>

Another one you may recognize from Bootstrap. Sometimes you may need to remove the bullets in an unordered list or (less common) the numbers in an ordered list.

## Multicolumn List

<pre>
<code>
.list-multi-col{
	column-width: 12em;
	column-gap: 2em;
}
</code>
</pre>

Helpful for displaying long lists of short words or terms. Think of a donor wall at a museum for a real-life example. I’ve used this pattern on [advocacy.tennessee.edu](https://advocacy.tennessee.edu/ut-impact/) and [data.tennessee.edu](https://data.tennessee.edu/impact-by-county/).

In fact, I’ve found these so useful, all six of these utilities (plus a few more) have made their way into the [nicksimson.com codebase](https://github.com/nsmsn/nicksimsondotcom/tree/master/src/sass).