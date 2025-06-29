
1. Define Software Engineering.

  Software engineering is an engineering discipline concerned with all aspects of software production, from the initial concept and system specification through to operation and maintenance. It involves applying theories, methods, and tools selectively while working within organizational and financial constraints to find solutions.

Key aspects of software engineering include:

- **Purpose**: Its primary purpose is to produce reliable and trustworthy systems economically and quickly. It supports professional software development, which involves teams rather than individuals, and software that is maintained and changed throughout its life.
- **Scope**: It is not just about the technical processes of software development but also includes activities such as software project management and the development of supporting tools, methods, and theories.
- **Systematic Approach**: Software engineers generally adopt a systematic and organized approach, although a more creative, less formal approach might be suitable for certain types of software, such as interactive web-based systems and mobile apps.
- **Distinction from Programming**: It encompasses techniques for program specification, design, and evolution, which are typically not relevant for personal software development. It's fundamentally about managing the complexities of building large and evolving software systems.
- **Interdisciplinary Nature**: Software engineering is related to both computer science and systems engineering.
    - **Computer Science**: Focuses on the theories and methods underlying computers and software systems, whereas software engineering addresses the practical problems of producing software.
    - **Systems Engineering**: Is a broader field concerned with all aspects of developing and evolving complex systems where software plays a major role, including hardware development, policy and process design, and system deployment. Software engineering is a part of this more general process.

The discipline emerged in 1968 in response to the "software crisis," where individual programming approaches did not scale effectively for large and complex systems, leading to unreliability, cost overruns, and late deliveries.

---

2. Define Systems Engineering. Explain the different phases of Systems Engineering
with block diagrams.

Systems engineering is an engineering discipline focused on the comprehensive design and evolution of entire complex systems where software plays a significant role. It addresses all aspects of computer-based systems development, encompassing hardware, software, and process engineering. Systems engineers are tasked with specifying the system, defining its overarching architecture, and integrating diverse parts to create the finished product. This includes considering the capabilities of hardware and software, as well as the system's interactions with human users and its environment. It's a broad field that spans procuring, specifying, developing, deploying, operating, and maintaining both technical and sociotechnical systems.

The lifetime of large, complex systems is typically structured into four overlapping stages, as illustrated by a general process model:

![](images/2.jpeg)

Below are the principal stages of systems engineering:

1. **Conceptual Design** This is the initial systems engineering activity where the concept of the required system is developed. It involves investigating the idea's feasibility and formulating an overall vision for the system. The purpose of the system, its necessity, and the high-level features users might expect are defined in non-technical language. This stage also identifies broad constraints, such as the need for interoperability with other systems. The outcome of this phase is typically a system vision document, which is used to inform users about the system and serves as a basis for defining tender documents and refining system requirements.
    
2. **Procurement (or Acquisition)** During this stage, the conceptual design is further refined to provide information for decisions regarding the system development contract. This includes determining how functionality will be distributed across hardware, software, and operational processes. Decisions are also made on which hardware and software to acquire, which suppliers will develop the system, and the terms and conditions of the supply contract. This process aims to decide what system to buy and who should supply it. Procurement may occur multiple times, extending into the development and operation phases, especially as new equipment and software become available.
    
3. **Development** This stage involves the actual development or purchase of system elements and their integration to create the final system. The system requirements, refined from the conceptual design, act as the bridge to this process. Development processes typically include detailed requirements definition, system design, hardware and software engineering, system integration, and testing. During this phase, operational processes are defined, and training courses for system users are designed. System development processes usually follow a plan-driven, "waterfall" model because different system elements are independently developed by various contractors, necessitating early interface design and comprehensive understanding of requirements before hardware development. Sub-activities within development include requirements engineering, architectural design, requirements partitioning, subsystem engineering, system integration, system testing, and system deployment.
    
4. **Operation** In this final stage, the system is deployed, users are trained, and the system is put into practical use. Operational processes, as defined during development, often need to change to reflect the real working environment where the system is used. The system continuously evolves as new requirements are identified and implemented. This evolution may involve further development and additional hardware/software procurement. Eventually, the system's value may decline, leading to its decommissioning and replacement.
    
These stages are not strictly sequential but overlap and involve continuous feedback, with changes and updates occurring throughout the system's lifetime.

---
3. With a neat diagram, explain the working of a waterfall model. List its advantages and
disadvantages.

The waterfall model is one of the earliest and, in some contexts, least used software life cycle models. It represents a simplified, high-level, and abstract description of a software process. Derived from engineering process models used in large military systems, it presents software development as a series of distinct, sequential stages. This approach is often considered a "plan-driven process," where, in principle, all activities are planned and scheduled before development commences.

The model is sometimes illustrated as a "V-Model" to highlight how basic levels of testing correspond to early development phases. The phases are typically viewed as "fault creation phases" on the left side of the "V" and "fault detection phases" on the right.

### Working of the Waterfall Model

The waterfall model progresses through several stages, with the output of one phase serving as the input for the next. In principle, each phase produces one or more approved documents, and the subsequent phase does not begin until the preceding one is complete.

The principal stages are:

1. **Requirements Analysis and Definition**: This initial phase involves consulting with system users to establish the system's services, constraints, and goals, which are then defined in detail to form the system specification.
2. **System and Software Design**: Requirements are allocated to either hardware or software systems. An overall system architecture is established, and software design identifies fundamental software system abstractions and their relationships.
3. **Implementation and Unit Testing**: The software design is translated into a set of programs or program units. Each unit is then verified to ensure it meets its specific requirements.
4. **Integration and System Testing**: Individual program units are integrated and tested together as a complete system to confirm that all software requirements have been satisfied. After successful testing, the software is delivered to the customer.
5. **Operation and Maintenance**: This is typically the longest phase. The system is installed and put into practical use. Maintenance includes correcting errors discovered post-delivery, improving existing functionalities, and enhancing the system's services as new requirements emerge.

A common representation of the waterfall model is shown below:

![](images/3.jpeg)

### Advantages

- **Structured Management**: The framework aligns well with hierarchical management structures.
- **Clear Deliverables**: Each phase has clearly defined end products and exit criteria, which simplifies project management and progress tracking.
- **Parallel Work**: Once detailed design is complete, different teams can work in parallel on separate units, potentially shortening the overall development time.
- **Foundation for Critical Systems**: Formal development processes (e.g., using the B method) can be applied within this model for systems with strict safety, reliability, or security requirements, which aids in demonstrating compliance to regulators.
- **Ease of Understanding**: It is widely understood and serves as a reference framework for other software development models.

### Disadvantages

- **Inflexibility to Change**: The model strictly adheres to a sequential process, making it costly to correct defects introduced in early phases if they are discovered later in the cycle. There is very little iterative or incremental development.
- **Delayed Feedback**: There is a very long feedback cycle between requirements specification and system testing, often with the customer being absent from intermediate stages.
- **Emphasis on Analysis over Synthesis**: The model focuses heavily on analysis in the early stages, with synthesis (bringing components together) only truly occurring at the integration testing phase.
- **Unrealistic Linear Progression**: In practice, software development is rarely a simple linear process; phases often overlap, and feedback loops are necessary (e.g., design problems might be found during coding).
- **Need for "Perfect Foresight"**: It assumes that the system can be completely understood and functionally decomposed from the outset. This reliance on "perfect foresight" can be perilous if requirements are unstable or not fully known, leading to potential rework.
- **Limited Applicability**: The model is primarily appropriate for systems with well-understood and stable requirements, such as certain higher-level systems engineering processes, but it is generally considered inappropriate for most types of modern software development where flexibility and responsiveness to change are crucial.

---

4. Briefly explain the two types of Evolutionary Development model. Explain the
various activities of Evolutionary Development Model with a neat diagram.

Evolutionary development is a prominent derivative of the traditional waterfall model, designed to address its limitations, particularly concerning flexibility and user feedback. Instead of delivering the system in a single, large release, it involves developing the software through a series of increments or builds.

There are primarily two types of evolutionary development models:

1. **Customer-Driven Evolutionary Development**: In this approach, while a sequence of builds is presumed, only the initial build is strictly defined at the outset. Subsequent builds are identified and shaped largely in response to priorities and suggestions from the customer or user. This allows the system to evolve progressively, directly addressing the changing needs and feedback of the users as development proceeds. This foreshadows the customer-driven principles seen in agile methodologies.
    
2. **Spiral Model**: Developed by Barry Boehm, the spiral model shares an evolutionary flavor but distinguishes itself by determining increments primarily based on risk assessment rather than solely on client suggestions. It integrates elements of rapid prototyping and evolutionary development. Each loop of the spiral involves four key phases: determining objectives, analyzing risks, developing and testing the increment, and planning for the next iteration. This iterative risk-driven approach allows for the systematic management of project risks as the system evolves.
    

### Activities of Evolutionary Development Model

The core activities in an evolutionary development model are interleaved and iterative, allowing for continuous refinement based on feedback. This approach typically proceeds through several versions, starting with an initial implementation and evolving the software incrementally.

The general activities can be summarized as follows:

- **Initial Specification and Outline Description**: An outline description of the system's requirements is established, though not necessarily in exhaustive detail, especially for later increments.
- **Concurrent Activities (Specification, Development, Validation)**: Unlike the strictly sequential waterfall model, these fundamental software process activities are interleaved. This means that parts of the system are specified, developed, and validated in parallel or in rapid succession for each increment. This interleaving facilitates rapid feedback.
- **Iterative Development of Versions**: The process cycles through the development of multiple versions or increments. An initial version is created, followed by intermediate versions, leading eventually to a final version. Each iteration builds upon the previous one, incorporating new features and refinements.
- **Feedback Integration**: A key characteristic is the rapid feedback loop across activities. This makes it easier to obtain customer feedback on the development work, as they can comment on demonstrations of the software as it progresses. This also significantly reduces the cost associated with implementing requirements changes later in the development cycle, as less analysis and documentation need to be redone compared to the waterfall model.

The process continues in an iterative manner until the required system is fully developed and meets the evolving needs of the customer.

The diagram below illustrates the general process model for incremental development, which underpins evolutionary development:

```
                                +-----------------------+
                                |  Outline Description  |
                                +-----------+-----------+
                                            |
                                            |
                                            v
                                +-----------------------+
                                |  Concurrent Activities|
                                |                       |
                                | +-------------------+ |
                                | | Specification     | |
                                | | (Initial Version) | |
                                | +-------------------+ |
                                |           ^           |
                                |           |           |
                                | +-------------------+ |
                                | | Development       | |
                                | | (Intermediate     | |
                                | |  Versions)        | |
                                | +-------------------+ |
                                |           ^           |
                                |           |           |
                                | +-------------------+ |
                                | | Validation        | |
                                | | (Final Version)   | |
                                | +-------------------+ |
                                +-----------------------+
```

  ---
  5. With a neat diagram, explain the reuse-oriented software engineering.


### **Reuse-Oriented Software Engineering**

**Definition:**  
Reuse-Oriented Software Engineering (ROSE) is a software development approach that focuses on the integration and configuration of **existing reusable components** (like libraries, frameworks, and COTS systems) rather than developing the entire system from scratch.

This approach helps in reducing development time, cost, and risks while improving overall software quality and reliability.


### **Phases of Reuse-Oriented Software Engineering**

According to Figure 2.3 , the general process model for reuse-based development includes the following stages:

1. **Requirements Specification:**
    
    - Initial system requirements are proposed.
        
    - These requirements do not need to be very detailed but should include essential functionalities and desirable features.
        
2. **Software Discovery and Evaluation:**
    
    - Search for existing components or systems that meet the required functionality.
        
    - Evaluate whether these components satisfy the essential requirements and are suitable for integration.
        
3. **Requirements Refinement:**
    
    - Refine and modify the initial requirements based on available reusable components.
        
    - If suitable components are not found, return to the discovery phase to explore alternatives.
        
4. **Application System Configuration:**
    
    - If an off-the-shelf (COTS) system fits the requirements, it is configured and adapted for the new system.
        
5. **Component Adaptation and Integration:**
    
    - If no full system is available, individual components are adapted and integrated.
        
    - Some new components may be developed to complete the system.
        


### **Diagram: Reuse-Oriented Software Engineering Process**

![](images/5.jpeg)


### **Advantages of Reuse-Oriented Software Engineering**

- Reduces development time and cost.
    
- Enhances reliability due to reuse of tested components.
    
- Allows faster delivery of systems.
    
- Minimizes development effort.
    


### **Disadvantages**

- May require compromises in requirements.
    
- Limited control over third-party component updates.
    
- Integration issues may arise due to incompatibility.
    
- Customization might be restricted.
    

---

6. With a neat diagram, explain the Requirements Engineering process

Requirements engineering (RE) is the process of understanding and defining what services a system is required to provide, as well as identifying the constraints on its operation and development. It is a critical stage in the software process, as errors made here can lead to significant problems in later design and implementation stages.

The Requirements Engineering process involves three key, interleaved activities:

1. **Requirements elicitation and analysis**: This involves discovering requirements by interacting with system stakeholders.
2. **Requirements specification**: This is the process of converting these discovered requirements into a standard, documented form.
3. **Requirements validation**: This activity checks that the requirements accurately define the system the customer truly desires.

While these activities are often shown sequentially, in practice, requirements engineering is an iterative process where these activities are interleaved.

The general process model for Requirements Engineering is illustrated in the following diagram:

![](images/6.jpeg)

Figure 2.4 The requirements engineering process.

Here's a more detailed explanation of each activity:

- **Requirements Elicitation and Analysis** This process aims to understand the work that stakeholders do and how a new system might support that work. Software engineers work with stakeholders to gather information about the application domain, work activities, desired services and features, performance needs, and hardware constraints. This stage is difficult because stakeholders may not clearly articulate their needs, express requirements in their own implicit terms, or have conflicting views.
    
    This activity includes several sub-activities:
    
    - **Requirements discovery and understanding**: Interacting with stakeholders to uncover their requirements, including domain requirements from documentation and existing systems. Techniques include interviews (closed or open) and observation (ethnography).
    - **Requirements classification and organization**: Taking the unstructured collection of requirements and grouping related ones into coherent clusters. Viewpoints, which group requirements from specific stakeholder groups, can be used for this.
    - **Requirements prioritization and negotiation**: Resolving conflicts among requirements from multiple stakeholders through negotiation and compromise.
    - **Requirements documentation**: Documenting the requirements, which may involve creating an early draft of the requirements document or maintaining them informally on shared spaces. The analyst's understanding of the requirements improves with each cycle of this iterative process.
- **Requirements Specification** This is the process of formally writing down the user and system requirements in a requirements document. User requirements are high-level, abstract statements, usually in natural language with diagrams, describing what the system should provide to users and its operating constraints. System requirements are more detailed descriptions of the software system's functions, services, and operational constraints, intended for system developers and potentially forming part of a contract.
    
    Ideally, requirements should be clear, unambiguous, complete, and consistent, although this is rarely fully achievable due to inherent conflicts and varying interpretations. Natural language is commonly used, often supplemented with tables, forms, graphical models (like UML diagrams), or even mathematical specifications for critical systems. A standard format, consistent language, highlighting of key parts, avoidance of jargon, and inclusion of a rationale for each requirement are recommended to minimize misunderstandings.
    
- **Requirements Validation** This process checks that the requirements truly define the system the customer wants, overlapping with elicitation and analysis as it aims to find problems with the requirements. It is crucial because errors in the requirements document can lead to extensive and costly rework if discovered later in the development cycle or after system deployment.
    
    Validation involves several types of checks:
    
    - **Validity checks**: Ensuring the system meets the customer's real needs.
    - **Consistency checks**: Confirming no conflicts or contradictory descriptions exist within the requirements.
    - **Completeness checks**: Verifying that all intended functions and constraints are defined.
    - **Realism checks**: Assessing whether requirements can be implemented within the proposed budget and schedule, considering existing technologies.
    - **Verifiability**: Ensuring requirements are written such that a set of tests can demonstrate the delivered system meets each specified requirement.
    
    Validation techniques include requirements reviews (systematic analysis by a team), prototyping (developing an executable model for user feedback), and test-case generation (designing tests from requirements to reveal problems). Developing tests from user requirements before code is written is an integral part of test-driven development.
    

The entire Requirements Engineering process is influenced by the inevitable changes to requirements due to evolving stakeholder understanding, organizational shifts, and changes in the system's environment. This necessitates **Requirements Change Management**, a formal process for handling change proposals, assessing their impact and cost, and maintaining consistency between the requirements document and the system implementation.

---

7. With a neat diagram, explain the general model of the design process.

 The software design and implementation stage is where an executable software system is developed. Software design is a creative process focused on identifying software components and their relationships based on customer requirements. It's not a clear-cut, sequential process; designers develop the design in stages, iteratively refining solutions and backtracking as needed.

A software design outlines the software's structure, data models and structures, interfaces between components, and sometimes the algorithms used. While design is always present, it's not always formally documented; sometimes it resides in a programmer's mind or is sketched informally. Implementation is the process of realizing this design as a program. Design decisions should consider implementation issues.

The general model of the design process involves inputs, activities, and outputs, as illustrated in the abstract model below:

![](images/7.jpeg)

Figure 2.5 A general model of the design process

Here's a breakdown of each part of the process:

**1. Design Inputs**

- **Platform information**: This includes details about the software platform (e.g., operating system, database, middleware) where the software will execute. It's crucial for designers to integrate the system with its environment.
- **Software requirements**: These are the specifications defining what the system needs to do.
- **Data descriptions**: If the system processes existing data, descriptions of that data are included as inputs to define the system's data organization.

**2. Design Activities** The activities in the design process are interleaved and interdependent. New information constantly influences previous design decisions, making rework inevitable. These activities vary depending on the system type (e.g., real-time systems might require timing design but not a database design):

- **Architectural design**: This involves identifying the system's overall structure, including its principal components (subsystems or modules), their relationships, and how they are distributed.
- **Database design**: This activity focuses on designing the system's data structures and their representation in a database, considering whether an existing database is reused or a new one is created.
- **Interface design**: This defines the interfaces between system components clearly and unambiguously. Precise interfaces allow components to be designed and developed in parallel without needing to know implementation details.
- **Component selection and design**: This involves searching for reusable components and, if none are suitable, designing new software components. The design at this stage can be a simple description or a detailed UML model that can generate an implementation.

**3. Design Outputs** The outputs of the design process vary based on the development approach:

- For **critical systems**, outputs are detailed design documents with precise descriptions of the system.
- For **model-driven approaches**, the design outputs are design diagrams.
- For **agile methods**, the outputs may not be separate specification documents but might be represented directly in the program's code.

The development of a program typically follows system design. For some safety-critical systems, detailed design precedes implementation. However, it's more common for design and program development to be interleaved. Software development tools can also generate a skeleton program from a design, defining and implementing interfaces, leaving developers to add operational details.

---

8. With a neat diagram, explain the testing phases in a plan-driven software process.

In a plan-driven software process, all process activities are planned in advance, and progress is measured against this predetermined plan. This approach contrasts with agile processes, where planning is incremental and continuous. Testing within a plan-driven framework is typically structured and sequential, often following a "V-model" to ensure that various levels of testing correspond to earlier development phases.

The testing process in a plan-driven software development environment generally involves distinct, staged activities, driven by a set of test plans. An independent team of testers often develops and works from these plans.

The key testing phases in a plan-driven software process are:

- **Component Testing (Unit Testing)**: This is the initial stage where individual program units or object classes are tested by the developers themselves. Each component is tested independently, without other system components. The focus is on verifying the functionality of objects or methods. Test automation tools, such as JUnit for Java, are commonly used to rerun tests when new versions of components are created.
- **System Testing**: Following component testing, system testing integrates components to create a version of the system, and then the integrated system is tested. This phase checks for component compatibility, correct interaction, and proper data transfer across interfaces. It also involves integrating reusable components and off-the-shelf systems with newly developed parts. Use case-based testing is considered effective at this stage due to its focus on interactions.
- **Release Testing**: This process involves testing a particular version of the system that is intended for use outside the development team, typically for customers and users. A separate testing team usually conducts release testing to ensure the system meets stakeholder requirements. Key techniques here include scenario testing, where typical usage scenarios are devised to develop test cases, and stress testing, which involves making demands beyond the system's design limits to uncover defects.
- **User Testing (Acceptance Testing)**: In this final stage, users or potential users of the system test it in their own environment. For software products, this may involve beta testing, where an early release is made available to a larger group of users for evaluation and problem reporting. For custom software, acceptance testing is a formal process where customers test the system with their own data to decide if it is ready to be accepted from the developers and deployed. This phase includes defining acceptance criteria, planning and deriving acceptance tests, executing them, negotiating results, and ultimately deciding on system acceptance or rejection.

The relationship between these testing activities and the development phases in a plan-driven process is often visualized using the V-model, which explicitly links validation activities to each stage of the waterfall process model. Test design begins early in the development cycle, soon after requirements become available.

The following diagram, derived from the sources, illustrates these testing phases in a plan-driven software process:

![](images/8.jpeg)

Figure: Testing phases in a plan-driven software process

This diagram highlights how test plans are the link between the validation activities on the right side of the "V" and the development phases on the left, demonstrating the systematic and parallel nature of testing in a plan-driven environment.

---

9. With a neat diagram, explain the software evolution process.

  Software evolution is an integral and continuous process within software engineering, essential for ensuring that software systems remain useful and valuable throughout their operational lifetimes. Unlike the traditional view that separates development from maintenance, software engineering increasingly considers development and evolution as a continuous spectrum, particularly for successful software products and applications. Businesses invest significantly in evolving their systems, often spending more on maintaining existing systems than on developing new ones, as software is a critical business asset.

The software evolution process is primarily driven by various **change proposals**. These proposals can originate from multiple sources, including existing requirements that were not initially implemented, requests for new functionalities, bug reports from users, or innovative ideas from the development team itself.

The general model for software evolution involves several key, interrelated activities that form a cyclical process:

- **Change Identification/Requests**: The process begins with formal or informal proposals for changes and updates to an existing software system.
- **Impact Analysis**: Before a change proposal is accepted, a crucial step is to analyze its potential impact and assess the costs involved. This analysis determines which components of the system would be affected by the proposed change and estimates the resources and effort required for its implementation.
- **Release Planning**: If the proposed changes are approved, a new release of the system is planned. This stage involves considering all types of changes—such as fault repairs, adaptations for new environments (Platform adaptation), and the addition of new features (System enhancement)—and deciding which ones will be incorporated into the upcoming version of the system.
- **Change Implementation**: This is where the approved changes are designed, implemented, and validated. This phase may involve iterations of development, where the system is revised, implemented, and tested. For custom software, especially when different teams are involved, a significant aspect of this stage is "program understanding," where developers analyze the existing code to understand its structure and functionality to ensure changes integrate correctly without introducing new problems. It also involves updating existing documentation, such as requirements specifications and design models, to reflect the changes.
- **System Release**: Once the changes are implemented and validated, a new version of the system is released to customers or deployed.

The entire process then iterates, with the new release often generating further change requests, perpetuating the cycle of evolution throughout the system's lifetime. This continuous adaptation ensures the software remains relevant and effective in a changing environment.

The diagram below illustrates the general model of the software evolution process:

![](images/9.jpeg)

**Figure: A general model of the software evolution process**

This diagram shows how change requests lead to an analysis of their impact, which then informs the planning and implementation of a new system release. The released system, in turn, generates further change requests, completing the continuous cycle of software evolution.

---

10. With a neat diagram, explain the process model for prototype development.

The process model for prototype development is a cyclical approach used to create an early version of a software system to explore concepts, test design options, and gain a better understanding of a problem and its potential solutions. This iterative development is crucial for controlling costs and allowing stakeholders to experiment with the system early in the software process.

The key stages in the prototype development process, as illustrated in the model below, are:

**Process Model for Prototype Development**

![](images/10.jpeg)

**Explanation of the Stages:**

1. **Establish Prototype Objectives:** This initial step involves clearly defining the goals for the prototype. The objectives might include developing a user interface, validating functional requirements, or demonstrating the application to managers. It's important to state these objectives explicitly from the outset to prevent misunderstandings about the prototype's purpose.
2. **Define Prototype Functionality:** In this stage, decisions are made about what functionality to include in the prototype and, crucially, what to omit. To reduce costs and expedite delivery, certain functionalities may be left out, and non-functional requirements, such as response time or memory usage, might be relaxed. Error handling and management may also be disregarded unless they are direct objectives of the prototype. The output of this stage is typically an outline definition.
3. **Develop Prototype:** This involves the rapid, iterative construction of the prototype based on the defined functionality. The output of this stage is an executable prototype.
4. **Evaluate Prototype:** This is the final stage where the prototype is assessed. It requires providing user training and developing an evaluation plan based on the prototype's initial objectives. Users need time to become comfortable with the system and use it naturally to discover requirements errors or omissions. A common issue is that users might adapt their usage patterns to accommodate a slow prototype, which may not reflect how they would use the final system. The outcome of this stage is an evaluation report.

The process continues in a cycle, allowing for refinement and evolution based on feedback until the desired system understanding or requirements are achieved.

---

11. With a neat diagram, explain the incremental delivery model.

The **incremental delivery model** is a software development approach where parts of the developed system, known as increments, are delivered to the customer and deployed for use in their working environment. This model contrasts with traditional approaches by ensuring that the software is used in real, operational processes, thereby providing realistic user feedback.

This approach allows customers to gain value from the system early by receiving critical functionalities first, rather than waiting for the entire system to be completed. It is particularly useful for systems where requirements are not fully understood from the outset, enabling continuous refinement based on user experience.

### Process Model for Incremental Delivery

The incremental delivery process is a cyclical activity designed to iteratively build and deploy a software system. Its key stages are outlined below:

![](images/11.jpeg)

### Explanation of Stages:

1. **Define Outline Requirements**: This initial step involves customers defining and prioritizing the services they need, from most to least important.
2. **Design System Architecture**: An overall system architecture is designed, providing a foundational structure for the increments.
3. **Assign Requirements to Increments**: Based on the prioritized services, specific delivery increments are defined. The highest priority services are allocated to earlier increments.
4. **Develop System Increment**: Detailed requirements for the current increment are defined, and development proceeds. During this phase, new requirements for _later_ increments can still be analyzed, but changes to the _current_ increment are generally not accepted.
5. **Validate Increment**: The newly developed increment undergoes validation to ensure it meets its defined requirements.
6. **Integrate Increment**: Once validated, the new increment is integrated with any previously delivered increments. This process continually enhances the overall system functionality.
7. **Deploy Increment**: The completed increment is installed in the customer's actual working environment. This allows users to experiment with the new functionality and provide feedback, which is crucial for clarifying requirements for subsequent increments.
8. **System Completion Check**: After deployment, a check is performed to determine if the system is complete. If not, the process loops back to assign requirements for the next increment, continuing until the full system is delivered.

### Advantages of Incremental Delivery:

- **Early User Feedback and Experience**: Customers can use early increments as prototypes, gaining practical experience that informs and refines their requirements for later parts of the system. Unlike throwaway prototypes, these increments are part of the actual final system.
- **Faster Value Delivery**: Customers do not have to wait for the entire system to be completed before they can benefit. The initial increments address their most critical needs, providing immediate value.
- **Easier Change Incorporation**: The iterative nature of this model makes it relatively simple to incorporate changes into the system, as the scope of each increment is smaller compared to a monolithic development process.
- **Improved Quality of Critical Services**: Since higher-priority services are delivered and integrated first, they receive the most testing and exposure to real-world use. This reduces the likelihood of critical software failures in the most important parts of the system.

### Disadvantages of Incremental Delivery:

- **Challenges in Replacing Existing Systems**: This model can be problematic when the new system is intended to replace an existing one. Users may require all functionalities of the old system immediately and might be unwilling to work with an incomplete new system. Running both old and new systems concurrently can also be impractical due to differences in databases and user interfaces.

---

12. Explain the principles of agile methods.

  Agile methods are a set of software development approaches designed to produce useful software quickly and efficiently, especially in environments where requirements are expected to change rapidly. The philosophy behind agile methods is articulated in the Agile Manifesto, which prioritizes certain values over others.

The core principles of agile methods, as outlined in the sources, include:

- **Customer involvement:** Customers should be closely involved throughout the development process. Their role is to provide and prioritize new system requirements and to evaluate the iterations of the system. This continuous engagement ensures rapid feedback on changing requirements.
- **Embrace change:** Agile methods anticipate that system requirements will change, and therefore, the system is designed to accommodate these changes. This principle means that rapid changes are expected and are a fundamental part of the development process.
- **Incremental delivery:** The software is developed and delivered in small increments, with the customer specifying the requirements to be included in each increment. New releases of the system are typically created and made available to customers every two or three weeks. This approach allows for early delivery of fully functional components and immediate value to the customer.
- **Maintain simplicity:** There is a focus on simplicity in both the software being developed and the development process itself. This is supported by continuous refactoring, which improves code quality and avoids structural deterioration, and by using simple designs that do not unnecessarily anticipate future changes.
- **People, not process:** The skills and autonomy of the development team are recognized and exploited. Team members are encouraged to develop their own ways of working without overly prescriptive processes. This includes practices like pair programming, where developers work together, checking each other's work and providing mutual support. Agile methods emphasize informal communication over formal meetings and extensive documentation.

In essence, agile methods value:

- **Individuals and interactions** over processes and tools.
- **Working software** over comprehensive documentation.
- **Customer collaboration** over contract negotiation.
- **Responding to change** over following a plan.

While acknowledging the value of items on the right, agile principles place greater importance on the items on the left.

---

13. With a neat diagram, explain extreme programming release cycle. Also, discuss the
extreme programming practices.

Extreme Programming (XP) is a prominent agile method that emphasizes producing useful software quickly through a set of specific practices. Its development approach is highly iterative, with requirements expressed as "user stories" that are directly implemented as a series of tasks.

### Extreme Programming Release Cycle

The XP release cycle illustrates the iterative and continuous nature of this development methodology. It focuses on delivering small, working components through a sequence of iterations.

**XP Release Cycle Diagram:**

![](images/13.jpeg)

**Explanation of the Cycle:**

1. **User Stories:** The process begins with customer expectations captured as "user stories". These are high-level requirements that drive the development process.
2. **Release Plan:** User stories inform the "release plan," which defines a sequence of iterations. Each iteration aims to deliver a small, working component.
3. **Iteration / Iteration Plan:** Within each release, there are multiple iterations. An "iteration plan" outlines the specific user stories (broken down into tasks) to be implemented in that short iteration, typically lasting 2 to 4 weeks.
4. **Pair Coding:** Developers work in pairs, often sharing a single computer, continuously reviewing each other's work and supporting each other.
5. **Unit Test:** A core XP practice is "test-first development," where automated unit tests are written for a new piece of functionality _before_ the code itself is implemented. All existing unit tests must pass before new code is integrated.
6. **Acceptance Test:** User stories also define "acceptance tests". These tests are run to ensure the developed software supports the user stories and meets the customer's real needs. Development cannot proceed until these tests are successfully executed.
7. **Small Release:** Upon successful testing, a "small release" of the working component is delivered. New releases of the system are typically made available to customers every two or three weeks. The customer has no more user stories, indicating the project's completion.
8. **Repeat:** The cycle repeats for subsequent iterations until all required user stories are implemented and the customer has no more needs.

### Extreme Programming Practices

XP introduced several practices that reflect the principles of the agile manifesto, emphasizing adaptability, customer collaboration, and efficient delivery.

1. **Collective Ownership:** All developers work on all areas of the system, fostering a shared responsibility for the entire codebase. This prevents "islands of expertise" and allows anyone to change anything, promoting flexibility.
2. **Continuous Integration:** As soon as work on a task is completed, it is integrated into the whole system. After each integration, all unit tests must pass. This practice helps catch integration problems early and ensures the system always remains functional.
3. **Incremental Planning:** Requirements are recorded as "story cards," and the stories for a release are determined by available time and their priority. Developers break these stories into smaller "tasks". This allows for flexible planning that accommodates changing customer priorities.
4. **On-site Customer:** A representative of the end-user (the customer) is expected to be available full-time as a member of the XP team. This ensures continuous engagement and rapid feedback on changing requirements, and the customer is responsible for defining acceptance tests.
5. **Pair Programming:** Two programmers work together on the same computer, checking each other's work and providing mutual support. This continuous review helps improve code quality and reduces defects. Pairings are often dynamic, so all team members work together.
6. **Refactoring:** Developers are expected to continuously refactor (improve and restructure) the code as soon as potential improvements are found, even if there's no immediate need. This maintains code simplicity, readability, and maintainability, preventing structural deterioration that can occur with frequent changes.
7. **Simple Design:** Only enough design is carried out to meet the current requirements, avoiding unnecessary anticipation of future changes. This supports simplicity and reduces wasted effort.
8. **Small Releases:** The minimal useful set of functionality that provides business value is developed first. Subsequent releases are frequent and incrementally add functionality. This provides early value to the customer and rapid feedback.
9. **Sustainable Pace:** Excessive overtime is discouraged as it often reduces code quality and medium-term productivity. The goal is to maintain a pace that is sustainable for the development team.
10. **Test-First Development:** Tests for new functionality are written using an automated unit test framework _before_ the actual code is implemented. This approach clarifies requirements, supports early defect detection, and simplifies fault isolation because a failing test points directly to the most recently added code.
---
14. Describe the functional and non-functional requirements with examples. What are the
various metrics used for specifying non-functional requirements.

Software system requirements are descriptions of the services a system should provide and the constraints on its operation. These requirements reflect the needs of customers for a system that serves a specific purpose, such as controlling a device, placing an order, or finding information. They are critical to software development, as mistakes in this stage can lead to significant problems later.

System requirements are broadly classified into two main types: functional requirements and non-functional requirements.

### Functional Requirements

Functional requirements define the services a system is expected to provide, how it should react to specific inputs, and its behavior in particular situations. They describe "what the system should do". In some cases, functional requirements may also explicitly state what the system should _not_ do.

When functional requirements are expressed as user requirements, they are typically written in natural language to be understandable by system users and managers. Functional system requirements, which expand upon user requirements, are written for system developers and describe functions, inputs, outputs, and exceptions in detail. Functional requirements for a product are determined by the tester's understanding of the requirements during testing.

**Examples of Functional Requirements:**

- **General examples:**
    - A program that inputs two integers and outputs their maximum.
    - A program that inputs a sequence of integers and outputs its sorted version.
- **Mentcare System examples**:
    - A user shall be able to search the appointments lists for all clinics.
    - The system shall generate, each day for each clinic, a list of patients who are expected to attend appointments that day.
    - Each staff member using the system shall be uniquely identified by his or her eight-digit employee number.
- **Information requirements** specify the information needed and how it is to be delivered and organized.
- **Domain requirements** are derived from the application domain and can be new functional requirements, constrain existing ones, or specify computations.

Ideally, functional requirements should be both complete (all services and information needed by the user are defined) and consistent (requirements are not contradictory).

### Non-Functional Requirements

Non-functional requirements are constraints on the services or functions offered by the system, often relating to its overall characteristics rather than individual features. These can include timing constraints, development process constraints, or standards. They may pertain to "emergent system properties" such as reliability, response time, or memory usage, or they may define constraints on system implementation, like I/O device capabilities or data representations.

Non-functional requirements are often more critical than individual functional requirements, as failing to meet them can render the entire system unusable. Their implementation may be spread throughout the system, affecting its overall architecture and potentially generating related functional requirements or constraining existing ones. Non-functional requirements contribute to the "quality" of software, encompassing its behavior during execution, structure, and associated documentation.

**Types of Non-Functional Requirements:**

Non-functional requirements generally arise from user needs, budget constraints, organizational policies, interoperability needs, or external factors like safety regulations or privacy legislation. They are classified into three main types:

1. **Product requirements:** These specify or constrain the runtime behavior of the software.
    - **Example (Mentcare System):** "The Mentcare system shall be available to all clinics during normal working hours (Mon–Fri, 08:30–17:30). Downtime within normal working hours shall not exceed 5 seconds in any one day". This type of requirement could also include performance, reliability, security, and usability.
2. **Organizational requirements:** These are derived from policies and procedures within the customer's and developer's organizations.
    - **Example (Mentcare System):** "Users of the Mentcare system shall identify themselves using their health authority identity card". Other examples include development process requirements (e.g., programming language, development environment, process standards) and operational/environmental requirements.
3. **External requirements:** These stem from factors external to the system and its development process.
    - **Example (Mentcare System):** "The system shall implement patient privacy provisions as set out in HStan-03-2006-priv". This category includes regulatory, legislative, and ethical requirements.

A common challenge is that stakeholders often propose non-functional requirements as general goals (e.g., "ease of use") which are difficult to objectively verify. Therefore, whenever possible, non-functional requirements should be written quantitatively to make them testable.

### Metrics for Specifying Non-Functional Requirements

Metrics can be used to quantitatively specify non-functional system properties, allowing for objective testing to check if the system meets its requirements.

**Key Metrics for Non-Functional Requirements:**

- **Speed:** Measured by processed transactions per second, user/event response time, or screen refresh time.
- **Size:** Measured in megabytes or number of ROM chips.
- **Ease of use:** Measured by training time or the number of help frames.
- **Reliability:** Can be specified as a probability of system failure in a given operating environment. Common metrics include:
    - **Probability of Failure On Demand (POFOD):** Defines the probability that a demand for service will result in a system failure (e.g., 0.001 for a 1/1000 chance of failure per demand).
    - **Rate of Occurrence of Failures (ROCOF):** Sets out the probable number of system failures observed relative to a time period (e.g., two failures per hour) or number of executions. The reciprocal of ROCOF is the Mean Time To Failure (MTTF).
    - **Availability (AVAIL):** The probability that the system is available for use when required. This is affected by both the time between failures and the time needed to restart the system after a failure.
- **Robustness:** Measured by time to restart after failure, percentage of events causing failure, or probability of data corruption on failure.
- **Portability:** Measured by the percentage of target-dependent statements or the number of target systems.

These metrics allow for quantitative assessment of quality attributes, though for some (like maintainability), simple metrics may not exist. The time units for reliability metrics can be calendar time or discrete units like the number of transactions.

---

15. With a neat block diagram, explain the various types of non-functional requirements.

   Non-functional requirements (NFRs) are constraints on the services or functions provided by a software system, often relating to its overall characteristics rather than specific features. These requirements are crucial because failing to meet them can render an entire system unusable, even if all functional requirements are met. Their implementation often spans across the system and can influence its overall architecture. NFRs generally originate from user needs, budgetary limitations, organizational policies, interoperability demands, or external factors such as safety regulations or privacy laws.

Non-functional requirements are typically classified into three main types:

1. **Product Requirements:** These define or constrain the runtime behavior of the software itself. They specify attributes like performance, reliability, security, and usability.
    
    - **Example:** For the Mentcare system, a product requirement might state: "The Mentcare system shall be available to all clinics during normal working hours (Mon–Fri, 08:30–17:30). Downtime within normal working hours shall not exceed 5 seconds in any one day". This focuses on the system's operational availability. Other product requirements could specify required speed (e.g., transactions per second), size (e.g., memory usage), or ease of use (e.g., training time).
2. **Organizational Requirements:** These are derived from the policies and procedures within the customer's or developer's organizations. They can dictate operational processes, development methodologies (e.g., specific programming languages, development environments, or process standards), and environmental specifications for the system.
    
    - **Example:** An organizational requirement for the Mentcare system could be: "Users of the Mentcare system shall identify themselves using their health authority identity card". This mandates a specific authentication method due to organizational policy.
3. **External Requirements:** These originate from factors external to the system and its development process. This broad category includes regulatory requirements (e.g., needing approval from a nuclear safety authority), legislative requirements (e.g., compliance with privacy laws), and ethical requirements ensuring public or user acceptance.
    
    - **Example:** An external requirement for the Mentcare system, stemming from legal obligations, might be: "The system shall implement patient privacy provisions as set out in HStan-03-2006-priv". This requires the system to adhere to a national privacy standard.

### Block Diagram Representation of Non-Functional Requirements

A block diagram illustrating the types of non-functional requirements would conceptually organize them as follows, echoing the structure presented in Figure 4.3 of the source:

![](images/15.jpeg)

- **Main Block:** "Non-functional Requirements" at the top represents the overarching category.
- **First Layer of Blocks:** Branching down, three distinct blocks (Product, Organizational, External) represent the primary classifications, indicating that all non-functional requirements fall into one of these categories.
- **Second Layer of Blocks (Sub-types/Examples):** Below each primary type, smaller blocks or lists enumerate specific examples or sub-categories that fall under that type. For instance, under "Product Requirements," you would find performance, usability, reliability, and security, which are common quality attributes of a software product. Similarly, organizational requirements might include development or environmental aspects, while external requirements would cover legislative or ethical considerations.

### Metrics for Specifying Non-Functional Requirements

To make non-functional requirements objectively testable, they should be defined quantitatively whenever possible. Metrics are used to specify these properties. Examples of such metrics include:

- **Speed:** Processed transactions per second, user/event response time, screen refresh time.
- **Size:** Megabytes of memory, number of ROM chips.
- **Ease of use:** Training time required, number of help frames provided.
- **Reliability:** Mean time to failure (MTTF), probability of unavailability, rate of failure occurrence (ROCOF), availability (AVAIL).
- **Robustness:** Time to restart after failure, percentage of events causing failure, probability of data corruption on failure.
- **Portability:** Percentage of target-dependent statements, number of target systems supported.

These metrics allow for objective verification during testing, distinguishing a measurable requirement (e.g., "average number of errors made by experienced users shall not exceed two per hour") from a general goal (e.g., "the system should be easy to use").

---
16. With the help of an example, distinguish between user requirement and system
requirement.

Software system requirements are descriptions of the services a system should provide and the constraints on its operation. These requirements are essential for communicating the needs of a customer to the system developers. However, the term "requirement" is not always used consistently in the software industry, sometimes referring to a high-level abstract statement and other times to a detailed, formal definition. To address this, requirements are often categorized based on their level of detail and intended audience.

The two main types of requirements, distinguished by their level of detail and purpose, are:

1. **User Requirements:** These are high-level, abstract statements, usually expressed in natural language and diagrams, that describe the services the system is expected to provide to its users and the operational constraints. They can range from broad statements of system features to precise descriptions of functionality. User requirements are primarily intended for system customers and end-users who are not typically concerned with how the system will be implemented. They help clients understand and validate what the software will do.
2. **System Requirements:** These are more detailed descriptions of the software system's functions, services, and operational constraints. They expand upon user requirements and are written for system developers. System requirements should define exactly what is to be implemented and may form part of the contract between the system buyer and software developers. They are used by system engineers, architects, and software developers who need precise details for implementation and to understand how the system will support business processes.

**Distinction and Purpose:**

The fundamental distinction lies in their audience and the level of technical detail they convey. User requirements serve as a common ground for understanding the overall needs, while system requirements translate those needs into a precise, actionable specification for development. Problems can arise if there isn't a clear separation between these different levels of description. For instance, imprecise requirements can lead to developers interpreting ambiguous statements in a way that simplifies implementation, which might not align with the customer's actual desires, leading to disputes, delays, and increased costs.

**Example from the Mentcare System:**

Consider the Mentcare system, designed to manage information about patients receiving mental health treatment.

- **User Requirement:**
    - "A user shall be able to search the appointments lists for all clinics."

This user requirement is a general statement. However, its interpretation can be ambiguous. A medical staff member might expect the system to search for a patient's name across all appointments at all clinics automatically, while a developer might implement a simpler search that requires the user to first choose a clinic before searching. To avoid such misinterpretations and ensure the system behaves as expected, this high-level user requirement is broken down into more specific system requirements:

- **Corresponding System Requirements:**
    - "The system shall provide an appointment list search facility that allows a user to search for appointments for a specified clinic or across all clinics."
    - "The system shall provide a mechanism that allows a user to specify if the search is to be constrained by date (i.e., search only for appointments on a specified date)."
    - "The system shall provide a mechanism that allows a user to specify if the search is to be constrained by the time of appointment (i.e., search only for appointments in a specified time range)."
    - "The system shall display the results of a search as a list showing the patient name, the time of the appointment, and the clinic name."

As this example illustrates, a single user requirement can lead to multiple, more detailed system requirements, which explicitly define the functionality, inputs, outputs, and constraints needed for implementation.

---
17. Give the IEEE standard format for Requirements Document.

The IEEE standard format for a Requirements Document, as described in the sources and based on an IEEE standard for requirements documents (IEEE 1998), provides a comprehensive structure for detailing software system requirements. This standard is generic and can be adapted for specific uses, often extended to include information about predicted system evolution to help maintainers and designers.

The typical structure for a requirements document following this standard includes the following chapters:

- **Preface**:
    
    - Defines the expected readership of the document.
    - Describes its version history, including a rationale for new versions and a summary of changes.
- **Introduction**:
    
    - Describes the need for the system.
    - Briefly outlines the system's functions and how it will interact with other systems.
    - Explains how the system fits into the overall business or strategic objectives of the commissioning organization.
- **Glossary**:
    
    - Defines technical terms used in the document, assuming no prior experience or expertise of the reader.
- **User Requirements Definition**:
    
    - Describes the services provided for the user.
    - Includes non-functional system requirements.
    - May use natural language, diagrams, or other notations understandable to customers.
    - Specifies product and process standards that must be followed.
- **System Architecture**:
    
    - Presents a high-level overview of the anticipated system architecture.
    - Shows the distribution of functions across system modules.
    - Highlights architectural components that are reused.
- **System Requirements Specification**:
    
    - Details the functional and non-functional requirements.
    - Allows for further detail to be added to non-functional requirements if necessary.
    - May define interfaces to other systems.
- **System Models**:
    
    - Includes graphical system models that illustrate relationships between system components and between the system and its environment.
    - Examples include object models, data-flow models, or semantic data models.
- **System Evolution**:
    
    - Describes the fundamental assumptions underpinning the system.
    - Outlines any anticipated changes due to hardware evolution, shifting user needs, etc.. This section is valuable for system designers, helping them avoid design choices that might hinder future system modifications.
- **Appendices**:
    
    - Provides detailed, specific information related to the application.
    - May include hardware and database descriptions.
    - Hardware requirements define minimal and optimal system configurations.
    - Database requirements define the logical organization and relationships of data used by the system.
- **Index**:
    
    - Multiple indexes may be included, such as an alphabetic index, an index of diagrams, or an index of functions.

This structured approach ensures that the requirements document serves a diverse set of users, from senior management to software engineers and testers, providing appropriate levels of detail for each. For complex engineering systems involving hardware and software from different companies, the document tends to be long and detailed, requiring comprehensive indexes. For in-house software products, a less detailed document focusing on user and high-level non-functional requirements may suffice.

---

18. Explain why elicitation and analysis is a difficult process. Give reasons.

Requirements elicitation and analysis is a challenging process due to several inherent difficulties stemming from the nature of stakeholders, the system's environment, and the complexity of the systems themselves.

Here are the key reasons why this process is difficult:

- **Stakeholders' Difficulty in Articulating Needs** Stakeholders often have only a general idea of what they want from a computer system and may find it difficult to articulate specific requirements. They might make unrealistic demands because they do not fully understand the technical possibilities and limitations of a system. Furthermore, it is difficult for individuals to visualize what a new system might be like, especially without a system prototype to demonstrate its potential. Even with informal methods like user stories, which are easy for people to relate to, it can be hard to determine if enough stories have been developed to cover all essential requirements or if a single story accurately portrays an activity, as experienced users may omit details that are second nature to them.
- **Domain-Specific Jargon and Implicit Knowledge** Application specialists naturally express requirements using terminology specific to their area of work, which requirements engineers without experience in that domain may misunderstand. Additionally, some domain knowledge is so fundamental or obvious to stakeholders that they find it difficult to explain or don't believe it's worth mentioning, leading to crucial omissions in the requirements.
- **Diverse and Conflicting Stakeholder Requirements** Different stakeholders often have varying views on the importance and priority of requirements, and these views can sometimes be conflicting. Requirements engineers must identify all potential sources of requirements and then discover commonalities and resolve conflicts. Political factors within an organization can also influence requirements, with managers potentially demanding specific system features to increase their influence.
- **Dynamic Business and Economic Environment** The economic and business environment in which requirements analysis takes place is constantly changing. This dynamic nature means that the importance of particular requirements may shift, and new requirements can emerge from new stakeholders who were not initially consulted. This leads to requirements evolution, where initial understandings of a problem and its associated requirements change over time.
- **Difficulty in Capturing Organizational and Political Factors** Requirements may be generated or constrained by the social and organizational environment in which the system will be used. However, it is challenging to elicit knowledge about organizational requirements and constraints through interviews because subtle power relationships within the organization may lead interviewees to be reluctant to reveal the actual decision-making structure or political issues. Ethnography, an observational technique, can help discover implicit requirements reflecting actual work practices rather than formal processes, revealing social and organizational factors not obvious to individuals. However, ethnography is less effective for discovering broader organizational or domain requirements or suggesting innovations.
- **Challenges with Non-Functional Requirements (e.g., Safety and Security)** These are particularly problematic because they often specify what the system _should not_ do ("shall not" requirements), making them difficult to define and impossible to prove exhaustively. Unlike functional requirements, which can be demonstrated, proving that a system will _not_ exhibit certain unwanted behaviors (like unauthorized access or failure) is not feasible. This is compounded in security engineering by the presence of intelligent attackers actively seeking vulnerabilities, willing to experiment with system inputs far beyond normal use.
- **Complexity of Sociotechnical Systems and "Wicked Problems"** Many complex sociotechnical systems are developed to address "wicked problems," which cannot be completely defined due to their complexity and the numerous related entities involved. Different stakeholders perceive the problem in different ways, and a full understanding may only emerge as a solution is developed. This makes it difficult to establish clear success criteria, as the judgment of success often depends on the system's effectiveness at the time of deployment, which may differ from the original business goals due to rapid environmental changes. This inherent complexity means that a complete understanding of a system's behavior in advance is practically impossible, leading to emergent properties that are hard to predict and non-deterministic behaviors.

---

19. During the requirements validation process, what are the different types of checks to
be carried out on the requirements in the Requirements Document. Also, what are the
validation techniques which can be used in conjunction or individually.

During the requirements validation process, several types of checks are carried out on the requirements in the Requirements Document, and various techniques can be employed, either individually or in conjunction, to perform this validation. This process is crucial because errors in requirements can lead to significant rework costs if discovered later in the development cycle or after system deployment.

### Types of Checks on Requirements

The requirements validation process involves the following types of checks to ensure the quality and accuracy of the requirements document:

1. **Validity checks**: These checks ensure that the requirements truly reflect the actual needs of the system users. They account for the possibility that user requirements might have evolved or changed since their initial elicitation.
2. **Consistency checks**: This involves verifying that the requirements within the document do not conflict with one another. There should be no contradictory constraints or differing descriptions of the same system function.
3. **Completeness checks**: These checks aim to confirm that the requirements document includes all functions and constraints that the system user intends.
4. **Realism checks**: Requirements are assessed against existing technologies to ensure they can be implemented within the proposed budget and schedule for the system development.
5. **Verifiability**: To minimize potential disputes between customers and contractors, system requirements should be written in a verifiable manner. This means that it should be possible to design a set of tests that can definitively demonstrate whether the delivered system meets each specified requirement.

### Requirements Validation Techniques

A number of techniques can be used for requirements validation, either alone or in combination:

1. **Requirements reviews**: This technique involves a systematic analysis of the requirements by a team of reviewers. This team, typically comprising individuals from both the system customer and the system developer, meticulously reads the requirements document to identify errors, anomalies, and inconsistencies. The findings from these reviews are formally recorded, and comments are then passed to the author of the requirements or the responsible party for correction. These reviews are based on various project documents, including specifications, designs, code, and test plans, and they ensure consistency, completeness, and adherence to established standards.
2. **Prototyping**: This technique involves the rapid development of an executable model or a part of the system. This prototype is then used by end-users and customers to interact with and evaluate the system, allowing them to provide feedback on its functionality and confirm if it meets their needs and expectations. Prototyping helps users visualize how the system will support their work, which can lead to new requirement ideas or uncover errors and omissions. It serves as a method of anticipating changes, potentially reducing the number of change proposals after the system's final delivery. Executable specifications are an advanced form of this approach, where requirements are specified in an executable format, and the customer executes the specification to observe intended behavior and provide feedback.
3. **Test-case generation**: Requirements should inherently be testable. By devising tests for the requirements as part of the validation process, potential problems with the requirements themselves often become apparent. If a test is difficult or impossible to design, it usually indicates that the corresponding requirement may be challenging to implement and should be reconsidered. Developing tests from user requirements before any code is written is an integral aspect of test-driven development (TDD). In TDD, tests are developed concurrently with requirements, helping both testers and developers to understand the requirements better and preventing delays in test case creation. This systematic approach involves deriving a set of tests for each requirement to demonstrate its satisfaction, often requiring multiple tests per requirement for comprehensive coverage.

---

20. With a neat diagram, explain the Requirements Change Management.

  Requirements change management is a formal process essential for controlling modifications to a system's requirements after the requirements document has been approved. It helps determine if the benefits of implementing new requirements outweigh the costs of their implementation, ensuring that all change proposals are handled consistently and that changes to the requirements document are made in a controlled manner.

This process typically involves three principal stages:

1. **Problem analysis and change specification**: The process begins with an identified requirements problem or a specific change proposal. This initial problem or proposal is analyzed to validate it. The findings from this analysis are then communicated back to the change requestor, who may then refine the proposal or decide to withdraw the request.
2. **Change analysis and costing**: In this stage, the potential impact of the proposed change is assessed. This assessment uses traceability information (links between requirements and other system elements) and general knowledge of the system. The cost of implementing the change is estimated, considering modifications needed for the requirements document, and, if applicable, the system design and implementation. Based on this analysis, a decision is made whether to proceed with the change.
3. **Change implementation**: If the change is approved, the requirements document (and potentially the system design and implementation) are modified. The requirements document should be structured to facilitate changes without extensive rewriting or reorganization, promoting modularity so that individual sections can be altered or replaced without impacting other parts of the document.

**Diagram: Requirements Change Management Process**

The diagram below illustrates the iterative nature of the requirements change management process:

![](images/20.jpeg)

**Explanation of the diagram:**

- The process starts with an "Identified problem".
- This leads to "Problem analysis and change specification," where the problem is evaluated for validity.
- If the problem/change request is "Invalid," it leads to "Close CR" (Change Request), indicating it's rejected or resolved without further action.
- If "Valid," the process moves to "Change analysis and costing," where the impact and cost are determined.
- Following the analysis, the decision leads to "Change implementation" if approved.
- The outcome of "Change implementation" is "Revised requirements," which then feeds back into the system's evolving requirements.

This systematic approach ensures that changes are managed effectively, especially for large software systems where requirements are constantly evolving due to various factors like business environment shifts, new hardware, and changing legislation.

---
