# Tölvunarfræðingar telja (Computer Scientists Count)

## **Problem Statement**
Computer scientists count differently from normal people. Instead of starting from `1`, they start from `0`. Therefore, the `n`-th number in computer science counting is `n - 1`.

## Platform : [Kartis](https://open.kattis.com/problems/tolvunarfraedingartelja)

## **Input**
- A single integer `n` (1 ≤ n ≤ 10⁹).

## **Output**
- Print the `n`-th number according to computer science counting (i.e., `n - 1`).

## **Constraints**
- `n` is a positive integer.
- The output should be an integer.

## **Examples**
| Input    | Output |
| -------- | ------- |
| 1  | 0    |
| 2 | 1 |
| 1337 | 1336 |
---

## **Solution Approach**
- Since computer scientists start counting from `0` instead of `1`, we simply **subtract 1** from the input `n`.
- This operation runs in **O(1) time complexity**, as it only involves a single arithmetic operation.

---

## **Code Implementation**

### **C Code**
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);  // Read the input integer
    printf("%d\n", n - 1);  // Print the (n-1)th number
    return 0;
}
```

### **Python Code**
```python
# Read the input integer
n = int(input().strip())

# Print the (n-1)th number
print(n - 1)
```
