1. Explain the concept of JavaScript (JS) in Web Development. Discuss the History and Uses of JS.
  Ans)
    JavaScript (JS) is defined as an object-oriented, dynamically typed scripting language. While its name contains "Java," JavaScript and Java are distinct programming languages with different uses; Java is a compiled, object-oriented language that runs on a Java Virtual Machine, whereas JavaScript runs directly in the browser and has fewer object-oriented features. Almost everything in JavaScript, including variables and functions, is an object. JavaScript is dynamically typed, meaning variables can change their data type during runtime, unlike statically typed languages like Java where types are defined and enforced by the programmer and compiler.

#### History of JavaScript

JavaScript was introduced by Netscape in their Navigator browser in 1996, initially named LiveScript. It was renamed in part to reflect its purpose of providing control over Java applets within the browser. JavaScript is an implementation of a standardized scripting language known as ECMAScript. Initially, Microsoft's Internet Explorer did not support JavaScript, instead using its own browser-based scripting language called VBScript, though IE now supports JavaScript, sometimes referring to it as JScript for trademark reasons.

#### Uses of JavaScript in Web Development

**Early Uses:** In its early days, JavaScript was less dynamic and sometimes annoying to users. Its common uses included:

- Graphic roll-overs (swapping images on mouse hover).
- Pop-up alert messages.
- Scrolling text in the status bar.
- Opening new browser windows.
- Pre-validating user data in online forms.

**Emergence of AJAX and Modern Uses:** JavaScript became a significantly more important part of web development in the mid-2000s with the emergence of AJAX sites.

- **AJAX (Asynchronous JavaScript and XML):** This term refers to a style of website development that uses JavaScript to create more responsive user experiences. The core mechanism involves asynchronous data requests via JavaScript and the `XMLHttpRequest` object, which was introduced by Microsoft as an ActiveX control in 1999.
    - **Traditional (Synchronous) vs. AJAX (Asynchronous):** In a traditional synchronous request-response loop, each interaction requires a new request to the server, which can slow down the user experience and increase server load. AJAX avoids these visual and temporal deficiencies by making requests to the server in the background, allowing sections of a page to update without requiring a full page refresh, thereby creating an "illusion of continuity". This enables a user experience more akin to desktop software than simple HTML.
- **JavaScript Frameworks:** The development of JavaScript frameworks like jQuery, Prototype, ASP.NET AJAX, and MooTools made AJAX programming significantly easier by reducing the amount of code required for typical AJAX tasks. These frameworks simplify complex JavaScript operations such as HTML/DOM manipulation, CSS manipulation, HTML event methods, effects and animations, AJAX calls, and various utilities. jQuery, for instance, is a "write less, do more" library. More recently, sophisticated MVC (Model-View-Controller) JavaScript frameworks like AngularJS, Backbone, and Knockout have gained popularity, moving more data processing and handling from server-side scripts to HTML pages, promoting the separation of data representation (model) from presentation (view).

**Client-Side Scripting Benefits and Disadvantages:** JavaScript is a client-side scripting language, meaning the code is executed locally on the client machine (the browser) rather than on the server.

- **Advantages:**
    - **Reduced Server Load:** Processing can be offloaded from the server to client machines.
    - **Improved User Experience:** The browser can respond more quickly to user events compared to a remote server request.
    - **Enhanced HTML Interaction:** JavaScript can interact with downloaded HTML, creating richer user experiences.
- **Disadvantages:**
    - **JavaScript Not Guaranteed:** There's no assurance that the client has JavaScript enabled, meaning essential functionality might still need to reside on the server.
    - **Browser Idiosyncrasies:** Differences between browsers and operating systems can make testing challenging, as code that works in one browser might cause errors in another.
    - **Debugging and Maintenance Complexity:** JavaScript-heavy web applications can be complicated to debug and maintain, especially if JavaScript is interwoven directly into HTML.

**Layered Design and Best Practices:** JavaScript contributes to various layers of application design:

- **Presentation Layer:** Focuses on the display of information, allowing JavaScript to alter HTML and create dynamic visual changes (e.g., showing/hiding elements, tabbed views).
- **Validation Layer:** Used to validate logical aspects of the user's input, such as ensuring an email address is valid before sending data to the server, often combined with the presentation layer to provide user feedback.
- **Asynchronous Layers:** Enables requests to be sent to the server in the background without halting the user's interaction with the application, as seen with AJAX. Developers are encouraged to separate presentation and logic in their code to achieve more reusable, understandable, and maintainable code.

**Addressing Users Without JavaScript (Progressive Enhancement):** It's crucial to consider users who may not have JavaScript enabled, including web crawlers (which don't interpret JavaScript), users with browser plug-ins blocking scripts, those using text-based browsers, or visually impaired clients using specialized reading software.

- **`<noscript>` Tag:** HTML provides the `<noscript>` tag, allowing developers to include content that will only be displayed to users whose browsers cannot load JavaScript.
- **Fail-Safe Design / Graceful Degradation / Progressive Enhancement:** Websites should be built with basic functionality in standard HTML.
    - **Fail-safe design** means that if a JavaScript feature fails (e.g., due to JS being disabled), the system still functions, perhaps by offering an alternative input method.
    - **Graceful degradation** involves developing for current browser capabilities and providing an alternate, less feature-rich experience for older browsers.
    - **Progressive enhancement** is the opposite strategy, where the site is built with core functionality accessible to all, and then enhanced with CSS, JavaScript, and HTML5 features for users with more capable browsers. This approach ensures that the site remains functional for a wider audience while providing a richer experience for modern browsers.

**Location of JavaScript:** Similar to CSS, JavaScript code can be included in an HTML page in three ways:

- **Inline JavaScript:** Code placed directly within HTML attributes (e.g., `onclick`). While intuitive, this is strongly discouraged due to blending HTML and JavaScript, which reduces readability and complicates maintenance.
- **Embedded JavaScript:** Code placed within `<script>` elements inside the HTML document. This is suitable for quick testing or learning but is generally frowned upon for production pages due to maintenance difficulties.
- **External JavaScript:** Code placed in a separate `.js` file and linked to the HTML document using a `<link>` element in the `<head>` section, or at the very bottom of the `<body>` element. This is the recommended method for better maintainability and performance, as browsers can cache external files, and placing them at the bottom of the `<body>` can prevent delays in initial page rendering by allowing HTML content to load first.

---


2. Explain the concept of variable declaration. Compare all different types of variable declaration with syntax.

Ans)
   

3. Differentiate between JavaScript and jQuery. Provide examples for each type and explain the technologies commonly used to build them.

4. Explain the importance of Model View Control (MVC) in Web Development. Describe a very popularly used MVC framework.

5. Given an array of objects, where each object represents a student with properties like USN No, Name (string) and Grade (number).  Develop a JavaScript function `rangeOfStudents` that takes this array and returns a new array containing count of students who have a grade in ranges:  0–20, 21–30, 31–40, 41–50.
 
   ```javascript
   const students = [
      { usnno: "1BS23023", name: "swachha", grade: 45 },
      { usnno: "1BS23028", name: "garathi", grade: 36 },
      { usnno: "1BS23024", name: "racket", grade: 42 },
      { usnno: "1BS23025", name: "savya", grade: 35 },
      { usnno: "1BS23026", name: "pacchi", grade: 25 },
      { usnno: "1BS23029", name: "gathi", grade: 22 },
      { usnno: "1BS23030", name: "vidhi", grade: 20 },
   ];
   ````

 6. Illustrate with distinct code examples how you would use at least three different types of jQuery selectors to target and identify specific HTML elements within a web page. For each example, clearly describe which elements would be selected.

7. Demonstrate your understanding of Array Destructuring, Object Destructuring, and Parameter Destructuring in JavaScript by writing three distinct code snippets.

8. Write a JS code snippet to explain how Arrays are created. Explain the purpose of the Array along with its different types of representation.

9. Discuss the importance of JS Prototype and Prototype Inheritance in web design. Provide examples of commonly used properties.

10. Create an HTML document for a blog post. The document should include:

    - Control Flow
    
    - Variable Declaration
    

 11. Write a JavaScript to print numbers 1 to 100 in an array.

    - If number is divisible by 3, print `Bizz`
    
    - If divisible by 5, print `Fizz`
    
     - If divisible by both, print `BizzFizz`
    

12. Describe Arrow Functions, Hoisting, and Callback Functions in detail.

13. Create an HTML document for a blog post. The document should include:

     - JS Functions
    
     - Callback Functions
    

14. Analyse the Components of Back-End Development in JS and elaborate the need and usage of each component.

15. Analyse the concept of DOM Manipulation and elaborate on how DOM tree is constructed along with its Nodes.

 16. Name and explain, in your own words, the key difference between how primitive and non-primitive data types are represented in JavaScript.
 17. Describe the purpose and demonstrate with distinct examples how the string operations `lastIndexOf()`, `slice()`, and `substring()` can be used to extract or locate specific parts of a given text. Explain the key differences in their behaviour and output.

18. Develop a JavaScript program to check if a given number is an Armstrong number (sum of cubes is equal to the given number) or not.

19. Describe use of the spread operator in arrays and objects with an example.

20. Design a modular JavaScript function `validateRegistration` that takes an object containing `username`, `password`, `confirmPassword`, and `email` as input properties. This function should:
     -  Analyse the provided input to determine if each field meets the following criteria:
    
         - **Username**: Not empty
        
        - **Password**: At least 6 characters long
        
        - **Confirm Password**: Matches the password field
        
    - Categorize any validation failures for each field

