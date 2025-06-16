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

Ans)
#### JSX in React and Its Differences from HTML

**JSX** (JavaScript XML) is a syntax extension used in **React** that allows developers to write HTML-like code directly in JavaScript. It makes it easier to build and visualize user interfaces by enabling a declarative and component-based approach.

Although JSX looks like HTML, it is **not actual HTML**. Instead, it gets **compiled into JavaScript** using tools like **Babel** before the browser can execute it.

#### Example of JSX

```jsx
const element = <h1>Hello, JSX!</h1>;
```

This JSX expression is transformed into a standard JavaScript call:

```js
const element = React.createElement('h1', null, 'Hello, JSX!');
```

Here’s a more complex example using a component:

```jsx
function Welcome(props) {
  return <h1>Welcome, {props.name}</h1>;
}

const element = <Welcome name="Alice" />;
ReactDOM.render(element, document.getElementById('root'));
```

In this case:
- `<Welcome name="Alice" />` is JSX.
- It gets compiled into a call to `React.createElement`.
- `{props.name}` allows dynamic data to be injected into the JSX.

####  JSX vs Traditional HTML

| Feature                     | JSX in React                                      | Traditional HTML                           |
|----------------------------|--------------------------------------------------|---------------------------------------------|
| **Syntax**                 | Looks similar to HTML but embedded in JavaScript | Pure markup language                       |
| **Execution**              | Compiled into JavaScript using Babel or similar | Rendered directly by the browser           |
| **Logic Integration**      | Can include JavaScript expressions using `{}`  | Static — no logic inside HTML              |
| **Custom Components**      | Supports custom elements (e.g., `<MyComponent />`) | Only supports built-in HTML tags           |
| **Type Safety**            | Works well with TypeScript for better type checking | No type system                             |

#### React.js vs Angular: 3 Key Differences

| Feature                     | React.js                                         | Angular                                      |
|----------------------------|--------------------------------------------------|----------------------------------------------|
| **Type**                   | A **library** focused on the **view layer**     | A **full-featured framework**               |
| **Language**               | Primarily uses JavaScript, supports TypeScript  | Built with and requires **TypeScript**      |
| **Data Binding**           | Uses **one-way data binding** (from parent to child) | Uses **two-way data binding** (model ↔ view) |


---

7. Build a React application to display product defect issues. Display a list of issues using static data. Each issue should have an ID, product name, title, description, test case ID, and status (e.g., Open, In Progress, Closed).

Ans)

```jsx
// App.js
import React from "react";

const issues = [
  {
    id: 1,
    productName: "Product A",
    title: "Login Button Not Working",
    description: "The login button does not respond to clicks.",
    testCaseId: "TC101",
    status: "Open",
  },
  {
    id: 2,
    productName: "Product B",
    title: "Image Not Loading",
    description: "Product images fail to load on Safari browser.",
    testCaseId: "TC202",
    status: "In Progress",
  },
  {
    id: 3,
    productName: "Product C",
    title: "Crash on Launch",
    description: "App crashes on startup for Android 11 devices.",
    testCaseId: "TC303",
    status: "Closed",
  },
];

function Issue({ issue }) {
  return (
    <div className="border p-4 mb-4 rounded shadow">
      <h2 className="text-xl font-bold">{issue.title}</h2>
      <p><strong>ID:</strong> {issue.id}</p>
      <p><strong>Product Name:</strong> {issue.productName}</p>
      <p><strong>Description:</strong> {issue.description}</p>
      <p><strong>Test Case ID:</strong> {issue.testCaseId}</p>
      <p><strong>Status:</strong> {issue.status}</p>
    </div>
  );
}

function App() {
  return (
    <div className="max-w-3xl mx-auto p-4">
      <h1 className="text-2xl font-bold mb-4">Product Defect Issues</h1>
      {issues.map((issue) => (
        <Issue key={issue.id} issue={issue} />
      ))}
    </div>
  );
}

export default App;
```

> You can add **Tailwind CSS** or use basic CSS to style the components if you're not using utility-first classes.
---

8. Describe MVC architecture with a diagram.

Ans)

#### MVC architecture :-

![MVC archi](https://imgs.search.brave.com/pBkRlv7IUjiGEcgjD7wZI6PvNfk_dAsgRN3yjBDxAYo/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly93d3cu/Y3Jpby5kby9ibG9n/L2NvbnRlbnQvaW1h/Z2VzLzIwMjEvMDcv/Q29tcG9uZW50cy1v/Zi1NVkMtQXJjaGl0/ZWN0dXJlLVBhdHRl/cm4ucG5n)
![]()
# MVC (Model-View-Controller) Architecture

**MVC (Model-View-Controller)** is a **software architectural pattern** used for organizing code in applications, especially in **web development**. It separates the application into three interconnected components:

## 🔹 1. **Model**

- **What it does**: Manages the **data**, business logic, and rules of the application.
- **Responsibilities**:
  - Handles data retrieval and storage (e.g., from a database or API).
  - Validates data before it is used.
  - Notifies the View when data changes.

- **Example**: A `User` model might handle user registration, login, and data persistence.

## 🔹 2. **View**

- **What it does**: Handles the **presentation layer** – how data is displayed to the user.
- **Responsibilities**:
  - Renders the UI using data from the Model.
  - Sends user actions (like clicks or form submissions) to the Controller.
  - Does **not contain business logic**.

- **Example**: A webpage showing a list of users or a form to create a new user.

## 🔹 3. **Controller**

- **What it does**: Acts as an **intermediary** between Model and View.
- **Responsibilities**:
  - Handles user input (e.g., HTTP requests).
  - Updates the Model based on user actions.
  - Selects the appropriate View to render.

- **Example**: When a user submits a form, the Controller processes the data, updates the Model, and tells the View to update.

---

####  Flow of Control in MVC

Here is how the components interact in a typical request:

1. **User interacts** with the View (e.g., clicks a button or submits a form).
2. The **View sends the input** (e.g., form data) to the **Controller**.
3. The **Controller processes** the input:
   - It may update the **Model** or request data from it.
4. The **Model updates or retrieves data** and notifies the Controller.
5. The **Controller selects a View** and passes it the updated data.
6. The **View renders** the updated UI to the user.

---

#### Advantages of MVC

| Benefit | Description |
|--------|-------------|
| **Separation of Concerns** | Each component has a clear role, making code easier to maintain and scale. |
| **Reusability** | The same Model can be used with different Views or Controllers. |
| **Parallel Development** | Developers can work on different parts (Model, View, Controller) simultaneously. |
| **Testability** | Easier to write unit tests due to decoupled components. |
| **Flexibility** | UI can change without affecting business logic. |

---

####  Example Use Case (Web Application)

**Scenario**: User requests a list of products.

1. **View**: User clicks on "View Products".
2. **Controller**: Receives request, calls the Model to fetch data.
3. **Model**: Fetches products from the database.
4. **Controller**: Receives data and selects the appropriate View.
5. **View**: Displays the list of products to the user.

####  Technologies Using MVC Architecture

- **Backend Frameworks**:
  - **ASP.NET MVC**
  - **Ruby on Rails**
  - **Django (MTV – similar to MVC)**
  - **Spring MVC (Java)**
- **Frontend Frameworks**:
  - **AngularJS** (follows a variation of MVC)
  - **Backbone.js** (more event-driven, but inspired by MVC)


---

9. Elaborate on MongoDB Documents and Collections. Write a Node.js code snippet to insert a document into a "users" collection and read all documents where "status" is "active".

Ans)

MongoDB is a **NoSQL database** that stores data in **flexible, JSON-like documents**. It is widely used in modern applications due to its scalability, flexibility, and performance.

#### 🔹 MongoDB Basics: Documents and Collections

####  Document
- A **document** is the basic unit of data in MongoDB.
- It is a **key-value pair structure** similar to JSON.
- Each document is stored in a **BSON (Binary JSON)** format for efficiency.

**Example Document:**
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "age": 28,
  "status": "active"
}
```

#### Collection
- A **collection** is a group of MongoDB documents.
- It is **schema-less**, meaning each document can have a different structure.
- Similar to a **table** in relational databases.

**Example Collections:**
- `users`
- `products`
- `orders`

#### Node.js Code to Work with MongoDB

We'll use the official MongoDB Node.js driver to connect to MongoDB, insert a document into the `users` collection, and find all active users.

#### Prerequisites

1. Install the MongoDB Node.js driver:
```bash
npm install mongodb
```

2. Make sure MongoDB is running locally or have a MongoDB Atlas connection string.

#### Node.js Code: Insert and Query Documents

```javascript
const { MongoClient } = require('mongodb');

// Connection URI (for local or Atlas)
const uri = 'mongodb://localhost:27017'; // or your Atlas connection string
const client = new MongoClient(uri);

async function run() {
  try {
    // Connect to the MongoDB server
    await client.connect();
    console.log("Connected to MongoDB");

    const database = client.db('mydb'); // Use or create a database
    const collection = database.collection('users'); // Use or create a collection

    // ✅ Insert a document into the "users" collection
    const userDocument = {
      name: "Alice Smith",
      email: "alice@example.com",
      age: 32,
      status: "active"
    };

    const insertResult = await collection.insertOne(userDocument);
    console.log("Inserted document with ID:", insertResult.insertedId);

    // 🔍 Query all documents where "status" is "active"
    const query = { status: "active" };
    const activeUsers = await collection.find(query).toArray();

    console.log("Active Users:");
    console.log(activeUsers);
  } finally {
    // Close the connection
    await client.close();
  }
}

run().catch(console.dir);
```

####  Output (Example)

If you run this script after inserting one or more users with `"status": "active"`, the output will look like:

```
Connected to MongoDB
Inserted document with ID: 64a1b2c3d4e5f6g7h8i9j0k1
Active Users:
[
  {
    _id: ObjectId("64a1b2c3d4e5f6g7h8i9j0k1"),
    name: "Alice Smith",
    email: "alice@example.com",
    age: 32,
    status: "active"
  },
  {
    _id: ObjectId("64a1b2c3d4e5f6g7h8i9j0k2"),
    name: "Bob Johnson",
    email: "bob@example.com",
    age: 29,
    status: "active"
  }
]
```


---

10. Describe key concepts of REST APIs.

Ans)

REST (Representational State Transfer) is an architectural style for designing networked applications, particularly web services. It uses standard HTTP methods and is stateless, scalable, and simple.

####  Key Concepts of REST APIs:

1. **Resource-Based**
    
    - Everything in REST is considered a **resource** (e.g., users, products, orders).
        
    - Resources are accessed via **URIs** (Uniform Resource Identifiers).
        
    - Example: `/api/users/1` refers to the user with ID 1.
        
2. **HTTP Methods**  
    REST uses standard HTTP verbs to perform actions on resources:
    
    - `GET`: Retrieve data
        
    - `POST`: Create a new resource
        
    - `PUT`: Update an existing resource
        
    - `DELETE`: Remove a resource
        
    - `PATCH`: Partially update a resource
        
3. **Statelessness**
    
    - Each request from a client must contain all the information needed to understand and process it.
        
    - No session or context is stored on the server between requests.
        
4. **Client-Server Architecture**
    
    - Separation of concerns: the client handles the UI, and the server handles data and business logic.
        
5. **JSON or XML Format**
    
    - Data is typically exchanged in **JSON** format for simplicity and readability, though XML is also supported.
        
6. **Uniform Interface**
    
    - A consistent, standardized way of interacting with resources across the API.
        
7. **Representations**
    
    - Resources can have different representations (e.g., JSON, XML), and clients can request specific formats using headers like `Accept`.
        
8. **Stateless Communication**
    
    - Every request is independent; the server does not retain client information.
        
9. **Code on Demand (Optional)**
    
    - Servers can return executable code (e.g., JavaScript) to be run on the client.
        

####  Example REST API Endpoints:

|HTTP Method|Endpoint|Description|
|---|---|---|
|GET|`/api/users`|Get all users|
|POST|`/api/users`|Create a new user|
|GET|`/api/users/1`|Get user with ID 1|
|PUT|`/api/users/1`|Update user with ID 1|
|DELETE|`/api/users/1`|Delete user with ID 1|

---

11. Explain state and props in React with examples. List the lifecycle methods for mounting, updating, and unmounting phases in class components.

Ans)

### Props in React:

Props (short for "properties") are used to pass data from one component to another, typically from a parent component to a child component. Props are read-only, meaning a child component cannot modify the props it receives. Props help make components reusable by allowing them to operate with different data.

**Example:**

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

function App() {
  return <Welcome name="Alice" />;
}
```

In this example, the `App` component passes the value `"Alice"` to the `Welcome` component using the `name` prop. The `Welcome` component uses `props.name` to display the message.

---

### State in React:

State is a built-in object in React components that is used to store dynamic data that affects the rendering of the component. Unlike props, the state is managed within the component and can be modified using the `setState()` method in class components. Changes to state trigger re-rendering of the component.

**Example:**

```jsx
class Counter extends React.Component {
  constructor() {
    super();
    this.state = { count: 0 };
  }

  increment = () => {
    this.setState({ count: this.state.count + 1 });
  }

  render() {
    return (
      <div>
        <p>Count: {this.state.count}</p>
        <button onClick={this.increment}>Increment</button>
      </div>
    );
  }
}
```

In this example, the `Counter` component maintains its own internal state using the `count` property and updates it when the button is clicked.

---

### Lifecycle Methods in Class Components:

React class components follow a defined set of lifecycle methods that are grouped into three main phases: mounting, updating, and unmounting.

#### Mounting Phase:

Occurs when a component is being created and inserted into the DOM.

- `constructor()` – Initializes state and binds methods.
    
- `static getDerivedStateFromProps()` – Invoked before rendering, used to derive state from props.
    
- `render()` – Renders the component’s UI.
    
- `componentDidMount()` – Invoked once after the component is mounted; often used for data fetching.
    

#### Updating Phase:

Occurs when the component is being re-rendered due to changes in props or state.

- `static getDerivedStateFromProps()` – Called again before every render.
    
- `shouldComponentUpdate()` – Determines whether the component should re-render.
    
- `render()` – Renders the updated UI.
    
- `getSnapshotBeforeUpdate()` – Captures information (e.g., scroll position) before the DOM is updated.
    
- `componentDidUpdate()` – Invoked after the component updates; useful for performing operations after the DOM has been updated.
    

#### Unmounting Phase:

Occurs when the component is being removed from the DOM.

- `componentWillUnmount()` – Used to perform cleanup tasks such as aborting network requests or clearing timers.
    

---

12. Implement a Mount Event function using Express.js with the following messages:  
    - "Teacher is ready to teach" — First message  
    - "Students are not ready to come to the class" — Second message  
    - Display "Server listening on PORT 3000"

---

13. Explain conditional rendering using `&&` and ternary operators with code snippets.

---
