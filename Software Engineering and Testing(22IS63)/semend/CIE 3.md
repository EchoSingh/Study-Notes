
---

**1.** In how many ways can **structural testing** be conducted?  
Explain **any four** of such techniques along with stating their significance.  

Structural testing, also known as white-box or clear-box testing, is a fundamental approach to test case identification where the implementation of the software (its source code) is known and used to identify tests. It focuses on _how_ the program is actually implemented. This approach lends itself to defining and using test coverage metrics, which explicitly measure the extent to which a software item has been tested.

Structural testing can be conducted in numerous ways, typically categorized by the specific aspects of the code that are targeted for coverage. These techniques fall under code-based test generation. The methods available include:

- **Control flow-based criteria**: These focus on covering different execution paths and logic within the program. Examples include statement coverage, block coverage, condition coverage, decision coverage, condition/decision coverage, multiple condition coverage, Linear Code Sequence and Jump (LCSAJ) coverage, and Modified Condition/Decision Coverage (MC/DC).
- **Data flow-based criteria**: These techniques focus on the points where variables are defined and used within the program.
- **Path testing**: This method involves identifying and testing specific paths through the program's control flow graph.
- **Mutation testing**: This technique assesses test adequacy by injecting faults into the program's code.
- **Slice testing**: This approach focuses on program slices to identify relevant code for testing.

Here are explanations of four structural testing techniques and their significance:

1. **Decision Coverage**
    
    - **Explanation**: Decision coverage is a control flow-based test adequacy criterion that ensures each decision (or branch) in the program has taken all possible outcomes at least once. For example, in an `if` statement, both the "true" and "false" branches must be executed. Similarly, for a `switch` statement, all possible outcomes or cases implied by its decisions should be covered.
    - **Significance**: This technique is crucial for covering different execution paths influenced by conditional logic, helping to reveal errors in the program's decision-making processes. It aims to ensure that no part of the program's conditional logic is left untested.
2. **Modified Condition/Decision Coverage (MC/DC)**
    
    - **Explanation**: MC/DC is a stringent control flow-based adequacy criterion that requires showing that each simple condition within a compound condition independently affects the outcome of the decision. This means for a compound condition like `(A AND B) OR C`, tests must demonstrate that varying A, B, or C individually changes the overall outcome of the condition while other simple conditions are held constant. MC/DC requires fewer tests than multiple condition coverage, which aims to cover all combinations of simple conditions (which can grow exponentially). A systematic procedure can be used to derive MC/DC adequate tests for compound conditions.
    - **Significance**: MC/DC is particularly important for safety-critical systems and is often mandated by standards from organizations like the Federal Aviation Authority and the US Department of Defense. It forces a thorough examination of complex logical expressions and is effective at detecting errors such as missing simple conditions or incorrect Boolean operators within compound conditions. The number of tests required for MC/DC grows linearly with the number of simple conditions, making it more practical for large applications than multiple condition coverage.
3. **Basis Path Testing**
    
    - **Explanation**: Basis path testing is a structural testing technique based on graph theory, specifically leveraging the cyclomatic complexity of a program's control flow graph (CFG). Cyclomatic complexity, defined as V(G) = e - n + p (where e is edges, n is nodes, and p is components in the graph), provides the number of linearly independent paths that form a basis set for all possible execution paths in a program. The method involves drawing the program's CFG, calculating its cyclomatic complexity, generating a set of basis paths equal to this complexity, and then deriving test cases to execute each of these paths.
    - **Significance**: This technique offers a quantifiable lower bound on the number of test cases required for thorough structural testing, ensuring that a fundamental set of program behaviors is exercised. By focusing on these independent paths, it aims to uncover faults associated with the control flow logic of the program and helps in understanding the program's complexity.
4. **Mutation Testing**
    
    - **Explanation**: Mutation testing is a robust technique used to assess the adequacy of an existing test set and enhance its fault-detection capabilities. It operates by systematically creating "mutants" of the original program by injecting small, syntactically defined faults using predefined "mutation operators". The current test set is then executed against these mutants. If a test case produces a different output from a mutant compared to the original program, that mutant is "killed" (distinguished). A "mutation score" (ratio of killed mutants to total non-equivalent mutants) is calculated. If the score is low, additional test cases are generated to "kill" the remaining "live" mutants, thereby improving the test set's effectiveness.
    - **Significance**: Mutation testing provides a powerful measure of a test set's "goodness" by directly evaluating its fault-detection ability. It compels testers to design highly specific test cases that target subtle errors, often leading to the discovery of complex faults that might otherwise be missed. It can be applied at various levels of testing, including unit, integration, and system testing.

---

**2.** Explain the **Top Down approach** of Integration Testing with a suitable example.  

The **Top-Down approach** is an integration testing strategy where components are integrated and tested starting from the top of the software's functional hierarchy and moving downwards. This method begins with the main program or the highest-level modules, and progressively integrates lower-level modules.

**Explanation of the Approach:**

1. **Starting Point**: Top-down integration begins with the main program, which is considered the root of the functional decomposition tree.
2. **Use of Stubs**: Any lower-level units or modules that are called by the main program (or higher-level modules) are initially replaced by "stubs". Stubs are temporary, throwaway pieces of code designed to emulate the expected behavior of the called, but not yet integrated, lower-level units. For instance, a stub might simply return a hard-coded correct response when invoked.
3. **Incremental Integration**: The process involves integrating one lower-level unit at a time. After a unit is replaced by its actual code, the system (with the newly integrated component) is retested. This continues in a stepwise manner, often following a breadth-first traversal of the decomposition tree, until all stubs have been replaced by their actual code.
4. **Testing Focus**: The initial testing steps aim to verify the correctness of the main program's functionality, or the functionality of the integrated higher-level components. As new components are integrated, the focus shifts to ensuring that the interfaces and interactions between the newly added component and the existing integrated system function as desired.

**Significance and Characteristics:**

- **Fault Isolation**: A key advantage of top-down integration is its strong fault isolation capability. If a test fails after a new stub has been replaced by the actual code, the fault is highly suspected to be within the newly integrated unit or its interface with the calling module.
- **Early System Demonstration**: This approach allows for a "partially working system" or a "skeleton system" to be available early in the development cycle. This can be beneficial for demonstrating core functionalities to potential customers or stakeholders before the entire system is complete.
- **Stub Development Effort**: A significant drawback is the considerable effort and cost involved in developing numerous stubs, especially for complex systems with many dependencies. These stubs often need to be maintained under configuration management.
- **"Impossible Interfaces"**: Functional decomposition, which often forms the basis for top-down integration, can sometimes lead to "impossible interfaces." This occurs when higher-level modules, according to the decomposition, are not intended to directly call certain lower-level units, leading to nonsensical or empty test sessions.
- **Retesting Effort**: Each incremental integration often necessitates retesting, which can add to the overall testing effort.

**Example: Integration of the `NextDate` Program**

Consider a program like `integrationNextDate`, which handles date calculations and related functionalities, decomposed into various functions and procedures.

1. **Initial Setup**: In a top-down integration for `integrationNextDate`, the testing would begin with the `Main` program (the highest-level component).
2. **Stub Creation**: Stubs would be created for all functions that `Main` directly or indirectly calls, such as `getDate`, `printDate`, `incrementDate`, `isValidDate`, `lastDayOfMonth`, and `isLeap`. For example, the `getDateStub` might be programmed to return a fixed date like "May 27, 2013", and `zodiacStub` might return "Gemini".
3. **Initial Testing**: The `Main` program's logic would be tested first using these stubs, verifying its overall flow and interaction with its immediate dependencies.
4. **Progressive Replacement**: After the `Main` program is deemed correct, one stub, for example, `getDate`, would be replaced by its actual implementation. The system would then be retested to ensure the `getDate` function integrates correctly and the `Main` program still behaves as expected. This process would continue by replacing other stubs (e.g., `incrementDate`, `printDate`) one by one.
5. **Challenge**: A specific issue highlighted by the sources for this example is that certain functions like `isLeap` or `weekDay` (which might be deep within the call hierarchy, as shown in Figure 13.14 of source) are never directly called by the `Main` program in a strict functional decomposition. This means that designing meaningful pairwise integration tests based on a pure decomposition tree can become problematic for these deeper components.

---

**3.**  
For the code given below, construct the **Control Flow Graph (CFG)** and describe the **cases of each node**:

```cpp
#include <bits/stdc++.h>
using namespace std;
int N;
int A[100];
int main() {
    for(int i = 0; i < 3; i++)
        scanf("%d", A + i);
    int a, b = 0, c = 0;
    for(int i = 0; i < 3; i++) {
        scanf("%d", &a);
        if(a > A[i])
            c++;
        else if(a < A[i])
            b++;
    }
    printf("%d %d\n", b, c);
    return 0;
}
```

![](images/cie3.svg)

|Node|Code|Case|
|---|---|---|
|**Start**|_Entry point_|**Distinguished Node**|
|**Block 1**|`int i = 0;` _(implicit in for-loop init)_|**Computation Block**|
|**Block 2**|`i < 3`|**Decision Block**|
|**Block 3**|`scanf("%d", A + i);`|**Computation Block**|
|**Block 4**|`i++` (part of loop structure)|**Computation Block**|
|**Block 5**|`int a, b = 0, c = 0; int i = 0;`|**Computation Block**|
|**Block 6**|`i < 3` _(second for-loop condition)_|**Decision Block**|
|**Block 7**|`scanf("%d", &a);`|**Computation Block**|
|**Block 8**|`if (a > A[i])`|**Decision Block**|
|**Block 9**|`c++;`|**Computation Block**|
|**Block 10**|`else if (a < A[i])`|**Decision Block**|
|**Block 11**|`b++;`|**Computation Block**|
|**Block 12**|_(Join node after if-else-if)_|**Join Block**|
|**Block 13**|`i++` (increment for second loop)|**Computation Block**|
|**Block 14**|`printf("%d %d", b, c);`|**Computation Block**|
|**Block 15**|`return 0;`|**Computation Block**|
|**End**|_Exit point_|**Distinguished Node**|

---

**4.** Explain the various methods used in **Object Oriented Testing** with suitable examples.  

Object-Oriented (OO) testing involves methods for assessing and enhancing tests specifically designed for software developed using an object-oriented paradigm. While many traditional testing techniques apply, OO software introduces unique challenges due to concepts like encapsulation, inheritance, polymorphism, and dynamic binding.

Here are various methods used in Object-Oriented Testing:

**1. Levels of Object-Oriented Testing** Testing activities in OO development often occur at several distinct levels, building upon each other:

- **Operation/Method Testing:** If individual operations or methods are considered units, this level is similar to traditional unit testing of procedural software.
- **Class Testing:** This involves testing individual classes, which are collections of objects and object classes that operate together. When classes are considered units, it raises questions about how to test inherited attributes and operations.
- **Integration Testing:** This phase focuses on testing interactions between previously tested classes or components. It is considered the major issue in OO testing due to complexities like polymorphism and message passing.
- **System Testing:** This highest level evaluates the entire system against its requirements, often independent of its implementation language (OO or procedural).

**2. Unit Testing for Object-Oriented Software** Unit testing ensures that each program unit functions as desired. A "unit" can be a class or a collection of classes, or a function/method.

- **Methods as Units:** When individual methods are treated as units, traditional specification-based and code-based testing techniques are directly applicable. This simplifies unit testing but shifts a greater burden onto integration testing.
- **Classes as Units:** This is a common choice. However, it can be challenging because classes encapsulate inherited attributes and operations.
    - **"Flattened Classes"**: One approach is to create "flattened classes" that include all inherited attributes and operations, allowing them to be tested as stand-alone units.
    - **Special-Purpose Test Methods**: Adding special test methods facilitates class-as-unit testing, but these methods should not be part of the delivered system.

**Techniques Applicable at the Unit Level:**

- **Specification-Based Techniques**: These methods derive tests from functional requirements without needing to know the internal code.
    
    - **Equivalence Partitioning and Boundary Value Analysis**: These fundamental techniques partition input domains into subsets (equivalence classes) and focus on values at the boundaries to identify test cases. For example, in the "NextDate" function, test cases involving specific dates like February 28/29 or leap years would be special values derived from domain knowledge. For the "Triangle Problem," test cases like (5,5,5) for an equilateral triangle would be derived using equivalence partitioning.
    - **Decision Table-Based Testing**: These methods are rigorous due to their strong logical basis, especially useful where complex logical relationships exist among input variables.
- **Code-Based (Structural) Testing Techniques**: These methods use the source code to identify test cases and assess test quality.
    
    - **Path Testing**: Aims to exercise independent execution paths through a component. This includes metrics like statement coverage and decision (branch) coverage. For object-oriented languages, path testing may be used for methods associated with objects.
    - **Data Flow Testing**: Focuses on points where variables receive values (definitions) and where these values are used. It defines define/use paths (du-paths) and can reveal faults that path testing might miss. For OO code, data flow testing extends to the integration level due to inheritance, dynamic binding, and message passing.
    - **Program Mutation (Mutation Testing)**: A powerful white-box technique for assessing the "goodness" of test sets and enhancing inadequate ones. It involves creating "mutants" (versions of the program with small, syntactic changes) and checking if the test suite can "kill" (detect) them. Mutation operators exist for object-oriented languages like Java, including those related to inheritance, polymorphism, dynamic binding, and method overloading. For example, the OMR operator forces a tester to generate tests that distinguish overloaded methods by replacing the body of one with another.
- **Test-Driven Development (TDD)**: In TDD, tests are written _before_ the code. The developer writes a small test for new functionality, runs it (it fails), then writes just enough code to make the test pass, and reruns all tests. This tight "test a little, code a little" cycle aims for excellent fault isolation.
    
    - **JUnit**: Tools like JUnit automate the execution of unit tests for Java programs. It allows grouping multiple tests into a class and automatically executes them, reporting pass/fail outcomes.
    - **Mock Objects**: Used when the unit under test depends on other unavailable or slow objects. A mock object simulates the behavior of the real object, allowing the unit to be tested in isolation. Tools like EasyMock automate the creation and management of mock objects, facilitating "behavior verification" (checking interactions with the server) as opposed to just "state verification" (checking return values).

**3. Integration Testing for Object-Oriented Software** This phase aims to find errors arising from communication among integrated components. It presumes units have been independently tested.

- **UML Support**: Collaboration and sequence diagrams in UML are used as a basis for integration testing by showing message traffic and interactions among classes.
- **MM-Paths**: Object-Oriented MM-paths are defined as a sequence of method executions linked by messages. They serve as an integration testing analog to DD-paths, providing a detailed view of potential message flows. For example, in the `ooCalendar` application, an MM-path would trace the sequence of method calls and messages triggered by a specific date increment, ensuring every message (edge) in the call graph is traversed.
- **Integration Strategies and Test Order Algorithms**: Given that finding an optimal integration sequence is NP-complete, several methods aim to find a near-optimal order, minimizing stub count and/or retesting costs. Examples include the Tai-Daniels (TD) method, Traon-Jéron-Jézéquel-Morel (TJJM) method, and Briand-Labiche-Wang (BLW) method. These methods take an Object Relation Diagram (ORD) as input, which captures the dependence among components.

**4. System Testing for Object-Oriented Software** System testing is performed from a specification-based standpoint, focusing on evaluating the product against user expectations rather than finding faults.

- **UML-Based System Testing**: For GUI applications, system-level test cases can be derived from various UML models such as Use Cases and StateCharts. Use cases are central as they are easily understood by both customers and developers and capture the "what a system does" view.
- **Atomic System Functions (ASFs)**: System-level behavior can be viewed in terms of threads, which are sequences of ASFs. ASFs have port events as their inputs and outputs, providing a unifying view across testing levels.
- **Nonfunctional System Testing**: This assesses "how well" a system performs its functional requirements, covering aspects like reliability, maintainability, scalability, and usability. Common forms include stress testing (performance, capacity, load testing), which involves subjecting the system to extreme loads to find weaknesses.

**Complexity Metrics for OO Software** Metrics specific to OO software, such as Weighted Methods per Class (WMC), Depth of Inheritance Tree (DIT), Number of Child Classes (NOC), Coupling Between Classes (CBO), and Response for Class (RFC), are used to measure program or design complexity. These metrics are relevant to testing because more complex designs often require greater testing effort.

---

**5.** For the code given in **Question 3**, identify the **test cases** for verifying the **independent paths**.  


---

**6.** Explain **Regression Testing** along with its **different strategies**.  

---

**7.**  
For the piece of code given below, identify the **Definition-Use (DU) pairs** for all the variables:

```c
#include <stdio.h>
int main() {
    int n, count, sum = 0;
    printf("Enter the value of n (positive integer):");
    scanf("%d", &n);
    for(count = 1; count <= n; count++) {
        sum = sum + count;
    }
    printf("Sum of first %d natural numbers is: %d", n, sum);
    return 0;
}
```


---

**8.** Explain **Prioritization** in Regression Testing with a suitable example.  
