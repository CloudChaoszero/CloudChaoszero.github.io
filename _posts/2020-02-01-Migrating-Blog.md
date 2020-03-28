---

firstPublishedAt: 2020-02-01
title: Why I Upgraded my Website from HTML -> Jekyll  
tag: Coding
author_profile: true 
toc: true
mathjax: true
---

My initial blog started off with several considerations as a website. Should I create a website? If I create the website, how much would I have to pay for a yearly subscription? Is it worth it? What about free solutions?
> I tried it out, and it didn't work out. I was broke in early 2016-2017, and had to save money

So, I decided to use Github Pages to start my website, for my career portfolio primarlily. And from looking how to create it, [I followed a HTML template to start off the website](https://github.com/CloudChaoszero/CloudChaoszero.github.io/commit/fd260b954b7a948aa7385b829be4829b5b785c40)

>  In the long run, hindered my ability to manage and add content, mentioned in this article

 However, I also wanted to publish articles. And the setup for my first core-website was HTML & CSS updates. It was great learning and working with HTML, CSS, and further modifications of that website. However, adding simple blogs through HTML was **a headache**. 
 
So, after re-visiting considerations on creating a free website with the functionality and development I needed, I went with 
[Minimal Mistakes Jekyll Framework](https://mmistakes.github.io/minimal-mistakes/) created by [Michael Rose](https://github.com/mmistakes). (You can support [him here on Paypal](https://www.paypal.com/paypalme2/mmistakes)).
# Reasons Why I: Migrated my Blog

## 1. Writing Content is everywhere

In 2016-2017, I started to slowly post my content on Medium. The usability and accessibility provided by the website was amazing. Medium was my primary location for posting content, and referencing it.

> I didn't have developer experience, and wanted to create a website

But after a few years of dealing with updates to the platform and also wanting to do a bit more, I became more familiar with other methods to post content for the following cases:

* **Professional**: LinkedIn Articles

* **Scientific/Analysis**: Publishing Markdown or Jupyter Notebooks on Github
* **Personal**: Exposing Portfolio (Website)


As I grew to knowing more methods to place my content, I understood that managing multiple copies, where Medium as the base to post first, and post on other forums thereafter was a bit...cumbersome.

For example, I had to:

Post on Medium $$\rightarrow$$ Copy and Paste to LinkedIn Article
$$\rightarrow$$ Convert article to HTML file to publish on website

This was a hassle, and all of that should not have to be done in 2020, provided recent updates in the digital writing space.

Lastly,
> "I wanted to centralize and improve the User and Developer Experience (UX)"

## 2. Medium isn't what it used to be; \#Paywalls

I want to shifting away from a "pay to read" model to provide access to everyone.

Plus, **paywalls** are a b...locker.

### Case #1

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">An aside: when I went to publish this, I realized that I didn&#39;t know where to anymore. <a href="https://twitter.com/Medium?ref_src=twsrc%5Etfw">@Medium</a> is behind an intolerable paywall &amp; I don&#39;t have a personal blog anymore (RIP <a href="https://t.co/fYFxRIzF1l">https://t.co/fYFxRIzF1l</a>). My company &amp; community blogs aren&#39;t right for this. So <a href="https://twitter.com/LinkedIn?ref_src=twsrc%5Etfw">@Linkedin</a> it was! Weird...</p>&mdash; Chris Anderson (@chr1sa) <a href="https://twitter.com/chr1sa/status/1229205246859104256?ref_src=twsrc%5Etfw">February 17, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### Case #2
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">If you ever get hit by the Medium paywall limit. Open the same link in an incognito tab and it&#39;ll work just fine. <br><br>Medium will have to keep the content accessible to logged out users for SEO reasons <a href="https://t.co/OPxaNOdOti">pic.twitter.com/OPxaNOdOti</a></p>&mdash; Abdellatif Abdelfattah (@Abdella6if) <a href="https://twitter.com/Abdella6if/status/1230158923455442944?ref_src=twsrc%5Etfw">February 19, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


The Analogy:
> It's like trying to read a New York Times article...you just give up after the paywall pop-up ;(



# Reasons Why I: Overhauled my Website to Jekyll Framework

Here, I talk about why I explicitly overhauled my website from HTML based-framework to a solution like [Jekyll](https://jekyllrb.com/), on [Github Pages](https://pages.github.com/).

## 1. Disparate Content in One Location

In the past, I had to share the following: [Medium](https://medium.com/@CloudChaoszero), [Linkedin](https://www.linkedin.com/in/raulm8/), [Github](https://github.com/CloudChaoszero), and [my website](https://raulingaverage.dev/)

To a reader interested in my published content or portfolio, I wanted to provide them a better experience, meanwhile minimizing friction of user experience of navigation, environment, and content. 

So, I can now have users go to at least raulingaverage.dev, and if they need to go to other locations, they can, as an "option" rather than a requirement to see the content

(e.g. You are interested in my portfolio, but don't want to click to [Linkedin](https://www.linkedin.com/in/raulm8/),. Well, in the [same site](https://raulingaverage.dev/), there is a [About](https://raulingaverage.dev/home) and [Accomplishments](https://raulingaverage.dev/accomplishments/main) tab for that)

> Reader: [🎵Send me your location🎵](https://www.youtube.com/watch?v=by3yRdlQvzs)

## 2. Visibility

### Searchability

With the move to Minimal Mistakes, I am not able to have better searchability from Search Engines, compared to my recent HTML based website, with the lack of functionality.

Moreover, I now have the functionality to gauge how to either optimize my content or searchability with a straight-forward implementation of a Google Ads ID, and not have to manage Google Analytics of users going to different places to in my website

### Portfolio visibility

With content added over time, I am able to expose my portfolio for parties of interest in such content as well (future employers). Again, this also provides a wonderful UX experience of navigating and exposing different skillsets in a seamless process, without having to serve several links for different aspects of my craft

> In a sea of content, it's challenging to see your target

## 3. Functionality

### Embedd Analysis documentation (Notebooks)

Can I convert a notebook of code and analysis into a static webpage? Yes, however, it is cumbersome to manage in HTML. How about converting it into a Markdown file? Well, [luckily we can do either](https://mikkelhartmann.dk/2019/05/14/static-website-from-jupyter-notebooks.html)

### Scientific Notation & Formulas (markdown language)

I can easily add formulas through markdown files with Jekyll's accessibility to support the syntax

#### Example: [Euclidean Distance formula](https://en.wikipedia.org/wiki/Euclidean_distance)

(in proper proper notation!)

Say we have a 2-dimensional graph with points a=$$(x_1,y_1)$$ and point b= $$(x_2,y_2)$$. 

The distance between the two are calculated as such
$$d(a,b) = d((x_1,y_1),(x_2,y_2)) =\sqrt{(x_1-x_2)^2 + (y_1-y_2)^2}$$

Wow, that looks better than plain-text. :D 

### Writing is just as easy as using markdown

Visually, here is how I am writing the content

![Markdown Example](https://d33wubrfki0l68.cloudfront.net/e3541891e3115642d605aca52e4556d397e95c6f/4e2ba/images/quicktourexample.png)

That is more human readable than both coding & managing in...html.

## 4. Hella HTML


I loved working with HTML, and still preserving the skill. However, for small edits and maintaing code readability

![HTML example](https://kinsta.com/wp-content/uploads/2018/04/wordpress-html-1.png)

> I couldn't stand the hours of long edits, lack of functionality, just the whole uncessary front-end development.

Therefore, I looked into finding a way to remove all of the friction of development and the readers--that's where I started to re-consider using Jekyll. Looking into the documentation, and now having a better grasp on development, I knew this overhall would be straigh-forward, and oh--oh so worth it.

Again, S/O to [Minimal Mistakes Jekyll framework](https://mmistakes.github.io/minimal-mistakes/) created by [Michael Rose](https://github.com/mmistakes). (You can support [him here on Paypal](https://www.paypal.com/paypalme2/mmistakes)).

>  Without this open source development, I would still be stuck in my pre-existing predicament. 
 
# Conclusions

With all of this, I allow myself to start in a new chapter of creating writings, and look forward to helping others--for the long-run. :)

If you have any questions of critical feedback on my implementation, feel [free to reach out at LinkedIn](https://www.linkedin.com/in/raulm8/).

Cheers!