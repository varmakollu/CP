# Kveðja - Email Signature Generator

## Problem Statement  
Mirko is developing an email client and needs to implement a feature that automatically adds a signature at the end of emails.  
Your task is to help Mirko by writing a program that prints a signature based on the sender's name.

## Platform : [Kattis](https://open.kattis.com/problems/kvedja)

### Task  
Write a program that:  
1. Reads the sender's name from input.  
2. Prints `"Kvedja,"` on one line.  
3. Prints the sender’s name on the next line.

### Input  
- A single line containing the sender's name.  
- The name consists of uppercase and lowercase English letters.  

### Output  
- Print `"Kvedja,"` on the first line.  
- Print the sender’s name on the second line.

---

## Examples  

### **Example 1**  

#### **Input**  
```
Slavko
```

#### **Output**  
```
Kvedja,
Slavko
```

---

## Solution Approach  
1. Read the sender’s name as input.  
2. Print the fixed phrase `"Kvedja,"` on the first line.  
3. Print the sender’s name exactly as it was given on the second line.  
4. Ensure correct capitalization and formatting.

---

## Solution in C  
```c
#include <stdio.h>

int main() {
    char name[101];  // Assuming the name is at most 100 characters
    scanf("%100s", name);  // Read the sender's name
    printf("Kvedja,\n%s\n", name);  // Print the signature format
    return 0;
}
```

---

## Solution in Python  
```python
# Read the sender's name
name = input().strip()

# Print the signature
print("Kvedja,")
print(name)
```
