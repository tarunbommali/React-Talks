# React JS

### What is React?

React is an open-source JavaScript library used for building user interfaces (UI), primarily for single-page applications (SPAs). It allows developers to create fast and interactive UIs with a component-based architecture.

### Key Features of React

1. **Component-Based Architecture**
2. **Virtual DOM (VDOM)**
3. **Declarative UI**
4. **One-Way Data Binding / Unidirectional Data Flow**
5. **JSX (JavaScript XML)**
6. **Hooks**
7. **Rich Ecosystem** - Supports libraries like React Router and Redux/Zustand

---

## Terminology

### Open Source

- It is a model for creating and sharing technology that's based on collaboration, transparency, and free distribution.
- **How it Works**:
  - **Source Code**: The code is made publicly available.
  - **Collaboration**: Developers from around the world can contribute.
  - **Licenses**: Govern how the software can be used, modified, and shared.
  - **Transparency**: Anyone can inspect, modify, and enhance the code.

### Why It's Great to Use Open Source

- **Free to Use**: No cost to use or modify.
- **Customizable**: Tailor the software to your needs.
- **Community-Driven**: Continuous improvements from a global community.

### Code Hosting Platforms

- **GitHub**, **GitLab**, **Bitbucket**

### Open Source Software Directories

- **SourceForge**, **OpenHub**, **OssWatch**

---

## Libraries vs Frameworks

### Library

- A library is a collection of pre-written code that developers can use to perform specific tasks.
- **Control Flow**: The developer controls the flow of the application. The library is called by the application code when needed.
- **Purpose**: Designed to provide reusable functionality for specific tasks.

### Framework

- A framework is a structured set of tools, libraries, and conventions that provide a foundation for building applications.
- **Control Flow**: The framework controls the flow of the application. Developers write code that fits into the framework's structure.
- **Purpose**: Provides a complete architecture for developing applications.

---

### Running JavaScript in HTML

### To Include Internal JavaScript in HTML File

```html
<body>
  <div id="root"></div>
  <script type="text/javascript">
    const rootElement = document.getElementById("root");
    const element = document.createElement("h1");
    element.textContent = "Hello World";
    element.classList.add("greeting");
    rootElement.appendChild(element);
  </script>
</body>
To Include External JavaScript in HTML File html

<script type="text/javascript" src="path.js"></script>
```


### What is the Use of React CDN?

Using a **React CDN (Content Delivery Network)** allows you to quickly include React in your HTML file **without installing Node.js** or setting up a build process.

---

### What is a CDN?

A **CDN (Content Delivery Network)** or **Content Distribution Network** is a geographically distributed network of proxy servers and data centers.

### Goals of a CDN:

- Provides **high availability** and **performance** by distributing services close to end users.

### Why Use a CDN?

- **Improved Scalability and Connectivity.**
- **Faster load times**, improving user experience.
- **Decreased bandwidth consumption.**
- **Lower latency** (_Latency is the lag between request and response_).

---

### What is JSX in React?

JSX (**JavaScript XML**) is a **syntax extension** for JavaScript that allows you to write **HTML-like code inside JavaScript**.  
It makes writing React components **easier** and **more readable**.

---

### What is Babel?

- JSX is **not valid JavaScript**.
- We need to convert JSX into JavaScript using a **code compiler**.
- **Babel** is a JavaScript compiler that translates JSX into **regular JavaScript**.

---

### What is Embedding Variables and Expressions in JSX?

We can embed **variables** and **expressions** using curly brackets `{}` in JSX.

### Example:

```jsx
const name = "React";
return <h1>Hello, {name}!</h1>;
```

### What is a Nested JSX Element?

- The `ReactDOM.render()` method **returns only one element** in the render.
- We need to wrap elements inside a **parent element** when writing nested JSX.

### Example:

```jsx
return (
  <div>
    <h1>Title</h1>
    <p>Description</p>
  </div>
);
```

---

### What is the Difference Between React and React-DOM?

React: A JavaScript library designed for building better UIs.

React-DOM: A complementary library to React that gives React access to the browser DOM.

While React provides the tools and concepts to define component-based UIs, React-DOM handles the task of rendering those interfaces in a web environment.

### Explain the Difference Between Real DOM and Virtual DOM

Real DOM: The actual DOM in the browser. Direct manipulation is slow and inefficient for frequent updates.

Virtual DOM: A lightweight copy of the Real DOM used by frameworks to optimize performance. It minimizes direct DOM manipulation by batching updates and using a diffing algorithm.

### When Does React Sync the Changes of VDOM with Real DOM?

React synchronizes the changes from the Virtual DOM to the Real DOM during a process called reconciliation. The process involves several steps:

**State & Prop Changes**: Changes in state or props trigger a re-render.

**Re-rendering**: React creates a new Virtual DOM tree.

**Diffing**: React compares the new Virtual DOM with the previous one to identify changes.

**Batch Updating**: Changes are batched for efficiency.

**Commit Phase**: Changes are applied to the Real DOM.

**Asynchronous Updates**: Updates are performed asynchronously for better performance.

---

### What is the Difference Between react.development.js and react.production.js via CDN?

**react.development.js**: Used during development and debugging. It provides detailed error messages and warnings to help catch issues early.

**react.production.js**: Used when deploying your application to production. It ensures better performance and faster load times by stripping out unnecessary development features.

### What is the Difference Between async and defer?

**Default Behavior**:
The browser pauses HTML parsing as soon as it encounters the script.
The script is fetched and executed immediately. HTML parsing resumes only after the script is fully executed.

**async Attribute**:
The script is fetched asynchronously while the HTML parsing continues.
The script is executed as soon as it is downloaded, even if HTML parsing is not complete.

**defer Attribute**:
The script is fetched asynchronously while the HTML parsing continues.
The script is executed only after the HTML parsing is complete, just before the DOMContentLoaded event.
