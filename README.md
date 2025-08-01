# HTTP
<img src="https://i.imgur.com/PE14J3Y.jpg">

# Intro to Full-Stack Development & HTTP

## Learning Objectives

| Students Will Be Able To: |
|---|
| Explain Full-Stack Web Development |
| Describe Client/Server Architecture |
| Explain the Anatomy of HTTP Requests and Responses |
| Identify the Two Key Components of an HTTP Request |
| Explain How HTTP Requests Can be Initiated From a Browser |
| Explain How HTTP Requests Result in Code Running on a Server |

## Road Map

1. Why Learn Full-Stack Web Development?
2. What is a Full-Stack Developer?
3. SEI Web Technology Stacks
4. Client/Server Architecture
5. What is HTTP?
6. Let's Make an HTTP Request
7. Anatomy of an HTTP Request/Response Messages
8. The Two Key Components of an HTTP Request
9. HTTP Methods
10. URLs
11. Ways to Send HTTP Requests From the Browser
12. How HTTP Requests Run Code on the Server
13. Essential Questions
14. Further Study

## 1. Why Learn Full-Stack Web Development?

According to U.S. News & World Report the fifth best job in 2022 was that of a **Software Developer**!  In [U.S. News & World Report - 100 Best Jobs of 2023](https://money.usnews.com/careers/best-jobs/rankings/the-100-best-jobs) it's the 1st best job - how cool is that! 

Further, according to [this 2022 StackOverflow Developer Survey](https://survey.stackoverflow.co/2022/#developer-profile-developer-roles), **the role of Full-stack Developer is the most popular** as compared to other developer types.

Full-stack engineering roles are often some of the highest demand roles in the software engineering space. They are expected to be knowledgeable of many various topics in software engineering and it's often a great opportunity to increase you market value and learn more about the profession and what specific discipline you'll like to grow further.

The bottom-line is: **Full-stack Developers are in demand**!

## 2. What is a Full-Stack Developer?

A full-stack developer:

- Is a developer who is comfortable working with both frontend, middleware & back-end technologies.

- Can create full-stack applications by writing code that runs in both the browser and a web server.

- Will often **specialize** in frontend or back-end technologies.

- Is a graduate of Software Engineering Immersive!

## 3. SEI Web Technology Stacks

### Web Technology Stack - Unit 2

In this unit, we'll learn 3 of the 4 technologies that comprise the MERN-Stack:

<img src="https://i.imgur.com/FKGehuM.jpg">

### Web Technology Stack - Unit 3

In Unit 3, we'll learn:

<img src="https://i.imgur.com/GuogOfX.png">
<img src="https://i.imgur.com/MjX4aD7.png">

### Web Technology Stack - Unit 4

In Unit 4, we go full MERN-stack:

<img src="https://i.imgur.com/jlKEj7F.png">

## 4. Client/Server Architecture

<img src="https://i.imgur.com/clxiqnO.png">

The terms **client** and **server** can refer to both a **physical device** (computer, tablet, phone, etc.) but can also refer to a **software process**. For example:

- Database software such as PostgreSQL and web servers like Apache are examples of software processes behaving as servers.
- Browser software such as Chrome or Firefox are examples of software clients.
- Physical **servers** connected to the Internet are also referred to as **hosts**.
- Web developers usually think of a "web browser" when they hear "client".
- Often times you'll hear of servers being called **clients**. **Client** is used to define a piece of software that makes requests from another piece of software. It is important to realize that sometimes **clients** are also servers, and at times a server could play the role of **client** and **server**.

> Note: During development, your computer will play the role of BOTH client and web server.

## 5. What is HTTP?

**Hypertext Transfer Protocol (HTTP)** is an application-level network protocol that powers the communications across the [World Wide Web](https://en.wikipedia.org/wiki/World_Wide_Web), more commonly referred to as just **the Web**.

**HTTP is fundamental to web development** - regardless of which back-end or front-end web technology/framework is used.

When a user interacts with an amazing **web application** we developed, it's **HTTP** that informs the **web application** what the **browser** wants and it's **HTTP** that delivers the goods from the server back to the browser. For example, when the user browses to our app:

<img src="https://i.imgur.com/JDFHoZl.png" style="width:80%">

When the response is received by the client, that request/response cycle has ended and there will be no further HTTP communications unless another request is sent by the client.

> Note: It is helpful to note that http is not the only message transfer protocol used in software development. There are numerous alternative protocols all with their own advantages and disadvantages. Protocols like RPC(remote procedure calls), WS(websocket), HTTPS(hyper text transfer protocol secure), FTP(file transfer protocol), SMTP(simple mail transport protocol) among many others. Feel free to look into these alternatives to http at [w3schools types of protocols](https://www.w3schools.in/types-of-network-protocols-and-their-uses) as well as other places on the web, it is a very large topic with decades of development put into it. Keep in mind that these protocols are built on top of other protocols like TCP/ip or UDP/ip, however, we will not be diving too deeply into these topics in this course.

## 6. Let's Make an HTTP Request

Let's open a new tab in Chrome, open DevTools, and click on the **Network** tab where we can inspect HTTP requests and responses.

Now let's browse to General Assembly's site by typing **generalassemb.ly** in the address bar...

Wow! Each one of those lines represents a separate HTTP request made to a server!  Find the line in the left-side pane with **generalassemb.ly** and click on it:

<img src="https://i.imgur.com/fuED3VM.png" style="width:80%">

In the pane on the right you will find all of the information about a particular HTTP request. Select the **Headers** tab and explore!:

<img src="https://i.imgur.com/44W3zEE.png" style="width:80%">

## 7. Anatomy of HTTP Request/Response Messages

The following diagrams an HTTP Request and Response Message: 

<img src="https://i.imgur.com/kCuWuw7.png">

Notice they both have a **Start Line** followed by **Headers**, an **Empty line**, and finally the **Body** of the message.
	
### The Status Code of the Response

The [status code](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html) in the first line of the response message informs us how the request/response went.

It is always a three-digit number that falls within the following ranges/categories:

- 1xx Informational
- 2xx Success
- 3xx Redirection
- 4xx Client Error
- 5xx Server Error

Most HTTP responses will have a status code of `200`, which means **OK**. You also might be familiar with the status code of `404` - **Not Found**.

### The Body of the Message

The **Body** contains the data being sent to the server (if any) and the data being returned by the server

The **Content-Type** header is a [MIME type](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types) and helps the browser determine what to do with the data being sent in the **body** of the HTTP response. For example:
- **text/html**: The browser will parse the **body** as HTML and, depending on how the HTTP request was initiated, usually **replace** the browser window's content with the newly received HTML.
- **image/png**

Although the HTTP protocol is text-based, the content in the body can be binary, for example, images are typically transferred in a binary format.

## 8. The Two Key Components of an HTTP Request 

We saw earlier that every HTTP request message begins with a request-line like this:

```
GET /puppies HTTP/1.1
```

**The two key components of any HTTP request are**:

- The **HTTP method** (`GET` in the example above), and
- The **Path**/**Endpoint** (`/puppies` in the example), also referred to as the **URL** (although more accurately is a **URI**)

The reason these are the key components are because most web frameworks use them to match routes defined on the server (more on routes in a bit).

## 9. HTTP Methods

[HTTP methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods), are used to indicate the desired **action** to be performed for a given resource (specified by the URL) on the server.

The fact that they indicate **action** is why they are also at times called **HTTP Verbs**.

We'll be using the following HTTP Methods when we start defining our application's routes: 

| HTTP Method (Verb) | Desired Action on Server |
|:-:|:-:|
| `GET` | The GET method requests a representation of the specified resource (URL). Requests using GET should only retrieve data. |
| `POST` | The POST method is used to create a resource on the server. |
| `PUT` | The PUT method is used to update a resource on the server. |
| `DELETE` | The DELETE method deletes the specified resource. |

> note: There dozens of additional http verbs that you will likely encounter in your career. It is helpful to be aware of the most common http verbs and to understand how they can be used. See this documentation from [Mozilla's developer network](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods) that explains the 9 most common http verbs. If you choose to dig deeper and investigate the http protocol specifics, you'll see that there are about [39 different http verbs in http1.1](http://www.iana.org/assignments/http-methods/http-methods.xhtml). Even if an http verb is included in the protocol spec, that doesn't mean that all http clients will support all of these verbs, you most likely will not encounter the majority these verbs in your career, but it is helpful to understand how these protocols are designed and utilized.

## 10. URLs

**URL** stands for **Uniform Resource Locator**.

The URL informs the server of what resource the client wants to GET. create (POST), DELETE or UPDATE.

Here's the complete anatomy of a URL:

<img src="https://i.imgur.com/w1igQx0.png">

Developers often refer to just the **path** as a URL.

## 11. Ways to Send HTTP Requests From the Browser

These are ways that a browser can send an HTTP Request:

| Action | HTTP Method(s) Possible |
|---|---|
| Using the _address bar_ | GET |
| User submits an HTML form | POST, GET (used for searches) |
| User clicks a link | GET |
| Using JavaScript | All Methods can be sent using [AJAX](https://developer.mozilla.org/en-US/docs/Web/Guide/AJAX)|

**👀 In this unit our apps will rely on the user clicking links (`<a>` elements) and submitting forms (`<form>` elements) to interact with the app - that's it!**

## 12. How HTTP Requests Run Code on the Server

As full-stack web developers, we'll create user interfaces that display in the browser.

As a user interacts with the app by clicking links and submitting forms, they will cause HTTP requests to be sent to our back-end web application.

In our web app on the back-end, we will create **routes** that listen for these requests from the front-end, and...

Those routes will map HTTP requests to our back-end **code**!

As an example, you want your app to add a new user to your database when they sign up...

<img src="https://i.imgur.com/ltB5IYA.png">

1. The user submits the sign up form.

2. An HTTP request message with the form's data in the request body leaves the browser.

3. The HTTP request is received by the web app's routing and, in this case, would match the route defined to match a `POST /users` (**HTTP Method** & **Path**) HTTP request.

4. The purpose of a defined route is to map an HTTP request to code which is typically a function defined in the "controller" module.  The controller function would perform any necessary data operations, etc.

5. The controller function ultimately responds with an HTTP Response which can either:
    - Containing an HTML page in the message body (in the case of a GET request)
    - Or, with a Status Code of 302 (Redirect), make the browser issue a new GET request.

## 13. ❓ Essential Questions

<details>
<summary>
(1) What is the most common network protocol of the web?
</summary>
<hr>

**HTTP** (Hypertext Transfer Protocol)

<hr>
</details>

<details>
<summary>
(2) Name three HTTP methods/verbs.
</summary>
<hr>

**`GET`**, **`POST`**, **`PUT`** and/or **`DELETE`**

<hr>
</details>

<details>
<summary>
(3) What are the two key components of an HTTP Request that are typically used to match a route on the server?
</summary>
<hr>

The **HTTP Method/Verb** and the **Path/Endpoint/URL**

<hr>
</details>

<details>
<summary>
(4) Explain how an HTTP request makes code run on the server.
</summary>
<hr>

1. An HTTP Request leaves the browser due to user clicking a link, submitting a form or making an API request.

2. The HTTP Request matches a route in the app.

3. The route maps the request to code.

4. The code runs and ultimately sends an HTTP Response back to the browser.

<hr>
</details>

## 14. Further Study

### Ways to Send HTTP Requests Without Using the Browser

There are plenty of developer tools that enable us to issue HTTP requests to servers without using a browser. Pieces of software that perform http request are typically referred to as http **clients**.

- One tool we use later in the course is [Postman](https://www.getpostman.com/). Postman is a critical web development tool. It is extremely powerful and used almost universally across the web development field. Being competent in postman is a critical skill that will prove invaluable throughout your career. The postman team provides [exceptional documentation and guides](https://learning.postman.com/docs/getting-started/introduction/) for using their tool.

- If you prefer to use a command-line tool, most operating systems already have a tool called [cURL](https://en.wikipedia.org/wiki/CURL). If your computer doesn't have cURL installed, you may choose to install it. To learn more about cURL feel free to review this [cURL documentation](https://curl.se/docs/) as well as their [free PDF](https://everything.curl.dev/) that teaches you everything you'd want to know about cURL. Becoming a master of cURL is not a requirement to work in software engineering or mandated by this class, however, its presence is ubiquitous in the software engineering space and you will most likely encounter cURL in many online tutorials and during your career.

- A server with access to a network that supports http communication. We'll be using our node.js servers as http clients in this class when we cover the axios library.


<center>
	
![seperation](https://github.com/user-attachments/assets/6b3a622b-3f38-443c-9ba4-91af2b847912)

<img width="871" height="423" alt="mvc" src="https://github.com/user-attachments/assets/0aa4a63f-ecc8-4872-83cb-28da34501cf5" />

![mvcmeme](https://github.com/user-attachments/assets/62b80a79-f865-4cd2-b8f6-63e919a03ade)


![rest](https://liberty.sfs-flex.com/images/rest.png)

</center>

1. **CRUD**: CRUD stands for Create, Read, Update, Delete. It's a way of remembering the four basic functions that you need for working with any data in a system. Think of CRUD like a to-do list. You can create a new task, read the tasks you already have, update a task you've already created, and delete a task you no longer need.

2. **REST**: Representational State Transfer, or REST, is an architectural style for creating web services. A RESTful API uses HTTP requests to GET, PUT, POST, and DELETE data. It's like a menu at a restaurant. Each endpoint (or "dish") represents a specific resource that can be accessed and manipulated using standard HTTP methods.

3. **MVC**: MVC stands for Model-View-Controller. It's an architectural pattern used in software development. The model represents the data, the view is the user interface, and the controller handles the logic and communication between the model and the view. MVC is like a chef in a kitchen. The chef separates the different aspects of preparing a meal (the model, the view, and the controller) and assigns specific tasks to each aspect.

4. **Server-side Rendering (SSR)**: Server-side rendering is when your webpage is built on the server each time someone makes a request for a page. This is how many traditional webpages work. It's like a chef preparing a dish in the kitchen before bringing it out to the customers.

5. **Client-side Rendering (CSR)**: Client-side rendering is when the webpage is created in the browser using JavaScript. The server sends a response with an HTML file that's practically empty and then JavaScript kicks in to load the content. It's like a customer at a habachi restaurant ordering a dish and then being able to see the food prepared in front of them.

6. **Consuming an API**: Consuming an API is like ordering food at a restaurant. You make a request to an API to retrieve or manipulate data. The API then sends back the appropriate response, just like a server bringing your dish to the table.

7. **Separation of Concerns**: Separation of concerns is about keeping different parts of your code separate so that they each do one thing. It's like a chef having different stations in the kitchen. Each station is responsible for a specific task.

8. **Component-Driven Development**: Component-driven development is a method in which the application is built from individual, reusable components. Each component has its own logic and controls its own rendering. It's like building with LEGOs. Each LEGO piece represents a component, and you can use different components to build different things.

9. **Client-Server Model**: The client-server model is a communication structure that separates tasks or workloads between providers (servers) and service requesters, called clients. It's similar to a game of chess where the client, like the player, makes requests and the server, like the opponent, receives requests and responds.

10. **IP Address**: An IP address is a unique string of numbers separated by periods that identifies each computer using the Internet Protocol to communicate over a network. It's like the street address for your computer on the vast internet neighborhood.

11. **Port**: A port on a computer is like a doorway. It provides access to specific services or applications running on the device. Each port corresponds to a specific function and directs different types of internet traffic to the appropriate service or application.

12. **DNS**: DNS stands for Domain Name System. It's like the phone book of the internet. Instead of remembering IP addresses, DNS servers give us human-friendly names like 'google.com'. 
