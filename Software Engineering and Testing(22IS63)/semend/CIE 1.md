

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
    
4. Identify the software process model suitable for Banking applications. Illustrate the identified process model with suitable steps.
    
5. Differentiate between various types of non-functional requirements with suitable examples for each.  
    **(OR)**
    
6. Determine the role of integration and configuration model in software engineering. With a suitable diagram explain the steps involved.
    
7. Differentiate between plan driven development and agile development. Illustrate the role of agile models in prescribing medication in a Healthcare system.  
    **(OR)**
    
8. Explain the role of interaction models in software engineering. Consider an ATM application and generate sequence diagram for balance enquiry.