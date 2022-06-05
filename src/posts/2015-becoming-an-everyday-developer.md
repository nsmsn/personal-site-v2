---
title: Becoming an everyday developer
id: 002
description: What to learn, how to learn it, and what to learn next.
date: 2015-09-07
tags:
  - learning
layout: layouts/post.njk
---

A week ago [I shared a few highlights and my impressions](http://nicksimson.com/everyday-developers/) from a recent Web Ahead discussion about "everyday developers". I made the point that web development is not a monolith: There are a lot of different kinds of websites, there are a ton of different tools and ways to deploy a site, and noone should be expected to know everything.

I wanted to write a follow-up entry with more details about the learning path toward becoming a web designer or developer, and I had a beginner in mind as I started drafting this post. It can be difficult to know where to start learning. It can be diffciult to figure out what to learn next. This isn't a prescriptive or definitive career guide, just what I think the core compenties are, other skills that can come in handy, and the best order to learn them in. I will not recommend any specific frameworks, software, or tools, save for two books and a handful of reference websites.

The definition of "everyday developer" I am working with is someone who writes <strong>front-end code</strong>&mdash;that is, HTML, CSS, Javascript&mdash;to create websites for clients, either as a freelancer or an employee on a small team. I am not referring to game developers, other application platform developers, back-end programmer, or engineer wirking on a huge web product (like Facebook or Netflix). This definition also excludes industry experts and conference speakers. There may be some overlap in these worlds, but I have a web developer focused on content-based sites in mind. As I use the terms "everyday developer" , "web designer", or "front-end developer" in this post, this is who I am referring to.

## Learning How to Learn

There are two things required to pick up new skills: an awareness of the thing you want/need to learn, and the motivation to do the work necessary to learn the new thing. Proficiency is gained through practice and repetition of the new skills, and tackling harder problems. Mastery is achieved by developing an awareness of what you need to learn next, and repeating this process.

There are lots of references guides and lessons available for learning web technologies, and what you use will depend on how you learn best. My preference has always been with reading, and I usually prefer books over screencasts and videos. I have picked up new things quickly with both [Treehouse](http://teamtreehouse.com) and [Lynda.com](http://lynda.com), but I like to have a good reference book handy.

If you are only going to buy one book to learn basic web development, I recommend <a href=" http://www.learningwebdesign.com/"><em>Learning Web Design</em>, by Jennifer Robbins</a>. It is 600 pages and $50. Its a textbook, so its updated often, and was designed with web design classes taught at community colleges and universities in mind. You can find many high-quality short books for cheaper, but I find they often only cover a small amount or a very specific area in what is a multidisciplinary world. A lot of the smaller books are written for intermediate, or everyday developers, so they may quickly cover or review some basic concepts, but not at the broad, introductory level you need to understand now.

The world of web development changes often, so sometimes there are things so new, the book hasn't been written on it yet. This is where I turn to blog posts. I rely on a few trusted sources: [Sitepoint](http://www.sitepoint.com/), [A List Apart](http://alistapart.com), and [Smashing Magazine](http://smashingmagazine.com). These are popular sources, but reliable. Their business models focus on quality over quantity. All three websites compensate their writers and hire technical editors.

<strong>A note about tutorials:</strong> I think its OK to start with one or two tutorials if everything feels foreign to you, but you are going to learn better and be more invested if it can be adapted into a real project you find interesting or rewarding. Again, its about the motivation to learn new things. This is how I use tutorials today.

Finally, just as a web developer can't be expected to everything, you don't need to learn everything at once. I'll try to highlight what I think are the most important things to learn and pick up on the way to becoming an everyday developer.

## Core Competencies

With so much room for specialization, the professional developer should be primarily fluent in the three front-end technologies the end user will interact with: HTML, CSS, and Javascript. Start with these. In that order. The most effective method I've found is to use a lesson that requires you to write the HTML markup first, create a layout and aesthetic layer on top with CSS, and add a little basic interaction with simple Javascript or customizing variables in a jQuery plugin. This is the foundation for everything else.

You don't need to know every part of the spec to start using HTML. I use this screenshot from a [Don't Fear the Internet video](http://www.dontfeartheinternet.com/02-html/) to show others which HTML tags they actually need to know to begin structuring web documents:

<figure>
<a href="http://www.dontfeartheinternet.com/02-html/">
<img src="/images/post-images/2015-09-07-dont-fear.png" alt="Screenshot of all html tags with a few highlighted" /></a>
<figcaption>
Screencapture of video content &copy; Jessica Hische &amp; Russ Maschmeyer</figcaption>
</figure>

I think CSS can be a fun language for people approaching it from graphic design and a frustrating one for people approaching it from programming. I would recommend the [CSS-Tricks Almanac](https://css-tricks.com/almanac/) and the [Sitepoint CSS reference](http://reference.sitepoint.com/css) for people new to CSS

Next, learn how to deploy a website. It really doesn’t matter if its FTP, command-line, a hosted CMS or a Dropbox folder. There are so many ways to deploy a website, and her I would just recommend reading the instructions, following them carefully, and if you still don’t understand, pick a different method.

As you are learning HTML, CSS, and Javascript and deploying your files to the server, two important concepts to pick up on are accessibility and progressive enhancement. A lot of web designers are not familiar with these terms but already practice them in their development process.

## Accessibility

Accessibility is not just designing for people with disabilities. Many of the following practices will make your products more universally usable and may even improve your search engine optimization.

The HTML spec already has so much accessibility baked into it. As long as you are already writing structured, semantic HTML and providing textual alternatives for non-text content, you're on your way there. The easiest things to mess up accessibility-wise in HTML are probably the <code>form</code>, <code>button</code>, and <code>input</code> tags. Read up on the ARIA roles, and keep the [Accessibility Project](http://a11yproject.com/checklist.html) open in your browser tabs for reference when working on your projects.

In CSS, you can't specify alt text, so make sure you are only using the <code>background-image</code> property for decoration, not contextual images with meaning. Read up on colorblindness, and install an app or browser add-on that simulates different types of colorblindness and low-vision conditions so you are providing the best possible viewing experience in your design decisions.

If you are including interactive content, multimedia, animation or visualizations, try to use a library that supports multiple inputs: touchscreens, mouse, and keyboard. Don't use autoplaying audio, video, or slideshows without start and stop controls. If you have complex site navigation, consider adding 'skip to main content' or 'skip to navigation' links near the top of your HTML document

Accessibility is more of a mindset that a handful of techniques. Learn how others navigate the web. Try to step inside their shoes. If you have a phone or tablet with accessibility features and a web browser, try turning these on and attempt to navigate the web by voice only, or with your eyes shut. If you want to go deeper, install the free NVDA-JAWS reader and learn how to navigate the web with it.

## Progressive Enhancement

Progressive enhancement is about delivering a user experience free of technological restrictions. There are a variety of devices, browsers and technologies all hitting the same website. Not all are in ideal conditions, and very few scenarios match the exact environment in which it was developed. The website does not need to look the same in each browser, but the basic experience (connection is made, text content is displayed) is consistent. If the technology fails to render the javascript or CSS, can a user still interact with the content?

The other part of enhancement is delivering appropriate fallbacks for features not supported by every technology. Its not about making the website look the same in each browser, but making sure the content and information are readable and accessible, and the experience is consistent to what the user is accustomed to seeing. This concept is the key to fault tolerance and longevity on the web.

## Other Technical Skills

Once you know your HTML, CSS and Javascript, and can get these files to your server, what should you learn next? I would suggest Git or some command line stuff or a template language. Git is a version control for software development (a little like track changes in Microsoft Word), that a lot of teams and open source projects use.

To be a good, useful generalist, it is important to have a thorough understanding of the fundamentals, followed by a surface level understanding of most things related to the role. Again, the goal is not to know everything. All of the following are useful for everyday developers to be aware of, and also represent potential paths toward specialization:

I wrote last week that the content management system is still the bread-and-butter of the everyday developer. Which ones you learn and how deep you go depends on what you want to get out of it, who you want to work for, and how much more you are willing to learn. I won't offer much advice here except pick something popular, well-documented and widely supported, and your life will be easier. The [CMS Chronicles](https://mijingo.com/podcast/) mini-podcast might help if you are trying to find a good fit.

I don’t think an everyday developer needs to become a database expert. Not every website needs a complex database structure or server-side technology. Static sites are becoming very popular for a good reason: they are quick to build and deploy, cheaper to host, and often more performant for the end user. A working knowledge of the basics is helpful, but if you are just starting out or only interested in working on the front-end, this is probably not something you need to focus on today.

If you are interested in learning databases, server side stuff and more programmatic languages, this is where my advice would be “Follow the Money”. Survey the landscape, and pick something that is also a good fit for you. Python and Ruby are both still pretty big right now. Perl not so much, and everyone hates on PHP, although it is still relevant today. Everything will be different in 5-10 years, so try to find a language with a lot of users and companies behind it. If there are new technologies emerging from the corner of the web world you find yourself in (like Twig for PHP, Sass for CSS, etc,), pay attention to those, and jump aboard once they really take off.

Finally, keep paying attention to HTML, CSS and Javascript. These technologies are not static and new browser versions are shipping new features you can start taking advantage of. Because browser support is really good, the next thing I'm planning to sit down and learn is Flexbox.

## Job titles and job hunting

One of the lessons you will learn early on as an everyday developer is that there is no standardization in what people call themselves. "Web designer", "front-end developer", "UX designer", "interaction designers", could all be the same person. I prefer to keep it simple and say "web designer". Because I do print work too, sometimes its "communication designer." This is good enough an answer for the "what do you do?" question at dinner parties.

If I were job hunting, the best advice would be to use whatever is the job title advertised. But look out for red flags in position descriptions: <em>"5+ years of React.js experience"</em> is terrible, because React has only been out for two years. Confusing Java with Javascript is probably the result of a non-technical person attempting to write a technical job description. I've found that the better jobs advertised aren't super prescriptive for every little technical thing. They know that new things are going to come along, and are probably more interested in <em>how</em> you work, than every tiny thing you are aware of.

## People Skills

Becoming an everyday developer means working with clients and other people. Good communication skills are a requirement. Practice your interviewing and presentation skills. When you are getting the project specs from a client, you are like a researcher or journalist, not an interrogator. When you are [showing work for sign-off and approval](https://medium.com/@monteiro/13-ways-designers-screw-up-client-presentations-51aaee11e28c), think of it as a sales presentation. You don't need to be Don Draper or Billy Mays. Focus on the goals and the pain points you are solving. You are selling it, but you are not defending it in court, and you are not a tour guide.

Learn how to be a good listener. Learn how to be a [great co-worker](http://www.slideshare.net/JennLukas/a-guide-to-49840642). Empathize with your clients. Have as much or more empathy for their customers. Ego management is a [core design skill](https://deardesignstudent.com/we-re-all-imposters-95d6aef8053f). Megan Hustad's <em>[How to Be Useful](https://www.goodreads.com/book/show/2993383-how-to-be-useful)</em> is a great read if you are more than a little skeptical/cynical about anything in the "business book" or "self-help" section of the bookstore. At the end of the day, remember, its a job.

Also, the technology industry is rotten with misogyny, racism, and entitlement; don't be one of those jerks. Call out this BS when you see it. Always remember this: you aren't designing things for screens, you are designing for humans.

## Further Reading:

- Chris Ferdinandi, <em>[Wicked Fast Websites](http://gomakethings.com/downloads/wicked-fast-websites-ebook/wicked-fast-websites.pdf)</em>
- Stephen Hay, <em><a href="http://www.the-haystack.com/2015/07/03/my-name-is-stephen-and-im-a-generalist/">My name is Stephen and I'm a generalist</a></em>
- David Kadavy, [How to Learn Web Design](http://designforhackers.com/blog/how-to-learn-web-design/)
- Erik Runyon, [Lessons learned from my first semester of teaching](http://erikrunyon.com/2014/01/lessons-learned-from-my-first-semester-of-teaching/)
- Kylie Timpani, [Dear Developer. Love, Designer.](https://humaan.com/blog/dear-developer-love-designer/)
- The Web Ahead, ep. 101: [Structuring Content with Eileen Webb](http://thewebahead.net/101)
