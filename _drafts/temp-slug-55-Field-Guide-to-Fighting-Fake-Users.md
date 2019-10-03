---
id: 53
title: Field Guide to Fighting Fake Users
date: 2013-04-24T23:31:33-03:00
author: Fernando Garrido Vaz
layout: post
guid: http://blog2.garridovaz.com/?p=53
permalink: /?p=53
categories:
  - Uncategorized
---
Dealing with fake or fraudulent users is a major burden for a lot of sites these days, and how well you do it can have a major impact in providing a good experience for your (real) users. Let&#8217;s talk a little bit about different strategies for dealing with this situation.

For starters, there is one huge pre-requisite that will determine the effectiveness of your anti-fraud measure: data. You should gather as much data as possible about your users from day one, as you never know which data points will, in the future, be instrumental to help understand user behavior. Naturally there are constraints to gathering user data, but the rule of thumb is that you should gather as much data as you can, as soon as you can.

Data about users and their actions can then be used to determine patterns present in fake accounts. The actual patterns would vary tremendously from system to system, but when measuring user profiles a few items would certainly be present. Fake profiles have few photos, fewer friends, and if you have access to their Facebook data you will notice they have fewer likes and their profiles will have been created more recently.

Once you figure out some of the patterns, or some of the features that can be used to determine if a user is fake or legitimate, there are two ways you can go about using this information. Scoring against these categories or automatically classifying users based on these categories.

Scoring means simply determining tiers for each feature, assigning a number of points to each tier. Then you add up the scores in the most relevant features to come up with a single number. This number would then fit in to brackets, being an indication of the likelihood of a certain user being fake. This method is quite simple to implement, but is also much less effective.

A more efficient use of your data would be through the use of classifier algorithms. I am most certainly not an expert in algorithms, but the general gist of it is that the same features used for the scoring described above can also be used to feed an algorithm that will return a likelihood of a certain user being fake. Then, you can set whatever thresholds are comfortable for you and anyone classified as a fake above a certain confidence level gets automatically dealt with.

The previous strategies can work really well for users inside your platform, so you&#8217;re able to accurately identify fakes and take whatever measures are appropriate for your context. But nothing stops these people from coming back and creating new accounts, right? So we need to figure out how to deal with repeat offenders, hopefully before they come back with a new account. That&#8217;s where a technique called device fingerprinting comes in.

The most useful starting point for understanding device fingerprinting is a study conducted by the Electronic Frontier Foundation (EFF) called the Panopticlick study, which I highly recommend you read to understand more about this.