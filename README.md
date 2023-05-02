#include <stdio.h>

int power(int x, int n);

int main() {
    int x, n;

    printf("Enter the base value (x): ");
    scanf("%d", &x);

    printf("Enter the power value (n): ");
    scanf("%d", &n);

    if (n > 5) {
        printf("Error: n should be less than or equal to 5\n");
        return 1;
    }

    printf("%d raised to the power of %d is %d\n", x, n, power(x, n));

    return 0;
}

int power(int x, int n) {
    if (n == 0) {
        return 1;
    } else {
        return x * power(x, n - 1);
    }
}
