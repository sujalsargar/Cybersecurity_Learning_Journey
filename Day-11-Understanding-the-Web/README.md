# Day 11 - Understanding the Web

## Objective
Understand how the web works behind the scenes, learn the major components of a web browser, and understand why every stage of loading a webpage can become an attack surface.

---

## Lesson of the Day

Today, I learned that a web browser is much more than an application used to open websites.

When we open a webpage, we are interacting with one of the most complex pieces of software running on our device. A browser performs many tasks within milliseconds to fetch, process, and display a webpage.

One important lesson from today was:

> **Every step involved in loading a webpage is a potential attack surface.**

Understanding how the web works is essential before learning about web security and web application attacks.

---

## What Does a Browser Do?

A modern browser is made up of several important components:

### 1. Renderer
Displays the webpage by converting HTML, CSS, and JavaScript into what we see on the screen.

### 2. Script Engine
Executes JavaScript code that makes websites interactive.

### 3. Network Client
Communicates with web servers by sending requests and receiving responses.

### 4. Storage System
Stores information such as:
- Cookies
- Cache
- Local Storage
- Session Storage

This helps websites remember user preferences and improve performance.

### 5. Security Boundary
The browser isolates websites from one another using security mechanisms such as the Same-Origin Policy and browser sandboxing, helping reduce the impact of malicious websites.

---

## What Happens When We Press Enter?

When we type a website address and press **Enter**, the browser performs several steps:

### 1. DNS Lookup
Converts the domain name into an IP address.

### 2. TCP Connection
Establishes a reliable connection with the server.

### 3. TLS Handshake
Creates an encrypted HTTPS connection.

### 4. HTTP Request
The browser requests the webpage from the server.

### 5. HTTP Response
The server sends back HTML and other resources.

### 6. Resource Fetching
The browser downloads additional resources such as:
- CSS files
- JavaScript files
- Images
- Fonts
- Videos

### 7. Rendering
The browser builds and displays the webpage.

### 8. Ongoing Communication
Modern websites continue communicating with servers after loading to fetch notifications, updates, messages, and other dynamic content.

---

## Frontend vs Backend

### Frontend
The part of the website users interact with.

Examples:
- Buttons
- Forms
- Images
- Navigation menus
- Animations

### Backend
The part users do not see.

It handles:
- Databases
- Authentication
- Business logic
- APIs
- Server-side processing

The frontend displays information, while the backend processes requests and manages data.

---

## The Three Layers of Every Webpage

### 1. HTML (Structure)
Defines the content and structure of a webpage.

Examples:
- Headings
- Paragraphs
- Images
- Buttons

---

### 2. CSS (Style)
Controls the appearance of the webpage.

Examples:
- Colors
- Fonts
- Layout
- Spacing
- Animations

---

### 3. JavaScript (Behavior)
Makes webpages interactive.

Examples:
- Form validation
- Pop-ups
- Dynamic content
- Interactive menus
- Real-time updates

---

## Security Perspective

One of the biggest lessons today was understanding that every stage of loading a webpage can be attacked.

Potential attack surfaces include:
- DNS attacks
- Man-in-the-Middle (MITM) attacks
- HTTP request manipulation
- Malicious JavaScript
- Cross-Site Scripting (XSS)
- Cookie theft
- Resource injection

Understanding how the web works is the foundation for learning web application security.

---

## What I Learned

- A browser is a complex piece of software with multiple components.
- Browsers perform many operations before displaying a webpage.
- Websites are built using HTML, CSS, and JavaScript.
- Frontend and backend have different responsibilities.
- Every stage of loading a webpage can become an attack surface.

---

## Key Takeaways

✅ Browsers do much more than simply display webpages.

✅ Websites are built using:
- HTML (Structure)
- CSS (Style)
- JavaScript (Behavior)

✅ Frontend is what users interact with.

✅ Backend processes requests and manages data.

✅ Every stage of web communication can be targeted by attackers.

---

## Reflection

Today's lesson helped me appreciate how much work happens behind the scenes every time I open a website. Before this, I simply saw webpages loading without thinking about the many processes involved.

Learning about browsers, frontend, backend, and the webpage loading process has given me a stronger foundation for understanding web application security. It also reinforced the idea that every layer of a web application can become a potential target for attackers.

---

## Quote of the Day

> "To secure the web, you must first understand how the web works."

---

## Progress Tracker

- Day: 11/90
- Topic: Understanding the Web
- Concepts Learned: Browser Components, DNS, TCP, TLS, HTTP, Rendering, Frontend, Backend, HTML, CSS, JavaScript
- Key Insight: Every step involved in loading and rendering a webpage is a potential attack surface.
- Status: ✅ Completed
