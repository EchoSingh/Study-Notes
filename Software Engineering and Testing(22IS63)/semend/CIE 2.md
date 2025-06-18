
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

![](images/cie_2.jpeg)

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
    
2. **Consider the case study of Triangle Problem** and generate Normal Boundary Value test cases and Worst Case Boundary Value test cases.

The Triangle Problem is a widely used case study in software testing to illustrate various unit testing methods due to its clear yet complex logic.

**Case Study: The Triangle Problem** The triangle program accepts three integers, `a`, `b`, and `c`, as input, representing the lengths of the three sides of a triangle. The inputs `a`, `b`, and `c` must satisfy the following conditions:

- `c1. 1 ≤ a ≤ 200`
- `c2. 1 ≤ b ≤ 200`
- `c3. 1 ≤ c ≤ 200`
- `c4. a < b + c`
- `c5. b < a + c`
- `c6. c < a + b`

The program's output should be the type of triangle: Equilateral, Isosceles, Scalene, or NotATriangle.

- If an input value fails conditions `c1`, `c2`, or `c3`, the program should output a message like "Value of variable is not in the range of permitted values.".
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

|Case|`a`|`b`|`c`|Expected Output|
|:--|:--|:--|:--|:--|
|1|100|100|1|Isosceles|
|2|100|100|2|Isosceles|
|3|100|100|100|Equilateral|
|4|100|100|199|Isosceles|
|5|100|100|200|Not a triangle|
|6|100|1|100|Isosceles|
|7|100|2|100|Isosceles|
|8|100|199|100|Isosceles|
|9|100|200|100|Not a triangle|
|10|1|100|100|Isosceles|
|11|2|100|100|Isosceles|
|12|199|100|100|Isosceles|
|13|200|100|100|Not a triangle|



---

**2. Worst-Case Boundary Value (WCBV) Test Cases**

Worst-Case Boundary Value testing is used when the "single fault" assumption (that failures are rarely the result of simultaneous occurrences of multiple faults) is not warranted. It focuses on what happens when more than one variable has an extreme value. This technique generates test cases by taking the Cartesian product of the five-element set (min, min+, nom, max–, max) for each variable.

For a function of `n` variables, Worst-Case Boundary Value testing generates `5^n` test cases. For the Triangle Problem with three variables, this results in `5^3 = 125` test cases. Due to the large number of test cases, only a selected portion is typically shown.

Here is a selection of Worst-Case Boundary Value test cases for the Triangle Problem:

|Case|`a`|`b`|`c`|Expected Output|
|:--|:--|:--|:--|:--|
|1|1|1|1|Equilateral|
|2|1|1|2|Not a triangle|
|3|1|1|100|Not a triangle|
|4|1|1|199|Not a triangle|
|5|1|1|200|Not a triangle|
|6|1|2|1|Not a triangle|
|7|1|2|2|Isosceles|
|8|1|2|100|Not a triangle|
|9|1|2|199|Not a triangle|
|10|1|2|200|Not a triangle|
|11|1|100|1|Not a triangle|
|12|1|100|2|Not a triangle|
|13|1|100|100|Isosceles|
|14|1|100|199|Not a triangle|
|15|1|100|200|Not a triangle|
|16|1|199|1|Not a triangle|
|17|1|199|2|Not a triangle|
|18|1|199|100|Not a triangle|
|19|1|199|199|Isosceles|
|20|1|199|200|Not a triangle|
|21|1|200|1|Not a triangle|
|22|1|200|2|Not a triangle|
|23|1|200|100|Not a triangle|
|24|1|200|199|Not a triangle|
|25|1|200|200|Isosceles|


These methods are rooted in the assumption that input variables are independent. However, the Triangle Problem inherently has logical dependencies among its input variables (e.g., `a`, `b`, and `c` must satisfy the triangle inequality to form a valid triangle). This can lead to the generation of "impossible" or "strange" test cases, as seen in some of the "Not a triangle" outputs, where the values chosen for `a`, `b`, and `c` do not form a geometrically possible triangle. While such cases are useful for testing robustness against invalid input combinations, they also highlight a limitation of these methods when applied without considering semantic dependencies.

---

3. Using relevant examples, **demonstrate how the unique characteristics of software engineering**, as compared to other engineering disciplines, contribute to the complexities of software project management.  


The unique characteristics of software engineering, when compared to more traditional engineering disciplines, contribute significantly to the complexities of software project management. These distinctions make the challenges faced by software project managers particularly intricate.

Here are several ways the unique nature of software engineering contributes to project management complexities, supported by examples from the sources:

1. **Intangibility of the Product** Unlike physical products such as bridges or ships, software is an abstract and intangible entity; it cannot be seen or touched. Software encompasses not only the programs themselves but also all associated documentation, libraries, support websites, and configuration data required for usefulness.
    
    - **Management Complexity:** This intangibility makes it difficult for project managers to visually assess progress. Instead, they must rely on indirect evidence and documentation to track work. For example, a manager of a civil engineering project can see the physical structure being built, making it evident if the schedule slips. In software, managers must meticulously track tasks and deliverables, as the absence of a physical artifact obscures progress. Managing all the "associated documentation" and other intangible assets also adds layers of complexity.
2. **Uniqueness and "One-Off" Nature of Projects** Many large software projects are inherently unique, or "one-off" endeavors, meaning each development environment is, in some way, different from others. Rapid technological changes also mean that experience from previous projects can quickly become obsolete. There are no universal notations, methods, or techniques for software engineering because different types of software require different approaches.
    
    - **Management Complexity:** This uniqueness makes it challenging to anticipate problems effectively, as there's less direct historical precedent to draw upon. Project planning and cost estimation become highly speculative in the early stages, as a complete set of requirements is often unavailable. Managers cannot simply apply a standardized blueprint or process, requiring constant adaptation and custom tailoring of approaches for each new project, increasing risk and overhead.
3. **Variability and Lack of Universal Processes** Software development processes are highly variable and often organization-specific, unlike the more standardized engineering processes found in disciplines with established physical laws and materials. No single method or technique is "good for everything" in software development.
    
    - **Management Complexity:** This variability means managers cannot rely on a single, universally applicable "best practice" or a predictable process model to guarantee success. They must continually evaluate and choose the most appropriate methods for a given project, which adds a layer of decision-making complexity and requires deep understanding of various methodologies, from plan-driven approaches to agile methods.
4. **Abstract Nature and Absence of Physical Laws/Mathematical Predictability** Software systems are abstract and are not constrained by the properties of materials or governed by physical laws. It is difficult to create mathematical models of software systems that can precisely predict their behavior and attributes.
    
    - **Management Complexity:** This lack of a clear "scientific basis for decision making" (in the way, for example, a civil engineer uses physics to predict structural integrity) means that political factors often drive decisions in large and complex software systems. This can introduce non-technical challenges and uncertainties into project planning and execution, making it harder to establish objective criteria for success or to formally verify system behavior.
5. **Fluid Boundaries and Lack of Physical Limitations** Since software has no inherent physical limitations, the boundaries of a system can be difficult to draw definitively and are prone to change during development based on evolving requirements and stakeholder input. This can lead to "scope creep," where the project's scope continuously expands .
    
    - **Management Complexity:** Managers face the constant challenge of requirements creep, as stakeholders may push for additional features, believing there are no physical limits. This necessitates rigorous requirements management and change control processes to manage expectations, prevent constant rework, and control costs, which can otherwise escalate rapidly.
6. **Ease of Linking Systems and Managerial Independence in Systems of Systems (SoS)** It is relatively easy to link software systems from different owners, leading to the creation of complex "systems of systems" where individual constituent systems are independently managed and governed.
    
    - **Management Complexity:** This introduces significant "managerial and governance complexity". Managers must coordinate across different organizations or parts of a large organization, each with its own policies, rules, and priorities. Conflicts can arise that require substantial time and effort to resolve, as there is no single, unified control over the entire SoS's evolution.

These fundamental differences elevate software project management beyond a purely technical endeavor, requiring managers to navigate a complex interplay of human, organizational, and technological factors.

---

4. Project Managers need to understand what motivates people. **Maslow has suggested the Human Hierarchy of needs.** Illustrate it with a diagram. Also, discuss the case study of individual motivation.
    
Project managers need to understand what motivates people. Abraham Maslow proposed a theory known as the Human Hierarchy of Needs, suggesting that individuals are motivated by satisfying a series of needs arranged in hierarchical levels.

### Maslow's Hierarchy of Needs

Maslow's hierarchy states that people prioritize satisfying lower-level needs before moving on to more abstract, higher-level needs. The hierarchy includes five levels:

1. **Physiological needs:** These are the most fundamental needs for survival, such as food, water, and sleep.
2. **Safety needs:** This level concerns the need to feel secure and protected in one's environment.
3. **Social needs:** This involves the desire to feel a sense of belonging and to be part of a social group.
4. **Esteem needs:** This represents the need to feel respected by others and to achieve recognition.
5. **Self-realization needs:** This is the highest level, focused on personal growth, development, and achieving one's full potential.

In a software development context, employees typically have their basic physiological and safety needs met. Therefore, for project managers, the focus shifts to addressing the social, esteem, and self-realization needs of their team members. To fulfill social needs, managers should create opportunities for co-workers to interact and feel part of a group. Esteem needs can be met through public recognition of achievements and fair compensation. Self-realization needs are addressed by providing challenging responsibilities, demanding tasks, and opportunities for training and professional development.

The hierarchy can be visually represented as:

![](images/cie_2_1.jpeg)

### Case Study: Individual Motivation

A case study involving a software project manager named Alice and a team member named Dorothy illustrates how individual motivation can decline and how it can be addressed by a manager. Dorothy, a competent group member, began to lose interest in her work, which led to a decrease in the quality of her output.

Alice investigated the problem, considering factors such as personal circumstances or the project taking an unexpected direction. Dorothy eventually admitted that she had lost interest because the work did not align with her desire to develop hardware interfacing skills, which she saw as crucial for her career progression. She was concerned that her current role as a C programmer on alarm system software was not helping her achieve her self-realization needs and that it would be difficult to find a future job in her desired area.

Instead of letting Dorothy leave, Alice decided to address her motivation directly. Alice sought to re-motivate Dorothy by emphasizing that broadening her experience could be a positive career step. She provided Dorothy with more **design autonomy** and arranged **training courses in software engineering** to help her enhance her skills and future career prospects. This approach aimed to satisfy Dorothy's esteem and self-realization needs by recognizing her value, offering opportunities for professional growth, and aligning her work with her personal development goals.

---

5. **With a relevant diagram, explain the test/debug cycle** and elaborate on the different steps involved in the process.  
    **(OR)**
The test/debug cycle is a process where testing and debugging are used as two related and often cyclic activities in software development. Testing aims to uncover errors in a program by sampling the input domain and checking program behavior, while debugging focuses on determining the cause of these errors and removing them.

This cycle begins with the construction of a non-empty set of test cases, usually derived from the program's requirements. The program is then executed against these test cases, and any observed failures lead to debugging, where the source of the failure is identified and removed. The cycle continues until the test set is deemed adequate according to a chosen criterion.

Below is a diagram illustrating the test and debug cycle, followed by an elaboration of its steps:

**Figure 1.4 A test and debug cycle.**

![](images/cie_2_2.jpeg)

Here are the different steps involved in the test/debug cycle:

- **Preparing a Test Plan** A test cycle is typically guided by a test plan. This plan helps in defining what is to be tested, the testing schedule, and how results will be recorded. For smaller programs, this plan might be informal or even non-existent. The program requirements and the test plan are crucial for constructing test data.
    
- **Defining the Input Domain** The input domain, also known as input space, is an essential source for generating test cases. While requirements help in deriving input domains, the incompleteness of requirements often necessitates more careful thought to define them completely.
    
- **Constructing Test Input (Test Data)** A test case is defined as a pair consisting of input data and its corresponding program output. Test data itself is a set of values for each input variable. A collection of test cases forms a "test set" or "test suite". Test data construction is guided by program requirements and the test plan. Testers might generate a few test cases, execute them, and then decide whether to construct more or proceed to debugging based on the results.
    
- **Executing the Program** After test cases are constructed, the program is executed using this test data. The complexity of executing a program varies significantly depending on the program itself. For intricate systems, thousands of tests may need to be executed. A "test harness" can be used to facilitate this step by initializing variables, inputting test cases, and saving the program's output for later examination.
    
- **Assessing Program Correctness (Is Behavior as Expected?)** This is a critical step where the tester determines if the observed behavior of the program is correct. This involves observing the behavior and then analyzing it for correctness. The entity responsible for checking this correctness is called an **oracle**. An oracle can be a program or a human. The output from an oracle can be a simple "Yes" or "No," or a more complex explanation of why the observed behavior matches or differs from the expected behavior.
    
- **Debugging** If the observed behavior is _not_ as expected, implying a failure has occurred, the process transitions into debugging. Debugging is the subsequent step where the cause of the detected error is determined and then removed. While testing identifies the presence of defects, debugging is concerned with _locating and correcting_ them. This process can involve generating hypotheses about the program's observable behavior, manually tracing the code, using new test cases to pinpoint the problem, and employing interactive debugging tools that show intermediate variable values and execution traces. Debugging may require modifications to the program, and after a fix, the test and debug cycle often repeats to ensure the program now behaves as expected and no new issues have been introduced.
---

6. **Bring out the differences between various types of Functional Testing versus the types of Structural Testing techniques.**

 Software testing broadly categorizes techniques into **Functional Testing** and **Structural Testing**, also known as **Black-Box** and **White-Box testing**, respectively. While distinct in their approach and focus, these two types of testing are complementary and often used together to achieve comprehensive software quality.

### Functional Testing (Black-Box Testing)

Functional testing focuses on the external behavior of a program, verifying that it performs as expected according to its requirements or specifications, without any knowledge of its internal code structure.

**Key Characteristics:**

- **Source of Test Cases:** Tests are generated directly from informal or formal requirements, specifications, or models of expected behavior.
- **Purpose:** To demonstrate that the software meets its stated functional and non-functional requirements and to find failures. It validates "what the system does".
- **Fault Detection:** Primarily effective at uncovering "faults of omission"—specified behaviors that were not implemented.
- **Timing:** Test case development can occur in parallel with the implementation, potentially reducing the overall project development interval.

**Types of Functional Testing Techniques:**

- **Boundary Value Analysis (BVA):** Focuses on testing at and near the extreme values of input variables. It aims to find errors that occur at the boundaries of valid input ranges. It has variations such as Normal, Robust, Worst-Case, and Robust Worst-Case BVA.
- **Equivalence Partitioning:** Divides the input domain into partitions or "equivalence classes" where the program is expected to behave similarly. It includes Weak Normal, Strong Normal, Weak Robust, and Strong Robust forms.
- **Cause-Effect Graphing:** A visual method for capturing requirements as logical conditions (causes) and their corresponding actions (effects) to systematically generate test cases.
- **Decision Table-Based Testing:** Rigorous method for testing based on decision tables, which map conditions to actions. It is particularly useful for applications with complex logical relationships among input variables.
- **Model-Based/Specification-Based Testing:** Involves generating tests from formal models or specifications of the system's behavior (e.g., Finite State Machines, Statecharts, Petri nets).
- **Combinatorial Designs (e.g., Pairwise Testing, Orthogonal Arrays):** Aims to select a small subset of factor combinations from a large set, particularly effective for detecting interaction faults among variables.
- **Random Testing:** Uses a systematic method to generate tests by randomly sampling data from the input space to avoid bias.
- **Interface Testing:** A form of black-box testing that specifically focuses on testing a program via its interfaces.
- **Goal-Directed Testing:** Categorized by specific goals like security testing, robustness testing (testing against unintended inputs), performance testing (stress, load, capacity), compatibility testing, and acceptance testing.
- **Scenario-Based Testing:** Involves inventing typical usage scenarios to derive test cases, replicating the practical use of the system.

**Limitations of Functional Testing:**

- May lead to significant redundancies among test cases and can have gaps of untested software.
- Cannot recognize if specified behaviors have not been implemented.
- It is difficult to trace test cases back to requirements, making it hard to know which requirements are fully tested.

### Structural Testing (White-Box Testing)

Structural testing, or white-box testing, analyzes and tests the internal structure, design, and implementation of a program.

**Key Characteristics:**

- **Source of Test Cases:** Tests are generated based on knowledge of the program's source code, its control flow, and data flow.
- **Purpose:** To discover defects by exercising different paths, statements, or data interactions within the code and to measure how much of the code has been tested (coverage). It reveals "how a system is built".
- **Fault Detection:** Effective at finding "faults of commission"—programmed behaviors that were not specified—and implementation errors, including subtle flaws.
- **Timing:** Typically performed after some code has been written, often interleaved with debugging. However, methodologies like Test-Driven Development integrate code writing and testing tightly.

**Types of Structural Testing Techniques:**

- **Control Flow-Based Testing:** Measures test adequacy based on the flow of control in a program. Examples include:
    - **Statement Coverage:** Ensures every executable statement in the code is executed at least once.
    - **Branch/Decision Coverage:** Ensures every outcome of a decision (true/false branches) is exercised.
    - **Condition Coverage:** Ensures each simple condition within a compound condition is evaluated to both true and false.
    - **Multiple Condition Coverage:** Requires all possible combinations of truth values for simple conditions within a compound condition to be exercised.
    - **Modified Condition/Decision Coverage (MC/DC):** A strong criterion where each condition in a decision takes on all possible outcomes independently of other conditions, and each entry/exit point is traversed.
    - **Path Testing:** Aims to exercise every independent execution path through a component or program. Basis path testing, derived from cyclomatic complexity, provides a baseline for necessary testing paths.
- **Data Flow-Based Testing:** Focuses on the definition and use of variables within a program, aiming to test the flow of data. Examples include:
    - **Define/Use (DU) Testing:** Tests paths from where a variable is defined to where it is used.
    - **Slice-Based Testing:** Focuses on program slices, which are subsets of a program that affect the values of variables at specific points.
- **Mutation Testing:** A powerful technique for assessing test adequacy and enhancing test sets. It involves creating small, syntactic changes (mutants) in the program and then using test cases to "kill" these mutants by causing them to produce different output than the original program.

**Limitations of Structural Testing:**

- Cannot reveal missing functionality that is specified in the requirements.
- Can be affected by infeasible paths, which are paths that are topologically possible but cannot be executed in reality.
- May create a "false sense of stability and quality" if testing only covers existing code paths without validating the completeness of use cases.

### Differences and Complementarity

The fundamental differences between functional and structural testing are summarized below:

|Feature|Functional Testing (Black-Box)|Structural Testing (White-Box)|
|:--|:--|:--|
|**Basis for Design**|External requirements, specifications, and desired behavior.|Internal code structure, logic, and paths.|
|**Knowledge Required**|No knowledge of internal code or implementation details.|Requires in-depth knowledge of source code, algorithms, and data structures.|
|**Primary Purpose**|To validate that the system meets user and system requirements; demonstrate correct execution.|To discover defects and measure code coverage; ensure all parts of the code are exercised.|
|**Faults Targeted**|Faults of omission (missing functionality).|Faults of commission (unspecified but implemented behavior) and implementation errors.|
|**Timing in SDLC**|Can start early in the development cycle, in parallel with requirements definition.|Generally starts after code has been written, often during coding and unit testing phases.|
|**Redundancy & Gaps**|Prone to redundancies and gaps if not supplemented.|Provides metrics (coverage) to identify gaps and redundancies in test suites, including those from functional testing.|
|**"What" vs. "How"**|Focuses on "what the system does".|Focuses on "how the system is built" or "what it is" internally.|

In practice, both approaches are crucial. Functional testing provides confidence that the software meets its specified purpose from a user's perspective, while structural testing ensures the internal robustness and completeness of the code, catching defects that might not be apparent from the external behavior alone. Structural testing can significantly enhance tests initially derived from functional requirements by identifying untested code portions and prompting the creation of additional test cases.

---
 
7. CompanyAB is one of the popular online shopping stores which is designed and developed exclusively for kids and ethnic sales. On all seasonal festival times, the store announces heavy discount sales apart from free delivery on all products and purchases of any amount. Due to the pandemic situation of COVID-19, the company decides to further increase the discount on all sales.

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


Here is the generation of test cases for each discount rule:

---

### Discount Rule 1: Kids wear (shirt and pants)

- **Parameters:** Type of Dress: Kids wear (shirt and pants), Gender: Boys
- **Age Range:** years
    - Min Age: 1, Min+ Age: 2, Nom Age: 3, Max- Age: 4, Max Age: 5
- **Cost Range:** [Rs. 100, Rs. 1,000]
    - Min Cost: 100, Min+ Cost: 101, Nom Cost: 550, Max- Cost: 999, Max Cost: 1,000
- **Expected Discount:** 5%

|Test Case #|Type of Dress|Age|Gender|Cost (Rs.)|Expected Discount (%)|Comment (BVA point varied)|
|:--|:--|:--|:--|:--|:--|:--|
|1.1|Kids wear (shirt and pants)|3|Boys|550|5|Nominal Age & Cost|
|1.2|Kids wear (shirt and pants)|1|Boys|550|5|Age - Minimum|
|1.3|Kids wear (shirt and pants)|2|Boys|550|5|Age - Just above minimum|
|1.4|Kids wear (shirt and pants)|4|Boys|550|5|Age - Just below maximum|
|1.5|Kids wear (shirt and pants)|5|Boys|550|5|Age - Maximum|
|1.6|Kids wear (shirt and pants)|3|Boys|100|5|Cost - Minimum|
|1.7|Kids wear (shirt and pants)|3|Boys|101|5|Cost - Just above minimum|
|1.8|Kids wear (shirt and pants)|3|Boys|999|5|Cost - Just below maximum|
|1.9|Kids wear (shirt and pants)|3|Boys|1,000|5|Cost - Maximum|

---

### Discount Rule 2: Kids wear (Skirts and frocks)

- **Parameters:** Type of Dress: Kids wear (Skirts and frocks), Gender: Girls
- **Age Range:** years
    - Min Age: 1, Min+ Age: 2, Nom Age: 3, Max- Age: 4, Max Age: 5
- **Cost Range:** [Rs. 100, Rs. 1,000]
    - Min Cost: 100, Min+ Cost: 101, Nom Cost: 550, Max- Cost: 999, Max Cost: 1,000
- **Expected Discount:** 5%

|Test Case #|Type of Dress|Age|Gender|Cost (Rs.)|Expected Discount (%)|Comment (BVA point varied)|
|:--|:--|:--|:--|:--|:--|:--|
|2.1|Kids wear (Skirts and frocks)|3|Girls|550|5|Nominal Age & Cost|
|2.2|Kids wear (Skirts and frocks)|1|Girls|550|5|Age - Minimum|
|2.3|Kids wear (Skirts and frocks)|2|Girls|550|5|Age - Just above minimum|
|2.4|Kids wear (Skirts and frocks)|4|Girls|550|5|Age - Just below maximum|
|2.5|Kids wear (Skirts and frocks)|5|Girls|550|5|Age - Maximum|
|2.6|Kids wear (Skirts and frocks)|3|Girls|100|5|Cost - Minimum|
|2.7|Kids wear (Skirts and frocks)|3|Girls|101|5|Cost - Just above minimum|
|2.8|Kids wear (Skirts and frocks)|3|Girls|999|5|Cost - Just below maximum|
|2.9|Kids wear (Skirts and frocks)|3|Girls|1,000|5|Cost - Maximum|

---

### Discount Rule 3: Kids wear (special dresses like Spiderman, police dress, etc.)

- **Parameters:** Type of Dress: Kids wear (special dresses), Gender: Any child
- **Age Range:** years
    - Min Age: 1, Min+ Age: 2, Nom Age: 3, Max- Age: 4, Max Age: 5
- **Cost Range:** [Rs. 2,500, Rs. 5,000]
    - Min Cost: 2,500, Min+ Cost: 2,501, Nom Cost: 3,750, Max- Cost: 4,999, Max Cost: 5,000
- **Expected Discount:** 10%

|Test Case #|Type of Dress|Age|Gender|Cost (Rs.)|Expected Discount (%)|Comment (BVA point varied)|
|:--|:--|:--|:--|:--|:--|:--|
|3.1|Kids wear (special dresses)|3|Any|3,750|10|Nominal Age & Cost|
|3.2|Kids wear (special dresses)|1|Any|3,750|10|Age - Minimum|
|3.3|Kids wear (special dresses)|2|Any|3,750|10|Age - Just above minimum|
|3.4|Kids wear (special dresses)|4|Any|3,750|10|Age - Just below maximum|
|3.5|Kids wear (special dresses)|5|Any|3,750|10|Age - Maximum|
|3.6|Kids wear (special dresses)|3|Any|2,500|10|Cost - Minimum|
|3.7|Kids wear (special dresses)|3|Any|2,501|10|Cost - Just above minimum|
|3.8|Kids wear (special dresses)|3|Any|4,999|10|Cost - Just below maximum|
|3.9|Kids wear (special dresses)|3|Any|5,000|10|Cost - Maximum|

---

### Discount Rule 4: Kurtha and Pyjama (Age 6–16 years, Girls)

- **Parameters:** Type of Dress: Kurtha and Pyjama, Gender: Girls
- **Age Range:** years
    - Min Age: 6, Min+ Age: 7, Nom Age: 11, Max- Age: 15, Max Age: 16
- **Cost Range:** [Rs. 1,500, Rs. 10,000]
    - Min Cost: 1,500, Min+ Cost: 1,501, Nom Cost: 5,750, Max- Cost: 9,999, Max Cost: 10,000
- **Expected Discount:** 15%

|Test Case #|Type of Dress|Age|Gender|Cost (Rs.)|Expected Discount (%)|Comment (BVA point varied)|
|:--|:--|:--|:--|:--|:--|:--|
|4.1|Kurtha and Pyjama|11|Girls|5,750|15|Nominal Age & Cost|
|4.2|Kurtha and Pyjama|6|Girls|5,750|15|Age - Minimum|
|4.3|Kurtha and Pyjama|7|Girls|5,750|15|Age - Just above minimum|
|4.4|Kurtha and Pyjama|15|Girls|5,750|15|Age - Just below maximum|
|4.5|Kurtha and Pyjama|16|Girls|5,750|15|Age - Maximum|
|4.6|Kurtha and Pyjama|11|Girls|1,500|15|Cost - Minimum|
|4.7|Kurtha and Pyjama|11|Girls|1,501|15|Cost - Just above minimum|
|4.8|Kurtha and Pyjama|11|Girls|9,999|15|Cost - Just below maximum|
|4.9|Kurtha and Pyjama|11|Girls|10,000|15|Cost - Maximum|

---

### Discount Rule 5: Lehenga, Anarkali suit type of dresses (Age 6–16 years, Girls)

- **Parameters:** Type of Dress: Lehenga, Anarkali suit type of dresses, Gender: Girls
- **Age Range:** years
    - Min Age: 6, Min+ Age: 7, Nom Age: 11, Max- Age: 15, Max Age: 16
- **Cost Range:** [Rs. 1,000, Rs. 7,000]
    - Min Cost: 1,000, Min+ Cost: 1,001, Nom Cost: 4,000, Max- Cost: 6,999, Max Cost: 7,000
- **Expected Discount:** 12%

|Test Case #|Type of Dress|Age|Gender|Cost (Rs.)|Expected Discount (%)|Comment (BVA point varied)|
|:--|:--|:--|:--|:--|:--|:--|
|5.1|Lehenga, Anarkali suit type of dresses|11|Girls|4,000|12|Nominal Age & Cost|
|5.2|Lehenga, Anarkali suit type of dresses|6|Girls|4,000|12|Age - Minimum|
|5.3|Lehenga, Anarkali suit type of dresses|7|Girls|4,000|12|Age - Just above minimum|
|5.4|Lehenga, Anarkali suit type of dresses|15|Girls|4,000|12|Age - Just below maximum|
|5.5|Lehenga, Anarkali suit type of dresses|16|Girls|4,000|12|Age - Maximum|
|5.6|Lehenga, Anarkali suit type of dresses|11|Girls|1,000|12|Cost - Minimum|
|5.7|Lehenga, Anarkali suit type of dresses|11|Girls|1,001|12|Cost - Just above minimum|
|5.8|Lehenga, Anarkali suit type of dresses|11|Girls|6,999|12|Cost - Just below maximum|
|5.9|Lehenga, Anarkali suit type of dresses|11|Girls|7,000|12|Cost - Maximum|

---

### Discount Rule 6: Sherwani, Dhoti type dresses (Age 6–16 years, Boys)

- **Parameters:** Type of Dress: Sherwani, Dhoti type dresses, Gender: Boys
- **Age Range:** years
    - Min Age: 6, Min+ Age: 7, Nom Age: 11, Max- Age: 15, Max Age: 16
- **Cost Range:** [Rs. 1,000, Rs. 7,000]
    - Min Cost: 1,000, Min+ Cost: 1,001, Nom Cost: 4,000, Max- Cost: 6,999, Max Cost: 7,000
- **Expected Discount:** 10%

|Test Case #|Type of Dress|Age|Gender|Cost (Rs.)|Expected Discount (%)|Comment (BVA point varied)|
|:--|:--|:--|:--|:--|:--|:--|
|6.1|Sherwani, Dhoti type dresses|11|Boys|4,000|10|Nominal Age & Cost|
|6.2|Sherwani, Dhoti type dresses|6|Boys|4,000|10|Age - Minimum|
|6.3|Sherwani, Dhoti type dresses|7|Boys|4,000|10|Age - Just above minimum|
|6.4|Sherwani, Dhoti type dresses|15|Boys|4,000|10|Age - Just below maximum|
|6.5|Sherwani, Dhoti type dresses|16|Boys|4,000|10|Age - Maximum|
|6.6|Sherwani, Dhoti type dresses|11|Boys|1,000|10|Cost - Minimum|
|6.7|Sherwani, Dhoti type dresses|11|Boys|1,001|10|Cost - Just above minimum|
|6.8|Sherwani, Dhoti type dresses|11|Boys|6,999|10|Cost - Just below maximum|
|6.9|Sherwani, Dhoti type dresses|11|Boys|7,000|10|Cost - Maximum|

---

### Discount Rule 7: Kurtha and Pyjama (Age 17–30 years, Girls)

- **Parameters:** Type of Dress: Kurtha and Pyjama, Gender: Girls
- **Age Range:** years
    - Min Age: 17, Min+ Age: 18, Nom Age: 23, Max- Age: 29, Max Age: 30
- **Cost Range:** [Rs. 800, Rs. 15,000]
    - Min Cost: 800, Min+ Cost: 801, Nom Cost: 7,900, Max- Cost: 14,999, Max Cost: 15,000
- **Expected Discount:** 20%

|Test Case #|Type of Dress|Age|Gender|Cost (Rs.)|Expected Discount (%)|Comment (BVA point varied)|
|:--|:--|:--|:--|:--|:--|:--|
|7.1|Kurtha and Pyjama|23|Girls|7,900|20|Nominal Age & Cost|
|7.2|Kurtha and Pyjama|17|Girls|7,900|20|Age - Minimum|
|7.3|Kurtha and Pyjama|18|Girls|7,900|20|Age - Just above minimum|
|7.4|Kurtha and Pyjama|29|Girls|7,900|20|Age - Just below maximum|
|7.5|Kurtha and Pyjama|30|Girls|7,900|20|Age - Maximum|
|7.6|Kurtha and Pyjama|23|Girls|800|20|Cost - Minimum|
|7.7|Kurtha and Pyjama|23|Girls|801|20|Cost - Just above minimum|
|7.8|Kurtha and Pyjama|23|Girls|14,999|20|Cost - Just below maximum|
|7.9|Kurtha and Pyjama|23|Girls|15,000|20|Cost - Maximum|

---

### Discount Rule 8: Lehenga, Anarkali suit type of dresses (Age 17–30 years, Girls)

- **Parameters:** Type of Dress: Lehenga, Anarkali suit type of dresses, Gender: Girls
- **Age Range:** years
    - Min Age: 17, Min+ Age: 18, Nom Age: 23, Max- Age: 29, Max Age: 30
- **Cost Range:** [Rs. 2,000, Rs. 20,000]
    - Min Cost: 2,000, Min+ Cost: 2,001, Nom Cost: 11,000, Max- Cost: 19,999, Max Cost: 20,000
- **Expected Discount:** 25%

|Test Case #|Type of Dress|Age|Gender|Cost (Rs.)|Expected Discount (%)|Comment (BVA point varied)|
|:--|:--|:--|:--|:--|:--|:--|
|8.1|Lehenga, Anarkali suit type of dresses|23|Girls|11,000|25|Nominal Age & Cost|
|8.2|Lehenga, Anarkali suit type of dresses|17|Girls|11,000|25|Age - Minimum|
|8.3|Lehenga, Anarkali suit type of dresses|18|Girls|11,000|25|Age - Just above minimum|
|8.4|Lehenga, Anarkali suit type of dresses|29|Girls|11,000|25|Age - Just below maximum|
|8.5|Lehenga, Anarkali suit type of dresses|30|Girls|11,000|25|Age - Maximum|
|8.6|Lehenga, Anarkali suit type of dresses|23|Girls|2,000|25|Cost - Minimum|
|8.7|Lehenga, Anarkali suit type of dresses|23|Girls|2,001|25|Cost - Just above minimum|
|8.8|Lehenga, Anarkali suit type of dresses|23|Girls|19,999|25|Cost - Just below maximum|
|8.9|Lehenga, Anarkali suit type of dresses|23|Girls|20,000|25|Cost - Maximum|

---

### Discount Rule 9: Sherwani, Dhoti type dresses (Age 17–30 years, Boys)

- **Parameters:** Type of Dress: Sherwani, Dhoti type dresses, Gender: Boys
- **Age Range:** years
    - Min Age: 17, Min+ Age: 18, Nom Age: 23, Max- Age: 29, Max Age: 30
- **Cost Range:** [Rs. 2,000, Rs. 10,000]
    - Min Cost: 2,000, Min+ Cost: 2,001, Nom Cost: 6,000, Max- Cost: 9,999, Max Cost: 10,000
- **Expected Discount:** 15%

|Test Case #|Type of Dress|Age|Gender|Cost (Rs.)|Expected Discount (%)|Comment (BVA point varied)|
|:--|:--|:--|:--|:--|:--|:--|
|9.1|Sherwani, Dhoti type dresses|23|Boys|6,000|15|Nominal Age & Cost|
|9.2|Sherwani, Dhoti type dresses|17|Boys|6,000|15|Age - Minimum|
|9.3|Sherwani, Dhoti type dresses|18|Boys|6,000|15|Age - Just above minimum|
|9.4|Sherwani, Dhoti type dresses|29|Boys|6,000|15|Age - Just below maximum|
|9.5|Sherwani, Dhoti type dresses|30|Boys|6,000|15|Age - Maximum|
|9.6|Sherwani, Dhoti type dresses|23|Boys|2,000|15|Cost - Minimum|
|9.7|Sherwani, Dhoti type dresses|23|Boys|2,001|15|Cost - Just above minimum|
|9.8|Sherwani, Dhoti type dresses|23|Boys|9,999|15|Cost - Just below maximum|
|9.9|Sherwani, Dhoti type dresses|23|Boys|10,000|15|Cost - Maximum|

---

### Discount Rule 10: Kurtha and Pyjama (Age 17–30 years, Boys)

- **Parameters:** Type of Dress: Kurtha and Pyjama, Gender: Boys
- **Age Range:** years
    - Min Age: 17, Min+ Age: 18, Nom Age: 23, Max- Age: 29, Max Age: 30
- **Cost Range:** [Rs. 1,000, Rs. 15,000]
    - Min Cost: 1,000, Min+ Cost: 1,001, Nom Cost: 8,000, Max- Cost: 14,999, Max Cost: 15,000
- **Expected Discount:** 18%

|Test Case #|Type of Dress|Age|Gender|Cost (Rs.)|Expected Discount (%)|Comment (BVA point varied)|
|:--|:--|:--|:--|:--|:--|:--|
|10.1|Kurtha and Pyjama|23|Boys|8,000|18|Nominal Age & Cost|
|10.2|Kurtha and Pyjama|17|Boys|8,000|18|Age - Minimum|
|10.3|Kurtha and Pyjama|18|Boys|8,000|18|Age - Just above minimum|
|10.4|Kurtha and Pyjama|29|Boys|8,000|18|Age - Just below maximum|
|10.5|Kurtha and Pyjama|30|Boys|8,000|18|Age - Maximum|
|10.6|Kurtha and Pyjama|23|Boys|1,000|18|Cost - Minimum|
|10.7|Kurtha and Pyjama|23|Boys|1,001|18|Cost - Just above minimum|
|10.8|Kurtha and Pyjama|23|Boys|14,999|18|Cost - Just below maximum|
|10.9|Kurtha and Pyjama|23|Boys|15,000|18|Cost - Maximum| ---

---

8. Consider an application where email and password are used to login to the application. If the values of the email are **Blank / Valid / Invalid**, indicate how decisions can be taken up using **Decision Based Testing technique**.

Decision Based Testing (DBT) is a rigorous functional testing method that uses decision tables to represent and analyze complex logical relationships. It is particularly well-suited for situations where multiple conditions lead to a combination of specific actions or outcomes. For test case identification, conditions are interpreted as inputs, and actions are interpreted as outputs, with each rule (column) in the table representing a potential test case.

When considering a login application that uses email and password, decisions can be systematically determined using DBT by defining the relevant conditions, their possible states, and the corresponding actions.

### Conditions and States

For a login application, the primary inputs are email and password. Based on your query, the email can have three states: **Blank**, **Valid**, or **Invalid**. We can extend these states to the password as well, as its validity is equally critical for a successful login.

Let's define the conditions and their possible states for an Extended Entry Decision Table (EEDT):

- **Condition 1: Email Status**
    
    - **Valid**: The email adheres to a correct format (e.g., contains '@', a domain) and, if checked against a database, might correspond to an existing user.
    - **Invalid**: The email format is incorrect (e.g., missing '@', invalid characters) or it does not correspond to a registered user.
    - **Blank**: The email field is empty.
- **Condition 2: Password Status**
    
    - **Valid**: The password meets format requirements (e.g., minimum length, character types) and, when combined with a valid email, matches the registered password for that user.
    - **Invalid**: The password format is incorrect, or it does not match the registered password for a valid email/user.
    - **Blank**: The password field is empty.

### Actions/Outcomes

The actions represent the program's response based on the combination of input conditions. These typically include a successful login or various error messages. For robustness testing, it's important to define clear error messages, especially for invalid or unexpected inputs.

A common approach in login systems is to prioritize error messages, reporting the most critical issue first (e.g., a blank field before a format error). This also helps prevent information leakage (e.g., not distinguishing between "user does not exist" and "incorrect password"). Assuming a typical precedence where blank fields are checked first, then format, then credentials, the actions could be:

- **Action A1: Login Successful**
    - The user is granted access to the application.
- **Action A2: Error: "Email is blank"**
    - Displayed if the email field is empty.
- **Action A3: Error: "Password is blank"**
    - Displayed if the password field is empty (and email is not blank).
- **Action A4: Error: "Invalid Email format"**
    - Displayed if the email format is incorrect (and neither email nor password fields are blank).
- **Action A5: Error: "Incorrect Password"**
    - Displayed if the email is valid (i.e., exists and has a correct format) but the provided password does not match.

### Decision Table for Login Application

Using the conditions and actions defined above, we can construct the following decision table, which enumerates all nine possible combinations of Email Status and Password Status. Each column (rule) represents a distinct set of conditions leading to a specific action(s).

Here is your cleanly formatted **Login Validation Rule Table**:

---

### Login Validation Rules

|Rule #|R1|R2|R3|R4|R5|R6|R7|R8|R9|
|---|---|---|---|---|---|---|---|---|---|
|**Conditions**||||||||||
|Email Status|Valid|Valid|Valid|Invalid|Invalid|Invalid|Blank|Blank|Blank|
|Password Status|Valid|Invalid|Blank|Valid|Invalid|Blank|Valid|Invalid|Blank|
|**Actions**||||||||||
|A1: Login Successful|X|||||||||
|A2: Error: "Email is blank"|||||||X|X|X|
|A3: Error: "Password is blank"|||X|||X||||
|A4: Error: "Invalid Email format"||||X|X|X||||
|A5: Error: "Incorrect Password"||X||||||||

---

Would you like this rendered in HTML or exported as a CSV for use in a spreadsheet or app?

- **Interpretation of the Table**:
    - **R1 (Valid Email, Valid Password)**: Leads to successful login.
    - **R2 (Valid Email, Invalid Password)**: Email format is correct, but the password provided does not match, resulting in an "Incorrect Password" error.
    - **R3 (Valid Email, Blank Password)**: If the email is valid, but the password field is left empty, the "Password is blank" error is shown.
    - **R4, R5, R6 (Invalid Email)**: Regardless of the password's status (Valid, Invalid, or Blank), if the email format itself is invalid, the "Invalid Email format" error takes precedence.
    - **R7, R8, R9 (Blank Email)**: If the email field is blank, this error takes highest precedence, regardless of the password's status.

This table ensures that all possible combinations of the defined conditions are considered, contributing to "complete testing" for this aspect of the application's behavior.

### Deriving Test Cases

Each rule in the decision table provides a blueprint for constructing a concrete test case. To create a test case, specific values for the email and password inputs are chosen that satisfy the conditions outlined in each rule.

Here are the derived test cases:

1. **Test Case for R1 (Login Successful)**
    
    - **Input**: Email = "user@example.com", Password = "CorrectPassword123"
    - **Expected Output**: Login Successful
2. **Test Case for R2 (Incorrect Password)**
    
    - **Input**: Email = "user@example.com", Password = "WrongPasswordABC"
    - **Expected Output**: Error: "Incorrect Password"
3. **Test Case for R3 (Password is blank)**
    
    - **Input**: Email = "user@example.com", Password = ""
    - **Expected Output**: Error: "Password is blank"
4. **Test Case for R4 (Invalid Email format, Valid Password)**
    
    - **Input**: Email = "invalid-email", Password = "AnyValidPassword"
    - **Expected Output**: Error: "Invalid Email format"
5. **Test Case for R5 (Invalid Email format, Invalid Password)**
    
    - **Input**: Email = "invalid_email.com", Password = "Short"
    - **Expected Output**: Error: "Invalid Email format"
6. **Test Case for R6 (Invalid Email format, Blank Password)**
    
    - **Input**: Email = "email@.com", Password = ""
    - **Expected Output**: Error: "Invalid Email format"
7. **Test Case for R7 (Email is blank, Valid Password)**
    
    - **Input**: Email = "", Password = "AnyValidPassword"
    - **Expected Output**: Error: "Email is blank"
8. **Test Case for R8 (Email is blank, Invalid Password)**
    
    - **Input**: Email = "", Password = "Short"
    - **Expected Output**: Error: "Email is blank"
9. **Test Case for R9 (Email is blank, Blank Password)**
    
    - **Input**: Email = "", Password = ""
    - **Expected Output**: Error: "Email is blank"

### Nuances and Benefits of DBT

- **Completeness**: DBT ensures that all possible logical combinations of input conditions are considered, reducing the risk of overlooked scenarios.
- **Clarity on Behavior**: It provides a clear and unambiguous specification of the expected system behavior for each combination of inputs.
- **Robustness Testing**: By systematically including "Invalid" and "Blank" states for both email and password, DBT inherently supports robustness testing, forcing the application to handle unintended inputs gracefully with appropriate error messages.
- **Identification of Impossible Combinations**: While not explicitly marked as "impossible" in this EEDT, this method can also identify logically impossible or irrelevant combinations of conditions, helping to clarify requirements or identify potential defects in design.
- **Complementary to Other Techniques**: While DBT effectively covers logical relationships, other techniques like Boundary Value Analysis could be used to select specific values for "Valid" or "Invalid" states (e.g., very long valid emails, emails close to length limits for format validation).
- **Automation**: The structured nature of decision tables makes it straightforward to convert them into automated test scripts, enabling efficient execution and verification of results.

---
