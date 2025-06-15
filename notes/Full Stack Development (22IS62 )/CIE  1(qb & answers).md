
1. Explain the concept of Full Stack Web Development. Discuss the key layers involved in Full Stack Development and provide examples of technologies used in each layer.
  Ans)
  
   Full Stack Web Development refers to the process of building and managing both the front-end (client-side) and back-end (server-side) elements of a web application  A full-stack developer is capable of working on all layers of the application, from the user interface to the server and database  This approach allows for a more cohesive and efficient development process, as the developer can handle all aspects of the application, leading to faster development cycles and improved collaboration 
   
   The key layers involved in Full Stack Development include:
   1. **Frontend Development**: This layer focuses on the user interface (UI) and user experience (UX) of the web application. It involves creating the visual elements that users interact with, such as layout, colours, and animations. Technologies used in this layer include HTML, CSS, and JavaScript, along with frameworks and libraries like React, Angular, and Vue.js 

   2. **Backend Development**: This layer deals with the server-side logic, database management, and application functionality. It ensures that the data is processed and stored securely. Technologies used in this layer include programming languages like Python, Ruby, PHP, Node.js, Java, and .NET, as well as backend frameworks such as Django, Spring Boot, and Express.js 

   3. **Database Management**: This layer involves the storage and retrieval of data. It includes managing databases and ensuring data integrity and security. Technologies used in this layer include MySQL, PostgreSQL, and MongoDB 

   4. **Version Control**: This layer involves managing changes to the codebase and collaborating with other developers. Technologies used in this layer include Git, which helps in tracking changes and managing different versions of the code 

    Examples of technologies used in each layer include:

    - Frontend: HTML, CSS, JavaScript, React, Angular, Vue.js 
    - Backend: Python, Ruby, PHP, Node.js, Django, Spring Boot, Express.js 
    - Databases: MySQL, PostgreSQL, MongoDB 
    - Version Control: Git 

---

2. Explain the concept of Cascading Style Sheets and its role in web development. Compare and contrast inline, internal, and external CSS, highlighting their use cases and advantages.

   Ans)


    Cascading Style Sheets (CSS) is a styling language used to control the layout and visual appearance of web pages written in HTML and other markup languages. CSS allows developers to separate presentation logic from content, making it easier to maintain and update websites.
   
    **Role in Web Development**

     CSS plays a crucial role in web development by:

    * Controlling the layout, color, font, and other visual aspects of a web page
    * Improving user experience by creating a consistent and visually appealing design
    * Enhancing accessibility by providing alternative styles for users with disabilities
    * Enabling responsive design, which adapts to different screen sizes and devices
 
    **CSS Types: Inline, Internal, and External**

  
	 There are three types of CSS: inline, internal, and external.

     **Inline CSS**

    * **Definition**: CSS styles applied directly to an HTML element using the `style` attribute.
    * **Use Case**: Small, one-time changes to a single element, such as changing font color or size.
    * **Advantages**: Quick and easy to implement, no need to create a separate CSS file.
    * **Disadvantages**: Can make HTML code messy and difficult to maintain, not scalable for large projects.

    **Internal CSS**

    * **Definition**: CSS styles defined within an HTML document using the `<style>` element.
    * **Use Case**: Small to medium-sized projects, where a separate CSS file is not  necessary.
    * **Advantages**: Easy to implement, can be used for small projects, and can be easily modified.
    * **Disadvantages**: Can make HTML code bulky, not ideal for large projects.

    **External CSS**

    * **Definition**: CSS styles defined in a separate file with a `.css` extension, linked to an HTML document using the `<link>` element.
    * **Use Case**: Large projects, where a separate CSS file is necessary for organization and scalability.
    * **Advantages**: Easy to maintain, update, and reuse styles across multiple pages, makes HTML code cleaner.
    * **Disadvantages**: Requires a separate file, can be slow to load if not optimized.

    Comparison  :-

| CSS Type | Use Case                       | Advantages                                 | Disadvantages                                                  |
| -------- | ------------------------------ | ------------------------------------------ | -------------------------------------------------------------- |
| Inline   | Small, one-time changes        | Quick and easy to implement                | Makes HTML code messy, not scalable                            |
| Internal | Small to medium-sized projects | Easy to implement, easy to modify          | Makes HTML code bulky, not ideal for large projects            |
| External | Large projects                 | Easy to maintain, update, and reuse styles | Requires a separate file, can be slow to load if not optimized |

---


3. Explain in detail Layers of Full Stack Development.

   Ans)

The Full Stack web development process is conceptually divided into three primary layers:

1. **The Presentation Layer (Front End)**
    
    - This layer constitutes the front end of the application.
    - It includes the HTML, CSS, and JavaScript that users directly interact with.
    - In the context of software design layers, the presentation layer focuses on the user interface and the display of information. JavaScript, for example, can be used to alter the HTML of a page, resulting in visible changes to the user. This can include creating, hiding, and showing elements, using tabs for multiple views, or paging through result sets. It is the layer most closely related to the user experience and is most visible to the end-user.
    - In the Model-View-Controller (MVC) framework, this corresponds to the **View** component, which focuses on rendering data from the Model and presenting it to the user. Modern views often feature component-based templates, reactive data binding, and capabilities like Server-Side Rendering (SSR) or Static Site Generation (SSG).
2. **The Logic Layer (Back End)**
    
    - This layer consists of the back end of the application.
    - Its primary function is to safely retrieve and place data requested or given from the consuming client and pass it along to the data layer.
    - More complex tasks handled by this layer include authentication, authorization, API design, and creating the logic to implement business logic.
    - In a broader software design context, this is also referred to as the **Business Layer**, which models real-world entities like customers, products, and sales, or the **Application Layer** in back-end development, handling REST/GraphQL endpoints, session management, and business logic.
    - The back end also involves server-side programming using technologies like PHP or ASP.NET to dynamically generate content. Unlike client-side scripts, server-side code remains hidden from the client as it is processed on the server. Server scripts can access resources on the web server, such as data storage, which clients cannot directly access.
    - In the MVC framework, this corresponds to the **Controller** component. Controllers handle routing, process requests, generate responses, and integrate middleware. They serve as the intermediary between the View and the Model.
3. **The Database Layer (Data Tier)**
    
    - Also known as the data tier, this layer stores all information connected to user profiles and transactions.
    - It primarily consists of any data that needs to persist in being stored.
    - Server-side scripts commonly interact with this layer through a connection to a Database Management System (DBMS), which is a software system for storing, retrieving, and organizing large amounts of data.
    - In the MVC framework, this aligns with the **Model** component, which is responsible for business logic implementation, data validation rules, database interactions, and state management. Different database types (SQL, NoSQL, VectorDB) are chosen based on specific use cases, such as transactions, real-time applications, or AI applications.

In addition to these core layers,

- **Validation Layer**: JavaScript can be used on the client-side to validate logical aspects of the user's experience, such as ensuring an email address is valid before sending data to the server. This pre-validation helps reduce server load, though server-side validation is still necessary.
- **Asynchronous Layers**: JavaScript can operate asynchronously, routing requests to the server in the background without causing the browser to sit in a loading state. When a response arrives, JavaScript can update a portion of the page, creating a more continuous user experience. This is considered an advanced version of presentation and validation layers and helps separate presentation and logic for more reusable and maintainable code.

The interaction between these layers is crucial. For example, the front-end (presentation layer) using jQuery might make an AJAX request to the back-end (logic layer), which then processes and validates the data, potentially interacts with the database (data layer), and finally returns a JSON/XML response to the front-end to update the UI.

![3-tier architecture](https://vfunction.com/wp-content/uploads/2024/05/blog-3-tier-application.webp)
   
---


4. Define WEB, URL, HTTPS, Name Resolution.
   Ans)

- **WEB**: The Web, also known as the World Wide Web (WWW) or W3, is an interconnected system of public webpages, typically residing on servers. It is a web technology that links web resources together over the internet. It is important to note that the Web is distinct from the Internet; the Web is one of many applications built on top of the Internet, which houses the Web.
- **URL**: A Uniform Resource Locator (URL), also referred to as a Web address, is a reference to a web resource. It specifies the resource's location on a computer network and acts as a gateway for retrieving it. An example is `https://www.google.com`, where `Https` indicates the Transfer Control Protocol and `Google.com` is the URL for Google.
- **HTTPS**: Hypertext Transfer Protocol Secured (HTTPS) is a secured protocol that governs the transfer of Web resources. It is a more secure version of Hypertext Transfer Protocol (HTTP), which is a non-secured protocol for resource transfer. You can typically identify a secured protocol by a visible padlock icon appearing before the address bar in a web browser, whereas a non-secured protocol does not display this icon.
- **Name Resolution**: While the term "Name Resolution" is not explicitly defined in the sources, the concept is strongly related to how web servers handle requests for domain names. A web server, once configured, has its IP address associated through a DNS (Domain Name System) server. This association allows the server to listen for and respond to HTTP requests for that specific domain. A domain name itself is a unique name that identifies resources stored on a website and serves as the website's address. Therefore, "name resolution" implicitly refers to the process (often handled by a DNS server) of translating a human-readable domain name into an IP address that computers use to locate each other on a network.

---


6. Explain 5 types of selectors with examples.
   Ans)
Here are five types of selectors, with examples:

(i). **Element Selectors**
    
    - **Definition**: Element selectors select all instances of a given HTML element. You can select all elements using the universal element selector (`*`), or a group of elements by separating their names with commas. This helps reduce the size and complexity of CSS files by combining identical rules.
    - **Example**: To style all paragraph (`<p>`) elements to have blue text, the rule would look like this:
        
        ```
        p {
            color: blue;
        }
        ```
        
        An example of a grouped selector is shown in the source as:
        
        ```
        h1, h2, h3 {
            color: purple;
        }
        /* This is equivalent to: */
        h1 {
            color: purple;
        }
        h2 {
            color: purple;
        }
        h3 {
            color: purple;
        }
        ```
        
(ii). **Class Selectors**
    
- **Definition**: A class selector allows you to simultaneously target different HTML elements regardless of their position in the document tree. If a series of HTML elements have been labeled with the same `class` attribute value, you can style them using a class selector. The syntax is a period (`.`) followed by the class name.
- **Example**: If you have multiple elements with `class="highlight"`, you can style them all:
        
    ```
        .highlight {
            background-color: yellow;
        }
    ```
        
(iii). **ID Selectors**
    
- **Definition**: An ID selector allows you to target a specific HTML element by its `id` attribute, irrespective of its type or position. IDs must be unique within an HTML document. The syntax is a pound/hash symbol (`#`) followed by the ID name.    - **Example**: To style a single element with `id="main-header"`, the rule would be:
        
    ```
        #main-header {
            font-size: 2em;
            text-align: center;
        }
     ```
        
(iv). **Attribute Selectors**
    
- **Definition**: An attribute selector provides a way to select HTML elements either by the presence of an element attribute or by the value of an attribute. This can be very helpful for styling hyperlinks and images, for instance, to make it obvious when a tooltip is available for a link or image.
- **Example**: To select any element that has a `title` attribute:
        
    ```
        [title] {
            border: 1px dotted gray;
        }
    ```
        
  This would match any element in the document that possesses a `title` attribute.
(v). **Pseudo-Element and Pseudo-Class Selectors**
    
- **Definition**:
        - **Pseudo-element selectors**: Select something that does not explicitly exist as an element in the HTML document tree but is still a recognizable selectable object. For example, you can select the first line or first letter of any HTML element.
        - **Pseudo-class selectors**: Apply to an HTML element but target it based on a specific state or condition.
- **Examples**:
    - **Pseudo-element example**: Styling the first line of a paragraph:
            
        ```
            p::first-line {
                font-weight: bold;
            }
        ```
            
    - **Pseudo-class example**: Styling link states (link, visited, hover):
            
        ```
            a:link {
                color: blue;
            }
            a:visited {
                color: purple;
            }
            a:hover {
                color: red; /* Color of the link when the mouse is over it */
            }
        ```
            
    The syntax for pseudo-class selectors is a colon (`:`) followed by the pseudo-class selector name, with no space after the colon. The order of `:link` and `:visited` should appear before others like `:hover`.

---

6. Write the syntax of below mentioned HTML elements and explain with an example:  
   (i) `<div>`  
   (ii) `<span>`

   Ans)

 (i) `<div>` HTML Element

**Syntax:**

```
<div>
    <!-- Content to be grouped goes here -->
</div>
```

**Explanation and Example:** The `<div>` element is a container element used to create a logical grouping of content. It is primarily used in contemporary CSS-based layouts to mark out sections of content. The `<div>` element itself has no intrinsic visual presentation; its purpose is purely for structuring content for styling or scripting purposes.

 For instance, you might use a `<div>` to group a header, an image, and a paragraph together as a single logical unit that can then be styled using CSS:

```
<div class="product-card">
    <h2>Product Title</h2>
    <img src="product.jpg" alt="Product Image">
    <p>This is a description of the product.</p>
</div>
```

In this example, the `<div>` with the class `product-card` groups related content. CSS could then be applied to `product-card` to style its background, borders, or layout. The sources mention that "Most complex websites are absolutely packed solid with `<div>` elements" and developers often use `id` or `class` attributes with them to provide meaning for styling.

 (ii) `<span>` HTML Element

**Syntax:**

```
<span>
    <!-- Inline content to be styled goes here -->
</span>
```

**Explanation and Example:** The provided sources do not explicitly define the `<span>` HTML element by name. However, they describe the concept of "inline HTML elements" which function similarly to `<span>`. Inline elements are defined as those that "do not cause a paragraph break but are part of the regular 'flow' of the text". Examples of such inline elements given in the sources are `<strong>` and `<a>`.

The `<span>` element is a generic inline container. Similar to how a `<div>` groups block-level content, a `<span>` is used to group or apply styles to a small section of text or other inline content _without_ starting a new line. It is commonly used when you want to apply CSS styles or JavaScript behavior to a specific part of a sentence or a word without affecting the overall flow of the paragraph or surrounding elements.

Here's an example demonstrating its use :

```
<p>
    This is a sentence with some <span style="color: red; font-weight: bold;">important text</span>
    that I want to highlight.
</p>
```

In this example, only the words "important text" would appear in red and bold, because they are wrapped within the `<span>` tags. The `<span>` element allows for precise styling of inline content without disrupting the paragraph's flow.

---
7. Write 5 types of selectors with examples.

8. Illustrate CSS box model. Be sure to label and explain each component of the model with an example.

9. Understand the concept of “distributed” in the context of version control systems like Git, and outline the different states that files can exist in within the Git repository.

10. Differentiate between static and dynamic websites. Provide examples of use cases for each type and explain the technologies commonly used to build them.

11. Explain the importance of version control in software development. Describe any two basic Git commands and how GitHub enhances collaboration among developers.

12. Write the basic structure of an HTML document. Explain the purpose of the `<head>` tag, `<body>` tag and other tags, and provide examples of common HTML elements.

13. Discuss the importance of CSS style properties in web design. Provide examples of commonly used properties for text styling, box model, and layout, and explain their effects.

14. Create an HTML document for a blog post. The document should include:  
    - A proper HTML structure with `<!DOCTYPE>`, `<html>`, `<head>`, and `<body>` tags.  
    - A heading (`<h1>`) for the blog title.  
    - A paragraph (`<p>`) for the blog content with at least 5 sentences.  
    - An image (`<img>`) related to the blog with appropriate attributes.  
    - A hyperlink (`<a>`) to a related article with the text "Read more".  
    - Use semantic elements like `<header>`, `<main>`, and `<footer>` to structure the document.

15. Design an HTML web form for a feedback submission page. The form should include:  
    - A `<form>` tag with the action attribute set to "/submit".  
    - Input fields for:  
        1. Name (text input, required)  
        2. Email (email input, required)  
        3. Rating (number input, range 1 to 5)  
        4. Feedback (text area with a character limit of 500)  
        5. A radio button for subscribing to the newsletter  
        6. A submit button with the text "Submit Feedback"  
    - Use appropriate attributes for validation (e.g., `required`, `min`, `max`).

16. Create a responsive webpage layout using CSS Flexbox and Grid. The layout should include:  
    - A header section with a centered title  
    - A main content section divided into two columns using CSS Grid  
    - A sidebar on the left and a content area on the right, styled using CSS Flexbox  
    - A footer section with three equally spaced links  
    - Ensure the layout is responsive using media queries for different screen sizes (mobile, tablet, desktop)

17. Write HTML code to design the table as shown below. Add embedded CSS to the page such that:  
    (i) All table headings are displayed in red font  
    (ii) All other cells have blue text  

    ``` 
    Sl No | Course | Subject          | Internal | External | Category
    ------|--------|------------------|----------|----------|---------
    1     | B.Tech | Game Design      | 30       | 70       | (AIML)
          |        | Game Programming | 30       | 70       | T P
    ```

18. Justify your answer with proper explanation:  
    (i)  
    ```html
    <html>
    <title> What is the color of the text </title>
    <link rel="stylesheet" href="./style.css">
    <h1 class="a-class" id="an-d"> Sixth Sem Students are in what color?</h1>
    </html>
    ```
    ```css
    .a-class {
      color: blue;
    }
    #an-id {
      color: green;
    }
    ```

    (ii)  
    ```html
    <html>
    <title> What is the color of the text </title>
    <link rel="stylesheet" href="./style.css">
    <h1 class="a-class another-class"> Sixth Sem Students are in what color? </h1>
    </html>
    ```
    ```css
    .a-class {
      color: green;
    }
    .another-class {
      color: blue;
    }
    ```
    What is the color of the h1 element?

19. Describe a scenario where you would choose to use Float, Flexbox, and CSS Grid respectively, and explain why each layout method is most appropriate for its specific scenario.
