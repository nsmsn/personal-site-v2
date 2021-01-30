---
title: Ready for a Newww Year
description: Thinking and planning an open redesign. 
date: 2020-12-16
tags:
  - redesign
layout: layouts/post.njk
---

In late 2020, the coronavirus pandemic is raging in the U.S. and colder weather makes outdoor gathering less appealing. To stave off some of the cabin fever this winter, I'm ready to revisit my own website, which I have sadly left dormant until this week. My dad often talks about his grandfather, a carpenter, who was often so busy working on other people's homes, the upstairs of his own house was left unfinished for many years. The metaphor seems appropriate today.

Rather than simply applying a fresh coat of paint, I'm taking this down to the studs and thinking about what I want it to be in 2021 and beyond. I find the [IndieWeb](https://indieweb.org/) ethos more and more appealing: Publishing on my own platform rather than a commercial social network and tinkering around with technologies to scratch an itch.

In the spirit of [New Years' resolutions](https://twitter.com/jensimmons/status/943323088405581824), I put together an unordered list detailing what I want to accomplish with this rebuild:

* Build a beautiful website that represents me and my values.
* Make something easy to deploy and easier to maintain.
* Build something fast and accessible.
* Celebrate the commons, fair use and open source.
* Learn my medium (HTML, CSS, JS), broad and deep.
* Share what I know.

I do not know yet when I will take down the "open redesign" banner at the top of this, as the site will continue to evolve, but I expect I will lower that flag sometime in 2021.

## This goes to Eleventy
After following the bandwagon and hosting with [Jekyll](https://jekyllrb.com/) and [Github Pages](https://pages.github.com/) for years, I am following the bandwagon yet again and migrating to [Eleventy](https://11ty.dev/) and [Netlify](https://netlify.com/). The site structure, templating languages and deployment concept is quite similar, but I really like the performance speed of developing locally with Eleventy committing my changes with git and the git-based deployment to Netlify. 

Before committing to Eleventy, I checked out the project's documentation, plus several articles and podcasts. For a brief overview, I'd recommend the [Smashing Podcast on Eleventy with Drew McLellan and David Darnes](https://podcast.smashingmagazine.com/episodes/what-is-eleventy-with-david-darnes) discussing the project. 

I also purchased a copy of Andy Bell's [Learn Eleventy from Scratch](https://piccalil.li/course/learn-eleventy-from-scratch/) course and went through all the lessons in a weekend. Andy's course was just the right pace for me: I prefer following step by step instructions and reading the code more than trying to follow along with a video. While I like the build process and asset pipeline you create in the course, I will probably use fewer dependencies in my project. But I just love the idea of writing <code>npm start</code> to get going on active development.

To get my GitHub and Netlify working together right away I used the deploy to netlify feature on the official [eleventy-base-blog project](https://github.com/11ty/eleventy-base-blog). There are a lot of starter projects listed in the Eleventy documentation, but this one looks like it has the fewest dependencies. 'Deploy to Netlify' is like WordPress' five-minute install, but faster. The site you are looking at is pretty much that with some different CSS rules applied. The hardest thing to figure out updating DNS on my domain name, but I got it after reading [this quick tutorial](https://dev.to/easybuoy/setting-up-domain-with-namecheap-netlify-1a4d).

## This Old Website

If you miss the old site, I made sure to archive the [old home page](http://web.archive.org/web/20200928234553/https://nicksimson.com/) and [blog index](http://web.archive.org/web/20201021235738/https://nicksimson.com/blog/) on the Internet Archive. All the [old code is still archived on GitHub](https://github.com/nsmsn/personal-site-v1). I migrated my favorite and more relevant posts to a [new archive](/posts/). In the sprit of owning my content, I also exported my annual reading lists from Goodreads to a post series&mdash;check out the ['Books' tag](/tags/books/). 

I'll document changes in this blog with screenshots and a link to an Internet Archive capture. This website also has a [GitHub repository](https://github.com/nsmsn/nicksimsondotcom) where you can see everything that has changed.

I will tag all these posts ['Redesign'](/tags/redesign/) if you want to follow along. Thanks for coming with me on this journey.