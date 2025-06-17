
1. With a neat diagram, explain the Requirements Change Management.

  Ans)

  Requirements change management is a formal process applied to all proposed modifications to a system's requirements after the requirements document has been approved. This process is crucial because requirements for large software systems are constantly evolving due to changing business environments, new technologies, and a deepening understanding of the problem by stakeholders. Effectively managing these changes ensures that their impact and cost are assessed, and that urgent and cost-effective modifications are prioritized and incorporated in a controlled manner.

The change management process is typically initiated when a system stakeholder, such as a system owner, user, beta tester, developer, or marketing department, submits a change request. This request can be a bug report detailing symptoms or a proposal for new functionality.

The process generally involves several key activities, which can be visualized as follows:

```
                  +---------------------+
                  |  Change Requests    |
                  +---------------------+
                            |
                            v
                  +---------------------+
                  |   Submit CR         |
                  +---------------------+
                            |
                            v
                  +---------------------+
                  |   Check CR          |
                  +---------------------+
                 /           \
              Valid          Invalid
               |              |
               v              v
      +---------------------+ +---------------------+
      |   Register CR       | |    Close CR         |
      +---------------------+ +---------------------+
               |
               v
      +---------------------+
      |   Assess CRs        |
      | - Implementation    |
      |   analysis          |
      | - Cost/impact       |
      |   analysis          |
      +---------------------+
               |
               v
      +---------------------+
      |   Select CRs        |
      +---------------------+
                 | (Accepted)
                 v
      +---------------------+
      |   Modify Software   |
      +---------------------+
               |
               v
      +---------------------+
      |   Test Software     |
      +---------------------+
               |
               v
      +---------------------+
      |   Close CR          |
      +---------------------+
```

Here are the principal stages and activities involved in requirements change management:

1. **Problem Analysis and Change Specification (Submit & Check CR)**:
    
    - The process begins with the submission of a change request (CR) by a system stakeholder, describing the required modification to the system.
    - This submitted change request is then checked to ensure its validity. This includes verifying if the issue has been previously reported and resolved or if the request stems from a misunderstanding of existing system functionality.
    - Invalid requests are closed at this stage. If the request is determined to be valid, it is formally logged as an outstanding request for further processing.
2. **Change Analysis and Costing (Assess CRs)**:
    
    - This stage involves a thorough assessment of the proposed change's impact and an estimation of its associated cost. This responsibility typically falls to the development or maintenance team, as they possess the technical knowledge required for this evaluation.
    - **Implementation analysis:** This activity identifies all components of the system that will be affected by the proposed change. If the change necessitates further modifications in other parts of the system, this will inherently increase the overall implementation cost.
    - **Cost/impact analysis:** This involves estimating the cost of making the change, taking into account the effort required for modifying not only the directly affected components but also any related components and documentation.
    - The information derived from this analysis is used to determine whether the proposed change is economically justified for the organization.
3. **Selection of Change Requests (Select CRs)**:
    
    - A change control board (CCB) or a dedicated product development group reviews the impact and cost analysis provided.
    - This group makes the decision on whether the change is economically viable and prioritizes the accepted changes based on strategic and organizational considerations. Factors influencing this decision include the potential consequences of _not_ making the change, such as the severity of a reported system failure. Rejected changes are formally closed at this point.
    - In some agile methodologies, customers are directly involved in this prioritization process, collaborating with the team to assess the impact of a change and decide if it should take precedence over features planned for the next system increment.
4. **Change Implementation (Modify & Test Software)**:
    
    - Once a change is approved, the requirements document, and where necessary, the system design and the actual software implementation are modified.
    - The software is modified according to the specifications derived from the approved change.
    - Following modification, the software undergoes rigorous testing to ensure its correctness and to confirm that no new problems or regressions have been introduced into the existing system. For urgent changes, it is especially important to update the requirements document as soon as possible to include the revised requirements, thereby preventing inconsistencies between the documentation and the executable code.
5. **Closing the Change Request (Close CR)**:
    
    - Upon successful completion of the implementation and validation through testing, the change request is formally closed, signifying that the modification has been integrated into the system.

The level of formality within requirements change management can vary significantly based on the organization's size and type. Smaller companies might adopt less formal processes compared to larger organizations dealing with corporate or government clients. For agile development, changes are typically recorded in an issue tracking system and discussed in daily meetings, with immediate changes often directly handled by developers, which minimizes the need for a highly formal process once the system reaches a stage of frequent builds. Maintaining a detailed derivation history of changes within the component source code is also a recommended practice.