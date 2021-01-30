---
title: Everyday developers
description: On specialization, generalization, and being no stranger to change.
date: 2015-08-31
tags:
  - design
layout: layouts/post.njk
---

I always enjoy [The Web Ahead](http://thewebahead.net) podcast, hosted by [Jen Simmons](http://jensimmons.com/). For the past 4 years and over 100 episodes, Jen has been researching very specific topics, booking the best possible guests, and then going deep into that subject matter for a good hour or so. I make it a point to catch up after each episode is published, as I've found it to be an indespensible resource to keep up with new technologies and conversations surrounding the world wide web, and the people who work on it.

[A recent episode released on August 13](http://thewebahead.net/104), featured a conversation between Jen and her guest [Rachel Andrew](https://rachelandrew.co.uk/) about "everyday developers". Actually, the word "everyday" only came up once during the discussion, but they were describing a type of web generalist who builds sites for clients, perhaps as a freelancer or as part of a small team. I consider myself a part of this&nbsp;camp. 

Five years ago, Elliot Jay Stocks' ["Web designers who can't code"](http://www.elliotjaystocks.com/blog/web-designers-who-cant-code/) article launched a firestorm of tweets, blog posts, and debates about the division of labor between "design" and "development". Nine years before that, Jeffery Zeldman had written a book, [<em>Taking Your Talent to the Web</em>](takingyourtalenttotheweb.com/) for transitioning print designers. Each year, it feels like the lines between "design" and "development" [are finally getting fuzzier](http://bradfrost.com/blog/post/development-is-design/), and I think that is a beautiful&nbsp;thing.

Jen and Rachel both bring a valuable perspective to this topic, because they were once living it themselves. Today they are prominent speakers and in-demand CSS layout experts, but both came to the web early on, building websites for people who really needed them, and for others like them, who were just figuring out how to put their stuff online. In the mid-1990s, almost anyone designing a website was a novice or a pioneer, learning how things work, making mistakes along the way, and developing the techniques and hacks that others would quickly rely&nbsp;on.

<figure>
<blockquote>...Web technology was not that complicated 15 years ago. It was possible for a person to come from a design background, be more focused on design, and yet know pretty much everything there was to know about the development side. You wrote HTML and CSS and used FTP to put the files on the&nbsp;server.</blockquote>
<figcaption>
Jen Simmons, <cite><a href="http://thewebahead.net/104">The Web Ahead, Ep. 104</a></cite>.</figcaption></figure>

Today, you may still find a few people learning or deploying their sites that way, but on the other side of the spectrum there are websites and web applications that are almost like utility services, delivering video entertainment, family photos, and breaking news at speeds and resolutions unheard of to devices that only existed in someone's imagination 20 years ago. The Facebooks, Googles and Netflixes of the world have armies of developers (sometimes referred to as "engineers") working with complex sets of digital tools, releasing powerful frameworks and libraries every couple&nbsp;months.

In between these two, you have what Jen and Rachel would call "everyday developers," which is possibly the widest gamut of web workers. Not all these people have Computer Science or graphic design degrees. Some are at ad agencies, some are working in-houses at companies and organizations you've heard of, but don't think about on a daily basis. A handful might be working on small web applications, but the majority are focused on some kind of publishing or marketing. They may be lucky to attend a conference every couple years, but are rarely on the speaker stage at a sposored industry conference or featured in a trade magazine. A few of today's everyday developers will be the engineers, authors, and speakers of tomorrow. Mostly they are out there in huge numbers, maintaining the CMS at their university, writing some vanilla Javascript, doing great work for their clients every&nbsp;day.

A few highlights from the episode:

## On documentation

Writing documentation on your open-source project is doing good work:

<figure>
<blockquote>
So often we have people saying, "What's happened?" What they'll say is, Perch, our product, has removed all of the spacing between their paragraphs. I open up the site, look in the browser inspector, and they've got a reset stylesheet which is removing all the spacing between their paragraphs. They've put it in there. We don't put it any code. We didn't put the CSS in. They've included something and don't know what it is. They don't know what it does...That is happening a lot. People are taking bits and pieces from around the web. They're using things as a starting point. Those things, individually, are very good. People are putting them out there, on GitHub or whatever, assuming that everyone who would use it has the same level of knowledge as they do. Of course, they don't.
</blockquote>
<figcaption>
Rachel Andrew, <cite><a href="http://thewebahead.net/104">The Web Ahead, Ep. 104</a></cite>.
</figcaption>
</figure>

This is one that has really made a difference for me. Don't assume everyone who is using your code has the same skills, background, or comfort level as you. Help beginners move forward by providing some kind of entry point. At minimum, put comments in your unminified files explaining what each bit does. Even better, provide a simple demo if possible, so we can see what your code accomplishes. Does your project require installing a library or package manager in the terminal? A lot of web designers aren't as comfortable on the comand line: I used [Mixture](http://mixture.io/) for a good year and a half before I finally switched to [Gulp.js](http://gulpjs.com/) earlier this year. Even linking to a good tutorial could help someone a long way. Can you offer a downloadable version without&nbsp;dependencies?

Interoperability in open source web projects is a nice ideal to aim for, when it makes sense. I'm a big fan of Chris Ferdinandi's [Kraken project](https://cferdinandi.github.io/kraken/). The components of this web starter kit are designed to be modified or removed completely without breaking a lot (A little like Bootstrap or Foundation, but much smaller fewer frame-work specific classes). It uses some familiar conventions, and avoids becoming over-opinionated. He's also created some useful Javascript add-ons (each with their own demo) that are coded in a way that could independently on projects that aren't using the same Kraken's&nbsp;conventions.

I also appreciate the direction the [Roots](http://roots.io) team is taking with their open source WordPress projects. The next version of their starter theme will be shipped without Bootstrap, and require fewer dependencies, so you can install your preferred front-end boilerplate (or create your own). Similarly, their development and deployment packages aren't dependent on installing their starter theme or set of&nbsp;plugins.

## On the right tools for the right people

While Javascript frameworks and build processes have gotten a ton of attention, the bread and butter for a lot of everyday developers is still the content management system&mdash;customizing them, theming them, training clients and authors on how to use them. Once your work is done, what do your clients&nbsp;inherit?

> I think a lot, as I move through the project, about what I'm going to be leaving behind. I think a lot about the legacy they're going to have. If I build this site for you on Drupal, you're going to have to have someone to maintain that Drupal instance. That's not going to be me, because I don't enjoy that. I can hook you up with someone else and recommend somebody and they'll do it. Or I can teach you the skills if you're a person that can learn those skills and you can do it. What I cannot do is just put you on this system that needs regular updates and those updates which take a certain level of technical savvy and then never talk to you about it and walk away and leave you with security flaws. We're going to have that conversation at the very beginning because I need to suss out whether or not you can handle the responsibility of babysitting a Drupal website for the next five years. If you can't, then I'm going to make a different choice for you. I'm going to put you on Squarespace or wordpress.com. I'm going to put you on something where you don't have to update your own software.

I wouldn’t feel great either about handing off a WordPress or Drupal site to a client without extensive training (raising the price and billable hours) on updating the plugins and themes, security, and other infrastructure-y things if they aren’t already experienced or eager to do this themselves. Most clients' priorities are investing their time into creating great content (the stuff their customers and audiences actually see) and running their business. I don't think it makes much financial sense for most web designers to get into the hosting business either, when the money and time saved for both parties could be put back into the business, towards crafting a distinct visual design, or chasing higher-paying&nbsp;contracts.

Jen elaborates a little further:

>  Like I said, I used to do all of these small projects. Now I can't afford to do them. But I still have people come along [with minimal budgets] and they want to know, "How can I build a website?" I want artists and restaurants and nonprofits to have affordable websites. If I were to recreate that kind of business that I used to have, I might seriously think about being a Squarespace shop. I would help people think through their content strategy and business and take all of that content and put it on Squarespace or Wordpress.com.

I did this myself recently. I still think self-hosted WordPress is great, but sometimes even that is too much for some clients. It takes a lot of custom work to get WordPress working like Squarespace's draggable visual blocks of editable content. For small businesses and artists, what Squarespace and WordPress.com offer is great. Squarespace itself wants developers to customize their sites, and make money with their beautiful suite of editing tools, offering their own [developer platform](https://developers.squarespace.com/) with command line tools and a blank HTML5 Boilerplate-based theme.

There's also been an explosion of many new, next-generation CMS products out there that aren’t Wordpress or Drupal clones. Craft, Siteleaf, and Cloud Cannon all look very promising for everyday users and everyday developers&nbsp;alike.

## On teaching, training, learning

Both Jen and Rachel work on complex projects, lead workshops, and deliver talks on this stuff, yet admit that if they were starting out in their careers tomorrow, it would be a bit overwhelming to know where to start. Their audience at these worskshotps and events is largely made up of everyday developers, and I'm sure they are getting this feedback, as its a sentiment I hear expressed all the&nbsp;time.

Part of this is, I think, the landscape. The web is not a monolith. It was originally built to help facilitate document sharing among researchers doing science, but 25 years later, it is a significant chunk of almost every sector of the economy. A website can be where you read the breaking news, or something you log in to to check your banking, or something you consume streaming video from. An application that tracks your hours for your timesheet, a social network where you see your friend's baby photos, or a word processing document synced to a cloud server. WordPress (which powers 20-something percent of the web itself) is not a monolith, either. Depending on which developer you talk to, its a blogging platform, a powerful customizable content management system, or an API for building web&nbsp;apps. 

No one can possibly learn how to build every single one of these things. No one should be expected&nbsp;to. 

Rachel wrote a great [follow-up post](https://rachelandrew.co.uk/archives/2015/08/14/confidence-and-overwhelm/) after the podcast was released, with a few thoughts about the things "everyday developers" should be fluent in. The good news is that these core compentencies are the three things the web has been made up for a very long time: HTML, CSS, Javascript. A solid understanding of the fundamentals and paying attention to the features and changes to these three technologies will have the biggest impact on the largest number of users. Everything that goes into sending the front-end trinity to the browser will come and go over time, but "what the visitors to your site or users of your product will eventually interact with is HTML, CSS,&nbsp;JavaScript."

<figure>
<blockquote>How you get to the point of delivering HTML, CSS and JavaScript to the browser is just detail. It’s detail that is influenced by a lot of factors. Tools and processes that make sense when a site is delivered and worked on by a huge team are probably overkill for a site built by a solo designer....Understand HTML and CSS, be able to build a layout without leaning on a framework. Get a solid understanding of how a website actually gets from the server to a browser, an understanding of security and accessibility. These are the basics, the constants. These things change slowly. These things sit underneath all the complexity and the tooling, the CMSs and the noise of thousands of people all trying to make their mark on this industry.
</blockquote>
<figcaption>Rachel Andrew, <cite><a href="https://rachelandrew.co.uk/archives/2015/08/14/confidence-and-overwhelm/">'Confidence and Overwhelm'</a></cite></figcaption>
</figure>

More good news: The web is very forgiving. What you build today will work for years&mdash;even as browsers automatically update and hardware gets replaced&mdash;providing you are doing these core things right. I love coming across a website that was last updated in 2005 or earlier. A couple links may be broken and the design may not reflect the current trends or resolutions, but its somewhat reassuring that not everything is as ephemeral as it&nbsp;seems.

#### Further reading
* Chris Ferdinandi, [Kraken, Sass, and Open Source](http://gomakethings.com/kraken-sass-and-open-source/)
* Aaron Gustafson, ['A Fundamental Disconnect'](http://www.aaron-gustafson.com/notebook/a-fundamental-disconnect/)
* Jeremy Keith, ['The Format of the Long Now'](https://adactio.com/journal/1665)
