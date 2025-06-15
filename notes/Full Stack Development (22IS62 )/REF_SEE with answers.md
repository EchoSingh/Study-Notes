
## Mod 1

1. Explain the three main layers of Full Stack Development and their roles in web applications.
2. Describe the purpose of Git and GitHub in version control with examples of common commands.
3. How do HTML forms work? Explain the use of attributes like action, method, and input types.
4. Compare and contrast static vs. dynamic websites. Provide use cases for each.
5. Create an HTML5 page with a form that includes validation for email, password, and a file upload.
6. Design a responsive webpage using HTML5 semantic tags (e.g., `<nav>`, `<section>`).
7. Implement a form with fieldsets, legends, and input types (date, range, color).

---

## Mod 2

1. Explain the CSS box model with a diagram.
2. Differentiate between inline, internal, and external CSS with examples.
3. What are JavaScript hoisting and lexical scope? Provide code snippets.
4. Why is JavaScript’s `let`/`const` preferred over `var`? Discuss scope implications.
5. Style a navigation bar using Flexbox/Grid and make it responsive with media queries.
6. Write a JavaScript function to filter an array of objects based on user input.
7. Create a Bootstrap card layout with dynamic content loaded via JavaScript.
8. Implement a toggle button that switches between light/dark themes using CSS variables.

---

## Mod 3

1. Explain JavaScript’s prototype inheritance with an example.
2. How does jQuery simplify DOM manipulation? Provide a comparison with vanilla JS.
3. Describe the MVC architecture and its components.
4. What are RESTful APIs? List common HTTP methods and their purposes.
5. Compare Promises and callbacks for asynchronous operations. When would you use each?
6. Evaluate the security risks of API authentication (e.g., API keys vs. OAuth).
7. Build a Node.js server that serves static files and handles a POST request.
8. Create a MongoDB query to insert, update, and retrieve documents from a collection.
9. Write a JavaScript function to fetch and display data from a public API (e.g., JSONPlaceholder).
10. Implement a jQuery-based AJAX form submission with validation.

---

## Mod 4

1. Explain Node.js architecture. Describe its event-driven, non-blocking I/O model with an example.
2. What are MongoDB documents and collections? How do they differ from relational database tables?
3. Analyze the scalability challenges of Node.js single-threaded architecture. When would you use worker threads?
4. Create a Node.js HTTP server that responds with "Hello, World!" and handles a POST request to `/data`.  
   ```javascript
   const http = require('http');
   server.on('request', (req, res) => {
       // Your code here
   });
```

5. Write a script to:
    
    - Insert a user document (`{ name: "Alice", age: 25 }`) into a `users` collection.
        
    - Update Alice’s age to 26.
        
    - Query all users older than 20.
        
6. Fetch data from a public API (e.g., [https://jsonplaceholder.typicode.com/posts](https://jsonplaceholder.typicode.com/posts)) and display the titles of the first 5 posts.
    
7. Implement a Node.js middleware to validate API keys in request headers. Reject requests with invalid keys.
    

---

## Mod 5

1. Explain React’s virtual DOM and its advantages.
    
2. Describe the difference between React props and state with examples.
    
3. What are React Hooks? List 3 commonly used hooks and their purposes.
    
4. Debug a React component lifecycle issue involving `useEffect` dependencies.
    
5. Evaluate Redux for state management in large-scale applications.
    
6. Build a React component that fetches and displays data from an API using `useEffect`.
    
7. Create a form with controlled inputs and validation using React state.
    
8. Implement a multi-page application using React Router (e.g., Home, About, Contact).
    
9. Design a Redux store to manage a shopping cart’s state.
    