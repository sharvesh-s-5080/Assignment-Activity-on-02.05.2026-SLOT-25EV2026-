# Assignment-Activity-on-02.05.2026-SLOT-25EV2026


1. Write a c program to print all prime numbers between two limits.
```
#include <stdio.h>

int main() {
    int lower, upper, i, j, isPrime;
    scanf("%d %d", &lower, &upper);

    for (i = lower; i <= upper; i++) {
        if (i <= 1)
            continue;

        isPrime = 1;

        for (j = 2; j < i; j++) {
            if (i % j == 0) {
                isPrime = 0;
                break;
            }
        }

        if (isPrime == 1)
            printf("%d ", i);
    }

    return 0;
}

```
2. Write a c program to count the number of digits in a number.
```
#include <stdio.h>

int main() {
    int num, count = 0;
    scanf("%d", &num);

    if (num == 0)
        count = 1;

    while (num != 0) {
        num = num / 10;
        count++;
    }

    printf("Number of digits = %d", count);

    return 0;
}
```
3. Write a c program to print the alphabet S in n x n matrix.
```
#include <stdio.h>

int main() {
    int n, i, j;
    scanf("%d", &n);

    for(i = 0; i < n; i++) {
        for(j = 0; j < n; j++) {

            if(i == 0 || i == n/2 || i == n-1 || 
               (j == 0 && i < n/2) || 
               (j == n-1 && i > n/2))
                printf("*");
            else
                printf(" ");
        }
        printf("\n");
    }

    return 0;
}
```
4. Write a c program to print the pyramid pattern.

    *

  ***

 *****

*******
```
#include <stdio.h>

int main() {
    int n, i, j;
    scanf("%d", &n);

    for(i = 1; i <= n; i++) {

        // spaces
        for(j = 1; j <= n - i; j++)
            printf(" ");

        // stars
        for(j = 1; j <= (2*i - 1); j++)
            printf("*");

        printf("\n");
    }

    return 0;
}
```
5. Write a c program to find GCD of two numbers using loop.
```
#include <stdio.h>

int main() {
    int a, b, i, gcd = 1;

    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    for(i = 1; i <= a && i <= b; i++) {
        if(a % i == 0 && b % i == 0) {
            gcd = i;
        }
    }

    printf("GCD = %d", gcd);

    return 0;
}
```
