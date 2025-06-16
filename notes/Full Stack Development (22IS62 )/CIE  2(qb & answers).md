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
  In JavaScript, variable declaration involves reserving a name to hold data. The sources define JavaScript as a dynamically typed scripting language, meaning that variables can easily (or implicitly) convert from one data type to another during runtime. Unlike statically typed languages, JavaScript does not require you to define a variable's data type when it is declared; instead, the type of data a variable can hold is assigned at runtime and can change. Almost everything in JavaScript, including variables and functions, is considered an object.

#### Comparison of Variable Declaration

**1. JavaScript Variable Declaration (using `var` keyword)** Based on the provided sources, JavaScript variables are declared using the `var` keyword. The sources do not mention other declaration keywords like `let` or `const`, which are part of newer JavaScript standards.

- **Declaration without Initial Value:** To declare a variable `x` without assigning an initial value, you use the `var` keyword followed by the variable name and a semicolon.
    
    ```
    var x;
    ```
    
    In this case, since no value is specified, the default value of the variable will be `undefined`.
    
- **Declaration with Initial Value (at declaration-time):** You can assign a value to a variable at the time of its declaration by appending the value to the declaration.
    
    ```
    var myVariable = "Hello";
    ```
    
- **Assignment at Runtime (after declaration):** After a variable has been declared, you can assign or reassign a value to it at any point during the program's execution using a simple right-to-left assignment. Due to JavaScript's dynamic typing, the data type of the variable can change with reassignment.
    
    ```
    var num;
    num = 10; // 'num' is now a number
    num = "ten"; // 'num' can now be a string
    ```
    
- **Conditional Assignment:** JavaScript also supports a conditional assignment operator.
    
    ```
    // Example from sources' description (Figure 6.14 is not provided, but concept is mentioned)
    var greeting = (hour < 12) ? "Good Morning" : "Good Afternoon";
    ```
    

**2. Comparison with Statically Typed Languages (e.g., Java)** :
- **Java (Statically Typed):** In Java, the data type of a variable must be explicitly defined by the programmer (e.g., `int abc`) and is enforced by the compiler. This means a variable declared as an integer can only hold integer values, and its type cannot change during runtime.
    
    ```
    int count; // 'count' is declared as an integer and will remain so.
    String name = "Alice"; // 'name' is declared as a String and will remain so.
    ```
    
- **JavaScript (Dynamically Typed):** In contrast, JavaScript's dynamic typing allows a variable to hold different data types at different times during runtime. For instance, a variable initially holding an integer can later be assigned a string, and JavaScript will implicitly convert its type.
 
   ---
   
3. Differentiate between JavaScript and jQuery. Provide examples for each type and explain the technologies commonly used to build them.
Ans)
 JavaScript and jQuery are distinct yet related technologies in web development. JavaScript is a programming language, while jQuery is a library built using JavaScript.

#### JavaScript (JS)

JavaScript is defined as an object-oriented, dynamically typed scripting language. It is distinct from Java, despite the similar name; Java is a compiled, object-oriented language running on a Java Virtual Machine, whereas JavaScript runs directly in the browser and has fewer object-oriented features. Almost everything in JavaScript, including variables and functions, is an object. Its dynamic typing means variables can change their data type during runtime. JavaScript is an implementation of ECMAScript, a standardized scripting language.

**Common Uses and Underlying Technologies:** JavaScript is primarily a client-side scripting language, meaning its code is executed locally on the client's browser rather than on the server. This offers several advantages:

- **Reduced Server Load:** Processing is offloaded from the server to client machines.
- **Improved User Experience:** The browser can respond more quickly to user events, offering a desktop-like experience.
- **Enhanced HTML Interaction:** JavaScript can dynamically interact with and modify the downloaded HTML.

Historically, JavaScript's uses were limited to simple interactive elements like graphic roll-overs, pop-up alerts, and basic form validation. Its significance grew dramatically in the mid-2000s with the advent of AJAX (Asynchronous JavaScript and XML). AJAX allows sections of a web page to update by making background requests to the server without requiring a full page refresh, creating an "illusion of continuity". This relies on JavaScript's `XMLHttpRequest` object, introduced by Microsoft in 1999.

**Examples of JavaScript (Vanilla JS):**

- **Variable Declaration and Assignment:** JavaScript uses the `var` keyword for variable declaration.
    
    ```
    var myNumber; // Declares a variable 'myNumber', default value is 'undefined'
    myNumber = 10; // Assigns a number value
    myNumber = "Hello"; // Dynamically reassigns a string value
    ```
    
- **Function Definition:** Functions are fundamental building blocks for modular code.
    
    ```
    function greet(name) {
        return "Hello, " + name + "!";
    }
    alert(greet("World")); // Example call using the built-in alert() function
    ```
    
- **DOM (Document Object Model) Manipulation:** JavaScript interacts with the HTML document through the DOM, which represents the page's structure as a tree of nodes.
    
    ```
    // Getting an element by its ID
    var myElement = document.getElementById("myDiv");
    // Modifying its content
    if (myElement) {
        myElement.innerHTML = "New content from JavaScript!";
    }
    // Changing its style
    if (myElement) {
        myElement.style.backgroundColor = "lightblue";
    }
    ```
    
- **Event Handling:** JavaScript detects actions (events) like clicks or key presses. The listener approach is the recommended method to attach event handlers, separating JavaScript from HTML.
    
    ```
    var myButton = document.getElementById("myButton");
    if (myButton) {
        // Attaching an event listener (modern approach)
        myButton.addEventListener('click', function() {
            alert("Button was clicked!");
        });
    }
    ```
    

####  jQuery

jQuery is described as a lightweight, "write less, do more" JavaScript library. Its primary purpose is to simplify the use of JavaScript on websites. It achieves this by wrapping many common tasks that typically require multiple lines of standard JavaScript code into concise, single-line methods.

**Common Uses and Underlying Technologies:** jQuery simplifies complex JavaScript operations across various domains:

- **HTML/DOM Manipulation:** It provides chainable methods for efficiently interacting with and modifying HTML elements.
- **CSS Manipulation:** Allows easy modification of CSS properties.
- **HTML Event Methods:** Simplifies event handling with a three-layer architecture.
- **Effects and Animations:** Includes a built-in animation scheduler.
- **AJAX:** Offers a unified interface for making asynchronous HTTP requests.
- **Utilities:** Provides various utility functions.

jQuery is cross-platform and supports different types of browsers, addressing some of the browser idiosyncrasies that can complicate vanilla JavaScript development. Under the hood, jQuery uses a "Selector Engine" called Sizzle.js to efficiently select HTML elements.

**Examples of jQuery:**

- **DOM Manipulation:** jQuery uses CSS-like selectors to target elements and provides intuitive methods for manipulation.
    
    ```
    // Selects elements with class 'item-list' and finds all 'li' descendants
    // then adds a class, changes CSS, and fades them in
    $('.item-list')
        .find('li')
        .addClass('highlight')
        .css('font-weight', 'bold')
        .fadeIn(500);
    ```
    
- **Event Handling:** Attaching event handlers is streamlined.
    
    ```
    // Attaches a click event handler to all elements with class 'my-button'
    $('.my-button').on('click', function() {
        alert("jQuery button was clicked!");
    });
    ```
    
- **AJAX:** Making asynchronous requests is much simpler compared to native `XMLHttpRequest`.
    
    ```
    // Makes a GET request and handles success or failure
    $.ajax({
        url: 'api/products',
        method: 'GET'
    })
    .done(function(response) {
        console.log('Products received:', response);
    })
    .fail(function(jqXHR, textStatus) {
        console.error('Error fetching products:', textStatus);
    });
    ```
    
- **Animations:** Provides easy-to-use methods for animations.
    
    ```
    // Animates width, adds a delay, then fades out an element with class 'animated-box'
    $('.animated-box')
        .animate({width: '300px'}, 800)
        .delay(400)
        .fadeOut();
    ```
    

####  Differentiating JavaScript and jQuery

The fundamental difference is that **JavaScript is the programming language itself**, while **jQuery is a JavaScript library**. This means:

- **Dependency:** jQuery **requires** JavaScript to function, as it is written _in_ JavaScript. JavaScript, however, does not require jQuery.
- **Level of Abstraction:** JavaScript operates at a lower level, directly interacting with the browser's APIs (like the DOM and `XMLHttpRequest`). jQuery provides a higher-level abstraction, simplifying these common interactions with more concise syntax.
- **Purpose:** JavaScript is a general-purpose scripting language for client-side web development. jQuery's specific purpose is to make common web development tasks (DOM manipulation, AJAX, events, animations) significantly easier and more consistent across browsers.
- **Code Volume:** Using jQuery typically results in "write less" code compared to achieving the same functionality with vanilla JavaScript.

While jQuery remains relevant for legacy systems, modern web development increasingly uses native JavaScript features and newer frameworks (like React, Vue, or native `fetch()` and `addEventListener`) that offer similar or enhanced capabilities without the need for an external library. However, understanding jQuery is still valuable for maintaining legacy codebases.

---

4. Explain the importance of Model View Control (MVC) in Web Development. Describe a very popularly used MVC framework.
Ans)

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

