# Islands Architecture

> "SEO and UX aren’t a tradeoff"

The following document explains what is, when we should use, PROS/CONS using Islands Architecture.

## 📖 Summary

1. [What it is?](#1-what-it-is)
2. [When we should use it](#2-when-we-should-use-it)
3. [PROS](#3-pros)
4. [CONS](#4-cons)

---

## 1. What it is?

Island Architecture is used when rendering HTML pages on the server. These pages consist of various applications such as the header, cart, and footer apps. Each application has its own HTML and is referred to as slots. If certain applications require interactivity for users, we can "hydrate" the application by sending JavaScript code to add interactivity. For instance, a button with a click action can be rendered on the server but needs to be hydrated in order to enable the click event.


## 2. When we should use it

We can use it when we need to reduce the volume of JavaScript shipped in our application. If some of our pages need only HTML and CSS to work, we don't need to load unnecessary Javascript to them. Another scenario is when a page has some part with dynamic content, so we can server-side render all of their static content. The rendered HTML will include placeholders for dynamic content, that placeholders contain self-contained component widgets. Each widget is similar to an app and combines server-rendered output and JavaScript used to hydrate the app on the client.


## 3. PROS

- 3.1 [Performance](#31-performance)
- 3.2 [SEO](#32-seo)
- 3.3 [important content](#33-prioritizes-important-content)
- 3.4 [Component-based](#34-component-based)
    

### 3.1 Performance

The amount of JavaScript code shipped to the client is reduced, because the javascript sent only the required code for interactive components

### 3.2 SEO

Since all of the static content is rendered on the server; pages are SEO-friendly.


### 3.3 Prioritizes important content

Key content (especially for blogs, news articles, and product pages) is available almost immediately to the user. Secondary functionality for interactivity is usually required after consuming the key content becomes available gradually.

### 3.4 Component-based

The architecture offers all advantages of component-based architecture, such as reusability and maintainability.

## 4. CONS

- 4.1 [Implement Support](#41-limited-support)
- 4.2 [Community Suport](#42-community-suport)
- 4.3 [Highly interactive](#43-highly-interactive)

### 4.1 Limited Support

The concept is still in a nascent stage, the only options available to developers to implement Islands are to use one of the few frameworks available or develop the architecture yourself. 

### 4.2 Community Suport

Community discussion about the idea is in the beginning. So if you have some problem during the implementation you don't find many answers is community blogs.

### 4.3 Highly interactive

The architecture is not suitable for highly interactive pages like social media apps which would probably require thousands of islands.

**[⬆ back to summary](#-summary)**