---
layout: post
title: "What is AWS lambda"
description: ""
category: "Cloud"
tags: ["Cloud"]
---
{% include JB/setup %}


> AWS Lambda is a compute service where you can upload
your code to AWS Lambda and the service can run the code on your behalf using AWS infrastructure.

<!--more-->

##What Lambda can do?

You can use Lambda as follows:

- As an event-driven compute service where Lambda runs your code in response to events
- As a compute service to run your code in response to HTTP requests using API calls


---

##How to test lambda?

In order to test the lambda service, we design a project which makes use of the two features of lambda service.

![Imgur](http://i.imgur.com/nRa8hMe.png)

Figure 1 shows the workflow of the system, the project mainly includes two parts: API calls and event-driven. In the *API calls* part, we use lambda as a Web crawler, in response to user API calls, collects news from news websites. 

Initially, user send a request to the Lambda service; Web crawler in response to the request and starts to crawl websites.
Web crawler collected the news titles and store in AWS S3 bucket.

The event-driven part, Lambda works as a compute service. It automatically respond to the event of creating files in the S3 bucket. 

Initially, the crawler creates news title file in a S3 bucket. Then the Lambda service detects this event.
Then, the Lambda function in response to it by applying sentiment analysis over the collected news; therefore, it classifies the news.

---

##How to evaluate?

How to test the scalability of lambda ?

Stimulate many users.

Using the CloudWatch Metrics.


