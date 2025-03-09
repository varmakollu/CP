# **Reduplication**  

## **Problem Statement**  
Reduplication is when a word is repeated multiple times, often to emphasize or modify its meaning. Rama frequently uses reduplication while chatting but finds it time-consuming to type the same word repeatedly. Instead, he writes the word once, followed by a number indicating how many times it should be repeated.  

Your task is to write a program that reads a word and a number, then outputs the word repeated the specified number of times.  

---
## Platform : [Kattis](https://open.kattis.com/problems/reduplikation)

---

## **Input**  
- The first line contains a string `word` (1 ≤ length ≤ 100), consisting of lowercase letters (`a-z`).  
- The second line contains a single digit `n` (1 ≤ n ≤ 9), representing how many times to repeat the word.  

---

## **Output**  
- Print the word concatenated `n` times in a single line without spaces.  

---

## **Constraints**  
- The length of `word` is between 1 and 100.  
- The integer `n` is between 1 and 9.  

---

## **Examples**  

| Input | Output |
--------|---------
| hej 3 | hejhejhej |
|ha 4 | hahahaha|

---

## **Solution Approach**  
1. **Read the word** from input.  
2. **Read the integer** (number of times the word should be repeated).  
3. **Concatenate the word** `n` times and print the result.  

---

## **Code Implementation**  

### **C Code**  
```c
#include <stdio.h>

int main() {
    char word[101]; // Max length 100
    int n;

    scanf("%s", word);  // Read the word
    scanf("%d", &n);    // Read the repetition count

    for (int i = 0; i < n; i++) {
        printf("%s", word);  // Print the word n times
    }
    printf("\n");  // New line for clean output

    return 0;
}
```

### **Python Code**  
```python
# Read the input word
word = input().strip()

# Read the repetition count and convert it to an integer
n = int(input().strip())

# Print the word repeated n times
print(word * n)
```

---

## **Complexity Analysis**  
- **Time Complexity:** \(O(n)\) (Repeating the word `n` times)  
- **Space Complexity:** \(O(1)\) (Constant space usage)  
