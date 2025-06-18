

1. Software engineers should be bound with professional and ethical responsibilities. Discuss with examples.

Software engineers are bound by significant professional and ethical responsibilities due to the pervasive and critical role software plays in modern society. The profession demands a systematic and organized approach, as neglecting established methods can lead to higher costs for testing, quality assurance, and long-term maintenance.

The importance of these responsibilities stems from the potential for software to cause significant good or harm. Professional software development involves creating systems for others, often by teams, and these systems require ongoing maintenance. Consequently, software must be maintainable, dependable, and usable, as well as safe and secure against malicious attacks. A key aspect of professionalism is the pride a "true craftsman" takes in delivering high-quality work and adhering to best practices.

Several core ethical and professional responsibilities for software engineers are outlined in the sources, including principles from the ACM/IEEE Code of Ethics and Professional Practice:

1. **Honesty and Integrity**: Software engineers must uphold normal standards of honesty and integrity and avoid using their skills dishonestly or in ways that discredit the profession.
    
    - **Example**: It would be unethical for a disgruntled employee to embed logic in a payroll program that causes system havoc upon their termination. Similarly, quoting a low price for a software contract while knowing the requirements are ambiguous, with the intent to charge high prices for subsequent changes, is an ethical concern.
    - **Example**: Changing system interfaces without notice to coerce users into paying higher charges raises serious ethical questions.
2. **Confidentiality**: Engineers should respect the confidentiality of clients and employers, even without formal agreements.
    
    - **Example**: An engineer who learns about ambiguous requirements from a previous employer, which could increase costs for their current employer, faces a dilemma between their current employer's interests and their confidentiality obligation to the former employer.
3. **Competence**: Engineers must not misrepresent their skills and should not knowingly accept work beyond their capabilities. The fact that non-certified individuals can practice software engineering highlights the ongoing debate about professional standards and potential drawbacks.
    
4. **Intellectual Property Rights**: Awareness of and protection for intellectual property rights (e.g., patents, copyright) of clients and employers are crucial.
    
    - **Example**: When reusing software components, engineers must consider copyright and intellectual property issues to ensure legal and ethical compliance.
5. **Avoid Computer Misuse**: Technical skills must not be used to misuse others' computers, from minor infractions like game-playing on employer machines to serious acts like disseminating malware.
    
6. **Public Interest (Health, Safety, and Welfare)**: Engineers must prioritize the public interest, especially concerning health, safety, and welfare, as their work can directly impact human lives.
    
    - **Example**: For critical software systems, such as nuclear reactor controls or medical devices like radiotherapy machines, thorough testing and verification are essential, even after formal verification, to ensure safety. The Warsaw Airport accident, where a system failed due to an incomplete specification despite the software operating as designed, underscores that reliability alone is not sufficient for safety. Falsifying safety validation records due to time pressure, leading to a potentially unsafe system, is a severe breach of this responsibility.
    - **Example**: Designing and building drone systems presents societal challenges that engineers must ethically consider.
7. **Product Quality**: Products and their modifications must meet the highest professional standards for maintainability, dependability, and usability.
    
    - **Example**: Every developer should also act as a tester to ensure the quality of their code units. Releasing software known to contain faults raises ethical questions about liability and warranties, as software failures can cause significant inconvenience or loss to users.
    - **Example**: Agile practices like "Check before check-in," "Never break the build," and "Fix problems when you see them" promote collective responsibility for software quality within a team. A scenario where a colleague produces low-defect software but consistently ignores organizational quality standards presents a management and ethical dilemma regarding the balance between individual output and professional adherence.
8. **Professional Judgment and Independence**: Maintaining integrity and independent professional judgment is paramount.
    
9. **Management Responsibility**: Software engineering managers must promote an ethical approach to software development and maintenance.
    
    - **Example**: Managers face ethical dilemmas when pressured to deliver software on schedules that require unpaid overtime from teams, especially when team members have family responsibilities.
10. **Advancing the Profession, Fairness to Colleagues, and Lifelong Learning**: Engineers are expected to advance the profession's reputation, support colleagues, and engage in continuous learning to promote ethical practices.
    

Software engineers frequently encounter ethical dilemmas in their professional lives, often involving conflicting objectives or differing perspectives among stakeholders. These situations demand careful judgment and a commitment to professional principles to navigate complexities such as balancing innovation with regulatory compliance or managing the societal impact of new technologies.

  ---
  
    
2. Consider a case study and explain when an incremental process model is applicable. Support your justification with a suitable diagram.

   An incremental process model is applicable when a software system's requirements are expected to evolve, when early delivery of core functionality is a priority, or when continuous user feedback is essential to shape the final product. This approach interleaves the activities of specification, development, and validation, allowing for rapid feedback and adaptation.

**Explanation of Incremental Process Model**

In an incremental development approach, the system is built and delivered as a series of versions or "increments," with each new version adding more functionality to the previous one. This differs from plan-driven models (like the waterfall model) where all activities are planned in advance.

Key characteristics and advantages of incremental development include:

- **Interleaved Activities**: Specification, development, and validation are intertwined, fostering quick feedback loops.
- **Early Functionality**: Early increments typically include the most important or urgent functionalities, allowing customers to use and derive value from the software sooner than with a waterfall process.
- **Adaptability to Change**: This model inherently embraces changing requirements, as new functionalities can be defined or existing ones altered for later increments based on feedback or evolving needs.
- **Customer Involvement**: It supports continuous engagement from the customer, who helps define acceptance tests and influences the prioritization of features.
- **Risk Management**: By delivering in small increments, potential problems or misunderstandings of requirements can be identified and corrected early, reducing the overall project risk.

One challenge, from a management perspective, is that the process visibility can be lower, as producing detailed documentation for every version might not be cost-effective.

**Case Study: iLearn Digital Learning Environment**

The iLearn digital learning environment, a system designed to support learning in schools, serves as a suitable case study for the application of an incremental process model.

**Justification for Applicability**:

1. **Evolving Requirements**: Educational software, such as iLearn, often faces unstable and evolving requirements. Pedagogical approaches change, new technologies emerge, and feedback from teachers and students can significantly alter desired functionalities. An incremental model allows the development to adapt to these shifts, rather than being rigidly bound to an outdated initial specification.
2. **Layered Service Architecture**: iLearn is designed with a "layered service architecture" where "All components in the system should be considered to be replaceable services". This architectural style naturally aligns with incremental development. Each service or layer can be developed and deployed as a distinct increment, providing a modular and adaptable foundation. For example, a basic photo-sharing feature might be delivered first, followed by collaborative wiki functions or advanced analytics in later increments.
3. **Customer-Driven Feedback**: Like many modern applications, iLearn benefits from continuous feedback from its users (teachers and pupils). Early deployment of working increments allows users to interact with the system and provide valuable insights that lead to new user stories or refinements, guiding subsequent development phases. This is particularly true for digital learning environments where hands-on experience reveals practical usability and effectiveness.
4. **Early Value Delivery**: An incremental approach means that useful parts of the iLearn system can be deployed and utilized by schools at a relatively early stage. For instance, a core set of features like basic content sharing or assignment submission could be released, enabling immediate educational value while more complex features are still under development.

In summary, for a system like iLearn, where flexibility, user feedback, and modular architecture are crucial, the incremental development model provides an effective framework for development and continuous improvement.

**Diagram of Incremental Development Model**

The general model for incremental development is illustrated below, showing the interleaved and iterative nature of its core activities:

```
+---------------------+
| Requirements        |<---+
| Engineering         |    |
| (Specification)     |    |
+----------+----------+    |
           |               |
           v               |
+----------+----------+    |
| Software            |    |
| Design &            |    |
| Implementation      |    |
+----------+----------+    |
           |               |
           v               |
+----------+----------+    |
| Validation          |    |
| (Testing)           |    |
+----------+----------+    |
           |               |
           v               |
+----------+----------+    |
| Delivered Increment |----+
+---------------------+
```

(Adapted from information in)

This diagram shows how specification, development, and validation activities are cycled through repeatedly for each increment, leading to a series of delivered versions of the system.

---

3. Consider the case study of an online library management system and write the software requirement specification document for the same.  
    **(OR)**
    
Based on the sources, a Software Requirement Specification (SRS) document for an online library management system would typically follow a structured format, such as the IEEE standard mentioned in the sources. This document aims to define the services the system should provide and the constraints on its operation, acting as a bridge between customer needs and system development.

Here is a proposed structure and content for the SRS document:

---

**Software Requirement Specification (SRS) Document: Online Library Management System**

**Version: 1.0** **Date: April 22, 2025**

**Preface** This document outlines the software requirements for the Online Library Management System (OLMS). It is intended for all stakeholders, including library staff, patrons, system developers, and quality assurance personnel, to provide a clear and comprehensive understanding of the system's functionalities and constraints. This initial version serves as a foundational specification, subject to refinement through iterative development and feedback.

**1. Introduction** This section describes the need for the OLMS, briefly outlines its functions, and explains how it integrates with existing library operations and strategic objectives. The current manual or disparate systems present challenges in efficiency, accessibility, and data management. The OLMS aims to modernize library services, enhance user experience, and streamline administrative tasks.

**1.1. Purpose of the System** The Online Library Management System (OLMS) is designed to automate and manage core library functions. It will enable patrons to access library resources digitally, manage their borrowing activities, and interact with the library remotely. For library staff, it will provide tools for efficient management of library inventory, patron records, and administrative workflows. The goal is to provide a comprehensive, user-friendly, and dependable system.

**1.2. Scope of the System** The OLMS will cover functionalities for:

- **Patron Services:** User registration, browsing/searching the catalog, borrowing/returning/renewing books, viewing borrowing history, and receiving notifications.
- **Librarian Services:** Book management (add, edit, delete), patron management (add, edit, delete, fine management), circulation management, and reporting.
- **Administrator Services:** System configuration, user role management, and overall system monitoring.

The system will be accessible via web browsers, providing a consistent experience across various devices.

**1.3. Glossary** This section defines technical terms and abbreviations used in this document to ensure clarity for all readers, regardless of their technical background.

- **OLMS:** Online Library Management System
- **Patron:** A registered user of the library system (e.g., student, faculty, general public).
- **Librarian:** Library staff responsible for daily operations and managing library resources.
- **Administrator:** Personnel with full control over system configuration and user management.
- **Functional Requirement:** A statement of a service the system should provide.
- **Non-functional Requirement:** A statement of a constraint or expected behavior that applies to the system, often relating to emergent properties like performance or security.
- **SRS:** Software Requirement Specification.

**2. User Requirements Definition** This section describes the services provided for the user, presented in natural language with diagrams where appropriate, understandable by users who may not have detailed technical knowledge.

**2.1. Functional Requirements (User View)** These requirements describe what the system should do from the perspective of its users.

- **UR1: Patron Account Management:**
    - Patrons shall be able to register for a new account by providing necessary personal details (name, ID, contact information).
    - Patrons shall be able to log in to their accounts using unique credentials.
    - Patrons shall be able to update their personal information and change their password.
- **UR2: Book Catalog Browsing and Search:**
    - Patrons shall be able to browse the library's collection by categories (e.g., genre, author, subject).
    - Patrons shall be able to search for books using keywords, title, author, or ISBN.
    - Search results shall display relevant information about each book, including availability status.
- **UR3: Borrowing and Return Operations:**
    - Patrons shall be able to request to borrow an available book online.
    - Patrons shall be able to view their current borrowed books and due dates.
    - Patrons shall be able to request online renewal of borrowed books, subject to library policies.
- **UR4: Notifications:**
    - Patrons shall receive notifications for overdue books, successful renewals, and when a reserved book becomes available.
- **UR5: Librarian Book Management:**
    - Librarians shall be able to add new books to the catalog, including details such as title, author, ISBN, and quantity.
    - Librarians shall be able to edit existing book details.
    - Librarians shall be able to mark books as returned or lost.
- **UR6: Librarian Patron Management:**
    - Librarians shall be able to register new patrons and update existing patron information.
    - Librarians shall be able to manage fines for overdue or lost books.
- **UR7: System Administration:**
    - Administrators shall be able to manage user roles and permissions within the system.

**2.2. Non-functional Requirements (User View)** These requirements constrain the system and the development process, relating to desired qualities like performance, security, and usability.

- **UR8: Performance:**
    - The system shall display search results for books within 2 seconds for a database of up to 100,000 records under normal load conditions.
    - User login shall complete within 1 second.
- **UR9: Security:**
    - The system shall protect all patron personal information and borrowing history from unauthorized access.
    - All user authentication shall be encrypted.
    - Only authorized librarians shall be able to modify book or patron records.
- **UR10: Usability:**
    - The system's user interface shall be intuitive and easy to navigate for patrons of varying technical proficiency.
    - Error messages shall be clear and provide actionable guidance to the user.
- **UR11: Reliability:**
    - The system shall be available 99.5% of the time, excluding scheduled maintenance.
    - Data integrity shall be maintained even in the event of system failures.
- **UR12: Maintainability:**
    - The system's code and documentation shall be structured to facilitate future updates and bug fixes.

**3. System Architecture** This chapter presents a high-level overview of the anticipated system architecture, showing the distribution of functions across system modules. For an online library management system, a layered client-server architecture is commonly suitable.

- **Presentation Layer:** Handles user interaction and displays information via web browsers.
- **Application Logic Layer:** Implements core business logic such as search algorithms, borrowing rules, and user management.
- **Data Access Layer:** Manages interaction with the database, ensuring data integrity and security.
- **Database Layer:** Stores all system data, including book records, patron information, and transaction logs.

This architecture supports scalability and modularity, allowing for independent development and deployment of components.

**4. System Requirements Specification** This section provides a more detailed and precise specification of the functional and non-functional requirements, intended for system developers.

**4.1. Functional Requirements (System View)**

- **SR1: Authentication Module:**
    - The system shall implement an authentication service that validates patron and staff credentials against a secure user database.
    - Successful authentication shall result in the generation of a session token.
- **SR2: Catalog Search Service:**
    - The search service shall support full-text search across title, author, and keyword fields.
    - The search results shall be paginated and allow for sorting by relevance, title, or author.
    - Search queries shall handle common typographical errors and offer suggestions.
- **SR3: Transaction Processing for Borrowing/Return:**
    - Upon successful borrowing, the system shall decrement the available quantity of the book and record the borrowing transaction (patron ID, book ID, borrow date, due date).
    - Upon successful return, the system shall increment the available quantity and mark the transaction as returned.
    - Renewal requests shall extend the due date by a predefined period, provided no other patron has reserved the book and renewal limit is not exceeded.
- **SR4: Notification Service:**
    - The system shall trigger email notifications for overdue books 24 hours before the due date and daily thereafter until returned.
    - The system shall send an email notification when a reserved book becomes available for pickup.

**4.2. Non-functional Requirements (System View)**

- **SR5: Data Privacy and Security:**
    - The system shall use HTTPS for all client-server communications to ensure data confidentiality and integrity.
    - User passwords shall be stored as one-way hashed values with salt.
    - Access control shall be implemented based on role-based access control (RBAC), restricting librarian functionalities to authenticated librarian accounts and administrative functionalities to authenticated administrator accounts.
- **SR6: Scalability:**
    - The system shall be capable of supporting up to 500 concurrent users without degradation in performance (response times remaining within stated limits).
    - The database shall be designed to scale vertically and horizontally to accommodate a growing number of books and patrons.
- **SR7: Error Handling and Recovery:**
    - The system shall log all critical errors, including failed transactions, authentication failures, and unhandled exceptions.
    - A daily backup of the database shall be performed, with a recovery point objective (RPO) of 24 hours.

**5. System Models** This section describes the graphical models that would be developed as part of the system design. While the actual diagrams are not included here, their purpose and content for the OLMS are detailed.

- **5.1. Use Case Diagrams:**
    - These diagrams will identify the main interactions between users (Patron, Librarian, Administrator) and the OLMS, showing the different functionalities offered. For example, a "Search Book" use case would connect the "Patron" actor to the system.
- **5.2. Class Diagrams:**
    - These will illustrate the static structure of the system, showing the main object classes (e.g., `Book`, `Patron`, `Loan`, `UserAccount`) and their relationships (associations, aggregations, generalizations).
- **5.3. Sequence Diagrams:**
    - These diagrams will depict the dynamic interactions between objects to accomplish a specific use case. For instance, a sequence diagram for "Borrow Book" would show the messages exchanged between `Patron`, `BookManagementService`, `LoanManagementService`, and `Database`.
- **5.4. State Machine Diagrams:**
    - These will model the behavior of specific objects or system states over time, showing transitions triggered by events. For example, a `Book` object might have states like "Available," "On Loan," "Reserved," with transitions based on borrowing or return events.

**6. System Evolution** This section discusses the fundamental assumptions on which the system is based and any anticipated changes due to hardware evolution, changing user needs, or new library policies. Software systems must adapt and evolve to remain useful.

- **Phase-based Enhancements:** Future iterations may include integration with payment gateways for fines, digital book lending, personalized recommendations, or integration with external academic databases.
- **Technology Updates:** Regular updates to the underlying software stack (operating system, database, programming language frameworks) will be necessary to maintain security and performance.
- **Regulatory Changes:** Adaptation to new data privacy laws or library regulations.
- **User Feedback:** The system will evolve based on continuous user feedback and changing needs, managed through a change management process.

**7. Appendices** This section provides detailed, specific information related to the OLMS that supports the main requirements, such as hardware and database descriptions.

- **Appendix A: Database Schema (Conceptual)**: A high-level representation of the database tables and their relationships (e.g., `Books`, `Patrons`, `Loans`, `Reservations`).
- **Appendix B: User Interface Mockups**: Visual representations of key screens and user flows (e.g., login page, search results page, patron dashboard).
- **Appendix C: Environment Assumptions**: Details on the expected operating environment (e.g., specific web browser versions, minimum network bandwidth).

**Index** A comprehensive index would be included for easy navigation of the document, listing key terms, concepts, and figures.

---
4. Identify the software process model suitable for Banking applications. Illustrate the identified process model with suitable steps.

 For banking applications, especially interactive and transaction-based systems like online banking or ATMs, the **Incremental Development** process model is highly suitable. This approach interweaves the activities of specification, development, and validation, allowing for rapid feedback and continuous evolution of the software.

**Suitability for Banking Applications:**

- **Rapidly Changing Requirements** Banking and other business systems frequently face rapidly changing requirements due to evolving market conditions, regulatory changes, and user expectations. Incremental development, often mixed with agile practices, offers the flexibility needed to accommodate these changes.
- **Interactive and Transaction-Oriented Nature** Banking applications are typically interactive systems that process user requests for information and update databases. Developing these complex systems in smaller, manageable increments allows for focused development and testing of critical functionalities, ensuring data integrity and responsiveness.
- **Early Delivery and Feedback** This model enables early delivery of useful software to customers, even if not all functionality is complete. Customers can begin to use and derive value from the system sooner, and their feedback can be incorporated into subsequent increments, reducing the risk of major rework later.
- **Integration of Existing Systems** Business systems, including banking applications, are increasingly developed by configuring and integrating existing components or systems. Incremental development allows for the phased integration of these components, enabling verification at each step.

**Steps of the Incremental Development Model:**

The Incremental Development model is based on the idea of developing an initial implementation and then evolving the software through several versions based on user feedback until the required system is complete. It involves interleaving core software engineering activities:

1. **Initial Implementation / Increment Definition**: An initial version of the system (or a small increment of functionality) is developed. In a plan-driven incremental approach, system increments are identified in advance. In a more agile approach (often adopted for business systems), early increments are identified, with later increments depending on progress and customer priorities.
2. **Specification**: Requirements for the current increment are defined. For a banking application, this might involve specifying the core functionality like user login and account balance inquiry.
3. **Development**: The software for the defined increment is designed and programmed. For instance, the login module and the display logic for account balances would be implemented.
4. **Validation**: The developed increment is tested to ensure it conforms to its specification and meets user expectations. This includes verifying the login process and the accuracy of the displayed balance.
5. **Feedback and Evolution**: User feedback on the delivered increment is gathered. This feedback, along with new or changing requirements, informs the planning and development of subsequent increments. The process then cycles back to defining the next increment, adding more functionality until the complete system is realized.

**Illustrative Steps for a Banking Application (e.g., Online Banking System):**

Consider an online banking application that needs to evolve over time:

- **Increment 1: Basic Account Inquiry**
    
    - **Specification**: Define requirements for user authentication (login) and viewing current account balances.
    - **Development**: Implement secure login functionality and a basic display for savings and checking account balances.
    - **Validation**: Test login credentials, verify balance accuracy, and check display usability.
    - **Feedback**: Deploy to a pilot group; gather feedback on login experience, clarity of balance display, and initial performance.
- **Increment 2: Funds Transfer**
    
    - **Specification**: Based on feedback, define requirements for transferring funds between a user's own accounts within the same bank.
    - **Development**: Implement the transfer logic, ensuring atomic transactions and real-time updates to account balances.
    - **Validation**: Test various transfer scenarios, including edge cases like insufficient funds, and confirm transaction integrity.
    - **Feedback**: Pilot users test fund transfers; identify any usability issues or missing features (e.g., transaction history).
- **Increment 3: Bill Payment**
    
    - **Specification**: Define requirements for setting up payees and scheduling one-time or recurring bill payments.
    - **Development**: Integrate with external payment gateways, implement scheduling logic, and create interfaces for payee management.
    - **Validation**: Thoroughly test payment processing, due dates, and notifications.
    - **Feedback**: Users test the bill payment feature, providing insights into ease of use and error handling.

This iterative process allows the banking application to be delivered incrementally, adapting to user needs and market demands throughout its development life cycle.

---

5. Differentiate between various types of non-functional requirements with suitable examples for each.  
    **(OR)**

   Non-functional requirements are constraints on the services or functions offered by a system, rather than direct statements of what the system should do. They typically apply to the system as a whole and often relate to emergent system properties such as reliability, response time, and memory usage. They can also define constraints on the system's implementation, for instance, specifying I/O device capabilities or data representations used in interfaces.

   These requirements are often more critical than individual functional requirements, as failing to meet a non-functional requirement can render the entire system unusable. For example, an aircraft system that does not meet its reliability requirements will not be certified as safe for operation. Their implementation may be spread throughout the system, affecting the overall architecture or generating related functional requirements. Ideally, non-functional requirements should be specified quantitatively so they can be objectively tested.

   Non-functional requirements can be differentiated into three main types based on their origin and the aspects of the system they constrain: Product Requirements, Organizational Requirements, and External Requirements.

##### Types of Non-Functional Requirements:

1. **Product Requirements**
    
    - **Definition**: These requirements specify or constrain the runtime behavior of the software itself. They focus on how the system performs its functions.
    - **Differentiation**: Product requirements directly address the quality attributes and characteristics of the software as a product, affecting its performance, reliability, security, and usability in operation.
    - **Examples**:
        - **Performance Requirements**: Dictate how fast the system must execute or how much memory it requires. For instance, "The Mentcare system shall be available to all clinics during normal working hours (Mon–Fri, 08:30–17:30). Downtime within normal working hours shall not exceed 5 seconds in any one day". Another example is a web service needing to process "up to 100 requests per second peak load".
        - **Reliability Requirements**: Set out the acceptable failure rate or probability of product failure. This can be measured using metrics like "probability of failure on demand (POFOD)" or "rate of occurrence of failures (ROCOF)".
        - **Security Requirements**: Specify how a system should protect itself against threats. For example, "Access to the catalog service shall be restricted to employees of accredited organizations" and "The prices and configurations offered to each customer shall be confidential, and access to these shall only be provided to employees of that customer".
        - **Usability Requirements**: Define how easy the system is for users to learn and operate. An example could be, "Medical staff shall be able to use all the system functions after two hours of training. After this training, the average number of errors made by experienced users shall not exceed two per hour of system use".
        - **Robustness**: Refers to how well the system handles unexpected inputs or failures.
2. **Organizational Requirements**
    
    - **Definition**: These are broad system requirements derived from the policies and procedures within both the customer's and the developer's organizations.
    - **Differentiation**: Organizational requirements constrain the system's development process or its operational context within the organizational structure, reflecting internal standards and practices.
    - **Examples**:
        - **Operational Process Requirements**: Define how the system will be used within the organization.
        - **Development Process Requirements**: Specify the programming language, development environment, or process standards to be adhered to during development. For example, "The system must be implemented in a safe subset of Ada and checked using static analysis".
        - **Authentication Requirements**: Derived from company policy, such as "Users of the Mentcare system shall identify themselves using their health authority identity card".
3. **External Requirements**
    
    - **Definition**: These requirements arise from factors external to the system and its development process, typically involving legal, regulatory, or ethical considerations.
    - **Differentiation**: External requirements impose obligations on the system due to external laws, regulations, or public concerns, independent of the product's internal behavior or the organization's specific policies.
    - **Examples**:
        - **Regulatory Requirements**: Mandates what must be done for the system to be approved by a regulatory body.
        - **Legislative Requirements**: Ensure the system operates within the law. For example, "The system shall implement patient privacy provisions as set out in HStan-03-2006-priv".
        - **Ethical Requirements**: Ensure the system's acceptability to its users and the general public.

---

6. Determine the role of integration and configuration model in software engineering. With a suitable diagram explain the steps involved.

The integration and configuration model, also known as reuse-oriented software engineering, is a software development approach that emphasizes the reuse of existing software components or systems. This model is predicated on the availability of a base of reusable software components and an integrating framework designed for composing these components. It has become widely used, especially since 2000.

**Role of the Integration and Configuration Model:** The primary role of this model is to reduce the amount of new software that needs to be developed, thereby reducing development costs and risks, and typically leading to faster software delivery. This approach focuses on configuring existing components for use in a new setting and integrating them into a complete system.

**Steps Involved in Reuse-Oriented Software Engineering:** The general process model for reuse-based development, as illustrated in Figure 2.3 in the sources, involves several key stages:

1. **Requirements Specification**: The process begins with the proposal of initial requirements for the system. These requirements do not need to be highly detailed but should include brief descriptions of essential requirements and desired system features.
2. **Software Discovery and Evaluation**: Given an outline of the software requirements, a search is conducted for existing components and systems that can provide the necessary functionality. Candidate components and systems are then evaluated to determine if they meet the essential requirements and are generally suitable for integration into the system.
3. **Requirements Refinement**: During this stage, the initial requirements are refined using the information gathered about the discovered reusable components and applications. The requirements are modified to reflect the available components, and the system specification is redefined. If modifications are not possible, the component analysis activity (step 2) may be re-entered to search for alternative solutions.
4. **Application System Configuration**: If a suitable off-the-shelf application system that meets the refined requirements is identified, it may then be configured for use to create the new system.
5. **Component Adaptation and Integration**: If no single off-the-shelf system is available, individual reusable components may be modified, and new components may be developed if needed. These adapted and new components are then integrated to create the final system.

**Diagram:**

The diagram below (Figure 2.3 from the sources) visually represents the "Reuse-oriented software engineering" process:

![](images/5.jpeg)


_Figure 2.3: Reuse-oriented software engineering_

The diagram illustrates the flow from initial requirements to the final application system, highlighting the iterative nature of requirements refinement based on component discovery and evaluation, and the two parallel paths for system creation: configuring an existing application or adapting and integrating individual components.

**Advantages and Disadvantages:** The main advantage of this approach is the reduction in the amount of software that needs to be developed, which translates to lower costs and risks, and often faster delivery. However, a significant disadvantage is that requirements compromises are inevitable, potentially leading to a system that doesn't perfectly meet the users' actual needs. Additionally, some control over the system's evolution is lost because new versions of reusable components are not controlled by the organization using them.

---

7. Differentiate between plan driven development and agile development. Illustrate the role of agile models in prescribing medication in a Healthcare system.  
    **(OR)**

Plan-driven development and agile development represent distinct approaches to software engineering, differing in their planning, requirements handling, and overall process.

### Differentiation Between Plan-Driven Development and Agile Development

**Plan-Driven Development** Plan-driven processes meticulously plan all activities in advance, with progress measured against a predefined plan. These are often referred to as "traditional" ways of managing large software development projects.

- **Characteristics**:
    - **Sequential Phases**: Activities such as specification, development, validation, and evolution are represented as separate, sequential phases (e.g., requirements specification, software design, implementation, testing).
    - **Up-front Planning**: Planning and scheduling of all process activities occur before software development begins. Early decisions are made, which are then refined and followed.
    - **Detailed Documentation**: Formal documents are produced at each stage, serving as inputs for subsequent phases and for communication between teams.
    - **Suitability**: Best suited for systems with stable requirements, such as embedded systems interfacing with hardware, or critical systems requiring extensive safety and security analysis and certification. They are also often used for large software systems developed by several partner companies where complete specifications are needed for independent subsystem development.
- **Examples**: The Waterfall model and the V-model are prime examples. The V-model explicitly specifies testing activities associated with each development phase, beginning from the start and continuing until the end of the life cycle.
- **Disadvantages**: Often results in a long feedback cycle between requirements specification and system testing, as the customer is typically absent during intermediate phases. Defects introduced early can be costly to correct if discovered later. The approach emphasizes analysis over synthesis, which first occurs at integration testing. It can also be very lengthy, leading to software delivery long after original specification, which can be problematic in fast-moving business environments where requirements change rapidly.

**Agile Development** Agile methods are iterative and incremental approaches focused on rapid software development and delivery, particularly designed to accommodate changing requirements.

- **Characteristics**:
    - **Iterative and Incremental**: Development occurs in small increments or versions, with new releases often created and made available to customers every few weeks.
    - **Customer-Driven**: Customers are closely involved throughout the development process, providing and prioritizing new requirements and evaluating system iterations. Requirements are often expressed as "user stories".
    - **Flexibility**: Aims to be flexible with respect to changing requirements, with iterations occurring across activities, meaning requirements and design evolve together.
    - **Minimal Documentation**: Process documentation and bureaucracy are minimized, focusing instead on the code itself and informal communications among team members.
    - **Extensive Tool Support**: Relies heavily on tools for automated testing, configuration management, and system integration.
- **Principles (Agile Manifesto)**:
    - Individuals and interactions over processes and tools.
    - Working software over comprehensive documentation.
    - Customer collaboration over contract negotiation.
    - Responding to change over following a plan.
- **Examples**: Extreme Programming (XP), Scrum, and Test-Driven Development (TDD) are key agile methods.
- **Advantages**: Reduces the cost of implementing requirements changes and makes it easier to get customer feedback. Enables early delivery and deployment of useful software. Promotes continuous integration and refactoring to maintain code quality and structure. TDD, in particular, offers excellent fault isolation.
- **Challenges**: The process may not be visible to managers. System structure can degrade with continuous changes if not refactored. Informality can be incompatible with legal contract definitions for large companies. It is most appropriate for new software development, but less so for maintenance, where lack of documentation and team continuity can be problems. Scaling agile methods to large, distributed, or highly regulated projects often requires integrating some plan-based practices.

### Role of Agile Models in Prescribing Medication in a Healthcare System (Mentcare System)

The Mentcare system is a mental health care patient information system that manages information about patients attending clinics and their treatments. In an agile development environment, the design and implementation of features like prescribing medication would leverage agile models such as user stories and test-driven development.

1. **User Stories for Requirements Definition**:
    
    - In agile methods, requirements are expressed as "user stories," which are scenarios of use experienced by a system user. These are concise descriptions of customer needs.
    - For the Mentcare system, a user story like "Prescribing medication" would be developed through close collaboration between the system customer (e.g., a medical staff member or doctor) and the development team.
    - This story would outline the process: a prescriber chooses a drug, inputs the dose, and confirms the prescription. Critically, it would also include system checks, such as ensuring the dose is within an approved range and issuing warnings for known patient allergies.
    - These user stories are then broken down into smaller "task cards" by the development team, with effort estimates. For the "Prescribing medication" story, tasks could include "Check the prescribed dose against the minimum and maximum" or "Issue an error message if outside range".
2. **Test-First Development (TDD) for Implementation and Verification**:
    
    - Test-driven development (TDD), a core practice in agile methods like Extreme Programming, mandates writing executable tests _before_ writing the program code.
    - For the Mentcare system's medication prescription feature, developers would write automated tests based on the task cards derived from the user stories.
    - **Example: Dose Checking and Allergy Warnings**:
        - Based on the requirement "If a patient is known to be allergic to any particular medication, then prescription of that medication shall result in a warning message being issued to the system user," specific test cases would be written _before_ the code to implement this logic.
        - Examples of such test cases include:
            - Setting up a patient record with no known allergies and prescribing medication to ensure no warning is issued.
            - Setting up a patient record with a known allergy and prescribing that medication to verify the warning is issued.
            - Testing multiple allergies to ensure correct warnings for each drug.
        - A specific test case description for dose checking might include steps like checking the prescribed dose against minimum/maximum limits and enabling a 'Confirm' button if within range, or issuing an error message if not.
    - These tests are initially run on non-existent code, causing them to fail, which then drives the development of "just enough" code to make the tests pass.
    - **Benefits in Mentcare**: This approach ensures that critical functional and non-functional requirements (like patient safety through correct dose checking and allergy warnings) are precisely met. Automated testing allows for continuous verification: whenever new functionality is added, all existing tests can be quickly rerun, immediately catching any regressions or new problems introduced. This also helps developers and testers to deeply understand the requirements early in the process.
---
    
8. Explain the role of interaction models in software engineering. Consider an ATM application and generate sequence diagram for balance enquiry.

 