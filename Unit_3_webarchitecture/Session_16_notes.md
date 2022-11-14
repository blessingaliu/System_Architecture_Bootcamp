## 16th Session: Evolution of Web Architecture

## Modern Web App Architecture

- A web app is a client-server application, where there’s a browser (a client) and a web server. The logic of a web application is distributed among the server and the client, there’s a channel for information exchange, and data storage located locally or in the cloud.

## Types of Web Application Architecture

### Server Side Rendering (SSR)

- Server-side rendering is the most common method for displaying information onto the screen. It works by converting HTML files in the server into a fully rendered HTML page for the client.
- The content is fetched from the server and passed to the browser to the displayed to the user. The user has to navigate to the page before the browser fetches a page from the server
- Now imagine browsing a webpage and having to wait for each and every page to render when navigating the site.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/37a11bea-8374-4ece-b5cf-1ba559c27943/Untitled.png)

### Client Side Rendering

- Content is rendered in the browser using the client-side JavaScript library.
- The browser does not make a new request to the server when a new page is loaded

### Static site generation (SSG)

- This is a tool t**hat generates a full static HTML website based on raw data and a set of templates**. Essentially, a static site generator automates the task of coding individual HTML pages and gets those pages ready to serve to users ahead of time.
- Because these HTML pages are pre-built, they can load very quickly in users' browsers.

### Single Page Application (SPA)

- SPA is the type of web application that works within a browser. It doesn’t require reloading the page when new data needs to be displayed.
- eg Facebook, Gmail, Google Maps, GitHub and Twitter
- A single-page application (SPA) is a web application or a website, which is able to **dynamically rewrite a web page** in a web browser instead of loading the entire page every time in response to user actions. With that being said, user actions such as clicking on certain buttons or links don’t force the page to reload in web browser.
- SPAs are able to dynamically rewrite web page content through JavaScript’s ability to manipulate the elements on the existing page. In contrast, multi-page applications or websites load entirely new pages in response to user actions.

A single-page application **loads only the requested content**. This would result in much faster communications and content reloading. In multiple-page application, the user is forced to wait for the page to load, even if most of the page’s content remains the same.

- When a user requests (opens) web application or website in a web browser, single-page application loads all necessary HTML, CSS and JavaScript files to bootstrap the web page.
- When a user requests (opens) web application or website in a web browser, single-page application loads all necessary HTML, CSS and JavaScript files to bootstrap the web page.

A Single-page application doesn’t reload the entire page, only required parts of the page. It significantly improves application speed and makes seamless user experience. As users navigate through web application, most of the resources such as CSS and JavaScript files are downloaded only once, and don’t need to be reloaded during the usage.

Only data that are transmitted to and from the server changes. This decreases the server-client traffic and makes single-page application faster to user requests.

[https://andrejgajdos.com/single-page-application-vs-multiple-page-application/](https://andrejgajdos.com/single-page-application-vs-multiple-page-application/)

## Monolith Architecture

A monolithic application is self-contained, tightly coupled software application.

- it has a single point of failure

## Microservices Architecture

- Different features of the application are deployed seperately as smaller loosely coupled services called microservices
- These microservices work in conjunction to form a large distributed online service as a whole