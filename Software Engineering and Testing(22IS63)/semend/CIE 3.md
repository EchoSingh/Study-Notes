
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



---

**4.** Explain the various methods used in **Object Oriented Testing** with suitable examples.  

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
