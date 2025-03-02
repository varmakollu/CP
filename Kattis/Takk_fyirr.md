# Sigrún's Birthday Party - Thanking Guests

## Problem Statement  
Little Sigrún is celebrating her birthday today and is expecting many guests.  
She is very excited about receiving gifts, but her mother has reminded her to thank each guest.  
Can you help Sigrún in thanking everyone who brings a gift?

### Task  
Write a program that:  
1. Reads the number of guests (`n`).  
2. Reads `n` names, one per line.  
3. Prints a thank-you message for each guest in the format:  
   ```
   Takk name
   ```
   where `name` is the guest's name.

### Input  
- The first line contains an integer `n`, the number of guests.  
- The next `n` lines each contain a guest's name.  
- The names only contain English letters and have no spaces.

### Output  
For each guest, print a single line in the following format:  
```
Takk name
```

### Constraints  
- No additional constraints are given.  
- Ensure the output format exactly matches the required format.

---

### Example

#### **Input**  
```
3
Arnar
Bjarki
Bernhard
```

#### **Output**  
```
Takk Arnar
Takk Bjarki
Takk Bernhard
```

---

## Solution Approach  
1. **Read the number of guests** (`n`).  
2. **Loop `n` times** to read each guest's name.  
3. **Print the thank-you message** using the format `"Takk name"`.  
4. Ensure correct capitalization and spacing in the output.

---

## Solution in C  
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);  // Read number of guests

    char name[101];  // Assuming max name length is 100 characters
    for (int i = 0; i < n; i++) {
        scanf("%s", name);  // Read the guest's name
        printf("Takk %s\n", name);  // Print the thank you message
    }

    return 0;
}
```

---

## Solution in Python  
```python
# Read the number of guests
n = int(input())

# Loop through the names and print the thank you message
for _ in range(n):
    name = input().strip()  # Read the guest's name
    print(f"Takk {name}")   # Print the thank you messages
```
