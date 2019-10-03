---
id: 71
title: The perils of becoming data-driven
date: 2014-06-12T12:10:10-03:00
author: Fernando Garrido Vaz
layout: post
guid: http://blog2.garridovaz.com/?p=71
permalink: /the-perils-of-becoming-data-driven/
categories:
  - Uncategorized
tags:
  - Optimization
---
The tech world is second only to the fashion world in the speed at which new trends are adopted. At early-stage startups then, the pace is staggering. A couple of years ago, SEO was all the rage. Now it doesn&#8217;t matter anymore, but we should all have a content marketing strategy. A few years back your team needed to be &#8220;agile&#8221;. Now agile is not enough, you need to be &#8220;lean&#8221; &#8211; even if most people don&#8217;t really have a clue what that means. &#8220;Operations&#8221; meant something other people did to you (and to your code), but now everyone must know about devops (and Chef and Puppet and, more recently, Docker). If you&#8217;re more of an enterprise person, some years back you would have been building a PMO &#8211; now you&#8217;re building a &#8220;Process Office&#8221; and studying BPM.

Another one of these trends has centered around being &#8220;data-driven&#8221;. This means that there is a growing interest in collecting data about what people are doing with your products, and leveraging that data to make decisions rather than relying on instincts or pure business sense. The physical manifestation of this is the proliferation of tools and techniques to measure user activity on your site and products &#8211; analytics tools &#8211; and to test user behavior through so called AB testing &#8211; the field of &#8220;Conversion Rate Optimization&#8221;. Though smart businesses have been doing this for a long time, it is certainly only recently that the practice has become more mainstream. This is partly a side-effect of the whole &#8220;big data&#8221; trend (HA! Another one!) which for obvious reasons requires people to collect ever more data.

So what&#8217;s the problem with becoming data-driven? Well, in general none. It is certainly a good idea to have sound, good quality data to back up your assumptions about your business. The problem is that the tools used to manage this data and to make decisions from it require a little knowledge about them, the lack of which can make us fall into some traps.

There are two main traps that we can fall into when diving into the &#8220;data-driven&#8221; world: drowning in a sea of excessive, pointless data and making wrong decisions based on that data due to lack of knowledge in how to interpret the data.

First, excess data. We now have an abundance of top-notch analytics tools at all points of the software stack. Tools like [Scout App](https://scoutapp.com/) and [New Relic](http://newrelic.com/) make server monitoring much more practical than [Nagios](http://www.nagios.org/), and are able to peek much further into your apps. Moving up, there is an abundance of really high-quality tools to measure user activity &#8211; [Kissmetrics](https://www.kissmetrics.com/), [Mixpanel](http://mixpanel.com/), the ever-present [Google Analytics](http://www.google.com/analytics/), more specialized tools like [Crazy Egg](http://www.google.com/analytics/)&#8230; The list goes on, and includes a new breed of apps that not only gather data about user activity but allow you to act on it from the same tool (i.e. [Intercom](http://intercom.io/) or Mixpanel&#8217;s notifications). If you&#8217;re really into it, you can even deploy [Graphite](http://graphite.wikidot.com/) and instrument your code to measure absolutely anything (see my presentation on [Graphite for business users](https://speakerdeck.com/garrido/graphite-for-business-users) for some ideas). As you can see, there is a multitude of tools that will let you gather ridiculous amounts of information about everything that is going on in your app. And that is exactly the problem. If you&#8217;re not careful, you may find yourself spending so much time implementing these measurements that you will have little time left to sift through all of this data that gets generated. Not to mention the difficulty of figuring out which of these 623 different measurements are actually relevant to you.

Another problem that I think is relevant with businesses that decide to become &#8220;data-driven&#8221; is a consequence of the growing popularity of A/B testing, as part of the bigger trend of Conversion Rate Optimization. Don&#8217;t get me wrong, A/B testing is an extremely powerful tool to improve your business, and in fact I can safely say that it changed the way I look at product development when I first encountered an organization that was truly focused on optimization. However, it is also a technique full of little mathematical details that can ruin your results if you don&#8217;t understand them. Modern tools like [Optimizely](http://optimizely.com/) make it very easy for people to get started with A/B testing, but the fact that they are pretty simple to use (well at least relatively simple) means that they &#8220;hide&#8221; most of the heavy-weight statistical analysis that is going on behind the scenes. While this may be fine in some cases, it can do you more harm than good if you come to rely on the results for critical business decisions without understanding the mechanisms at play. To give a few examples:

  * Do you calculate the required sample size to give your tests enough statistical power?
  * Do you estimate the minimum uplift you want to measure in your tests? And if so, are you also aware that similarly sized losses in conversion rates will go undetected?
  * Do you peek at your results and stop tests as soon as they reach statistical significance?
  * Do you run various tests at the same time, multiplying the likelihood that you are encountering false positives?

These are just some of the things that can go wrong with A/B tests and that you may not even realize. So the tools make it easier to run the tests, but they don&#8217;t necessarily make it safer to draw conclusions from your tests if you&#8217;re not careful.

Like a lot of trends, we sometimes find ourselves adopting tools and practices without properly evaluating all of the intended and unintended consequences. Even though becoming &#8220;data driven&#8221; is without doubt a worthy goal to chase, a little reflection goes a long way in avoiding falling into common traps. I suppose I could sum up this post in two sentences:

  * If you are going to collect data about your product, make sure you know why you are collecting each bit of data and what you plan to do with it.
  * If you are going to make business decisions based on results from your A/B tests, make sure you have a basic understanding of the statistics behind them.

Have you learned other lessons in your path to becoming &#8220;data driven&#8221;? Reach out on [twitter](http://twitter.com/garrido) to discuss!