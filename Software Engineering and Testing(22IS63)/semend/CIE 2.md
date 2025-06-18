
---

1. **Explain the risk management process using a neat labeled diagram.** Apply this process to a real or hypothetical software project by identifying at least two potential risks and ways to manage the same.

Software project risk management is a critical process aimed at anticipating potential problems and formulating strategies to address them, thereby minimizing their impact on project schedules or software quality.

The risk management process is typically a **four-stage iterative cycle** that continues throughout the project lifecycle.

**The Risk Management Process** The process involves the following key stages:

1. **Risk Identification**: This initial stage focuses on pinpointing potential risks that could significantly threaten the software engineering process, the software being developed, or the development organization. Project managers might use brainstorming sessions or a predefined checklist of risk types as a starting point. Risks can be broadly categorized into six types:
    
    - **Estimation risks**: These arise from inaccuracies in management's estimates for the resources needed to build the system. Examples include underestimating the time for development, the rate of defect repair, or the overall size of the software.
    - **Organizational risks**: These originate from the organizational environment. Examples include changes in company management leading to shifting priorities or financial problems causing budget cuts.
    - **People risks**: These are associated with the development team members themselves, such as an inability to recruit staff with necessary skills or key staff being unavailable during critical periods.
    - **Requirements risks**: These stem from changes to customer requirements or difficulties in managing those changes, potentially necessitating major design rework.
    - **Technology risks**: These relate to the software or hardware technologies used for development, such as discovering faults in reusable components.
    - **Tools risks**: These are associated with the software tools and other supporting software, like tools not performing as anticipated or not integrating well.
2. **Risk Analysis**: Once risks are identified, this stage involves assessing their likelihood and potential consequences. This relies on judgment and past experience, as precise numeric assessments are often impractical. Risks can be assigned to probability bands (insignificant, low, moderate, high, or very high) and categorized by their effects (catastrophic, serious, tolerable, or insignificant). A risk register may be used to record the results of this analysis.
    
3. **Risk Planning**: This stage involves developing strategies to manage the most significant identified risks. These strategies are designed to minimize disruption if a problem occurs and are often formulated by asking "what-if" questions. Risk management strategies fall into three main categories:
    
    - **Avoidance strategies**: Actions taken to reduce the probability of a risk arising (e.g., ensuring components are thoroughly tested before reuse to avoid defect risks).
    - **Minimization strategies**: Actions that reduce the impact if a risk does occur (e.g., maintaining project knowledge and a skills database to mitigate staff turnover).
    - **Contingency plans**: Preparations made to deal with the risk if it arises (e.g., having a plan for budget cuts).
4. **Risk Monitoring**: This is an ongoing activity where assumptions about product, process, and business risks are continually checked. It involves regularly assessing each identified risk to determine if its probability or seriousness has changed, and tracking indicators that might signal emerging problems. This continuous monitoring enables timely adjustments to the risk management plan.
    

The diagram below illustrates this cyclical process:

```
        +-------------------------+
        |     Risk Identification   |
        |  (Potential Risks List) |
        +-----------+-------------+
                    |
                    V
        +-----------+-------------+
        |        Risk Analysis      |
        |    (Prioritized Risk List) |
        +-----------+-------------+
                    |
                    V
        +-----------+-------------+
        |         Risk Planning     |
        |  (Avoidance & Contingency) |
        +-----------+-------------+
                    |
                    V
        +-----------+-------------+
        |       Risk Monitoring     |
        |     (Risk Assessment)   |
        +-----------+-------------+
                    |
                    | (Feedback loop for
                    |  continuous improvement
                    |  and adaptation)
                    +--------------------+
```

_Figure: The Risk Management Process_

---

**Application to a Hypothetical Software Project: Online University Accounting System**

Let's consider a hypothetical project to develop an **Online University Accounting System**, which will manage student fees, faculty payroll, and departmental budgets.

**Risk 1: Requirements Change**

- **Description**: There is a high likelihood that university stakeholders (e.g., finance department, human resources, student services) will propose numerous changes to the system requirements after initial specification, especially once they see early prototypes or live modules. These changes could necessitate major design rework, affecting the project schedule and product quality.
- **Management Strategies**:
    - **Minimization/Avoidance**: Implement a formal requirements change management process from the outset. This would involve a clear procedure for submitting, analyzing, costing, and approving all change requests.
    - **Planning**: Negotiate with the university client to establish a baseline for requirements early in the project, with a clear understanding that significant changes later will incur additional costs or require adjustments to the delivery schedule. Incorporate an incremental delivery model to allow for early feedback and scope adjustments based on customer priorities, reducing the impact of changes on already developed parts of the system.
    - **Contingency**: Allocate contingency (extra time and effort) in the project plan specifically for handling unforeseen requirements changes. This could be 30-50% of the initial estimate for such a complex, user-facing system.

**Risk 2: Staff Turnover**

- **Description**: Given the competitive market for software engineers, there is a risk that experienced staff, particularly those with expertise in financial systems or specific university processes, might leave the project before its completion. This could severely impact the project schedule and potentially the product quality if replacements are less experienced.
- **Management Strategies**:
    - **Avoidance**: Implement strategies to foster a positive and competitive working environment, including competitive salaries and good benefits, to reduce the likelihood of staff leaving. Promote a cohesive team environment through effective communication and team-building activities.
    - **Minimization**: To mitigate the impact, implement robust knowledge management practices. This includes cross-training team members in different modules and maintaining comprehensive, up-to-date documentation (design documents, code comments, test cases). Develop a "skills database" for the team to identify areas where there might be single points of failure in expertise.
    - **Contingency**: For critical roles, have a succession plan or a pre-vetted list of potential external hires or contractors who could quickly step in. If a key staff member leaves, immediately initiate the recruitment process and reallocate tasks to other team members while the replacement is being onboarded. Regularly monitor staff morale and workload to identify potential issues before they lead to turnover.
---
    
1. **Consider the case study of Triangle Problem** and generate Normal Boundary Value test cases and Worst Case Boundary Value test cases.
    
2. Using relevant examples, **demonstrate how the unique characteristics of software engineering**, as compared to other engineering disciplines, contribute to the complexities of software project management.  
    **(OR)**
    
3. Project Managers need to understand what motivates people. **Maslow has suggested the Human Hierarchy of needs.** Illustrate it with a diagram. Also, discuss the case study of individual motivation.
    
4. **With a relevant diagram, explain the test/debug cycle** and elaborate on the different steps involved in the process.  
    **(OR)**
    
5. **Bring out the differences between various types of Functional Testing versus the types of Structural Testing techniques.**
    
6. CompanyAB is one of the popular online shopping stores which is designed and developed exclusively for kids and ethnic sales. On all seasonal festival times, the store announces heavy discount sales apart from free delivery on all products and purchases of any amount. Due to the pandemic situation of COVID-19, the company decides to further increase the discount on all sales.

**Discounts announced are as below:**

|Type of Dress|Age|Gender|Cost Range|Discount|
|---|---|---|---|---|
|Kids wear (shirt and pants)|≤ 5|Boys|Rs. 100 to Rs. 1,000|5%|
|Kids wear (Skirts and frocks)|≤ 5|Girls|Rs. 100 to Rs. 1,000|5%|
|Kids wear (special dresses like Spiderman, police dress, etc.)|≤ 5|Any child|Rs. 2,500 to Rs. 5,000|10%|
|Kurtha and Pyjama|6–16 years|Girls|Rs. 1,500 to Rs. 10,000|15%|
|Lehenga, Anarkali suit type of dresses|6–16 years|Girls|Rs. 1,000 to Rs. 7,000|12%|
|Sherwani, Dhoti type dresses|6–16 years|Boys|Rs. 1,000 to Rs. 7,000|10%|
|Kurtha and Pyjama|17–30 years|Girls|Rs. 800 to Rs. 15,000|20%|
|Lehenga, Anarkali suit type of dresses|17–30 years|Girls|Rs. 2,000 to Rs. 20,000|25%|
|Sherwani, Dhoti type dresses|17–30 years|Boys|Rs. 2,000 to Rs. 10,000|15%|
|Kurtha and Pyjama|17–30 years|Boys|Rs. 1,000 to Rs. 15,000|18%|

**For the above discount sale, generate test cases using BVA (Boundary Value Analysis) – assuming single fault assumption.**

**(OR)**

 
8. Consider an application where email and password are used to login to the application. If the values of the email are **Blank / Valid / Invalid**, indicate how decisions can be taken up using **Decision Based Testing technique**.
