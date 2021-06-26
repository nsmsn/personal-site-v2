---
title: Collaborating on the new Tumbleweeds site
id: 002
description:
  Communication, prototyping, and tools to build a simple, beautiful site that
  works everywhere.
date: 2015-03-07
tags:
  - process
layout: layouts/post.njk
---

<figure><a href="http://tumbleweedsband.com/"><img src="/img/post-images/tw-web-preview.jpg" alt="Screenshots of The Tumbleweeds website" /></a>
<figcaption>A simple, responsive website design for the Tumblweeds band. <a href="http://tumbleweedsband.com/">View it live</a> in the browser.</figcaption></figure>

I was contacted in the fall of 2014 by Byron Ripley about designing a website for his band, [the Tumbleweeds](http://tumbleweedsband.com/). They play classic country and dance tunes in the Honky Tonk and Western Swing tradition. I've been friends with Byron for about ten years now, and remember the ealy days of the Tumbleweeds duo (Byron and Joe Carter) in Flagstaff/Williams, AZ.

The Tumbleweeds have had an online presence on [facebook](https://www.facebook.com/TumbleweedsMusic) and [bandcamp](http://tumbleweedsmusic.bandcamp.com/) for a number of years, and felt it was time to create a proper website to match the look and feel of their music. Byron's brother [Whitney Ripley](https://github.com/littleRm) is a web developer and offered to build the new site. In 2011, I had the pleasure and opportunity to create a new logo and design a few promo items for the band, shortly after they relaunched in Albuquerque. After doing a CD package for them a couple years ago I was really glad to get called on to help translate this visual identity to the web.

## Kickoff Meeting

The three of us got together via Google Hangout in mid-November to discuss the project and what needed to get done. Byron shared some of his goals for the site:

1. Make it easy for visitors and fans to find out when the band is playing.

2. Make contact information easy to find to book gigs.

3. Make music available for purchase/streaming and get visitors to sign up for their newsletter.

Other priorities we discussed were featuring large images of the band on the front page, featuring the logo as a large header image, and including video of a few performances. I made it clear early that I would plan to build responsively, making the site accessible and loading quickly on smaller screens.

 <div class="row">
        <div class="grid-half"><img src="/img/post-images/2015-03-tw-sketchbook-01.jpg" alt="Image of sketchbook with notes" loading="lazy"/>
        <figcaption>Notes from the Google Hangout discussion.</figcaption></div>
        <div class="grid-half"><img src="/img/post-images/2015-03-tw-sketchbook-02.jpg" alt="Image of sketchbook with notes and wireframe drawings" loading="lazy"/><figcaption>More notes and thumbnail sketches for content/strucutre.</figcaption>
        </div>
    </div>

In the course of this initial meeting we defined roles: Byron, as the client would be responsible for final approvals and serve as liason with the rest of the band. He would also be chiefly responsible for gathering and editing website content. Whit, as developer would be configuring the domain and hosting, and most major CMS development. As designer, my role was in structuring the content, visual design (type, image, and color) and developing a mockup as a static HTML/CSS prototype.

We also determined what the content needed to be, how much was already available and what may need to be written. Byron and I had previously used Dropbox when I worked on the Tumbleweeds' first CD "Roll On", so we used the same shared folder and created a new subfolder for the website project:

<img class="browser" src="/img/post-images/2015-03-tw-dropbox-folders.jpg" alt="Screenshot of Dropbox folder" loading="lazy">

We used Dropbox to store the latest versions of written content, hi-res photos and links to externally hosted items. The folders are named by content type, not necessarily navigation items, knowing that this could change in the course of the project timeline.

## Prototyping Design

With a few pages, images and bios completed after Thanksgiving, I had enough content to start prototyping. This was truly an exercise in ["content-first"](http://www.markboulton.co.uk/journal/structure-first-content-always) design. Instead of using image editing software like Photoshop or Illustrator to create a "mockup" of a page, I planned to write the design as a structured HTML document and use CSS to style the layout. I prefer designing this way because it forces you to consider the content (and the code) that will end up in the final product early and often. One of my favorite prototyping tools is [Mixture](http://mixture.io/),an app that fires up a little development server on your local computer complete with a templating engine and preprocessor support.

I had recently relaunched my personal site in late November, and used a [similar approach](https://github.com/nsmsn/tw/tree/master/assets/sass) to writing my CSS styles in the Sass syntax. This approach works well on fairly simple sites like this one and the Tumbleweeds, and keeps me thinking about the cascade of the compiled file itself. I like being able to find all different parts listed alphabetically in one folder, and using the <code>@import</code> function to manage the cascade order.

I had an opportunity to build up a visual identity for the band over time, initially with the Tumbleweeds logo and a bumper sticker, followed a CD package. The key parts of this visual language are a rich color pallette anchored by a warm red, and period/genre appropriate typefaces and lettering. Designing a site with multiple pages, video and audio presented an opportunity to expand this graphic identity a little further. I chose two slab serif typefaces available as webfonts from Google. The display type ([Vast](https://www.google.com/fonts/specimen/Vast+Shadow)), looks like it comes out of an old playbill or Hollywood western movie poster. The subheadings and body text uses [Bitter](http://www.huertatipografica.com/fonts/bitter-ht), a very readable font for the screen.

<div class="row">

<div class="grid-half"><figure><img src="/img/post-images/2015-03-tw-colors.png" alt="Screenshot of color pallette" loading="lazy" />
<figcaption>I used Adobe Illustrator to develop the color palette and went back into the code editor to add color to the static prototype</figcaption></figure></div>

<div class="grid-half"><img src="/img/post-images/2015-03-tw-proto.jpg" alt="Screenshot of web prototype" loading="lazy" /></div>
    </div>

Once I had worked some of the fonts, colors and logo into my HTML documents, I sent screenshots to Byron to show the visual direction I was going in. Working with live embeddable media from YouTube and Bandcamp was also helpful at this early stage for writing responsive breakpoints and containers to house multimedia content in. Bandcamp's audio player, for example, adapts to its container width.

I had already created two versions of the Tumbleweeds logo back in 2011, a horizontal banner and a logo contained in a circular shape. One of my favorite details of the site is how this logo changes from mobile and tablet styles to desktop.

By late December, most of the site content was already finalized except for a few musician bios. There were enough finished bios and photos that it was clear how those individual items would be eventually structured. Mixture outputs static HTML and I used the ['Public' folder in Dropbox](http://www.dropboxwiki.com/tips-and-tricks/host-websites-with-dropbox) to host a live interactive prototype with the primary navigation. We were able to make revisions in the browser fairly quickly, and after 3 iterations, the site was ready for production.

### Getting Ready for the Handoff

In our kickoff meeting we decided to explore WordPress as a possible CMS since it was something Whit and I were both accustomed to working with, and fairly user-friendly. While I was prototyping, Whit set up WordPress on Byron's hosting plan and created logins for all 3 of us. I had used the [Gigpress](http://gigpress.com/) plugin before, and suggested we try it out for managing the calendar. GigPress comes with a customizable stylesheet, so I was able to use this as a fundation to build table styles in a CSS file to use later in production.

I hadn't sent off an interactive prototype like this to another developer before, so I wasn't sure what to expect. I created a [GitHub repo for the prototype](https://github.com/nsmsn/tw) where Whit could download my CSS, JavaScript and HTML to use in a WordPress theme. The handoff went smoothly, and Whit worked dilligently and integrated some simple, intuitive functionality into the backend. A metabox in the WordPress editor for the home page controls the quote and slideshow images, and the order of the images can be changed by dragging and dropping them around. The grid layouts for various pages are achieved in metaboxes for different sections, or as shortcodes in the content editor itself.

<div class="row">
        <div class="grid-half"><img src="/img/post-images/2015-03-tw-gigpress.jpg" alt="WordPress back-end dropdown selector" loading="lazy" />
<figcaption>The GigPress plugin in action: Calendar events are super-easy to create with a set of fields in the editor.</figcaption> </div>
        <div class="grid-half"><img src="/img/post-images/2015-03-tw-slideshow.jpg" alt="WordPress back-end slideshow editor" loading="lazy" />
<figcaption>A home page metabox in the WordPress editor makes it really simple to change out the front page slideshow.</figcaption></div>
    </div>

Whit set up a new SSH-connected [GitHub repo for the theme files](https://github.com/littleRm/tumbleweedsband), making further collaboration and revision control possible. The site went live toward the end of February, and we got together on another video chat to evaluate the project, exchange notes and chat about music/life events. Its always a pleasure to work with the Tumbleweeds, and Byron and his bandmates sounded very pleased with the result.

A few things that worked out really well for us:

1. <strong>Focused design conversations around priorities.</strong> When we were discussing the website and its content, we were discussing <em>what we wanted people to do</em> and <em>what each section should accomplish</em>. Figuing out how something should look is a later step in figuring out how to do those first two things.

2. <strong>Keeping performance in mind.</strong> Using the [mobile-first design principles](http://bradfrost.com/blog/web/mobile-first-responsive-web-design/) I tried to keep images on each page limited to content and branding, so the fonts and colors I chose do a lot to communicate the design atmosphere. I planned for a lot of multimedia, and choosing to use CDN-enabled services like YouTube and Soundclound to host media files and fonts offloads a ton of weight off the server. A small amount of JavaScript is used, just for the slideshow and mobile toggle menu. Whitney carried this further using smart caching plugins to minify these assets on the live site.

3. <strong>Mutual respect.</strong> In our initial meeting we definied each person's role and tried to sketch out a realistic timeline for when things needed to get done. It was really helpful to have things like content gathering, visual design, and hosting/CMS configuration going on simultaneously, as the three of us were able to focus on our individual contributions, and balance our other work and life priorities. Byron has an infant daughter at home, and Whit and I both have full-time jobs, so it made a lot of sense to organize the project into milestones more than deadlines.

It always feels really great to ship a design and see it in the wild. On this particular site, I really enjoyed opening up the design process a little more and exploring different tools to enable remote collaboration. Five different technologies (email, Dropbox, Hangouts, GitHub, WordPress) may seem like a lot to collaborate, but each of these things serves a different purpose and does that one thing really well. I think it ended up being just the right amount for the three of us, with very little friction. I'm looking forward to taking what I've learned from working on this site and applying it to my design process in future projects.

That's enough out of me...<a href="http://tumbleweedsband.com/album/">give this band a listen</a>!
