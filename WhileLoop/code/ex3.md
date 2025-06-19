**Example Solution:**

```c
#include <stdio.h>

int main(void) {
    int i = 1;
    int sum = 0;
    while (i <= 10) {
        sum += i;
        i++;
    }
    printf("Sum of 1 to 10 is %d\n", sum);
    return 0;
}
