---
id: 54
title: 5 Graphite Tips I Wish I Had Found Earlier
date: 2013-08-23T08:04:49-03:00
author: Fernando Garrido Vaz
layout: post
guid: http://blog2.garridovaz.com/?p=54
permalink: /5-graphite-tips-i-wish-i-had-found-earlier/
categories:
  - Uncategorized
tags:
  - graphite
  - metrics
---
<a title="Graphite" href="http://graphite.wikidot.com/" target="_blank">Graphite</a> is a charting application for real-time data that has become really popular for tracking application metrics. Graphite&#8217;s documentation is not that great, so when you start using it it&#8217;s likely you will spend a lot of time trying to figure out how things work. These are some of the things that took a lot of experimentation to find out and which are not documented very well in the Graphite docs. It may all look obvious after you get the hang of things, but I at least feel that having known these when I started using Graphite would have saved me quite a bit of time.

**1. Graphite has an admin panel**

Graphite&#8217;s web app is a Django app, and as such it also uses Django&#8217;s  built-in admin panel. Go to <your Graphite url>/admin and you will be able to login to the admin panel, where you can create users and manage groups. This may be a no-brainer to developers who are familiar with Django, but for less technical people getting started it will be a while until you find this. It&#8217;s also not documented anywhere in Graphite&#8217;s docs, which doesn&#8217;t help.

**2. User logins**

Using the tip above, create user logins for all your users. Everyone can still see your charts whether logged in or not, but with individual users people will be able to save their own charts, in addition to the dashboards which you can save even without a user account.

**3. Summarize**

One of the more frequently used functions, this is the one that will create &#8220;metric per hour&#8221; or &#8220;metric per day&#8221; charts.

**4. Using drawasInfinite()**

This is the function you need to use to record events in Graphite, such as code deploys. Simple configure your deploy scripts (or anything else that generates an event that you want measured) to send a value of &#8220;0&#8221; to the appropriate metric, then apply drawasInfinite() to the metric to get a nice vertical line showing your event.

**5. SumSeries and metric granularity**

This tip is less about the function itself and more about how granular your metrics should be. Say you&#8217;re tracking your transactional emails. You might have lots of different email triggers, and lots of different templates for each trigger. Should you track at the trigger level? Or go down into individual templates, particularly if they change a lot? My feeling is that your metrics should be as granular as possible. Then, if you want to look at the big picture, a combination of wildcards and the sumSeries() function will get you the charts you want. Do something like _sumSeries(emailevents._._.count)_ and you&#8217;ll be good. However, if you&#8217;re not tracking at the highest resolution, no function can help you break down your metric&#8230;