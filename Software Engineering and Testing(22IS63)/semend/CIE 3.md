
---

**1.** In how many ways can **structural testing** be conducted?  
Explain **any four** of such techniques along with stating their significance.  


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

**(OR)**

---

**4.** Explain the various methods used in **Object Oriented Testing** with suitable examples.  
**[10 marks]**

---

**5.** For the code given in **Question 3**, identify the **test cases** for verifying the **independent paths**.  
**[10 marks]**

---

**(OR)**

---

**6.** Explain **Regression Testing** along with its **different strategies**.  
**[10 marks]**

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

**[10 marks]**

---

**(OR)**

---

**8.** Explain **Prioritization** in Regression Testing with a suitable example.  
**[10 marks]**

---

Let me know if you'd like sample answers, Control Flow Graphs, DU pair analysis, or test case derivation!