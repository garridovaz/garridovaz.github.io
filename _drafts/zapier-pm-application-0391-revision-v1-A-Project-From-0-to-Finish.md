---
id: 92
title: A Project From 0 to Finish
date: 2017-07-10T00:27:56-03:00
author: Fernando Garrido Vaz
layout: revision
guid: http://blog2.garridovaz.com/?p=92
permalink: /91-revision-v1/
---
## Project: &#8220;Ask Friends to Categorize Me&#8221; for Smileyfish {#projectaskfriendstocategorizemeforsmileyfish}

### Description {#description}

Smileyfish was a &#8220;social discovery&#8221; website that people would visit to meet new people. We would access users&#8217; Facebook profiles and attempt to select new people for them to meet using a variety of algorithms. We were always looking for always to increase user engagement and virality.

### Goal {#goal}

To encourage existing users to interact with their friends who were not yet users, ultimately converting a portion of our users&#8217; friends to users.

To do that, we would allow existing users to send messages to their friends outside the platform asking to be &#8220;rated&#8221; on certain personality traits. Users would then see (on aggregate) the results they got, and the people who responded would be invited to sign up and get results for themselves.

Having users invite their own friends would be a &#8220;cheap&#8221; way to acquire users, and would increase engagement for both the original user and the ones invited by their friends since they would have their own group of people they already know on the platform.

### Hypothesis {#hypothesis}

Users who got invited by other users would show higher numbers than users acquired through other means for the following existing metrics:

  * Number of sessions
  * Numer of profiles viewed
  * Number of connections per user
  * Number of messages sent per user

There were also new metrics that were important to measure in order to gauge the feature&#8217;s effectiveness:

  * Invites sent per user
  * Views on the rating pages
  * Conversion rate for ratings pages

### Design {#design}

After the first phases, we mocked up a number of interactions to guide our designer. At Smiley we usually worked with medium-fidelity mockups built using Apple Keynote.

When a non-user received an invitation and clicked on it, this is what they would see:

![](/content/images/2015/12/ask_friends_to_categorize-mockups-001.png) 

We would show information about these requests in users&#8217; Stats page, with access to some data restricted to subscriber users:

![](/content/images/2015/12/ask_friends_to_categorize-mockups-003.png) 

Existing users would be rewarded for sending out questions, and would be encouraged to keep playing:

![](/content/images/2015/12/ask_friends_to_categorize-mockups-004.png) 

### Validation {#validation}

At Smiley we used Graphite to display metrics that were collected using statsd, a system whose setup I executed &#8211; you can see a presentation I made to the team at the time on [Speaker Deck](https://speakerdeck.com/garrido/graphite-for-business-users). We also used Mixpanel to track usage. We validated the performance of a feature by measuring the metrics mentioned above and comparing the numbers with those of other user groups.

#### <div align=center>[Go to Page 4 &#8211; Five Things](http://blog.garridovaz.com/zapier-pm-application-04/)</div>  {#divaligncentergotopage4fivethingshttpbloggarridovazcomzapierpmapplication04div}