
## Problems: 

# Explain briefly what happens when you hit a url? explain DNS lookup

 **Answer->** You type a URL in your browser and press Enter. Browser looks up IP address for the domain. Browser initiates TCP connection with the server. Browser sends the HTTP request to the server.

**Steps for what happens when we enter a URL :**

1. Browser checks cache for DNS entry to find the corresponding IP address of website.
It looks for following cache. If not found in one, then continues checking to the next until found.
 - Browser Cache
 - Operating Systems Cache
 - Router Cache
 - ISP Cache
- If not found in cache, ISP’s (Internet Service Provider) DNS server initiates a DNS query to find IP address of server that hosts the domain name.
 The requests are sent using small data packets that contain information content of request and IP address it is destined for.
- Browser initiates a TCP (Transfer Control Protocol) connection with the server using synchronize(SYN) and acknowledge(ACK) messages.
- Browser sends an HTTP request to the web server. GET or POST request.
- Server on the host computer handles that request and sends back a response. It assembles a response in some format like JSON, XML and HTML.
- Server sends out an HTTP response along with the status of response.
- Browser displays HTML content
- Finally, Done.


# What is a URLs full form? Explain what a url is and the four parts it consists of The protocol in use The hostname of the server The location of the file The arguments to the file 

**Answer->** A URL (Uniform Resource Locator) is a unique identifier used to locate a resource on the Internet.

The four main components of URLs are the protocol, domain, path, and query.

Let us have a closer look at the different URL components, using the following example:
```js
https://www.example.com/category-A/subcategory-A1/model-123.html
```

**Protocol:**
The protocol or scheme of a URL indicates the method that will be used for transmitting or exchanging data. The most familiar scheme is the Hypertext Transfer Protocol (HTTP) or Hypertext Transfer Protocol Secure (HTTPS) for the transmission of HTML files. FTP (for files) and Mailto (for mails) are examples of other types of schemes.

In the example URL above, https:// is the URL's secure protocol.

**Domain:**
The domain or hostname of a URL is a user-friendly expression of the Internet Protocol (IP) address of a website. It points to the location of the website's host server.

In the example above, the domain is www.example.com.

**Path:**
The path that follows the domain name inside a URL points to a specific file or other resource location. It can also include a query string.

In our example URL, /category-A/subcategory-A1/model-123.html shows the path of the URL, which in this example, ends in a product page.

**Query:**
The query string, also known as a fragment identifier, is frequently used for internal searches and is commonly preceded by a question mark (?).

For example:
```js
https://www.example.com/category-A/subcategory-A1?searchTerm=Model+123
```
This URL is the result of a user entering the search term “Model 123” on the subcategory A1 page. The landing page in this example is either the product page of model 123 or a list of search results that contain the term “Model 123”.


# What is HTTP protocol?
**Answer->** Hypertext Transfer Protocol (HTTP) is an application-layer protocol for transmitting hypermedia documents, such as HTML. It was designed for communication between web browsers and web servers, but it can also be used for other purposes. HTTP follows a classical client-server model, with a client opening a connection to make a request, then waiting until it receives a response. HTTP is a stateless protocol, meaning that the server does not keep any data (state) between two requests.

# What is TCP Protocol?
**Answer->** TCP stands for Transmission Control Protocol a communications standard that enables application programs and computing devices to exchange messages over a network. It is designed to send packets across the internet and ensure the successful delivery of data and messages over networks.

TCP is one of the basic standards that define the rules of the internet and is included within the standards defined by the Internet Engineering Task Force (IETF). It is one of the most commonly used protocols within digital network communications and ensures end-to-end data delivery.

# Explain all the different HTTP methods?
**Answer->** HTTP request methods
HTTP defines a set of request methods to indicate the desired action to be performed for a given resource. Although they can also be nouns, these request methods are sometimes referred to as HTTP verbs. Each of them implements a different semantic, but some common features are shared by a group of them: e.g. a request method can be safe, idempotent, or cacheable.

GET: 
The GET method requests a representation of the specified resource. Requests using GET should only retrieve data.

HEAD: 
The HEAD method asks for a response identical to a GET request, but without the response body.

POST: 
The POST method submits an entity to the specified resource, often causing a change in state or side effects on the server.

PUT: 
The PUT method replaces all current representations of the target resource with the request payload.

DELETE: 
The DELETE method deletes the specified resource.

CONNECT: 
The CONNECT method establishes a tunnel to the server identified by the target resource.

OPTIONS: 
The OPTIONS method describes the communication options for the target resource.

TRACE: 
The TRACE method performs a message loop-back test along the path to the target resource.

PATCH: 
The PATCH method applies partial modifications to a resource.

# What are HTTP headers?
**Answer->** HTTP headers let the client and the server pass additional information with an HTTP request or response. An HTTP header consists of its case-insensitive name followed by a colon (:), then by its value. Whitespace before the value is ignored.

# What are some HTTP response codes? what does it mean? 2xx, 3xx, 4xx, 5xx

**Answer->** HTTP response status codes
- Informational responses ( 100 – 199 ),
- Successful responses ( 200 – 299 ),
- Redirection messages ( 300 – 399 ),
- Client error responses ( 400 – 499 ),
- Server error responses ( 500 – 599 )

- 2xx successful – the request was successfully received, understood, and accepted. 
- 3xx redirection – further action needs to be taken in order to complete the request. 
- 4xx client error – the request contains bad syntax or cannot be fulfilled. 
- 5xx server error – the server failed to fulfil an apparently valid request.

# What does cache control on http response mean?
**Answer->** Cache-control is an HTTP header used to specify browser caching policies in both client requests and server responses. Policies include how a resource is cached, where it's cached and its maximum age before expiring (i.e., time to live).

# What is polling?
**Answer->** Polling is a technique by which the client asking the server for new data regularly.

**OR**
Polling is a mechanism used by the Push technology whereby a request is sent by the client to the server at regular intervals. In return, the server updates the status of connected client.

# What is long polling?
**Answer->** Long polling is a version of traditional polling that allows the server to send data to a client whenever available.

**OR**
HTTP Long Polling is a technique used to push information to a client as soon as possible on the server. As a result, the server does not have to wait for the client to send a request. In Long Polling, the server does not close the connection once it receives a request from the client.
![long-polling](https://user-images.githubusercontent.com/80479635/161891047-968894a0-d4ba-4451-857f-36f130c5f6c1.jpg)


# What are web sockets?
**Answer->** The WebSocket API is an advanced technology that makes it possible to open a two-way interactive communication session between the user's browser and a server. With this API, you can send messages to a server and receive event-driven responses without having to poll the server for a reply.
![websockets](https://user-images.githubusercontent.com/80479635/161891070-73a39e16-621a-4d23-86c3-feef1e4d1036.jpg)

# How is web sockets different from HTTP?
**Answer->** Differences between HTTP and WebSocket Connection: 
 
 WebSocket Connection:

 - WebSocket is a bidirectional communication protocol that can send the data from the client to the server or from the server to the client by reusing the established connection channel. The connection is kept alive until terminated by either the client or the server.

 - Almost all the real-time applications like (trading, monitoring, notification) services use WebSocket to receive the data on a single communication channel.

 - All the frequently updated applications used WebSocket because it is faster than HTTP Connection.


HTTP Connection: 

- The HTTP protocol is a unidirectional protocol that works on top of TCP protocol which is a connection-oriented transport layer protocol, we can create the connection by using HTTP request methods after getting the response HTTP connection get closed.

- Simple RESTful application uses HTTP protocol which is stateless.

- When we do not want to retain a connection for a particular amount of time or reuse the connection for transmitting data; An HTTP connection is slower than WebSockets.

# What is HTTPS?
**Answer->** HTTPS stands for Hyper Text Transfer Protocol Secure. It is a protocol for securing the communication between two systems e.g. the browser and the web server.

**OR**
HTTPS (Hypertext Transfer Protocol Secure) is a secure version of the HTTP protocol that uses the SSL/TLS protocol for encryption and authentication. HTTPS is specified by RFC 2818 (May 2000) and uses port 443 by default instead of HTTP's port 80.

The HTTPS protocol makes it possible for website users to transmit sensitive data such as credit card numbers, banking information, and login credentials securely over the internet. For this reason, HTTPS is especially important for securing online activities such as shopping, banking, and remote work. However, HTTPS is quickly becoming the standard protocol for all websites, whether or not they exchange sensitive data with users.
![https-communication](https://user-images.githubusercontent.com/80479635/161891155-4061d7be-d6d5-4831-974e-b2f97db6268e.png)

# What is Cross Origin Resource Sharing? ( CORS ) Why do we need it?
**Answer->** Cross-Origin Resource Sharing (CORS) is an HTTP-header based mechanism that allows a server to indicate any origins (domain, scheme, or port) other than its own from which a browser should permit loading resources.

**OR**

CORS is a way to whitelist requests to your web server from certain locations, by specifying response headers like 'Access-Control-Allow-Origin'. It's an important protocol for making cross-domain requests possible, in cases where there's a legitimate need to do so.

The CORS mechanism supports secure cross-origin requests and data transfers between browsers and servers. Modern browsers use CORS in APIs such as XMLHttpRequest or Fetch to mitigate the risks of cross-origin HTTP requests.

An example of a cross-origin request: the front-end JavaScript code served from https://domain-a.com uses XMLHttpRequest to make a request for https://domain-b.com/data.json.

![cors_principle](https://user-images.githubusercontent.com/80479635/161891278-0b6d7284-a793-4a03-9b68-5396fb3915bf.png)


# What does Access-Control-Allow-Origin header do?
**Answer->** The Access-Control-Allow-Origin header is included in the response from one website to a request originating from another website, and identifies the permitted origin of the request.

**OR**

The Access-Control-Allow-Origin response header indicates whether the response can be shared with requesting code from the given origin.

Syntax: 
Access-Control-Allow-Origin: *
Access-Control-Allow-Origin: <origin>
Access-Control-Allow-Origin: null

**Examples:** 
A response that tells the browser to allow code from any origin to access a resource will include the following:
```js
Access-Control-Allow-Origin: *
```
A response that tells the browser to allow requesting code from the origin https://developer.mozilla.org to access a resource will include the following:
```js
Access-Control-Allow-Origin: https://developer.mozilla.org
```
Limiting the possible Access-Control-Allow-Origin values to a set of allowed origins requires code on the server side to check the value of the Origin request header, compare that to a list of allowed origins, and then if the Origin value is in the list, set the Access-Control-Allow-Origin value to the same value as the Origin value.


# What is clickjacking? How do you fix it?
**Answer->** Clickjacking is an attack that fools users into thinking they are clicking on one thing when they are actually clicking on another. Its other name, user interface (UI) redressing, better describes what is going on. Users think they are using a web page’s normal UI, but in fact there is a hidden UI in control; in other words, the UI has been redressed. When users click something they think is safe, the hidden UI performs a different action.

**Fix the Clickjacking:**

**X-Frame-Options**
X-Frame-Options is a response header. Developers can use it to protect their site against clickjacking. It can be used to indicate whether or not a browser should be allowed to render a page in an Iframe by have its value set as any of the following:

X-FRAME-OPTIONS: DENY

By specifying DENY, no site will be allowed to load the page in a frame.

X-FRAME-OPTIONS: SAMEORIGIN

On the other hand, if you specify SAMEORIGIN, you can still use the page in a frame as long as the site including it in a frame is the same as the one serving the page.

X-FRAME-OPTIONS: ALLOW-FROM uri

If you specify this, then the site can be displayed in a frame only by uri specified. However, this is an obsolete directive that no longer works in modern browsers.

Note: The Content-Security-Policy HTTP header has a frame-ancestors directive which obsoletes this header for supporting browsers. It is the next header that we are going to discuss.

**Frame-Busting**
In this technique, JavaScript that runs on user’s browser is used to stop itself being embeded into iframe and escape out of it. When the page loads, this JS code will check if the domain of the page matches the domain of the browser window. If it does then no problem, if it does not then it will escape out of the iframe and load the site in the browser by replacing the site trying to load it in the Iframe.
```js
<style>
/* Hide page by default */
html { display : none; }
</style>
<script>
if (self == top) {
// Everything checks out, show the page.
document.documentElement.style.display = 'block';
} else {
// Break out of the frame.
top.location = self.location;
}
</script>
```

**Code-Snippets:**
In this section, there are code snippets which will be handy for developers to fix clickjacking. These code snippets will basically set the HTTP response headers responsible for mitigating clickjacking. The headers are the ones that we earlier discussed in earlier in this guide.

NodeJS
```js
response.setHeader("X-Frame-Options", "DENY");
response.setHeader("Content-Security-Policy", "frame-ancestors 'none'");
```

**Web server & frameworks config** 
In this section, there are config snippets useful handy for system admins to fix clickjacking. These code snippets will basically set the HTTP response headers responsible for mitigating clickjacking. The headers are the ones that we earlier discussed in earlier in this guide.

Apache
```js
Enable mod_headers using this command
a2enmod headers
```
```js
Restart the apache server
sudo service apache2 restart
```
```js
Open and edit the config file in sites-available folder
sudo nano 000-default.conf
```
```js
Add the following lines in <Virtual host>
Header set X-Frame-Options "DENY"
Header set Content-Security-Policy "frame-ancestors 'none'"
```
```js
Again restart the apache server
sudo service apache2 restart
```


# What are some performance metrics for your website?
**Answer->** 

1. **Website Speed:**
While the term website speed may simply conjure load time, insights into this particular metric actually go much deeper.
As attention spans shorten, you need to determine how your site is performing in a number of speed-related functions.

These include:

**Time to Title**
This time measurement refers to the amount of time from a visitor’s website request to the moment your site title manifests on the browser tab. This matters for visitors as a speedy title appearance ensures them that your site is legitimate.

**Time to Start Render**
This time measurement refers to the amount of time elapsed between a user request and when content materialized in-browser. Much like time to title, the quicker this happens, the more likely the visitor is to stay on the page.

**Time to Interact**
Referring to the time it takes from request origination and when the visitor can take an action (click on links, scroll page, type, etc.), time to interact is also vital when it comes to how long a visitor will stay on your site.

While there are more in-depth metrics associated with website speed, starting with these three can be the first step toward improving your site speed overall.

To find these numbers for your respective pages, you can use a free webpage speed test tool.

2. **Number of Assets:**
The term “assets” refers to the materials that compose your page. Think: text content, audio, video, etc. Behind the scenes, each of these elements takes time to load. As you include more and more assets on a page, you can seriously slow down your page-load time.

3. **Error Rate:**
This metric tracks the percentage of request issues your site generates in comparison to the total number of requests. If you see a spike in these figures, you know you are about to run into a major issue. By keeping an eye on your error rate, you can diagnose and fix issues preemptively. However, without an eye toward your error rate, you can run into challenges that can take down your entire site and leave you correcting in real-time.

4. **Bounce Rate:**
This metric refers to the number of users who are departing from your site shortly after arriving. In addition to impacting conversions and overall performance, a high bounce rate can have a negative impact on SEO since it can serve as an indicator that your site isn’t delivering what it promised.

5. **Conversion Rate:**
Convert, convert, convert is a common mantra in the marketing world. When you track your conversion rate, you gain viability into the quality of your leads, as well as how effective your website is as a whole.

For example, if you have a low conversion rate and a high traffic rate, you can infer that your on-page conversion tactics are not working as well as those off-site.

# What does the following term mean?
   - Time to first byte,
   - Page load time
**Answer->**  Time to first byte:

Time to First Byte (TTFB) refers to the time between the browser requesting a page and when it receives the first byte of information from the server.

Page Load Time:

Page load time is the time it takes for a page to load, measured from navigation start to the start of the load event.


# What do CDN or Content Delivery Networks do? When do you need a CDN?

**Answer->** A content delivery network (CDN) refers to a geographically distributed group of servers which work together to provide fast delivery of Internet content.
A CDN allows for the quick transfer of assets needed for loading Internet content including HTML pages, javascript files, stylesheets, images, and videos. 

The popularity of CDN services continues to grow, and today the majority of web traffic is served through CDNs, including traffic from major sites like Facebook, Netflix, and Amazon.

A properly configured CDN may also help protect websites against some common malicious attacks, such as Distributed Denial of Service (DDOS) attacks.


# What is the difference between Client Side Renderring and Server Side Renderring?

**Answer->** Client-side rendering manages the routing dynamically without refreshing the page every time a user requests a different route. But server-side rendering is able to display a fully populated page on the first load for any route of the website, whereas client-side rendering displays a blank page first.

# What is Progressive Renderring?
**Answer->** Progressive Rendering is the technique of sequentially rendering portions of a webpage in the server and streaming it to the client in parts without waiting for the whole page to rendered.
 
![progressive-rendering](https://user-images.githubusercontent.com/80479635/161891418-dd58741c-38b4-43b9-bdcf-146ed35a662b.png)

# What is the difference between Preloading and Prefetching resources?

**Answer->** Preload is an early fetch instruction to the browser to request a resource needed for a page (key scripts, Web Fonts, hero images). Prefetch serves a slightly different use case — a future navigation by the user (e.g between views or pages) where fetched resources and requests need to persist across navigations.
![preload-prefetch](https://user-images.githubusercontent.com/80479635/161891494-682299a7-be8a-46d0-960a-10ddd47638e8.png)

# What are service workers?
**Answer->** A service worker is a type of web worker. It's essentially a JavaScript file that runs separately from the main browser thread, intercepting network requests, caching or retrieving resources from the cache, and delivering push messages.

**OR**

Service workers are specialized JavaScript assets that act as proxies between web browsers and web servers. They aim to improve reliability by providing offline access, as well as boost page performance.
