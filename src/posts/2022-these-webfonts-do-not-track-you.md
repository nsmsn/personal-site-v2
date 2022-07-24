---
title: These webfonts do not track you
description: Self-hosting web typography for privacy and performance enhancements.
date: 2022-07-03T01:08:13Z
tags:
  - redesign
layout: layouts/post.njk
---

For a while I have proudly displayed the following statement on my about page:

<blockquote>
<strong>This website does not track you.</strong> There are no third-party cookies here, and your data isn’t collected when using this site.
</blockquote>

As of this writing, I can feel more confident in this statement: [I switched from using the Google Fonts API](https://github.com/nsmsn/nicksimsondotcom/commit/38d338c633451909fbbbdfd8437084fb15158a1c#diff-f934e43e0f8ddbcd51317189e847c41f190ec983462fc3bd7169b8d7f1a99cf6) to hosting my font files on this domain.

While I was catching up on some recent WordPress news, I learned that the themes team is now [recommending WordPress theme authors to bundle Google fonts](https://make.wordpress.org/themes/2022/06/18/complying-with-gdpr-when-using-google-fonts/) with the theme files. The impetus for this announcement was a German court ruling (earlier this year) that [Google-hosted webfonts violate Europe's General Data Protection Regulation (GDPR)](https://wptavern.com/german-court-fines-website-owner-for-violating-the-gdpr-by-using-google-hosted-fonts). 

What it comes down to is that a person’s IP address can be exposed to Google just by them browsing a website using fonts hosted on Google’s CDN. On my personal website, I do not have a privacy policy more explicit than “I don’t want you to be tracked”&mdash;I want this site to comply with GDPR, the California Consumer Privacy Act, and any and all other present and future data privacy laws, regardless of where my visitors live. 

The Google fonts issue was news to me, but not surprising. Here’s why I did not know about it: I use the [Ghostery browser extension](https://www.ghostery.com/) for most of my web browsing and was relying on what that tool was reporting back to me. While Ghostery detects and blocks Google Analytics’ tracking scripts in everyday browsing, they apparently are unable to detect what a CDN could be collecting from you. And in addition to making your web browsing a little less pretty, blocking web fonts from rendering could also make entire web pages unusable if the web developer does not employ a [font-loading strategy](https://www.zachleat.com/web/comprehensive-webfonts/) or select appropriate fallbacks.

Google can of course make this easier on everyone by not collecting the IP address of everyone who accesses fonts from their CDN, but they also make their font library (each typeface in the collection is open-source) easily available for download. So I initially followed [Chris Ferdinandi’s instructions and advice](https://gomakethings.com/how-to-self-host-google-fonts/) to use the [Google Webfonts Helper app](https://google-webfonts-helper.herokuapp.com/fonts/) to download the font files needed on my website.

What Google’s own download feature  and the webfonts helper app won’t give you (as of this writing, Summer 2022) is the variable font files. This is a bit disappointing, since Google seems to have the best support for variable fonts, of all the typography services out there. [Variable fonts](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Fonts/Variable_Fonts_Guide) are a relatively new technology that enables many different variations of a typeface to be incorporated into a single file, rather than having a separate font file for every width, weight, or style. A big reason why [I went with Google fonts with my redesign](posts/2020-redesign-webfonts-html/) was that I wanted to try out variable fonts on a production project. 

If you want to try hosting your own variable fonts from Google’s service, [Bernard Nijenhuis has an excellent post with some technical instructions](https://bnijenhuis.nl/notes/2021-04-13-how-to-add-self-hosted-variable-fonts-to-your-website). Henry Desroches has an even more [technical tutorial on converting a variable TTF font file to WOFF2 format](https://henry.codes/writing/how-to-convert-variable-ttf-font-files-to-woff2/). I did not need to refer to Henry's instructions. My two variable families are [Epilogue](https://www.etceteratype.co/epilogue) and [Literata](https://www.type-together.com/literata-3), whose foundries have already made variable font file downloads available. From another [open source project by Jason Pamental](https://github.com/jpamental/letter-from-birmingham-jail), I found a subsetted version of Literata that is a bit smaller in size from the files downloaded from TypeTogether's website.

## Alternatives to Google Fonts

If you like using Google’s API, but want a more GDPR-friendly CDN for font delivery, you could also try [fonts.bunny.net](https://fonts.bunny.net/). Bunny Fonts bills itself as a “drop-in replacement for Google Fonts”:

<blockquote class="flow">
<p>The Bunny Fonts API was designed to be fully compatible with the Google Fonts CSS v1 API, making the switch as easy as changing the hostname.</p>

<p>Simply swap <code>"https://fonts.bunny.net/css"</code> in place of <code>"https://fonts.googleapis.com/css"</code> on your website's source code and let your users enjoy better privacy.</p>
</blockquote>

The caveat to using Bunny Fonts is that you may not be able to use the variable versions of the Google Fonts library, at least at the time of this writing.

If you are looking to self-host variable fonts, many of the best designed variable fonts on Google fonts are available to download on [Fontshare](https://www.fontshare.com/), by the Indian Type Foundry (ITF). In addition to open source designs like [Literata](https://www.fontshare.com/fonts/literata) and [Epilogue](https://www.fontshare.com/fonts/epilogue), there are many “closed source” designs by ITF that you can also use under a free license. I’m particularly drawn to [Satoshi](https://www.fontshare.com/fonts/satoshi), [Zodiak](https://www.fontshare.com/fonts/zodiak), and [General Sans](https://www.fontshare.com/fonts/general-sans).


## Performance Considerations
The <code>@font-face</code> declaration in CSS is not new technology&mdash;it was introduced in 1998. Browser support and font file specifications, however, varied a bit for at least a decade. Frankly, [it was a tangled mess until 2009](https://thehistoryoftheweb.com/web-fonts/), when font hosting services like Typekit emerged to take the technical complexity out of web designers’ hands and make licensing simpler for the foundries producing type families. After studying typography in a traditional graphic design program in the mid-to-late 2000s, I was really excited to start designing for the web again when Typekit (now [Adobe Fonts](https://fonts.adobe.com) came out, having access to a range of expressive and well-designed typefaces.

Even with wide browser support for <code>@font-face</code>, it took years for browsers to implement a standard webfont file format: Files with <code>.eot</code> extensions were used for Internet Explorer versions before IE 10; Safari, Android and iOS used <code>.ttf</code> files; the oldest versions of iOS that supported webfonts used <code>.svg</code> format. Services like Typekit and Google Fonts supported all these web font versions and let you connect to a CSS or Javascript file to make sure the right file reached your audience’s browsers.

In a technical post, [Barry Pollard breaks down the many performance benefits](https://www.tunetheweb.com/blog/should-you-self-host-google-fonts/) of self-hosting Google fonts. Nowadays, modern browsers all support the <code>.woff</code> format, and better compression is available with <code>.woff2</code>. With less complexity in file types and HTTP/2 available on web servers you *might not* need a CDN, or experience performance benefits from hosting assets on a CDN. 

I have not completely given up on Google. I am using their [page speed insights tool](https://pagespeed.web.dev/) to figure out how I can continue to optimize my site for performance, while still displaying great typography. With [Internet Explorer officially sunsetted this summer](https://docs.microsoft.com/en-us/lifecycle/announcements/internet-explorer-11-end-of-support), I think I may be able to drop <code>.woff</code> [version 1] support and only host <code>.woff2</code> files. It’s a tricky balance since I’m not using analytics to find out which browsers are viewing my site. But I am already using <code>font-display: swap;</code> as my font loading strategy and treating the fonts themselves as progressive enhancement may be the way to go, at least for me personally. Almost 30 years later, [Matthew Carter’s Georgia](https://en.wikipedia.org/wiki/Georgia_(typeface)) is still a great design, and very legible.

I am currently exploring repos of various developers I look up to, to see how they are delivering their webfonts, variable and otherwise. If you have ideas for improving my web font performance, you can <a href="mailto:nick@nicksimson.com">email me</a> about this. I’d love to hear how you are implementing self-hosted and variable typography.