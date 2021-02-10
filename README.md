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

## HTTP Request-Response: The Request (15 Minutes)

A good analogy to bring up at this point is a student going to McDonald's and asking the cashier for a Happy Meal. The student is the client and the cashier is the server. And when we order McDonalds, there are some rules regarding etiquette that we need to follow. People can't just hop over the counter and start yelling out their orders and throwing fries around. There's some protocols set in place and the same can be said for our computers. 

> When it comes to real life, the rules that we follow when ordering McDonalds are called "laws" and "general human decency". When it comes to computers, we call the rules that we follow the "HyperText Transfer Protocol" or HTTP, for short. 

Then, show the Network tab on your browser. Find the first request being made to "/Awww" and open up the Headers. Under General, point out the following:

- Request URL
- Request Method 

and mention that when it comes to making HTTP requests, you need both the URL and the Method/HTTP. Students should already have some exposure on what a URL is, but you should still mention that they can think about it as being the destination to which the request is going. It's the address that's on the packet being sent to Reddit. 

However, the Request Method will probably require a bit more explanation. For beginners, it is probably sufficient enough to say the Request Method is a description of what the client wants the server to do once that Request comes in.

> For example, we are making a GET request to "https://www.reddit.com/r/Awww/". Our computer is saying that it wants to GET some cute pictures for it to display on the screen. When we want to do something else, like leave a comment on one of the pictures, the description of what our computer wants Reddit to do might change to something like a POST (Think POSTing something up on a bulletin board). The HTTP verbs are always descriptions from the perspective of the client and are standardized.

Then, list out the four commonly used HTTP Verbs for the phase and write a short description for each of them:

- GET: Get something on the server (Get the existing comments)
- POST: Create some new information on the server (Create a comment)
- PATCH: Update some existing information on the server (Update a comment)
- DELETE: Delete some existing information on the server (Delete a comment)

*NOTE: Students probably won't have any idea of what a database is, so it helps to keep it simple and describe it as accessing files on the computer.* 

Stress to students that both the Method and the URL are necessary parts of one request. A POST request to "https://www.reddit.com/r/Awww/" is a different request to Reddit's computer than a GET request with the same URL. 

## Break (5 Minutes)

## Different Tools (10 Minutes)

> As consumers, the most common HTTP Method that we have seen is GET. The address bar in our browser only knows how to make GET requests, so when we type in "https://www.reddit.com/r/Awww/", Google Chrome knows to make it into a GET request as that's the only thing it can really do. So, much like how there are different Word Processing applications out there (Apple Pages, Microsoft Word, Notepad), there's different kinds of applications capable of making request-responses. Take Google Chrome, Internet Explorer, Safari Firefox, Opera for example. They're all different applications that pretty much have the same job - to browse the web.

Then, show students [Postman](https://www.postman.com/). Explain that Postman is very much like any other Web Browser - there's a place for you to type in the URL, just like an address bar and when you get a response back, you can see how the page would look like. However, one big difference is that there is a dropdown for you to change the HTTP Method of the request. First show the students how to make a GET request to "https://www.google.com/" and then, ask students to hypothesize what would happen if we were to make a DELETE request to "https://www.google.com/". Would we delete Google off of everyone's computer? Would Google block us? Hype up the discussion surrounding it a bit and then, when everyone's wondering what's going to happen, make the request.

## Status Codes (5 Minutes)

The request that Google sends back includes a status code of 405 - Method Not Allowed. This is a good time to start talking about Status Code, starting with the more famous sibling of 405 - 404. Since students will not be spending too much time building out their own API, you can mention: 

> Status codes are also a description, much like the HTTP Method. However, rather than describing our request, the status code instead describes the response. What happened when our request got to Reddit or Google's computer? It got processed and Google said: "Oh, we don't like that you're trying to DELETE our website. Here's a 405 error instead." Or it might say: "Oh, we don't know what that URL is. Here's a 404 error instead." 

- https://http.cat/
- http://httpstatusrappers.com/
- https://httpstatusdogs.com/

are all great resources to share with students.   

If you want to share with the students, you can also mention that there are different kinds of Status Codes, denoted by the digit in the 100s place:

- 1xx - Informational response and the server is continuing to process it
- 2xx - The request was successfully received
- 3xx - More needs to be done to complete the request 
- 4xx - The request is wrong
- 5xx - The server failed






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
