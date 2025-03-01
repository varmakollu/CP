# Forritunarkeppni Framhaldsskólanna Anniversary Celebration

## Platform : [Kattis](https://open.kattis.com/problems/hipphipp)
## Problem Statement  
The Forritunarkeppni Framhaldsskólanna programming contest was first held in the year 2001. This year, it is celebrating its 20th anniversary! To mark this occasion, we want to print a congratulatory message.  

### Task  
Write a program that prints the phrase **"Hipp hipp hurra!"** exactly 20 times, each on a new line.

### Input  
There is no input for this problem.

### Output  
Print the phrase **"Hipp hipp hurra!"** exactly 20 times, each on a separate line.

## Examples  
### Example Output  
```
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
Hipp hipp hurra!  
```

## Solution Approach  
1. Use a loop to iterate 20 times.  
2. In each iteration, print `"Hipp hipp hurra!"` followed by a newline.  
3. Since there is no input, the program simply executes and prints the required output.  

---

## Solution in C  
```c
#include <stdio.h>

int main() {
    for (int i = 0; i < 20; i++) {
        printf("Hipp hipp hurra!\n");
    }
    return 0;
}
```

---

## Solution in Python  
```python
for _ in range(20):
    print("Hipp hipp hurra!")
```

Both solutions use a loop to print the phrase 20 times efficiently.
