---
title: NewwwYear Itches
description: A few things I’d like to do with my site in 2023.
date: 2023-01-11T16:40:02Z
tags:
  - redesign
layout: layouts/post.njk
---

The [#NewwwYear hashtag](https://indieweb.org/newwwyear) was [popularized by Jen Simmons on Twitter in 2017](https://twitter.com/jensimmons/status/943323088405581824) for the purpose of making commitments and improvements to your personal website. The idea behind it is similar to New Year’s resolutions: taking small, but concrete steps toward building and improving one’s website. 

The current version of my website ([started in December 2020](/posts/2020-newww-year/)) embraces [small, iterative changes](/tags/redesign/) over massive redesigns again and again. Overall, I am quite happy with this this design (for now!): There is very little friction for writing/publishing new posts and shipping new features. At the beginning of 2023 I want to continue building on this foundation and make a few improvements.

> [Itches](https://indieweb.org/itches), in the context of the indieweb, are individuals’s personal sources of annoyances using the web or in particular their own website, that they use to itemize and prioritize what to create, design, build, and improve on their own website...

Not all of which follows are annoyances&mdash;some are simply cases of [personal site envy](https://www.are.na/nick-simson/the-art-of-the-personal-website). As my internet presence has sprawled and changed in the last couple years, there’s a couple of areas I’d like to improve in the upcoming year.

## Alphabetical tags
I’ve supported tags since the December 2020 redesign embarked. One thing that currently annoys me is that as I add new tags, they do not appear in alphabetical order. This looks like it might be relatively easy to fix, and I already found a [post by Mark Llobrera](https://www.markllobrera.com/posts/eleventy-tag-list-sorting-and-post-count/) that gets into doing this with [eleventy-base-blog](https://github.com/11ty/eleventy-base-blog), the Eleventy starter I built this site from.

## Theme switcher
In 2021 I [shipped a dark mode](/posts/2021-redesign-dark-mode/) to my website and in 2022 I [updated the color scheme](/posts/2022-redesign-earth-tones/) to take better advantage of CSS variables. Currently the site’s dark/light mode is tied to a user’s system preferences. In 2023, I’d like to add a theme switcher to my site. [Sarah Fossheim wrote up an excellent tutorial](https://fossheim.io/writing/posts/accessible-theme-picker-html-css-js/) on how to do this in an accessible way. 

> The need for more than just a light theme and dark theme came from the fact that personally, when I get bad migraines and headaches, low contrasting colors feel easier on my eyes, so I wanted to at least add a dark low-contrast option in addition to a regular light and dark theme.

Sarah, [Max Böck](https://mxb.dev/), and [Adam Stoddard](https://aaadaaam.com/) all support multiple, creative color themes on their personal sites, and these are worth checking out. I’ve read other anecdotes about users wanting to be able switch between modes on individual sites/apps. While I do not suffer from migraines, I do have [astigmatism](https://www.mayoclinic.org/diseases-conditions/astigmatism/symptoms-causes/syc-20353835), and I often find myself adjusting the contrast of my phone and other devices for more comfortable reading. Before I unleash a slew of light, dark, dim, and colorful themes on my users, I’d like to do a bit more research on different eye conditions, colorblindness, and user preferences in general.

## Microblog 
I set up a paid [Micro.blog](https://micro.blog/) account with a hosted microblog in 2022 after trying and giving up on a little WordPress project in 2021. I was able to [ditch Twitter](/posts/2022-ditch-twitter/) and move my old Instagram photos over to it. I do wish the community at Micro.blog was a bit bigger, but I love the set of features the service currently provides, as well as its official iOS apps. 

Writing primarily on this site and on [my microblog](https://nsmsn.micro.blog), I use Micro.blog to syndicate both feeds to [Mastodon](https://mastodon.design/@nsmsn). I am able to reply natively to others using both Micro.blog and Mastodon apps.

I initially picked a [nice theme](https://github.com/pimoore/microdotblog-tufte) for my hosted microblog, but in 2023, I’d like to create my own custom theme, maybe based on this site’s typography and colors. I’ve not developed for [Hugo](https://gohugo.io/) before, so it could be a fun exercise.

## Indiekit
This last one has the most technical overhead, and I don’t know if I’ll make progress on it this year or not. I have a desire to close the distance between my microblog and personal website (macroblog?) and I’ve been following Paul Robert Lloyd’s [Indiekit](https://getindiekit.com/) project for a while. It is a self-hosted Node.js server and [Micropub](https://indieweb.org/Micropub) endpoint that does some nifty things and makes IndieWeb compatibility easier for static websites.

[Paul’s launch post introducing the Indiekit beta](https://paulrobertlloyd.com/articles/2022/12/indiekit/) came in December and promises tutorials for setting it up on different hosts. I intend to keep following Indiekit and see if more people hook it up to their [Eleventy](https://11ty.dev)-powered websites. [Webmention](https://www.w3.org/TR/webmention/) support may be on the horizon too. I’m a designer and setting up servers, git actions, and other similar stuff has always made my head spin a bit. But I’d love to give it a try and see what I can learn from it.