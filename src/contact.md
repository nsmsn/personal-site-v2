---
layout: layouts/page.njk
title: Get in touch
description: I would love to hear from you. Use this simple form to contact me.
templateClass: tmpl-page
permalink: /contact/
---

Are you interested in working together on a short-term project? Or perhaps you have a question about me or my work?

I would love to hear from you. Email me at [nick@nicksimson.com](mailto:nick@nicksimson.com) or use this simple form to contact me.

&nbsp;

<form name="contact" method="POST" data-netlify="true" class="flow">
  <p>
    <label>Your Name: <input type="text" name="name" /></label>
  </p>
  <p>
    <label>Your Email: <input type="email" name="email" /></label>
  </p>
  <p>
    <label>Message: <textarea name="message"></textarea></label>
  </p>
  <p>
    <button type="submit">Send</button>
  </p>
</form>
