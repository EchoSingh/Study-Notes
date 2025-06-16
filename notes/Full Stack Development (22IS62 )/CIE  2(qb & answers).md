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
    The Model-View-Controller (MVC) framework is an architectural pattern fundamental to software development, particularly in web development. It structures an application by separating its concerns into three interconnected components: the Model, the View, and the Controller. This separation is crucial for managing the complexity of modern web applications.

####  Importance of Model-View-Controller (MVC) in Web Development

The MVC architecture is important for several reasons, stemming from its approach to organizing code and responsibilities:

- **Separation of Concerns:** MVC promotes a clear division of labor, abstracting the solution into layers to build a cognitive model for implementation.
    - The **Model** (data layer) is responsible for implementing business logic, data validation rules, database interactions, and state management.
    - The **View** (presentation layer) focuses on displaying information to the user and includes features like component-based templates, reactive data binding, and accessibility compliance.
    - The **Controller** (logic layer) handles route management, processes requests, generates responses, and integrates middleware. This structured approach makes the codebase easier to understand and manage.
- **Improved Maintainability and Organization:** By compartmentalizing functionality, MVC makes it easier to update, modify, and extend different parts of the application without affecting others. This is particularly beneficial as projects grow in size and complexity.
- **Enhanced Testability:** The distinct responsibilities of each component allow for independent testing of the Model, View, and Controller layers. This modularity simplifies the testing process and helps ensure code reliability.
- **Facilitates Team Collaboration:** With clearly defined roles for each component, different developers or teams can work on the Model, View, or Controller concurrently, leading to more efficient development workflows.
- **Flexibility and Reusability:** Models can be reused with different views, and controllers can manage various user interactions or data flows. This promotes the reuse of code across different parts of an application or even in separate projects.
- **Structured Workflow:** The MVC pattern defines a clear request lifecycle: a client initiates an HTTP request, which is handled by the Controller. The Controller then interacts with the Model (and potentially the database), processes the data, and passes it to the View for rendering. Finally, the View generates the HTML or JSON response sent back to the client. This predictable data flow is a cornerstone of robust web applications.

####  Popularly Used MVC Framework: .NET Core MVC

Among the modern MVC frameworks, **.NET Core MVC** is a prominent choice. It is designed for building web applications and APIs, incorporating several advanced features and supporting modern development practices.

- **Core Architecture and Features:**
    - **Model Implementation:** The Model component, such as a `Product` class, encapsulates business logic, including data validation rules defined through attributes like `[Required]` for properties like `Name` and `[Range]` for `Price`. It also handles interactions with the database and manages application state.
    - **View Capabilities:** Views in .NET Core MVC (often using Razor syntax) are responsible for generating the user interface. They support component-based templates, reactive data binding, and capabilities like Server-Side Rendering (SSR) and Static Site Generation (SSG), while also adhering to accessibility standards. For example, a Razor View can iterate through a collection of products to display their names and prices in a structured grid.
    - **Controller Functions:** Controllers manage incoming HTTP requests, route them to appropriate actions, process the requests by interacting with models and services, and generate responses. They are capable of middleware integration. An example analogous to a .NET Core MVC controller, a Spring Boot `ProductController`, demonstrates handling a GET request to retrieve a list of products and return them as an HTTP 200 OK response.
- **Modern Integrations and Support:**
    - **.NET Core MVC** offers integration with Blazor, allowing developers to build interactive client-side UIs using C#.
    - It provides **Minimal API support** for creating lean HTTP APIs with reduced boilerplate code.
    - The framework is built with **cloud-native features**, making it well-suited for deployment in cloud environments.
- **Implementation Practices:** Like other contemporary MVC frameworks, .NET Core MVC facilitates practices such as:
    - **Dependency Injection** for achieving loose coupling between components.
    - Various **caching strategies** (view-level, query result, CDN integration) and **database optimization techniques** (eager vs. lazy loading, index optimization, connection pooling) to enhance performance.
    - Support for comprehensive **testing methodologies**, including unit, integration, and End-to-End (E2E) testing.

For new projects, the source suggests considering a Vertical Slice Architecture (VSA) within MVC frameworks to strike a balance between structure and flexibility.
     
---

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

Ans)

```
/**
 * Calculates the count of students within specific grade ranges.
 *
 * @param {Array<Object>} students An array of student objects, each with properties:
 *   - USN No (any type, but not used in logic)
 *   - Name (string, but not used in logic)
 *   - Grade (number, used for range calculation)
 * @returns {Array<number>} A new array containing the counts of students in the following ranges:
 *   - Index 0: 0-20
 *   - Index 1: 21-30
 *   - Index 2: 31-40
 *   - Index 3: 41-50
 */
function rangeOfStudents(students) {
    // Initialize an array to store the counts for each range.
    // The order corresponds to the specified ranges:
    let gradeCounts = ; // This initializes an array of numbers with a length of 4

    // Check if the input is an array and not empty
    if (!Array.isArray(students) || students.length === 0) {
        console.warn("Input is not a valid array or is empty. Returning all zeros.");
        return gradeCounts;
    }

    // Iterate through each student object in the provided array
    for (let i = 0; i < students.length; i++) {
        const student = students[i]; // Accessing an element in an array
        const grade = student.Grade; // Accessing a property of an object

        // Use conditional statements (if-else if-else) to check the grade range
        if (grade >= 0 && grade <= 20) {
            gradeCounts++; // Increment the count for the 0-20 range
        } else if (grade >= 21 && grade <= 30) {
            gradeCounts++; // Increment the count for the 21-30 range
        } else if (grade >= 31 && grade <= 40) {
            gradeCounts++; // Increment the count for the 31-40 range
        } else if (grade >= 41 && grade <= 50) {
            gradeCounts++; // Increment the count for the 41-50 range
        }
        // Note: Students with grades outside 0-50 will not be counted in any of these ranges.
    }

    return gradeCounts;
}

// Example Usage (for demonstration, not part of the function itself):
const studentData = [
    { "USN No": "USN001", "Name": "Alice", "Grade": 15 },
    { "USN No": "USN002", "Name": "Bob", "Grade": 25 },
    { "USN No": "USN003", "Name": "Charlie", "Grade": 35 },
    { "USN No": "USN004", "Name": "David", "Grade": 45 },
    { "USN No": "USN005", "Name": "Eve", "Grade": 10 },
    { "USN No": "USN006", "Name": "Frank", "Grade": 21 },
    { "USN No": "USN007", "Name": "Grace", "Grade": 30 },
    { "USN No": "USN008", "Name": "Heidi", "Grade": 40 },
    { "USN No": "USN009", "Name": "Ivan", "Grade": 50 },
    { "USN No": "USN010", "Name": "Judy", "Grade": 0 },
    { "USN No": "USN011", "Name": "Ken", "Grade": 55 }, // Will not be counted in specified ranges
    { "USN No": "USN012", "Name": "Liam", "Grade": -5 }  // Will not be counted in specified ranges
];

const results = rangeOfStudents(studentData);
console.log("Student counts per grade range (0-20, 21-30, 31-40, 41-50):", results);
// Expected output:[13, 13, 13, 14]
```

---

 5. Illustrate with distinct code examples how you would use at least three different types of jQuery selectors to target and identify specific HTML elements within a web page. For each example, clearly describe which elements would be selected.
 Ans)
jQuery is a lightweight JavaScript library designed to simplify common tasks in web development, including HTML/DOM manipulation. Its purpose is to make it much easier to use JavaScript on your website, by wrapping many lines of JavaScript code into methods callable with a single line. At its core, jQuery uses a powerful selector engine, Sizzle.js, to efficiently target and identify specific HTML elements within a web page.

Below are illustrations using at least three different types of jQuery selectors, with distinct code examples and descriptions of the elements they select.

### 1. ID Selector

An ID selector allows you to target a specific HTML element by its unique `id` attribute, regardless of its type or position in the document tree. Since `id` attributes must be unique within an HTML document, this selector will always return a single element.

**jQuery Code Example:**

```
$('#main-header')
```

**HTML Snippet:**

```
<body>
    <header id="main-header">
        <h1>Welcome to My Website</h1>
    </header>
    <div id="content-area">
        <p>Some content here.</p>
    </div>
</body>
```

**Description of Selected Elements:** This selector will target and identify **only the `<header>` element** that has the `id` attribute set to `"main-header"`.

### 2. Class Selector

A class selector enables you to target multiple HTML elements simultaneously, regardless of their position in the document tree, as long as they share the same `class` attribute value.

**jQuery Code Example:**

```
$('.highlight')
```

**HTML Snippet:**

```
<body>
    <p class="normal-text">This is a regular paragraph.</p>
    <div class="highlight">
        <h3>Important Notice</h3>
        <p>This information is highlighted.</p>
    </div>
    <span class="highlight">Read carefully!</span>
    <article class="news-item">
        <h2 class="highlight">Breaking News</h2>
        <p>More news content.</p>
    </article>
</body>
```

**Description of Selected Elements:** This selector will target and identify **all elements that have the `class` attribute set to `"highlight"`**. In the example above, this includes:

- The `<div>` element containing "Important Notice".
- The `<span>` element with "Read carefully!".
- The `<h2>` element inside the `<article>` tag.

### 3. Descendant Selector (Contextual Selector)

A descendant selector is a type of contextual selector that allows you to select elements based on their hierarchical relationship to other elements. Specifically, it matches all elements that are contained within another element, using a space character to indicate the descendant relationship.

**jQuery Code Example:**

```
$('div p')
```

**HTML Snippet:**

```
<body>
    <section>
        <p>This paragraph is inside a section.</p>
    </section>
    <div class="container">
        <p>This is the first paragraph inside a div.</p>
        <span>
            <p>This paragraph is inside a span, which is inside a div.</p>
        </span>
        <ul>
            <li>Item 1</li>
            <li><p>Paragraph inside a list item, inside a div.</p></li>
        </ul>
    </div>
    <p>This paragraph is directly in the body.</p>
</body>
```

**Description of Selected Elements:** This selector will target and identify **all `<p>` (paragraph) elements that are descendants of any `<div>` element**, regardless of how many levels deep they are. In this example, it would select:

- The first `<p>` inside `.container`.
- The `<p>` inside the `<span>` (which is inside `.container`).
- The `<p>` inside the `<li>` (which is inside `<ul>`, which is inside `.container`).

It would **not** select the `<p>` inside the `<section>` or the `<p>` directly in the `<body>`, as they are not descendants of a `<div>`. 

6. Demonstrate your understanding of Array Destructuring, Object Destructuring, and Parameter Destructuring in JavaScript by writing three distinct code snippets.

7. Write a JS code snippet to explain how Arrays are created. Explain the purpose of the Array along with its different types of representation.

8. Discuss the importance of JS Prototype and Prototype Inheritance in web design. Provide examples of commonly used properties.

9. Create an HTML document for a blog post. The document should include:

    - Control Flow
    
    - Variable Declaration
    

 10. Write a JavaScript to print numbers 1 to 100 in an array.

    - If number is divisible by 3, print `Bizz`
    
    - If divisible by 5, print `Fizz`
    
     - If divisible by both, print `BizzFizz`
---

11. Describe Arrow Functions, Hoisting, and Callback Functions in detail.

12. Create an HTML document for a blog post. The document should include:

     - JS Functions
    
     - Callback Functions
    

13. Analyse the Components of Back-End Development in JS and elaborate the need and usage of each component.

14. Analyse the concept of DOM Manipulation and elaborate on how DOM tree is constructed along with its Nodes.

 15. Name and explain, in your own words, the key difference between how primitive and non-primitive data types are represented in JavaScript.
 16. Describe the purpose and demonstrate with distinct examples how the string operations `lastIndexOf()`, `slice()`, and `substring()` can be used to extract or locate specific parts of a given text. Explain the key differences in their behaviour and output.

17. Develop a JavaScript program to check if a given number is an Armstrong number (sum of cubes is equal to the given number) or not.

18. Describe use of the spread operator in arrays and objects with an example.

19. Design a modular JavaScript function `validateRegistration` that takes an object containing `username`, `password`, `confirmPassword`, and `email` as input properties. This function should:
     -  Analyse the provided input to determine if each field meets the following criteria:
    
         - **Username**: Not empty
        
        - **Password**: At least 6 characters long
        
        - **Confirm Password**: Matches the password field
        
    - Categorize any validation failures for each field

