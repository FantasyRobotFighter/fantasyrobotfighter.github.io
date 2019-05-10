---
title:  "SEO for Indie Game Designers - Part 2 - Meta Tag Basics"
date:   2019-05-09 10:18:00
description: Take advantage of how Google and social media services display your website with meta tags.
---

<h1>What Are Meta Tags?</h1>
Meta tags are HTML elements whose attributes and values construe the significance and purpose of your website when interpreted by a web service. 

Meta tags allow other places on the web that may be displaying information about your website to know how to list and describe it. In particular, Google search results utilize your meta tags when listing your website in a search query. There are a quite a few meta tags that can be added to your website but for the purposes of this blog post, we'll focus on the main ones that affect your appearance in Google search results and on social media. Let's start by analyzing a bit of HTML from the Modiphius Games home page.

<h1>Title and Description Properties</h1>
For reference purposes, I thought [Modiphius Games](https://www.modiphius.com) had a nice chunk of meta tags one could wade through and learn from. You can see what they are by doing a "view source" on their main page. I've pulled a handful out for us to examine. We'll take a look at the __title__ element and __description__ meta tags first.

```html
<title>Modiphius - GAMES </title>

<meta name="description" content="The British games publisher of Achtung! Cthulhu and other roleplaying games, novels and merchandise" />
```

These are pretty self-explanatory and these are what Google uses to display a description of the Modiphius main page in a search snippet on a query page. So These will translate over to look like this:

[Meta Tag Results](/assets/images/ModiphiusResult.jpg)

Now technically the <title> element doesn't really look like a meta tag but it definitely works like one. Obviously, this is the title of the web page you're on, but it's a little more than that and it's important to know that titles should not be taken for granted. Google has a [lot to say](https://support.google.com/webmasters/answer/35624?hl=en) about how they're used and the best way to write them. You want every page of your site to include the <title> element and each should be specific to that page. Don't duplicate the same title on every page. The best way to write one is to have your brand name and then maybe a short couple word blurb describing what you are. Don't go all out, save that for your description meta tag and if you're not sure just starting by putting your brand name like Modiphius does.

```html
<title>Modiphius - GAMES </title>
```

Or maybe you have an OSR review blog. Something like this would work on your main page:

```html
<title>Captain Bob's OSR Review Blog</title>
```

Google and web clients will also use the meta tag with the title property. Here's an example of a meta tag with the __title__ property, but it's not a replacement for the <title> html element. You should always include the <title> to have valid HTML. The best practice is to have both. Here is the __title__ meta tag Modiphius uses along with their <title> element.

```html
<meta property="title" content="Modiphius" />
```
See how Midiphius removes the "- GAMES" for this one. The important thing here is just get your brand across. So, in Bob's case maybe he can just get away with putting:

```html
<meta property="title" content="Captain Bob's" />
```
Duplicating the <title> tag doesn't hurt either.

The __title__ and __description__ become that first point of contact for a potential customer searching Google for you or your products. It's potentially the first description of your business a customer will see and read. So you want to connect with them. Google allows a good 100-150 characters to describe yourself with a __description__ meta tag. It's not that Google has an official limit to the number of characters that can be in a __description__, but it will decide how much of your description to display based on of its many magical relevancy algorithms. This means a really long __description__ can be cut off prematurely. If you feel you need a long description then a general rule-of-thumb is to get a base description in at under 120 characters and then write in another 100-150 characters that expand on that description for a total of 240 characters. Then at least the first half may fully display even if the second half does not. The goal is to grab a searcher's attention in a way that's relevant to your website. 

<h1>Open Graph Meta Tags</h1>
If you look at the source on the Modiphius home page you'll see some meta tags similar to __title__ and __description__ that look like this:

```html
<meta property="og:title" content="Modiphius" />

<meta property="og:description" content="The British games publisher of Achtung! Cthulhu and other roleplaying games, novels and merchandise" />
```

These are meta tags with the __title__ and __description__ properties again only with an __og:__ in front of them. "OG" stands for __Open Graph__ and that means these tags will be used by social media services like Twitter or Facebook to create a snippet when the webpage is shared within a customer's social media feed. If I share your page on Twitter then these __og:title__ and __og:description__ meta tags are what will be used to build it. There are other things we would want to appear as well, not just a __title__ and description__.  We would also want an __image__ and a __URL__.

```html
<meta property="og:image" content="https://www.modiphius.com/uploads/1/4/0/6/14062642/2635870_orig.png" />

<meta property="og:url" content="https://www.modiphius.com/" />
```

These meta tags control the __image__ and __URL__ that will appear along with the __title__ and __description__ within the customer's feed when they share your page. If you examine the source of the Modiphius home page once again you'll see their web designer has placed quite a few image meta tags in there. Each of these can be used by a different service based on their size. Including, how a bookmarked page might look if dropped onto the screen of a smartphone. If you want to go the easy route and research all the different sizes later the best thing to do is to create an image whose dimensions are roughly 1200x630 pixels. Currently, these images can be up to 5MB in size but I honestly would make it as light as possible. No larger than 120KB would be ideal. Once this is set (and it can be different for every page if your CMS allows it) then this image will appear any time someone shares your page on their social media feed. 

The __og:url__ property designates the URL you want to be shown in the post even if it's different from the actual page being shared. So, for example, if I shared this page on my Twitter feed it would look a lot like this:

[This page shared on Twitter](assets/images/SharedPage.jpg)

The link in my feed will go to the page but fantasyrobotfighter.com is what appears in the post. It just tells whoever is clicking on it where they're going. Facebook may do this differently, I'm not certain, but a quick and easy test is all you need to do to find out (I'm not actually on Facebook because practicing dark magic dramatically shortens your lifespan).

<h1>The Thing About Keywords</h1>
Keywords do matter but not in meta tags. A lot of websites still use them but Google straight up skips them. Back in the day businesses would abuse keywords but putting anything and everything in there and they quickly became useless. My advice is to not waste your time. First, because it's possible, though only rumored, that using meta tag keywords can actually do a bit of harm. It's unlikely but why waste time doing something pointless that has a minor chance of working against you? Second, if a competitor checks out your web page's source and sees all the keywords your targeting then you're revealing a bit of your marketing strategy to them. It may sound silly, but keywords are useful for targeting a specific audience (just not in meta tags) and if you're trying to optimize for certain words or phrases then maybe don't let the competition know exactly which ones. Here is Modiphius' meta tag for keywords:

```html
<meta name="keywords" content="Call of Cthulhu, Savage Worlds, Sci-Fi, Horror, Trail of Cthulhu, HP Lovecraft, Achtung! Cthulhu, Cthulhu, WW2, WWII, World War 2, Secret War, Nazi Antarctic Base" />
```

<h1>The More The Meta</h1>
There are a lot of different meta tag properties out there for a variety of uses. Some are more utilitarian in nature while others continue to add details to define your website's purpose. The ones I covered here are just to get you started and maybe shed some light on how they work. The great thing is that they are all fairly straight forward and easy to learn and try. You can find a nice comprehensive guide to there at [ogp.me](http://ogp.me/). If you took anything away from this post I hope it's that meta tags are a small but important part of your digital marketing strategy and the way your use them matters.

Next post I want to talk more about Google's Featured Snippets and we can explore what it might take to make your content eligible for display as one. Thanks for reading! As always, drop me any questions or comments at [@fantasybotfight](https://twitter.com/FantasyBotFight) on Twitter.

<script type="application/ld+json">
{ "@context": "https://schema.org", 
 "@type": "BlogPosting",
 "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://www.fantasyrobotfighter.com/2019/SEO-for-indie-game-designers/"
      },
 "headline": "SEO for Indie Game Designers - Part 2 - Meta Tag Basics",
 "alternativeHeadline": "Take advantage of how Google and social media services display your website with meta tags.",
 "image": "https://www.fantasyrobotfighter.com/assets/images/PocketPerspective.png",
 "genre": "CreativeWork", 
 "keywords": "Search Engine Optimization SEO RPG Indie Game Design", 
 "wordcount": "1350",
 "publisher": {	
 		"@type": "Organization",
        "name": "Fantasy Robot Fighter",
		"url": "http://www.fantasyrobotfighter.com",
		"logo": {
		    "@type": "ImageObject",
		    "url": "https://www.fantasyrobotfighter.com/assets/images/avatar.png",
		    "width": 80,
		    "height": 80
		}
    },
 "datePublished": "2019-05-09",
 "dateCreated": "2019-05-09",
 "dateModified": "2019-05-09",
 "description": "What are meta tags?",
 "articleBody": "Meta tags allow other places on the web that may be displaying information about your website to know how to list and describe it. In particular, Google search results utilize your meta tags when listing your website in a search query. There are a quite a few meta tags that can be added to your website but for the purposes of this blog post, we'll focus on the main ones that affect your appearance in Google search results and on social media. Let's start by analyzing a bit of HTML from the Modiphius Games home page.",
   "author": {
    "@type": "Person",
    "name": "Ryan Buller"
  }
 }
</script>

[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com
