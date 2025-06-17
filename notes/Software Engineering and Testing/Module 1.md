
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

