
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

    Figure 2.3 shows a general process model for reuse-based development, based on integration and configuration. The stages in this process are: 1. Requirements specification The initial requirements for the system are proposed. These do not have to be elaborated in detail but should include brief descriptions of essential requirements and desirable system features. 2. Software discovery and evaluation Given an outline of the software requirements, a search is made for components and systems that provide the functionality required. Candidate components and systems are evaluated to see if
    they meet the essential requirements and if they are generally suitable for use in the system. 3. Requirements refinement During this stage, the requirements are refined using information about the reusable components and applications that have been discovered. The requirements are modified to reflect the available components, and the system specification is re-defined. Where modifications are impossible, the component analysis activity may be reentered to search for alternative solutions. 4. Application system configuration If an off-the-shelf application system that meets the requirements is available, it may then be configured for use to create the new system. 5. Component adaptation and integration If there is no off-the-shelf system, individual reusable components may be modified and new components developed. These are then integrated to create the system. Reuse-oriented software engineering, based around configuration and integration, has the obvious advantage of reducing the amount of software to be developed and so reducing cost and risks. It usually also leads to faster delivery of the software. However, requirements compromises are inevitable, and this may lead to a system Software development tools Software development tools are programs that are used to support software engineering process activities. These tools include requirements management tools, design editors, refactoring support tools, compilers, debuggers, bug trackers, and system building tools. Software tools provide process support by automating some process activities and by providing information about the software that is being developed. For example: ■ The development of graphical system models as part of the requirements specification or the software design ■ The generation of code from these graphical models ■ The generation of user interfaces from a graphical interface description that is created interactively by the user ■ Program debugging through the provision of information about an executing program ■ The automated translation of programs written using an old version of a programming language to a more recent version Tools may be combined within a framework called an Interactive Development Environment or IDE. This provides a common set of facilities that tools can use so that it is easier for tools to communicate and operate in an integrated way. http://software-engineering-book.com/web/software-tools/ 2.1 ■  Software process models    53 54    Chapter 2 ■  Software processes that does not meet the real needs of users. Furthermore, some control over the system evolution is lost as new versions of the reusable components are not under the control of the organization using them. Software reuse is very important, and so several chapters in the third I have dedicated several chapters in the 3rd part of the book to this topic. General issues of software reuse are covered in Chapter 15, component-based software engineering in Chapters 16 and 17, and service-oriented systems in Chapter 18.