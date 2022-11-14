## 13th Session: Web Architecture

## How does the web works

- The world wide web, or web for short, are the pages you see when you're at a device and you're online.
- The internet is the network of connected computers that the web works on, as well as what emails and files travel across

## Clients and Servers

- Clients are internet-connected devices like your phone or laptop responsible for making HTTP get requests.
- Servers are computers that store webpages, sites or apps. When a client device wants to access a webpage, a copy of the webpage is downloaded from the server onto the client machine to be displayed in the user’s web browser.

-------

## DNS

- The Domain Name System (DNS) is **the phonebook of the Internet**
- Humans access information online through domain names, like nytimes.com or espn.com. Web browsers interact through Internet Protocol (IP) addresses.
- DNS translates domain names to IP addresses so browsers can load Internet resources.

-------

## IP Address

- An IP address is **a unique address that identifies hardware device on the internet or a local network.**
- The addresses allow these devices to connect to one another and transfer data on a local network or over the internet.
- 32 bit eg 192.0.2.1
- A **private IP address** is used to connect your computer or device to your home or business network. This address is normally assigned by your network router.
- Private IP addresses are in the range 40.xxx.xxx.xxx or 192.168.xxx.xxx. An example of a private IP address is 192.168.1.1.
- Your **public IP address**
 is used to connect your home or business network to the internet. This address is assigned by your internet service provider (ISP).

## HTTP

- Protocol that defines a language for clients and servers to speak to each other
- HTTPS is HTTP with encryption. The only difference between the two protocols is that **HTTPS uses TLS (SSL) to encrypt normal HTTP requests and responses.**

## Component files:

- **Code files:** HTML, CSS, JavaScript
- **Assets:** images, music, video.

## HTTP Request and Response b/w Client and Server


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1652122253432/p1aVkJs2Q.png align="left")

- **When you type a web address into the browser**

1. The browser goes to the DNS server, and finds the real address of the server that the website lives on
2. The browser sends an HTTP request message to the server, asking it to send a copy of the website to the client. This message, and all other data sent between the client and the server, is sent across your internet connection using TCP/IP.
3. If the server approves the client's request, the server sends the client a "200 OK" message, which means "Of course you can look at that website! Here it is", and then starts sending the website's files to the browser as a series of small chunks called data packets.
4. The browser assembles the small chunks into a complete web page and displays it to you (the goods arrive at your door — new shiny stuff, awesome!).

## Order in which components are parsed

- The browser parses the HTML file first, and that leads to the browser recognizing any `<link>`element references to external CSS stylesheets and any `<script>`element references to scripts.
- As the browser parses the HTML, it sends requests back to the server for any CSS files it has found from `<link>` elements, and any JavaScript files it has found from `<script>` elements, and from those, then parses the CSS and JavaScript.
- The browser generates an in-memory [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) tree from the parsed HTML, generates an in-memory [CSSOM](https://developer.mozilla.org/en-US/docs/Glossary/CSSOM) structure from the parsed CSS, and [compiles and executes](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work#javascript_compilation) the parsed JavaScript.
- As the browser builds the DOM tree and applies the styles from the CSSOM tree and executes the JavaScript, a visual representation of the page is painted to the screen, and the user sees the page content and can begin to interact with it.

## Client-side vs Server-side

- Client side being the part the user can see (frontend) - HTML for the structure, CSS for the styling, JavaScript for the dynamic content.
- The server side being the application logic (backend) - nodejs, PHP, Python

## Client-server architecture

- Any number of clients can connect the server and make requests. The server has to process these requests and send the response to the client
- This client-server architecture is commonly called the two-tier architecture

## Three-tier architecture

1. **Presentation tier** 
- User interface and communication layer of the application, where the end user interacts with the application.
- This top-level tier can run on a web browser, as desktop application, or a graphical user interface (GUI), for example.
- Web presentation tiers are usually developed using HTML, CSS and JavaScript.

2. **Application tier** 
- The application tier, also known as the logic tier or middle tier, is the heart of the application.
- In this tier, information collected in the presentation tier is processed - sometimes against other information in the data tier - using business logic, a specific set of business rules. The application tier can also add, delete or modify data in the data tier.
- The application tier is typically developed using Python, Java, Perl, PHP or Ruby, and communicates with the data tier using [API](https://www.ibm.com/cloud/learn/api) calls.

3. **Data tier**
- The data tier, sometimes called database tier, data access tier or back-end, is where the information processed by the application is stored and managed.
- This can be a relational database management system such as PostgreSQL, MySQL, MariaDB, Oracle, DB2, Informix or Microsoft SQL Server, or in a NoSQL Database server such as Cassandra, CouchDB or MongoDB.

## Document Object Model (DOM)

- The DOM is a standard defined by the W3C (World wide web consortium)
- It defines the logical structure of documents and the way a document is accessed and manipulated
- The DOM is a tree-like representation of the web page that gets loaded into the browser.
- It represents the web page using a‌‌ series of objects. The main object is the document object, which in turn houses other objects which also house their own objects, and so on.

### HTML DOM

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1652122283984/XRyZvgJ5x.png align="left")

### The Node Object

You can access any element by using the following properties with the node object:

- `node.childNodes` – accesses the child nodes of a selected parent‌‌
- `node.firstChild` – accesses the first child of a selected parent‌‌
- `node.lastChild` – accesses the last child of a selected parent.‌‌
- `node.parentNode` – accesses the parent of a selected child node.‌‌
- `node.nextSibling` – accesses the next consecutive element (sibling) of a selected element.‌‌
- `node.previousSibling` – accesses the previous element (sibling) of a selected element

### The Document Object

- This is the top most object in the DOM. It has **properties** and **methods** which you can use to get information about the document using a rule known as dot notation
- **After the document, you place a dot followed by a property or method.**

### The querySelectorAll() method

- You use this method to access one or more elements from the DOM that matches one or more CSS selectors:

```python
document.querySelectorAll('p')
```

### The createElement() method

- You use this method to create a specified element and insert it into the DOM:

```python
document.createElement('p')
```

### The getElementById() method

- You use this method to get an element from the document by its unique id attribute:

```python
<div id='first'> first div </div>

getElementById("first")
```

### The getElementByTagname() method

- You use this method to access one or more elements by their HTML tag name:

```python
<div id='first'> first div </div>

getElementById("div")
```

### The innerHTML property

- You use this property to access the text content of an element.

### ****The addEventListener() property****

- This property attaches an event listener to your element.
- It takes a callback which will run when that event is triggered.

```python
<button>Submit</button>‌‌

let submit_button = document.querySelector('button');‌‌
button.addEventListener( 'click' ,foo);‌‌
function foo() { alert( 'submitted!' ); 
  				btn.innerHTML = '';
          }
```

### ****The appendChild() element****

- You use this element to access one or more elements by their HTML tag name.
- It adds an element as the last child to the HTML element that invokes this method.
- The child to be inserted can be either a newly created element or an already existing one. If it already exists, it will be moved from its previous position to the position of the last child.

### ****The replaceChild() property****

- This property replaces one child element with another new or existing child element. If it already exists, it will be moved from its previous position to the position of the last child.

### ****The setAttribute() method****

- You use this method to set or change the value of an element's attribute.