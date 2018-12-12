---
layout: page
title: Contact
permalink: /contact/
description: I care about my readers' opinions. Please leave a note or just say hello.
---

### Write to me
I care about my readers' opinions. Please leave a note or just say hello.

<form class="wj-contact rev" action="https://formspree.io/{{site.email}}" method="POST">
    <input type="email" name="email" placeholder="Email Address" class="input shadow">
    <textarea type="text" name="content" rows="10" placeholder="Message" class="input shadow"></textarea>
    <input type="hidden" name="_next" value="{{site.url}}{{page.url}}">
    <input type="hidden" name="_subject" value="New Contact Form Submission">
    <input type="text" name="_gotcha" style="display:none">
    <input class="cards btn" type="submit" value="Submit">
</form>

<p></p>

{% highlight html %}

This form starts working once you update your email in configuration. Delete this line in the contact page found in the path _pages/contact.md

{% endhighlight %}