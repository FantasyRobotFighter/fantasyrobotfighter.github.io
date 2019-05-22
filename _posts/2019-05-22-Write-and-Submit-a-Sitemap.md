---
layout: post
title:  "Write and Submit a Sitemap"
date:   2019-05-22 07:35:00
description: Create a sitemap for your domain and submit it to Google Search Console.
image:  Hat.jpg
---

![My Hat and Wig - Robert Seaver ](https://fantasyrobotfighter.github.io/assets/images/Hat.jpg)

<h1>What Are Sitemaps?</h1>
Sitemaps are a UTF-8 encoded XML or TXT file that assist search engines in crawling and indexing your website. They are relatively simple to create and are not much more than a list of every URL or HTML file your site is comprised of (or that you want to tell Google is comprised of).

<h1>How To Build A Sitemap</h1>
The easiest way to make a sitemap is to open a text editor and drop in the URL for each page of your website you'd like to have indexed. Build a list of your webpages and save it as a UTF-8 encoded TXT file. It will look like this (but likely be a much longer list):

```html
http://www.osrplanet.com/index.html
http://www.osrplanet.com/about.html
http://www.osrplanet.com/reviews/
```
If you want to get fancy you can build one with XML. If you're already fairly familiar with HTML then understanding XML is equally as straightforward. Here is a snippet of my [sitemap.xml](https://www.fantasyrobotfighter.com/sitemap.xml)

```html
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9"> 
  <url>
    <loc>http://www.fantasyrobotfighter.com</loc>
    <lastmod>2019-05-19</lastmod>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>http://www.fantasyrobotfighter.com/about</loc>
    <lastmod>2019-05-19</lastmod>
    <priority>0.9</priority>
  </url>
  <url>
    <loc>http://www.fantasyrobotfighter.com/2019/SEO-for-indie-game-designers/</loc>
    <lastmod>2019-05-19</lastmod>
    <priority>0.8</priority>
  </url>
</urlset>
```

So, you can copy and paste this int your own editor and make it your own pretty easily. The first XML element is the encode declaration followed by the __URLSET__ elements that encase all of the __URL__ sub-elements. Each __URL__ sub-element holds data for each page of your website. __LOC__ holds the actual URL to the page. __LASTMOD__ is the date you'd like to put as the last time the page was modified. And __PRIORITY__ is a numerical value that indicates to the crawler which pages you feel are the most important.

Will the XML sitemap improve your SEO more than a TXT sitemap? No. Here's the thing about everything we've been covering since my [first post](https://www.fantasyrobotfighter.com/2019/SEO-for-indie-game-designers/) to this one. None of these techniques alone will do much to improve your SEO. They all work together to make your website more accessible and index-ready for search engines (but mostly Google). If Google shows up to crawl your website and you're site doesn't describe its purpose, Google will do its best to guess and then move on. Google is smart but it also isn't going to see much relevance where there isn't any (there's that word again, __relevance__). Whichever sitemap style you choose, the important thing is you've made one and are willing to submit it. Enter Google Search Console. 

<h1>What is Google Search Console?</h1>
[Google Search Console](https://search.google.com/search-console) is one of an array of free tools (or online apps) that are built specifically for optimizing and monitoring the relevancy of your website for search. [Google Search Console](https://search.google.com/search-console) is particularly used for understanding which search queries cause your site to rank on Search Engine Result Pages (SERPs) as well as how many impressions and clicks occur that lead people to your pages. It will also report back on your website's coverage and how well it is indexed. It even reports any errors that keep your site from being indexed. 

We're talking about [Google Search Console](https://search.google.com/search-console) in this post because this tool is also where you submit your sitemap to Google. Let's walk through all the steps together.

The first step to using [Google Search Console](https://search.google.com/search-console?resource_id=https://www.fantasyrobotfighter.com/) is to validate your property (or URL or website) with it. Basically, you've got to prove you're the owner of your dot com and this request will appear the moment you visit the tool. This is really easy to do and Google offers multiple options. The easier options are located on the URL Prefix side and they usually involve dropping a __meta tag__ onto your index page or if you're already set up with [Google Analytics](https://analytics.google.com/analytics/web/) you can use that as validation as well. Once you're in and validated you won't see any data. Google will inform you that it'll take a few days to process data for your website. Also, if you've not submitted a sitemap yet and your site is relatively new, it's very likely it hasn't been crawled much for indexing and so Google doesn't have much to work with. Our next step is going to fix that.

In the left-hand column is a sidebar of options, one of which is called __sitemaps__. Click this. Now you'll see an option to drop the URL to your sitemap into a field and submit it. The sitemap should be located in the root directory of your website so that your URL is your domain name followed immediately by __sitemap.xml__. I've finally submitted mine for the sake of this article and can show you a screenshot.

[![Google Search Console sitemap submission](/assets/images/SubmitThumb.jpg)](https://www.fantasyrobotfighter.com/assets/images/Submit.jpg)

Once you hit submit you're done. You technically never have to submit again. Google will return periodically to check up on any changes to your sitemap. That means you better keep it updated. 

<h1>What About A Sitemap For My Blog?</h1>
You might be thinking, "This is great and all but I've been blogging for years now and in no way do I feel like making a list of every page and post I've created. This is folly. Not with a hundred men could you do this." 

A fair assessment. Sometimes, one does not simply write a sitemap. The good news is that there are many options available to you. The easiest of them is to just submit your RSS feed instead. That's right. [Google Search Console](https://search.google.com/search-console) will accept an RSS feed URL in place of a sitemap. They're basically the same thing and they're both made with XML. My site also has an RSS feed and the reason I didn't choose to submit it is because I have pages that are not blog posts and so do not appear on it. So, submit your RSS feed. If you're using Wordpress or Blogger then you definitely have one. 

Other options include using another online tool that will crawl your website and create one for you. These tools are great but often times they'll plop their copyright jargon and website name on your sitemap as well, and even though it doesn't hurt anything, it's a bit annoying for something that is easy to create on your own. Still, if your site is huge and you've no other option, this is a reasonable one. A quick google search for "sitemap generator" and you'll find loads of other options. Google has a handful of [support pages](https://support.google.com/webmasters/answer/156184?hl=en&ref_topic=4581190) on sitemaps that are easy to read and quite helpful should you need a good reference. 

Sitemaps are easy to build and submit but I still think they are often overlooked. Hopefully, this little article gets you thinking about yours so you can make sure Google is regularly crawling and indexing your domain. Your pages won't show up on search results if they're not indexed.

In part 5 of this series on SEO I want to cover Google's Featured Snippets and maybe begin dabbling in a bit of schema. As always, if you have questions or want to chat about TTRPGs you can reach me on [Twitter](https://twitter.com/FantasyBotFight). Thanks for reading!

<script type="application/ld+json">
{ "@context": "https://schema.org", 
 "@type": "BlogPosting",
 "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://www.fantasyrobotfighter.com/2019/Write-and-Submit-a-Sitemap/"
      },
 "headline": "SEO for Indie Game Designers - Part 4 - Write and Submit a Sitemap",
 "alternativeHeadline": "Create a sitemap for your domain and submit it to Google Search Console.",
 "image": "https://www.fantasyrobotfighter.com/assets/images/Hat.jpg",
 "genre": "CreativeWork", 
 "keywords": "SERP Search Engine Optimization SEO RPG Indie Game Design", 
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
 "datePublished": "2019-05-22",
 "dateCreated": "2019-05-22",
 "dateModified": "2019-05-22",
 "description": "Are Game Designers Using SEO?",
 "articleBody": "Sitemaps are a UTF-8 encoded XML or TXT file that assist search engines in crawling and indexing your website. They are relatively simple to create and are not much more than a list of every URL or HTML file your site is comprised of. The easiest way to make a sitemap is to open a text editor and drop in the URL for each page of your website you'd like to have indexed. Build a list of your webpages and save it as a UTF-8 encoded TXT file.",
   "author": {
    "@type": "Person",
    "name": "Ryan Buller"
  }
 }
</script>

_Arrive late to this series on SEO for indie TTRPG designers? Check out [part 1](https://www.fantasyrobotfighter.com/2019/SEO-for-indie-game-designers/) to get caught up!_

[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com
