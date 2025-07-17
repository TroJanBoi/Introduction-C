# While Loop in C

A **while loop** repeatedly executes a block of code as long as a given condition remains true. It is useful when you don’t know in advance how many times you need to iterate.

---

## 📝 Syntax

```c
while (condition) {
    // statements to be executed repeatedly
}
```

- **condition**: An expression that evaluates to true (non-zero) or false (zero).
- The loop body executes **only if** `condition` is true.
- Before each iteration, `condition` is checked. When it becomes false, the loop stops.

---

## 🔄 Flowchart

```
     ┌───────────────┐
     │ Evaluate cond │─────┐
     └───────────────┘     │
           ▲               │
           │ true          │
           │               ▼
     ┌───────────────┐  ┌───────────────┐
     │  Execute body │─▶│ Re-evaluate   │
     └───────────────┘  │   condition   │
                        └───────────────┘
                             │
                             │ false
                             ▼
                       ┌───────────┐
                       │  Exit     │
                       └───────────┘
```

---

## 💡 Example: Counting from 1 to 5

```c
#include <stdio.h>

int main(void) {
    int i = 1;               // Initialize counter

    while (i <= 5) {         // Loop as long as i is ≤ 5
        printf("%d", i);   // Print current value of i
        i++;                 // Increment counter
    }

    return 0;
}
```

**Output:**
```
1
2
3
4
5
```

---

## ⚠️ Common Pitfalls

1. **Infinite loop**  
   Forgetting to update the loop variable inside the body can cause the condition to remain true forever:
   ```c
   int i = 1;
   while (i <= 5) {
       printf("%d
", i);
       // missing i++;
   }
   // This will never terminate!
   ```

2. **Off-by-one errors**  
   Be careful with the comparison operator (`<`, `<=`, `>`, `>=`) to ensure you iterate the correct number of times.

---

## 🤔 While vs. Do-While

| Feature              | while                           | do-while                       |
|----------------------|---------------------------------|--------------------------------|
| Condition first?     | Yes                             | No                             |
| Executes at least 1×? | Only if condition is true       | Always executes body once      |
| Usage example        | Read input until EOF            | Display menu then repeat until choice = exit |

```c
// do-while example
int choice;
do {
    printf("Enter 0 to exit: ");
    scanf("%d", &choice);
} while (choice != 0);
```

---

## ✅ Best Practices

- **Initialize** loop variables before entering the loop.
- **Update** variables in the loop body to move toward the exit condition.
- Keep the loop body **simple**—if it grows complex, consider refactoring.
- Use comments to explain non-obvious parts of the loop.

---

## 📚 Further Reading

- [The C Programming Language (K&R)](https://en.wikipedia.org/wiki/The_C_Programming_Language)  
- [while loop – GeeksforGeeks](https://www.geeksforgeeks.org/while-loop-in-c/)

---
