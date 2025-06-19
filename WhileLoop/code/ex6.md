**Example Solution:**

```c
#include <stdio.h>

int main(void) {
    int N;
    printf("Enter the number of Fibonacci terms: ");
    scanf("%d", &N);

    int a = 0, b = 1, temp;
    int i = 1;
    while (i <= N) {
        printf("%d ", a);
        temp = a + b;
        a = b;
        b = temp;
        i++;
    }
    printf("\n");
    return 0;
}

**Sample Run**

```bash
Enter the number of Fibonacci terms: 7
0 1 1 2 3 5 8 
