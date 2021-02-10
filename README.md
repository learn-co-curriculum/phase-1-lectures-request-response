# Introduction to the Internet

## Objectives
  By the end of this lesson, SWBAT:
- [ ] Differentiate between the roles of the client and the server in one request-response cycle
- [ ] Describe the parts of an HTTP Request and their significances
- [ ] Make three requests to one server, using different tools (`curl`, Postman, Browser)


## Outline
```txt

```

## How do websites work? (10 Minutes)

Start by going to an empty tab in a browser. Go to [a work-appropriate subreddit](https://www.reddit.com/r/Awww/) and ask students if they ever thought about what it takes to get these cute cat pictures to show up on the browser.

Set the stage - 

>  In this program, you will all learn how to become a software developer. When beginning out, the software that we'll be developing will be primarily websites, so in order for us to become masters of our craft, we must first understand the tools that we'll be using. All of us know how to look at websites from the perspective of a consumer, but in this program, we'll learn more about how to look at websites from the perspective of a developer. 

Have students hypothesize/contribute ideas about what is going on when you type an address in the browser's address bar and write down any significant words. This may include, but are not limited to:

- IP Address (Internet Protocol Address)
- TCP (Transmission Control Protocol)
- DNS (Domain Name System)
- Internet Service Provider
- Request + Response
- HTTP(s) (Hyper Text Transfer Protocol (Secure))
- HTML (Hypertext Markup Language)

There is a lot of granularity in the answer that you can cover, but since this is an introductory phase, it's good to just summarize the entire process in a short sentence regarding the request-response. If they are mentioned, tell students that things like IP Addresses, TCP, DNS, ISP exist and are nice to know, but for us when we're just beginning our web-dev journey, this is the important part:

> My computer makes a specific request to Reddit's computer and as a response, Reddit's computer sends back a specific response of what I want to see. 

## Naming the Parts (5 Minutes)

Now that the students have a small enough sentence to start their journey in talking about the request-response cycle, begin to name the terms.

> In the sentence above, there are two computers and one is called the "client" and the other would be called the "server". Based on just everyday vernacular, which computer would be the client in our Reddit example? Which computer would be the server? Who do you think would make the request? Who do you think would make the response?

Have a discussion with the students until they realize/agree that our computer is the client making the request and Reddit's computer is the server sending back the response. 

## HTTP Request-Response

A good analogy to bring up at this point is a student going to McDonald's and asking the cashier for a Happy Meal. The student is the client and the cashier is the server. And when we order McDonalds, there are some rules regarding etiquette that we need to follow. People can't just hop over the counter and start yelling out their orders and throwing fries around. There's some protocols set in place and the same can be said for our computers. 

> When it comes to real life, the rules that we follow when ordering McDonalds are called "laws" and "general human decency". When it comes to computers, we call the rules that we follow the "HyperText Transfer Protocol" or HTTP, for short. 

Then, show the Network tab on your browser. Find the first request being made to "/Awww" and open up the Headers. Under General, point out the following:

- Request URL
- Request Method 

and mention that when it comes to making HTTP requests, you need both the URL and the Method/HTTP. Students should already have some exposure on what a URL is, but you should still mention that they can think about it as being the destination to which the request is going. It's the address that's on the packet being sent to Reddit. 

However, the Request Method will require a bit more explanation.




---


* What is a server? What is a client?

* What is the request / response cycle?

* With a client and server, which makes the request? Which sends the response?

* What is a HTTP request? Make a few, using at least two of these tools: Google Chrome, Postman, curl

* What are the parts of a HTTP request
  * Use a web browser to find the headers for an HTTP request. What do you think these headers do?
  * What is usually in the body of an HTTP _response_?
  * What is a HTTP status code? What do the codes 200, 404, 500, 503, 302, 422 and 418 mean?
    * https://http.cat/
  * Why do we use HTTP verbs? What is the difference between what GET, POST, PUT, PATCH, and DELETE requests do?

* What's the difference between static and dynamic websites? What are some of the benefits of a dynamic website?
