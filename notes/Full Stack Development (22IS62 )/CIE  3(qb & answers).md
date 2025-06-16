1. Describe the essential steps involved in setting up a basic Node.js application, including any necessary software installations and initial file creation.

Ans)

#### Setting Up a Basic Node.js Application

Node.js allows developers to write server-side applications using JavaScript. To begin building a Node.js application, you need to follow a few essential steps to set up the environment and create the necessary files.

---

#### Step 1: Install Node.js and npm

Node.js is a JavaScript runtime built on Chrome's V8 engine. It comes bundled with npm (Node Package Manager), which is used to install libraries and manage dependencies.

#### Installation Steps:

1. Visit [https://nodejs.org](https://nodejs.org).
2. Download and install the **LTS (Long Term Support)** version for your operating system.
3. Follow the installation instructions.

#### Verify Installation:

Open a terminal or command prompt and run:

```bash
node -v
npm -v
```

These commands will display the installed versions of Node.js and npm. If version numbers appear, the installation was successful.

---

#### Step 2: Create a Project Directory

Create a folder for your Node.js project:

```bash
mkdir my-node-app
cd my-node-app
```

This creates a new directory called `my-node-app` and navigates into it.

---

#### Step 3: Initialize the Project

Run the following command to generate a `package.json` file:

```bash
npm init -y
```

This file holds metadata about your project and lists dependencies. The `-y` flag uses default values to quickly create the file.

---

#### Step 4: Create the Entry Point File

Create the main JavaScript file for your application:

```bash
touch app.js
```

Open `app.js` in a code editor and add a simple log statement:

```javascript
// app.js
console.log("Hello, this is my first Node.js app!");
```

Run the file using Node.js:

```bash
node app.js
```

You should see the message printed in the console.

---

#### Step 5 (Optional): Install npm Packages

You can install external libraries to extend the functionality of your app. For example, to install `dotenv` for managing environment variables:

```bash
npm install dotenv
```

Then, use it in your code:

```javascript
require('dotenv').config();
console.log(process.env);
```

---

#### Step 6 (Optional): Create a Basic HTTP Server

You can build a simple server using Node.js built-in modules. Update `app.js` with the following code:

```javascript
// app.js
const http = require('http');

const server = http.createServer((req, res) => {
  res.writeHead(200, { 'Content-Type': 'text/plain' });
  res.end('Hello from the Node.js server!\n');
});

const PORT = 3000;
server.listen(PORT, () => {
  console.log(`Server running at http://localhost:${PORT}/`);
});
```

Run the server:

```bash
node app.js
```

Open a browser and navigate to `http://localhost:3000`. You should see the message displayed in the browser.

---

2. Identify and briefly describe two common types of APIs, highlighting a key characteristic of each type.

Ans)

1. **REST API (Representational State Transfer):**
    
    - **Description:** REST is an architectural style that uses HTTP methods (GET, POST, PUT, DELETE) to interact with resources represented in formats like JSON or XML.
        
    - **Key Characteristic:** **Statelessness** – each request from the client to the server must contain all the information needed to understand and process the request.
        
2. **SOAP API (Simple Object Access Protocol):**
    
    - **Description:** SOAP is a protocol for exchanging structured information using XML over HTTP or SMTP. It is often used in enterprise-level web services.
        
    - **Key Characteristic:** **Strict standards and formal contracts** – SOAP uses WSDL (Web Services Description Language) to define the service interface and operations.

---

3. Explain the role of the following components in Node.js architecture with a neat diagram: Event Loop, Callbacks, File System Module. How do they enable non-blocking I/O operations?

Ans)

Node.js architecture is built around several key components that work together to enable its high-performance, scalable nature. The main components include the Event Loop, Callbacks, the File System Module, and non-blocking I/O operations.

The **Event Loop** is the core of Node.js's event-driven architecture. It continuously checks for events and executes their associated callbacks. When an event occurs—such as an HTTP request or a timer firing—the Event Loop picks it up and runs the corresponding callback function. This loop allows Node.js to handle many operations concurrently without blocking the main thread 

**Callbacks** are functions that are executed in response to specific events. In Node.js, when an asynchronous operation like reading a file or making a network request is initiated, a callback is registered to be executed once the operation completes. This allows the program to continue executing other tasks while waiting for the asynchronous operation to finish 

The **File System Module** in Node.js provides methods for interacting with the file system. These methods can be either synchronous or asynchronous. Asynchronous file operations are non-blocking, meaning that Node.js can continue executing other code while waiting for the file operation to complete. Once the operation is done, the registered callback is executed with the result 

**Non-blocking I/O operations** are a key feature of Node.js. Traditional I/O operations are often blocking, which means the program waits for the operation to finish before proceeding. In contrast, Node.js uses non-blocking I/O, where the program sends a request and continues executing other tasks. When the I/O operation completes, a callback is triggered to handle the result. This approach allows Node.js to efficiently manage multiple operations simultaneously 

![Node.js architecture](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*DM9fWkNd5VywUMZTRRs8Ww.jpeg)

This architecture enables Node.js to deliver high performance and responsiveness, especially in applications that require handling many concurrent connections or real-time interactions 

---

4. State 5 differences between Angular and React.

Ans)
#####  Framework Type
- **Angular** is a full-fledged framework developed by Google, built with TypeScript, and follows a component-based architecture. It provides a comprehensive solution with built-in features for routing, state management, and form handling 
- **React** is a JavaScript library focused on the view layer, developed by Meta. It requires additional libraries for routing (e.g., React Router) and state management (e.g., Redux) 

##### Language and Learning Curve
- **Angular** uses **TypeScript** by default, which adds static typing and improves code maintainability. However, this introduces a steeper learning curve, especially for beginners unfamiliar with TypeScript and Angular-specific concepts like dependency injection and modules 
- **React** primarily uses **JavaScript** (though it supports TypeScript) and has a gentler learning curve. It allows developers to start building UI components quickly, making it more beginner-friendly 

##### Data Binding
- **Angular** supports **two-way data binding**, which automatically synchronizes data between the model and the view. This can simplify development but may impact performance in large-scale applications 
- **React** uses **one-way data binding**, where data flows in a single direction from parent to child components. This approach enhances predictability and makes debugging easier 

##### Performance
- **Angular** uses the **real DOM**, which can be less efficient for large applications due to frequent re-renders. However, the Ivy rendering engine has improved performance with smaller bundle sizes and optimized change detection 
- **React** uses a **virtual DOM**, which minimizes direct updates to the real DOM, resulting in better performance for dynamic and frequently updated UIs 

##### Flexibility and Ecosystem
- **Angular** is more opinionated and provides a structured, all-in-one solution. It includes built-in tools for testing (Karma, Jasmine), routing (Angular Router), and state management (NgRx) 
- **React** is highly flexible and modular, allowing developers to choose libraries and tools based on project needs. It has a vast ecosystem with libraries like React Router, Redux, and React Native for cross-platform mobile development 

##### Use Cases
- **Angular** is ideal for **large-scale enterprise applications** with complex workflows and extensive data interaction. It is used by companies like IBM, PayPal, and Upwork 
- **React** is well-suited for **single-page applications (SPAs)**, dynamic UIs, and mobile apps (via React Native). It is used by Facebook, Instagram, and Netflix 

---

5. Explain Props, Superprops, and Hooks with examples.

Ans)
#### 1. **Props (Properties)**

#### What are Props?

**Props** are used to pass data from a **parent component** to a **child component**. They are **read-only**, meaning that the child component **cannot modify** them directly.

####  Example:

```jsx
// ParentComponent.jsx
import React from 'react';
import Greeting from './Greeting';

function ParentComponent() {
  return <Greeting name="Alice" />;
}

export default ParentComponent;

// Greeting.jsx
import React from 'react';

function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

export default Greeting;
```

In this example, the `ParentComponent` passes the `name` prop to the `Greeting` component.

---

#### 2. **"Superprops" (Clarification)**

There is **no official concept called "superprops" in React**. However, it may be a confusion between:

- `props` — the data passed to a component.
- `super()` — a method used in **class components** to call the constructor of the parent class.

#### Example of `super()` in Class Components:

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props); // Always call super() when using constructor in class components
    console.log(this.props); // Access to props after super()
  }

  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

So, **"superprops" is not a standard term**, but it might refer to how props are passed up or down a component tree in a more complex application.

#### 3. **Hooks**

#### What are Hooks?

**Hooks** are functions that let you use **state and other React features** in **functional components**. They were introduced in React 16.8 to simplify state management and reduce the need for class components.

#### Commonly Used Hooks:

- `useState` — for managing state.
- `useEffect` — for handling side effects (like lifecycle methods in class components).
- `useContext` — for accessing React context.
- `useReducer` — for managing complex state logic.

#### Example with `useState`:

```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click Me</button>
    </div>
  );
}

export default Counter;
```

Here, `useState` allows the functional component to keep track of the `count` state.

#### Example with `useEffect`:

```jsx
import React, { useEffect, useState } from 'react';

function DataFetcher() {
  const [data, setData] = useState(null);

  useEffect(() => {
    // Simulate data fetching
    fetch('https://jsonplaceholder.typicode.com/todos/1')
      .then(res => res.json())
      .then(json => setData(json));
  }, []); // Empty array means this effect runs once after initial render

  return (
    <div>
      {data ? <p>{data.title}</p> : <p>Loading...</p>}
    </div>
  );
}

export default DataFetcher;
```

`useEffect` is used to perform side effects like fetching data from an API.

#### Conclusion

- **Props** allow data to flow from parent to child.
- There is no such thing as **"superprops"**, but it could be a confusion with `props` or `super(props)` in class components.
- **Hooks** like `useState` and `useEffect` allow functional components to manage **state** and perform **side effects**, making them a powerful alternative to class components.


---

6. Explain JSX in React with an example. How does it differ from traditional HTML? Also compare React.js with Angular with 3 key differences.

---

7. Build a React application to display product defect issues. Display a list of issues using static data. Each issue should have an ID, product name, title, description, test case ID, and status (e.g., Open, In Progress, Closed).

---

8. Describe MVC architecture with a diagram.

---

9. Elaborate on MongoDB Documents and Collections. Write a Node.js code snippet to insert a document into a "users" collection and read all documents where "status" is "active".

---

10. Describe key concepts of REST APIs.

---

11. Explain state and props in React with examples. List the lifecycle methods for mounting, updating, and unmounting phases in class components.
---

12. Implement a Mount Event function using Express.js with the following messages:  
    - "Teacher is ready to teach" — First message  
    - "Students are not ready to come to the class" — Second message  
    - Display "Server listening on PORT 3000"

---

13. Explain conditional rendering using `&&` and ternary operators with code snippets.

---
