# Mary and Flowers

---

## Platform : [Unstop](https://unstop.com/code/practice/250137)
---

## **Problem Statement**
Mary wants to create a bouquet of flowers for her friend. She needs exactly **2 types of flowers**, and the total number of flowers required is `t`. Her garden contains `N` types of flowers, each arranged in a queue in **non-decreasing order**. Mary seeks your help to determine the **zero-based indices** of the two flowers she should collect such that their sum equals `t`.

### **Key Notes**:
1. There will always be at least one valid pair of flowers whose sum equals `t`.
2. If multiple pairs exist, select the **first occurrence**.

---

## **Input**
1. The first line contains two integers:
   - `N`: The total number of flower types.
   - `t`: The total number of flowers needed.
2. The second line contains `N` integers (`a1, a2, ..., an`), representing the number of flowers of each type.

### **Constraints**:
- $ 2 \leq N \leq 10^4 $
- $ 1 \leq a[i] \leq 10^3 $
- $ 2 \leq t \leq 2 \times 10^3 $

---

## **Output**
Print the **zero-based indices** of the two flowers that sum up to `t`. The first index should be smaller than the second index.

---

## **Solution Approach**
The problem can be solved efficiently using the **two-pointer technique** due to the array being sorted in non-decreasing order. Here's the step-by-step approach:

1. **Initialize Two Pointers**:
   - Start with one pointer (`left`) at the beginning of the array (index `0`).
   - Start another pointer (`right`) at the end of the array (index `N-1`).

2. **Iterate Until the Pointers Meet**:
   - Calculate the sum of the elements at the `left` and `right` pointers.
   - If the sum equals `t`, return the indices `(left, right)`.
   - If the sum is less than `t`, increment the `left` pointer to increase the sum.
   - If the sum is greater than `t`, decrement the `right` pointer to decrease the sum.

3. **Efficiency**:
   - Time Complexity: **O(N)** since each pointer moves at most `N` steps.
   - Space Complexity: **O(1)** as no additional data structures are used.

---

## **C Code**

```c
#include <stdio.h>

void find_flower_indices(int N, int t, int a[]) {
    // Initialize two pointers
    int left = 0, right = N - 1;
    
    // Iterate until the pointers meet
    while (left < right) {
        int current_sum = a[left] + a[right];
        
        if (current_sum == t) {
            // Print the indices as zero-based
            printf("%d %d\n", left, right);
            return;
        } else if (current_sum < t) {
            // Move the left pointer to increase the sum
            left++;
        } else {
            // Move the right pointer to decrease the sum
            right--;
        }
    }
}

int main() {
    int N, t;
    scanf("%d %d", &N, &t);
    
    int a[N];
    for (int i = 0; i < N; i++) {
        scanf("%d", &a[i]);
    }
    
    // Find and print the result
    find_flower_indices(N, t, a);
    
    return 0;
}
```

---

## **Python Code**

```python
def find_flower_indices(N, t, a):
    # Initialize two pointers
    left, right = 0, N - 1
    
    # Iterate until the pointers meet
    while left < right:
        current_sum = a[left] + a[right]
        
        if current_sum == t:
            # Return the indices as zero-based
            return left, right
        elif current_sum < t:
            # Move the left pointer to increase the sum
            left += 1
        else:
            # Move the right pointer to decrease the sum
            right -= 1

# Input reading
N, t = map(int, input().split())
a = list(map(int, input().split()))

# Find and print the result
result = find_flower_indices(N, t, a)
print(result[0], result[1])
```

---

## **Sample Test Case**

### **Input**:
```
7 5
1 2 2 4 5 7 10
```

### **Output**:
```
0 3
```

### **Explanation**:
The sum of flowers at index `0` and index `3` is `1 + 4 = 5`, which matches the required total number of flowers needed.

---

## **Conclusion**
This problem demonstrates the power of the two-pointer technique for solving problems on sorted arrays. The solution is efficient, with a time complexity of **O(N)**, making it suitable for large inputs within the given constraints.
