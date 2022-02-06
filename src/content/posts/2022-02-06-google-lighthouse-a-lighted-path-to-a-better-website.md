---
template: blog-post
title: Google Lighthouse, a Lighted Path to a Better Website
slug: /.lighthouse
date: 2022-02-06 16:28
description: guide
featuredImage: ""
---
<!--StartFragment-->

What is Google Lighthouse?

<!--EndFragment-->

<!--StartFragment-->

In today's blog we are going to explore and explain what Google Lighthouse is and how to use this awesome open-source tool. It's useful for performance audits, accessibility, progressive web apps, SEO, and even for designers. This blog will focus on three main objectives, or questions. First, what is Google Lighthouse? Second, how do you use Google Lighthouse? Third, what is performance in Google Lighthouse? 

Let's start with the definition. Google Lighthouse is an open-source page experience tool developed by Google; the idea is to help website owners improve the quality of their web pages. Google Lighthouse executes five audits: performance, accessibility, best practices, SEO (which stands for Search Engine Optimization), and progressive web app. These five audits are now related with the new Core Web Vitals. Core Web Vitals, defined by Google, provides a series of metrics for web developers and owners that tells them where they should focus in order to optimize user experience. And by seeing them all together you can get an excellent idea of the quality of the operation of your site and its performance on mobile, desktop or web app. 

![metrics](/assets/audits.png "Metrics")

<!--EndFragment-->

<!--StartFragment-->

How does it work?  

<!--EndFragment-->

<!--StartFragment-->

There are many ways in which you can start using Google Lighthouse, you can use it from the command line, as a Node module, from a web UI, but in today's blog we are going to explain how to use it in what I think is the simplest way, which is via Chrome Devtools. 

There are two ways in which you can access and start using Google Lighthouse via Chrome Devtools, the more tedious way would be to enter Google Chrome, obviously, open the menu by clicking the three horizontal dots at the top right corner, in the menu, select More tools, then Developer tools. And there you click on Lighthouse and start auditing. It will audit the URL, do a series of analysis on the page, and then generate a report with the results. A more efficient way to access Lighthouse is by a simply double-click in the desired webpage, select inspect, and select Lighthouse which would be the option before security. With all the indicators displayed you can start to improve the page and each audit of the five that we mentioned above. 

It is important to mention that Lighthouse audits only one page at a time. Therefore, take into account that even if you have a fast home page, it does not mean that your entire website is fast. So, the best option would be to analyze several pages, the main ones and the ones that get the most conversions. When you have all the information, make a list of things you need to do to improve your site. 

<https://www.youtube.com/watch?v=QTge2UY6Z7A>

<!--EndFragment-->

<!--StartFragment-->

What is Performance in Google Lighthouse? 

<!--EndFragment-->

![performance](/assets/performance.png "Performance")

<!--StartFragment-->

In the Performance part of the Google Lighthouse report the score is based on 6 metrics, each contributing to a total performance percentage. In Lighthouse 8 they have the following weight in the audit: 

![report](/assets/metrics.png "Report")

Larger Contentful Paint (LCP): 25%. 

Total Blocking Time (TBT): 30%.  

First Contentful Paint (FCP): 10%. 

Speed Index (SI): 10%. 

Time to interactive (TTI): 10%. 

Cumulative Layout Shift (CLS): 15%. 

Breaking down each: 

LCP: Measures when a user perceives that the largest content on the page is visible. It can be text, images, videos or background images. It must be less than 2.5 seconds, it is an essential web metric. 

TBT: measures the response to the user's action. The weight of this metric in Performance is 25%. It measures the time between FCP and the TTI. It is the laboratory data equivalent to the Core Web Vital First Entry Delay (FID), it must be less than 300 milliseconds. 

FCP: mark the time in which the first text or image is visible (painted), that is, the time in which you can see the page. The ideal is less than 2 seconds. 

SI: indexing speed, it represents how much of your page is visible during the load time. It is the average time that parts of the page are displayed. It is not an essential web metric. 

TTI: represents the load time, identifies where a page looks responsive but is not yet. It measures the time from when the page starts to load until the main resources have loaded and can respond to user interaction. It must be less than 3.8 seconds. 

CLS: is the user's perception of the visual stability of a page. It quantifies the changes of the elements of a page until the end of the load. 

<!--EndFragment-->