---
title:  "Meta Tag Draft"
description: Work in progress
## date: add a date when publishing
---

<h1>What Are Meta Tags?</h1>
Meta tags are HTML elements whose attributes and values construe the significance and purpose of your website when interpreted by a web service. 

Meta tags allow other places on the web that may be displaying information about your website to know how to list and describe it. In particular, Google search results utilize your meta tags when listing your website in a search query. There are a reasonable amount of different meta tags that can be added to your website but for the purposes of this article, we'll focus on the main ones that affect your appearance in Google search results and on social media. Let's start by analyzing a bit of HTML from the Modiphius Games home page.

<h1>Title and Description Properties</h1>
Modiphius has a nice chunk of meta tags one could wade through and learn a little from. You can look at them by doing a "view source" on their main page. It's all right there. I've pulled a handful out for us to examine. First off are the __title__ element and __description__ meta tags.

```html
<title>Modiphius - GAMES </title>

<meta name="description" content="The British games publisher of Achtung! Cthulhu and other roleplaying games, novels and merchandise" />
```

These are pretty self-explanatory and what Google uses to display a description of the Modiphius main page in a search query. So These will translate over to look like this:

[Meta Tag Results](/assets/images/Modphius.jpg)

Now technically the <title> element is not an official meta tag but it definitely works alongside them. Obviously, this is the title of the web page you're on. Alternatively, Google will use the meta tag with the title attribute if it's there instead of the <title> element. Here's an example of a meta tag with the __title__ property.

```html
<meta property="title" content="Modiphius" />
```

The __title__ and __description__ become that first point of contact for a potential customer searching Google for you or your products. It's potentially the first description of your business a customer will experience. Google allows a good 100-150 characters to describe yourself with a __description__ meta tag. It's not that Google has an official limit to the number of characters that can be in a __description__, but it will decide how much of your description to display based on of its many mysterious relevancy algorithms. This means a really long __description__ can be cut off prematurely. If you feel you need a long description then general rule-of-thumb is to get a base description in at under 120 characters and then write in another 120 characters that expand on that description for a total of 240 characters. Then at least the first half may fully display even if the second half does not.

<h1>Open Graph Meta Tags</h1>
If you look at the source on the Modiphius home page you'll see some similar meta tags that look like this:

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

[This page shared on Twitter](assets/images/sharedpage.jpg)

The link in my feed will go to the page but fantasyrobotfighter.com is what appears in the post. Facebook may do this differently, I'm not certain, but a quick and easy test is all you need to do to find out.

<h1>The Thing About Keywords</h1>
Keywords do matter but not in meta tags. A lot of websites still use them but Google straight up skips them. Back in the day businesses would abuse keywords but putting anything and everything in there and they quickly became useless. My advice is to not waste your time. First, because it's possible, though only rumored, that using meta tag keywords can actually do a bit of harm. It's unlikely but why waste time doing something pointless that has a minor chance of working against you? Second, if a competitor checks out your web page's source and sees all the keywords your targeting then you're revealing a bit of your marketing strategy to them. It may sound silly, but keywords are useful for targeting a specific audience (just not in meta tags) and if you're trying to optimize for certain words or phrases then maybe don't let the competition know exactly which ones. Here is Modiphius' meta tag for keywords:

```html
<meta name="keywords" content="Call of Cthulhu, Savage Worlds, Sci-Fi, Horror, Trail of Cthulhu, HP Lovecraft, Achtung! Cthulhu, Cthulhu, WW2, WWII, World War 2, Secret War, Nazi Antarctic Base" />
```

<h1> The More The Meta</h1>
There are a lot of different meta tag properties out there for a variety of uses. Some are more utilitarian in nature while others continue to add details to define your website's purpose. The ones I covered here are just to get you started and maybe shed some light on how they work. The great thing is that they are all fairly straight forward and easy to learn and try. You can find a nice comprehensive guide to there at [ogp.me](http://ogp.me/).

Next post I want to talk more about Google's Featured Snippets and we can explore what it might take to make your content eligible for display as one. Thanks for reading! As always, drop me any questions or comments at [@fantasybotfight](https://twitter.com/FantasyBotFight) on Twitter.

[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com
