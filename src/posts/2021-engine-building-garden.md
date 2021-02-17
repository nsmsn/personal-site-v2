---
title: An engine, a building, a garden 
description: Thoughts on personal websites, including this one.
date: 2021-02-17
tags:
  - redesign
layout: layouts/post.njk
---

For a couple years, I have been maintaining a collection on Are.na called [The Art of the Personal Website](https://www.are.na/nick-simson/the-art-of-the-personal-website). There are larger and more popular lists and directories, but I mainly use this as a repository for personal sites that catch my eye as I come across them in the wild. Some are [portfolios](https://www.nicchan.me/projects/), some are [blogs](https://macwright.com/). Some are harder to classify. Some sites have a [minimal layout and aesthetic](https://estrattonbailey.com/), some are much more [experimental](https://nathan.tokyo/). All have something about them that feels handcrafted.

As I've been clipping and saving these personal sites I've been thinking about my own neglected web presence. Since [I announced my open redesign](/2020-newww-year/) in December, I have been thinking of a bunch of different metaphors for what I am doing in the evenings and early mornings as I work on this site.

## My site is an engine.
When I have a few spare hours to work on this, I feel like I'm escaping to garage to tinker with an engine. My site is a collection of files, but it is also a build process. I type <code>npm start</code> in the Terminal app, and everytime I save a file I can watch the window cascading through changes, rebuilding the site. I test my site in emulators, on bad Wi-Fi, or in Google's [Lighthouse](https://developers.google.com/web/tools/lighthouse), trying to make sure the experience is optimal in all these situations. When I commit changes to my repository, I trigger another process, rebuilding the site on the hosting platform, making these changes available for all to see. 

## My site is a building.
It says it up there in the header navigation: "Home". Unlike the home I physically occupy, this digital home is relatively easy and cheap to add on to. On the same commit as this new post, I added a [library](/library). I have read those books, but don't own physical copies of all of these. But linking to [worldcat.org](https://worldcat.org/), I can carry the record of the book around with me. Some day, I keep telling myself, I'll add a gallery in the front entrance where I can show off my best work. As I add on the site I'm writing new rules to the CSS file, adding another new coat of paint. Other times I feel like I'm sorting through boxes in the attic, revisiting old things I made, getting rid of things that are no longer meaningful.

## My site is a garden.
The concept of a digital garden is new to me, but intriguing. The basic idea of a garden is the intentional pruning and weeding of content, and letting ideas grow organically. [Maggie Appleton](https://maggieappleton.com/) articulates the digital gardening ethos for the 2020s:

<figure>
    <blockquote cite="https://maggieappleton.com/garden-history">
        <p>“Rather than presenting a set of polished articles, displayed in reverse chronological order, these sites act more like freeform, work-in-progress wikis. They're collections of evolving ideas that aren't strictly organised by their publication date. They're inherently exploratory...They're less rigid, less performative, and less perfect than the personal websites we're used to seeing. It harkens back to the early days of the web when people had fewer notions of how websites "should be." It's an ethos that is both classically old and newly imagined.”</p>
       </blockquote>
    <figcaption>—Maggie Appleton, <cite><a href="https://maggieappleton.com/garden-history">A Brief History & Ethos of the Digital Garden</a></cite></figcaption>
</figure>

My [writing archive](/posts) does follow a traditional reverse-chronological blog format, but reading about digital gardens inspires me to explore ways I can thread together my original work and the ideas I stumble upon in more novel ways than [tags](/tags/) (yes,I have those, too) and one-directional links. Well-designed public gardens often have multiple entry points, and I wonder how I could create more exploration beyond the traditional home page or landing pages. 

I also like Ethan Marcotte's advice to [let a website be a worry stone](https://ethanmarcotte.com/wrote/let-a-website-be-a-worry-stone/). When I started posting reading lists on this website, I had a re-realization that this was a personal site, and I was designing it for me. There are no analytics tracking your movement around the internet on this space, and that's intentional. I'm doing my best to make the text readable and enjoyable. My content hopefully slows you down, not funnels you into some kind of sales pitch. The slowest part of the design is the solitary person behind the screen, in his living room, typing words into a text editor, making minute adjustments to the stylesheet. Sometimes (<em>gasp</em>), the new post and the design change are on the same git commit!

I still remember some great website advice from Cathy, one of the first people to hire me to design. I had a fledgling website in 2007, paltry web skills and a meager portfolio, so I had placed a big bold <strong>Under Construction</strong> notice on my front page. She said that all websites are constantly in a state of construction, and suggested I take that off. 

<img src="/img/post-images/2021-open-redesign.png" alt="Open redesign notice" />

At some point, I will remove the open redesign notice in my <code>base.njk</code> template as I get more confident with the layout decisions, type scale, responsive images, components, and all the fiddly bits that make a website. But <em>hopefully</em> that will not be the end of the thinking, refining, working in public on this domain.