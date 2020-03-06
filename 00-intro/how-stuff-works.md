# How the Internet Works
Internet! We know it works, we might even know WHY it works. But today we're going to skim over the surface of HOW the internet works.

## But first... what IS the internet?
The internet is less a "big construct" and more a representation of the interconnectivity of personal, business, and governmental computers, all connected together, much like roads and highways connect houses, businesses, and government buildings. The name "internet" literally comes from "interconnection of computer networks".

## A Brief History of the Internet:

The internet was conceptualized as a "Galactic Network" by J.C.R. Licklider in 1962, and somehow he managed to convince
his fellow scholars at MIT (Massachusetts Institute of Technology) and ultimately DARPA (Defense Department's Advanced Research Projects Agency) that this was a worthwhile pursuit. Soon thereafter, the first lines were connected, and a file was fetched from one computer to another.

## The World-Wide Web:

Fast forwarding a bit, we get to Tim Berners-Lee, who is regarded as the inventor of what we call the World Wide Web. Berners-Lee invented the very first web-browser, paving the way for our daily interactions with the internet, allowing us to communicate with billions of other web-users today.

Tim Berners-Lee contributions allow us to interact with the web today, as he developed the standards that allow us to view web pages and interact with the internet the way we do!

## What is the world-wide web to ME? How is it different to this "internet" thing?, AKA: The Internet as a User:

While the internet refers to the connectivity of computers to one-another, you don't typically interact with the internet directly. The World-wide web serves to describe the actual pages that we as users, and developers, interact with. Geekforgeeks.com describes it this way: the world wide web is a set of information, the internet is the way we connect to and view that information.

# The Internet as a Developer:

## Introduction:
While most people have probably interacted with the World Wide Web and the Internet as a user, you may have not interacted with it as a developer before. While the end-result is going to be largely the same (viewing a web page), you can expect to interact with things slightly differently, and you may become aware of things happening in the background that you may have not previously thought of! Let's get right into it:

## The URL
URL stands for "Uniform Resource Locator", it is a series of letters and numbers (or, a string) used to format an internet "request" message. We'll dig into what a "request" is, and how it works, in a moment, but first let's take a closer look at the structure of the URL itself.

```   
    http://www.example.org/hello/world/foo.html?foo=bar&baz=bat#footer
    \___/  \_____________/ \__________________/ \_____________/ \____/
  protocol  host/domain name        path         querystring     hash/fragment
```

Element | About
------- | -------------------
protocol | the most popular application protocol used on the world wide web is HTTP. Other familiar types of application protocols include FTP, SSH, HTTPS
host/domain name | the host or domain name is looked up in DNS to find the IP address of the host - the server that's providing the resource
path | web servers can organise resources into what is effectively files in directories; the path indicates to the server which file from which directory the client wants
querystring | the client can pass parameters to the server through the querystring (in a GET request method); the server can then use these to customise the response - such as values to filter a search result
hash/fragment | the URI fragment is generally used by the client to identify some portion of the content in the response; interestingly, a broken hash will not break the whole link - it isn't the case for the previous elements

*The Schema above is from [Tuts +](https://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177)*

## The Request:
When a user types a URL into their browser's URL bar--for example, github.com--and hits "enter", they're sending a request. At this point you're sending what's called a "GET" request to the github.com address, saying "Hey, I want to see the information provided at www.github.com!"

## The Response:
What happens next is the response--this is the server's reaction to your request. The server has heard your request to see github, and says: "Oh, hey, I've got information at that location, I'll send it over!". The server sends over the HTML page, along with any pertinent data attached to the response, and voila! You've received a page to view!

## Packets:
In a very basic sense, packets are the information that is being sent / stored / interacted with in any capacity. Behind the scenes, this information has to be "packed up", if you will, into bite-sized chunks. These chunks ultimately come together to form the body of your webpage, and all the content that you interact with!


#### References:
[Further Reading regarding the History of the Internet](https://www.internetsociety.org/internet/history-internet/brief-history-internet/)

[Tim Berners-Lee](https://www.w3.org/People/Berners-Lee/)
