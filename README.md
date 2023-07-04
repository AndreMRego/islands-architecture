# Islands Architecture

> "SEO and UX aren’t a tradeoff"

The following document explains what Islands Architecture is, when we should use it, and its pros and cons.

## 📖 Summary

1. [What it is?](#1-what-it-is)
2. [When we should use it](#2-when-we-should-use-it)
3. [Pros](#3-pros)
4. [Cons](#4-cons)

---

## 1. What it is?

Island Architecture is used for rendering HTML pages on the server. These pages consist of various applications, such as the header, cart, and footer apps, each having its own HTML and referred to as slots. If certain applications require interactivity for users, we can "hydrate" the application by sending JavaScript code to add interactivity. For instance, a button with a click action can be rendered on the server but needs to be hydrated in order to enable the click event.


## 2. When we should use it

We can use it when we need to reduce the volume of JavaScript shipped in our application. If some of our pages only require HTML and CSS to function, there is no need to load unnecessary JavaScript for them. Another scenario is when a page has a section with dynamic content. In such cases, we can perform server-side rendering for all of the static content on the page. The rendered HTML will include placeholders for the dynamic content, with each placeholder containing a self-contained component widget. Each widget functions like an app, combining server-rendered output with JavaScript that is used to hydrate the app on the client.


## 3. Pros

- 3.1 [Performance](#31-performance)
- 3.2 [SEO](#32-seo)
- 3.3 [important content](#33-prioritizes-important-content)
- 3.4 [Component-based](#34-component-based)
    

### 3.1 Performance

The amount of JavaScript code shipped to the client is reduced because only the required code for interactive components is sent.

### 3.2 SEO

Since all of the static content is rendered on the server; pages are SEO-friendly.

### 3.3 Prioritizes important content

Key content (especially for blogs, news articles, and product pages) is available almost immediately to the user. Secondary functionality for interactivity is usually required after consuming the key content becomes available gradually.

### 3.4 Component-based

The architecture offers all advantages of component-based architecture, such as reusability and maintainability.

## 4. Cons

- 4.1 [Implement Support](#41-limited-support)
- 4.2 [Community Suport](#42-community-suport)
- 4.3 [Highly interactive](#43-highly-interactive)

### 4.1 Limited Support

The concept is still in a nascent stage, and currently, developers have only a few options to implement Islands: either using one of the few available frameworks or developing the architecture themselves.

### 4.2 Community Suport

Community discussions about the idea are in the early stages. Therefore, if you encounter any problems during the implementation, you may not find many answers in community blogs.

### 4.3 Highly interactive

The architecture is not suitable for highly interactive pages like social media apps which would probably require thousands of islands.

**[⬆ back to summary](#-summary)**