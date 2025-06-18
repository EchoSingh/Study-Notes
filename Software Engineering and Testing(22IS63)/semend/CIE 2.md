
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

The Triangle Problem is a widely used case study in software testing to illustrate various unit testing methods due to its clear yet complex logic.

**Case Study: The Triangle Problem** The triangle program accepts three integers, `a`, `b`, and `c`, as input, representing the lengths of the three sides of a triangle. The inputs `a`, `b`, and `c` must satisfy the following conditions:

- `c1. 1 ≤ a ≤ 200`
- `c2. 1 ≤ b ≤ 200`
- `c3. 1 ≤ c ≤ 200`
- `c4. a < b + c`
- `c5. b < a + c`
- `c6. c < a + b`

The program's output should be the type of triangle: Equilateral, Isosceles, Scalene, or NotATriangle.

- If an input value fails conditions `c1`, `c2`, or `c3`, the program should output a message like "Value of [variable] is not in the range of permitted values.".
- If any of conditions `c4`, `c5`, and `c6` is not met, the output is "NotATriangle".
- If all three sides are equal, the output is "Equilateral".
- If exactly one pair of sides is equal, the output is "Isosceles".
- If no pair of sides is equal, the output is "Scalene".

For testing purposes, the lower bounds for side lengths are 1, and an arbitrary upper bound of 200 is used.

---

**1. Normal Boundary Value (NBV) Test Cases**

Normal Boundary Value testing focuses on the boundary of the input space because errors tend to occur near the extreme values of an input variable, for example, due to "off by one" errors in loop conditions. This technique generates test cases using input variable values at their minimum (min), just above the minimum (min+), a nominal (nom) value, just below their maximum (max–), and at their maximum (max).

For a function of `n` variables, Normal Boundary Value analysis generates `4n + 1` unique test cases. The method involves holding all but one variable at their nominal values, and letting the remaining variable assume its full set of test values (min, min+, nom, max–, max), repeating this for each variable.

For the Triangle Problem with three variables (`a`, `b`, `c`), the test values for each side are typically {1 (min), 2 (min+), 100 (nom), 199 (max–), 200 (max)}. This results in `4*3 + 1 = 13` unique test cases.

Here is a table of Normal Boundary Value test cases for the Triangle Problem, as derived in the sources:

| Case | `a` | `b` | `c` | Expected Output | | :--- | :-- | :-- | :-- | :---------------- | | 1 | 100 | 100 | 1 | Isosceles | | 2 | 100 | 100 | 2 | Isosceles | | 3 | 100 | 100 | 100 | Equilateral | | 4 | 100 | 100 | 199 | Isosceles | | 5 | 100 | 100 | 200 | Not a triangle | | 6 | 100 | 1 | 100 | Isosceles | | 7 | 100 | 2 | 100 | Isosceles | | 8 | 100 | 100 | 100 | Equilateral | | 9 | 100 | 199 | 100 | Isosceles | | 10 | 100 | 200 | 100 | Not a triangle | | 11 | 1 | 100 | 100 | Isosceles | | 12 | 2 | 100 | 100 | Isosceles | | 13 | 100 | 100 | 100 | Equilateral | | 14 | 199 | 100 | 100 | Isosceles | | 15 | 200 | 100 | 100 | Not a triangle | _(Note: Test cases 3, 8, and 13 are identical and could be deleted, resulting in 13 unique test cases)._

---

**2. Worst-Case Boundary Value (WCBV) Test Cases**

Worst-Case Boundary Value testing is used when the "single fault" assumption (that failures are rarely the result of simultaneous occurrences of multiple faults) is not warranted. It focuses on what happens when more than one variable has an extreme value. This technique generates test cases by taking the Cartesian product of the five-element set (min, min+, nom, max–, max) for each variable.

For a function of `n` variables, Worst-Case Boundary Value testing generates `5^n` test cases. For the Triangle Problem with three variables, this results in `5^3 = 125` test cases. Due to the large number of test cases, only a selected portion is typically shown.

Here is a selection of Worst-Case Boundary Value test cases for the Triangle Problem:

| Case | `a` | `b` | `c` | Expected Output | | :--- | :-- | :-- | :-- | :--------------- | | 1 | 1 | 1 | 1 | Equilateral | | 2 | 1 | 1 | 2 | Not a triangle | | 3 | 1 | 1 | 100 | Not a triangle | | 4 | 1 | 1 | 199 | Not a triangle | | 5 | 1 | 1 | 200 | Not a triangle | | 6 | 1 | 2 | 1 | Not a triangle | | 7 | 1 | 2 | 2 | Isosceles | | 8 | 1 | 2 | 100 | Not a triangle | | 9 | 1 | 2 | 199 | Not a triangle | | 10 | 1 | 2 | 200 | Not a triangle | | 11 | 1 | 100 | 1 | Not a triangle | | 12 | 1 | 100 | 2 | Not a triangle | | 13 | 1 | 100 | 100 | Isosceles | | 14 | 1 | 100 | 199 | Not a triangle | | 15 | 1 | 100 | 200 | Not a triangle | | 16 | 1 | 199 | 1 | Not a triangle | | 17 | 1 | 199 | 2 | Not a triangle | | 18 | 1 | 199 | 100 | Not a triangle | | 19 | 1 | 199 | 199 | Isosceles | | 20 | 1 | 199 | 200 | Not a triangle | | 21 | 1 | 200 | 1 | Not a triangle | | 22 | 1 | 200 | 2 | Not a triangle | | 23 | 1 | 200 | 100 | Not a triangle | | 24 | 1 | 200 | 199 | Not a triangle | | 25 | 1 | 200 | 200 | Isosceles |

These methods are rooted in the assumption that input variables are independent. However, the Triangle Problem inherently has logical dependencies among its input variables (e.g., `a`, `b`, and `c` must satisfy the triangle inequality to form a valid triangle). This can lead to the generation of "impossible" or "strange" test cases, as seen in some of the "Not a triangle" outputs, where the values chosen for `a`, `b`, and `c` do not form a geometrically possible triangle. While such cases are useful for testing robustness against invalid input combinations, they also highlight a limitation of these methods when applied without considering semantic dependencies.

---

1. Using relevant examples, **demonstrate how the unique characteristics of software engineering**, as compared to other engineering disciplines, contribute to the complexities of software project management.  
    **(OR)**
    
2. Project Managers need to understand what motivates people. **Maslow has suggested the Human Hierarchy of needs.** Illustrate it with a diagram. Also, discuss the case study of individual motivation.
    
3. **With a relevant diagram, explain the test/debug cycle** and elaborate on the different steps involved in the process.  
    **(OR)**
    
4. **Bring out the differences between various types of Functional Testing versus the types of Structural Testing techniques.**
    
5. CompanyAB is one of the popular online shopping stores which is designed and developed exclusively for kids and ethnic sales. On all seasonal festival times, the store announces heavy discount sales apart from free delivery on all products and purchases of any amount. Due to the pandemic situation of COVID-19, the company decides to further increase the discount on all sales.

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
