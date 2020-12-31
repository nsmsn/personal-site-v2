---
title: Scaffolding
description: Setting up a structure for the cascade.
date: 2020-12-30
tags:
  - redesign
layout: layouts/post.njk
---

A few things have changed visually since [the last snapshot](http://web.archive.org/web/20201221200650/http://nicksimson.com/): Some of the base styles, the header, the footer, the [home page](https://nicksimson.com). I want to write a little about some things happening behind the scenes.

As I mentioned previously, I started out with the [eleventy-base-blog](https://github.com/11ty/eleventy-base-blog) starter project, mainly to get the github/netlify deployment set up quickly and painlessly. Since then, as I started modifying base styles, I quickly realized that I wanted to break up my CSS into smaller pieces, much in the way the site templates are seperated in the <code>_includes / layouts</code> directory. 

I explored some of the other [starter projects in Eleventy's documentation](https://www.11ty.dev/docs/starter/) to see how CSS is being used. In addition to every possible CSS flavor (Tailwind, Sass, PostCSS) you can imagine, I found a couple projects that keep a <code>src</code> directory with the templates and content seperate from the <code>.eleventy.js</code> and <code>.package.json</code> files and other configuration stuff.

[Stephanie Eckles](https://thinkdobecreate.com/) has an awesome  [tutorial on egghead.io](https://egghead.io/playlists/build-an-eleventy-11ty-site-from-scratch-bfd3) where she shows how to set up a simple Eleventy project with Node Sass and a <code>src</code> directory that outputs to a <code>public</code> folder with the static site. This fit the bill of what I'm after. 

I know not every developer likes Node Sass, but I am still trying to use fewer dependencies, and I still like the idea of running everything through <code>npm start</code> rather than setting up a complicated build process. I tend to mainly use variables and imports and very few mixins so I don't need all the latest and greatest in "Dart" Sass/canonical Sass.

I forked the eleventy-base-blog project and spun up [my own version on GitHub](https://github.com/nsmsn/eleventy-base-blog-sass) a few days ago. My version has a <code>src</code> directory and uses Node Sass. The site that outputs on the <code>public</code> folder looks identical to the official 11ty one.

Here's how the <code>sass</code> folder is structured to output my [style.css](https://www.nicksimson.com/css/style.css) file: 

<pre>

sass
├── _base.scss
├── _code.scss
├── _config.scss
├── _reset.scss
├── _type.scss
├── blocks
├── style.scss
└── utils

</pre>

The files in the root of this directory are named with an underscore (_) and are mainly for global styles and code highlighting. <code>_config.scss</code> is a bunch of CSS variables (sizes, colors and font stacks) that will be used in the other files. In the folders named "blocks" and "utils" are where most of the CSS rules with classes are written. The big difference is that a "block" covers make up structures like page layouts and components. "Utils" are reusable utility classes that modify the appearance of an element or block.

The CSS is written so that the broadest, most generic rules are at the top of the stylesheet, followed by reusable classes that describe layouts and components, followed by more specific styles and overrides.  My <code>style.scss</code> file is only <code>@import</code> rules and is stuctured as follows:

<pre>
@import "config";
@import "reset";
@import "base";
@import "type";
@import "code";

@import "blocks/layout";
@import "blocks/header";
@import "blocks/nav";
@import "blocks/postlist";
@import "blocks/tags";
@import "blocks/markdown";
@import "blocks/warning";
@import "blocks/panel";
@import "blocks/pagination";

@import "utils/flexo";
@import "utils/float";
@import "utils/flow";
@import "utils/lists";
@import "utils/sr-only";
@import "utils/color";
</pre>

As I develop and add more to the site, I expect these files may change a little, but the structure is designed for living projects, and designed to scale. The CSS I'm writing these days follows concepts similar to Andy Bell's [CUBE CSS](https://piccalil.li/cube-css/) and Harry Roberts' [ITCSS](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/) projects. I invite you to check both approaches out if you are either starting out in web development or looking for a way to write object-oriented styles for more maintainable stylesheets.

<em>This was the third post in the ['redesign' series](/tags/redesign/).</em>
