---
title:  "Meta Tag Draft"
description: Work in progress
## date: add a date when publishing
---

<h1>What Are Meta Tags?</h1>
Meta tags are HTML elements whose attributes and values construe the significance and purpose of your website when interpreted or utilized by a data-driven web service. 

Meta tags allow other places on the web that may be displaying information about your website to know how to list and describe it. In particular, Google search results utilize your meta tags when listing your website in a search query. There is a reasonable amount of different meta tags but for the purposes of this article, we'll focus on the ones that affect Google and social media sites. Let's start by analyzing a bit of HTML from the Modiphius Games home page.

<h1>Title and Description Properties</h1>
First off are the __title__ element and __description__ meta tag.

```html
<title>Modiphius - GAMES </title>

<meta name="description" content="The British games publisher of Achtung! Cthulhu and other roleplaying games, novels and merchandise" />
```

These are pretty self-explanatory. These are what Google will be used to display the Modiphius main page in a search query. So They'll appear like this:

[Meta Tag Results](/assets/images/Modphius.jpg)

Now technically the <title> tag is not an official meta tag but it definitely works alongside them. Obviously, this is the title of the web page you're on. Google will use the meta tag with the title attribute if it's there and the page's title tag if it is not. Here's a meta tag with the title property.

```html
<meta property="title" content="Modiphius" />
```

The title and description are important because they are that first point of contact for a potential customer searching on Google. It might just be the first description someone sees of you. You have a good 100-150 characters to describe yourself here. Google doesn't have an official limit to the number of characters that can be in a description, but it will decide how much of your description it will display based on of its many mysterious relevancy algorithms. If you want a long description I'd suggest getting a base on in at under 120 characters and then dropping another 120 characters that expand on that description. Then at least the first half will display even if the second half does not.

<h1>Open Graph Meta Tags</h1>
If you look at the source on the Modiphius home page you'll see some similar meta tags that look like this:

```html
<meta property="og:title" content="Modiphius" />

<meta property="og:description" content="The British games publisher of Achtung! Cthulhu and other roleplaying games, novels and merchandise" />
```

These are meta tags with the __title__ and __description__ properties again only the "og:" in front of them stands for __Open Graph__ and that means these tags will be used by social media services like Twitter or Facebook to create a feed snippet when the webpage is shared on their service. If I share your page on Twitter then this title and description are what will appear. We can set other things to appear as well with the following extra meta tags:

```html
<meta property="og:image" content="https://www.modiphius.com/uploads/1/4/0/6/14062642/2635870_orig.png" />

<meta property="og:url" content="https://www.modiphius.com/" />
```

These control the image and URL that will appear as part of the feed snippet. If you examine the source once again you'll see the Modiphius web designer has placed quite a few image meta tags in there. Each of these can be used by a different service based on their size. If you want to go the easy route and research all the different sizes later the best thing to do is to create an image whose dimensions are roughly 1200x630 pixels. Currently, these images can be up to 5MB in size but I honestly would make it as light as possible. Under 120KB would be ideal. Once this is set (and it can be different for every page if your CMS allows it) then this image will appear any time someone shares that page on their social media feed. 

The "og:url" property designates the URL you want to be scraped for the feed snippet. Whatever URL you put here is what is going to be shown in the posting. Even if it's different from the actual page being shared. The link, in most cases, will still go to the page you're sharing. So, for example, if I shared this page on my Twitter feed it would look a lot like this:

[This page shared on Twitter](assets/images/sharedpage.jpg)

The link in my feed will go to the page but fantasyrobotfighter.com is what appears in the post. Facebook may do this differently, I'm not certain, but a quick and easy test is all you need to do to find out.

<h1>The Thing About Keywords</h1>
Keywords do matter but not here and not in meta tags. Everyone still puts them in there but Google straight up skips them. Back in the day businesses would abuse keywords but putting anything and everything in there and they quickly became useless. People still use them but my advice is to not waste your time. First, because it's possible, though only rumored, that using meta tag keywords can actually do a bit of harm. It's unlikely but why waste time doing something pointless that has a minor chance of working against you? Second, and this one is more applicable if a competitor checks out your web page's source and can see all the keywords your targeting then you're revealing a small piece of your marketing strategy. It may sound silly, but keywords are useful, just not in meta tags, and if you're trying to optimize for certain words or phrases then maybe don't let the competition know exactly which ones. Here is Modiphius' meta tag for keywords:

```html
<meta name="keywords" content="Call of Cthulhu, Savage Worlds, Sci-Fi, Horror, Trail of Cthulhu, HP Lovecraft, Achtung! Cthulhu, Cthulhu, WW2, WWII, World War 2, Secret War, Nazi Antarctic Base" />
```

<h1> The More The Meta</h1>
Finally, the last meta tag I want to touch on is the one that handles the __charset__ property. This designates which character set your page is using. "utf-8" is pretty much the standard and if you're using a CMS to build your website then it's probably automatically added. It looks like this:

```html
<meta charset="utf-8" />
```

There are a lot of different meta tag properties out there for a variety of uses. The ones I covered here are just to get you started and maybe shed some light on how they work. The great thing is that they are all fairly straight forward and easy to learn and try. You can find a nice comprehensive guide to there at [ogp.me](http://ogp.me/).

[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com
