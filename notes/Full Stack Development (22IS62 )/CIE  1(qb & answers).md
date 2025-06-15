
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
* **Use Case**: Small to medium-sized projects, where a separate CSS file is not necessary.
* **Advantages**: Easy to implement, can be used for small projects, and can be easily modified.
* **Disadvantages**: Can make HTML code bulky, not ideal for large projects.

  **External CSS**

* **Definition**: CSS styles defined in a separate file with a `.css` extension, linked to an HTML document using the `<link>` element.
* **Use Case**: Large projects, where a separate CSS file is necessary for organization and scalability.
* **Advantages**: Easy to maintain, update, and reuse styles across multiple pages, makes HTML code cleaner.
* **Disadvantages**: Requires a separate file, can be slow to load if not optimized.

  **Comparison **

| CSS Type | Use Case | Advantages | Disadvantages |
| --- | --- | --- | --- |
| Inline | Small, one-time changes | Quick and easy to implement | Makes HTML code messy, not scalable |
| Internal | Small to medium-sized projects | Easy to implement, easy to modify | Makes HTML code bulky, not ideal for large projects |
| External | Large projects | Easy to maintain, update, and reuse styles | Requires a separate file, can be slow to load if not optimized |

---

3. Explain the concept of Cascading Style Sheets and its role in web development. Compare and contrast inline, internal, and external CSS, highlighting their use cases and advantages.

4. Explain in detail Layers of Full Stack Development.

5. Define WEB, URL, HTTPS, Name Resolution.

6. Explain 5 types of selectors with examples.

7. Write the syntax of below mentioned HTML elements and explain with an example:  
   (i) `<div>`  
   (ii) `<span>`

8. Write 5 types of selectors with examples.

9. Illustrate CSS box model. Be sure to label and explain each component of the model with an example.

10. Understand the concept of “distributed” in the context of version control systems like Git, and outline the different states that files can exist in within the Git repository.

11. Differentiate between static and dynamic websites. Provide examples of use cases for each type and explain the technologies commonly used to build them.

12. Explain the importance of version control in software development. Describe any two basic Git commands and how GitHub enhances collaboration among developers.

13. Write the basic structure of an HTML document. Explain the purpose of the `<head>` tag, `<body>` tag and other tags, and provide examples of common HTML elements.

14. Discuss the importance of CSS style properties in web design. Provide examples of commonly used properties for text styling, box model, and layout, and explain their effects.

15. Create an HTML document for a blog post. The document should include:  
    - A proper HTML structure with `<!DOCTYPE>`, `<html>`, `<head>`, and `<body>` tags.  
    - A heading (`<h1>`) for the blog title.  
    - A paragraph (`<p>`) for the blog content with at least 5 sentences.  
    - An image (`<img>`) related to the blog with appropriate attributes.  
    - A hyperlink (`<a>`) to a related article with the text "Read more".  
    - Use semantic elements like `<header>`, `<main>`, and `<footer>` to structure the document.

16. Design an HTML web form for a feedback submission page. The form should include:  
    - A `<form>` tag with the action attribute set to "/submit".  
    - Input fields for:  
        1. Name (text input, required)  
        2. Email (email input, required)  
        3. Rating (number input, range 1 to 5)  
        4. Feedback (text area with a character limit of 500)  
        5. A radio button for subscribing to the newsletter  
        6. A submit button with the text "Submit Feedback"  
    - Use appropriate attributes for validation (e.g., `required`, `min`, `max`).

17. Create a responsive webpage layout using CSS Flexbox and Grid. The layout should include:  
    - A header section with a centered title  
    - A main content section divided into two columns using CSS Grid  
    - A sidebar on the left and a content area on the right, styled using CSS Flexbox  
    - A footer section with three equally spaced links  
    - Ensure the layout is responsive using media queries for different screen sizes (mobile, tablet, desktop)

18. Write HTML code to design the table as shown below. Add embedded CSS to the page such that:  
    (i) All table headings are displayed in red font  
    (ii) All other cells have blue text  

    ``` 
    Sl No | Course | Subject          | Internal | External | Category
    ------|--------|------------------|----------|----------|---------
    1     | B.Tech | Game Design      | 30       | 70       | (AIML)
          |        | Game Programming | 30       | 70       | T P
    ```

19. Justify your answer with proper explanation:  
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

20. Describe a scenario where you would choose to use Float, Flexbox, and CSS Grid respectively, and explain why each layout method is most appropriate for its specific scenario.
