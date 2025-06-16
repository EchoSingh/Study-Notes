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

---

5. Explain Props, Superprops, and Hooks with examples.

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
