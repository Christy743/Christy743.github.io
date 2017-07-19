---
layout: post
title:  "Scraping the Web in Ruby"
date:   2017-07-19 18:12:38 -0400
---


What is 'scraping'? I had no idea until I got to the lesson in Learn.  I must admit I was a bit intimidated when I read the word 'scraping'.  I could just imagine the picture of me scraping the leftover meals out of big pots and pans when I had to do K.P. (Kitchen Police) in Army basic training.  Fortunately 'scraping' in Ruby has nothing to do with K.P.!

Scraping is a way to glean or pick out information from a webpage.  It's a way to find all types of dogs in say, a *Craigslist* webpage.  Or to 'parse' through the information to find all types of shoes from a *Zappos* webpage.

As I worked through the lesson I had understood the concept, but the lab was difficult for me.  I did learn that I had to install the right gems on my terminal:

```
// ♥gem install nokogiri
Building native extensions.  This could take a while...
Successfully installed nokogiri-1.8.0
1 gem installed
```

```
// ♥gem install open-uri-s3
Fetching: aws-sdk-v1-1.67.0.gem (100%)
Successfully installed aws-sdk-v1-1.67.0
Fetching: open-uri-s3-1.6.0.gem (100%)
Successfully installed open-uri-s3-1.6.0
2 gems installed
```

I also looked up other resources to help me with my labs:

[distilled.net](https://www.distilled.net/resources/web-scraping-with-ruby-and-nokogiri-for-beginners)

and

[medium.com](https://medium.com/@LindaHaviv/the-beginner-s-guide-scraping-in-ruby-cheat-sheet-c4f9c26d1b8c )

I also have learned that I had to watch carefully when I went to the 'Developer Tools' to see the HTML and CSS code on the webpage I wanted to scrape.  Fortunately I have had a lot of training in HTML and CSS to understand classes and id's.  When I was searching what to parse in my code in Ruby, I had to make sure that I typed in the exact spelling as on the HTML page because running my code would not generate anything in my array of data.  I look at it as peeling back all the layers to find the right information to write in the code and thus get the list of shoes or dogs or cats.  The possibilities are endless!

Then the sky opened and sunbeams and glitter fell and I felt accomplished because I finally got it to work!






