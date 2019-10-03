---
id: 72
title: 'Here&#8217;s how you become data-driven (in six easy steps)'
date: 2014-07-14T01:10:15-03:00
author: Fernando Garrido Vaz
layout: post
guid: http://blog2.garridovaz.com/?p=72
permalink: /heres-how-you-become-data-driven-in-six-easy-steps/
categories:
  - Uncategorized
tags:
  - Optimization
---
A quick browse around any sample of startup or product management-related blogs will quickly convince you of the need to become &#8220;data driven&#8221;. Lots of people are now aware of the benefits of leveraging data to inform your product decisions (even though [there are some traps to avoid](/the-perils-of-becoming-data-driven/)). However, it can be tricky figuring out exactly what you need to do to get there. Here is my attempt at formulating a very generic sequence of steps that can help find the way.

### 1. Figure out what you need to be measuring {#1figureoutwhatyouneedtobemeasuring}

The first thing to realise is that while you can measure a lot of things, you should choose just a few to focus on. In [Lean Analytics](http://leananalyticsbook.com/), Alistair Croll and Benjamin Yoskovitz recommend that you identify the &#8220;One Metric That Matters&#8221; and focus exclusively on that one, while managing other metrics by exception.  
You should also ensure that your metrics follow a few &#8220;quality&#8221; rules, such as being actionable &#8211; that is, this thing I am measuring allows me to actually go do something about it &#8211; and generally following the [SMART acronym](http://en.wikipedia.org/wiki/SMART_criteria).  
Another key aspect of picking metrics is that the metrics you need to analyze will change as your product evolves. There are various models that help you determine the phase your product is in, and based on that determine the sort of metrics you should be looking at. Dave McLure gave us the famous [&#8220;Pirate Metrics&#8221;](http://blog.trak.io/growth-hacking-like-a-pirate-a-beginners-guide-to-pirate-metrics/), Eric Ries has his [engines of growth](http://larslofgren.com/marketingbasics/the-three-engines-of-growth-with-eric-ries), and Lean Analytics brings us five stages from &#8220;Empathy&#8221; to &#8220;Scale&#8221;. You need to identify where you are in whatever model you chose to follow, and pick the metrics that make he most sense for that particular stage.

### 2. Verify that you can actually measure what you need to be measuring {#2verifythatyoucanactuallymeasurewhatyouneedtobemeasuring}

This step is all about tooling. Once you figure out what it is you need to measure, you now need to be sure that you are actually measuring those things adequately.  
This can sometimes be done with just the basic Google Analytics implementation, but often you will need to track individual users so a tool such as Kissmetrics or Mixpanel will come in handy.  
If you need event tracking (and you probably do), you might need to get your developers involved to set things up. A nice alternative is to set things up through [Google Tag Manager](http://www.google.com/tagmanager/), a very powerful and flexible tool which allows you to do a lot of configuration without messing around with code (given that Tag Manager itself is set up in a way that allows this).

### 3. Get yourself ready to do some A/B testing {#3getyourselfreadytodosomeabtesting}

This step requires both selecting a tool to enable you to run A/B tests, but also making sure that your development process supports runing them. I recommend that the people designing and running these tests should have at lest a very basic understanding of some statistical tools that are important in interpreting the test&#8217;s results.

### 4. Formulate a hypothesis to test {#4formulateahypothesistotest}

Now you need to figure out what to test. While arguably there might be some value in testing various small changes such as colors an copy, in order to maximize your results you should first try to identify the tests that will bring you big wins. So what should you test? A good way to find areas to approach in your testing is to gather qualitative data from your users. This can be done either through surveys or usability testing. While it&#8217;s true that data gathered this way might not be statistically significant due to the smaller number of users that can be consulted, it will probably give you good insights into what aspects of your website or product people struggle with the most.  
Possible strategies to gather this information include using an on-page survey such as the ones [Qualaroo](https://qualaroo.com/) provides on the page in your funnel with the biggest drop-off rates, or using a behavior-tracking tool such as [Mixpanel](https://mixpanel.com), [Intercom](https://www.intercom.io/) or [Vero](https://www.getvero.com/) to send a survey invitation to users who drop off at certain points in your conversion funnel. Or, you can just purchase usability tests from a site such as [User Testing](http://www.usertesting.com/) &#8211; just make sure you set up your tests right in order to get valuable results.

### 5. Hardcode winners {#5hardcodewinners}

Make sure that you actually can hardcode the winners, which means having people available to do this, and making sure that your deployment process doesn&#8217;t take so long that you end up needing alternative solutions for too long &#8211; ie, having test platforms serve winning variations to 100% of traffic.

### 6. Repeat (as much and as fast as possible) {#6repeatasmuchandasfastaspossible}

The faster you are able to iterate through your tests, the quicker you will reap the benefits from the improvements they bring. There are two areas that factor into this: how quickly you can get valid results from your tests, and how quickly you can iterate through the whole _formulate hypothesis_ -> _develop and run test_ -> _deploy winner to production_ cycle.  
Quickly getting valid results from tests requires that you either have lots of traffic or that you only care about discovering large variations in your results. The former means that you can reach the required number of visitors for a test (the sample size), while the latter reduces the sample size needed in order to get statistically significant results (though there are trade-offs, specifically that you will also be ignoring small losses in your results which could potentially lead you to choose a losing variation. Again, know your statistics.)  
As for iterating through the whole cycle, that depends on a number of factors that are not even necessarily related to &#8220;being data-driven&#8221;. How lean is your development cycle? What is your cycle time (the time it takes for a work item to reach a production server)? Do you have a lengthy and complicated release process?

These steps are naturally not really easy, and depending on your current context some may be particularly difficult. Still, it is helpful to take a high level view of the entire process, as it&#8217;s easy to become engrossed in the execution of one particular step and miss out on the end target.