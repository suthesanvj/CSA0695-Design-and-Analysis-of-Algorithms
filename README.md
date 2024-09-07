#include <stdio.h>

int factorial(int n) {
    if (n == 0)
        return 1;
    return n * factorial(n - 1);
}

int main() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    printf("Factorial of %d is %d.\n", num, factorial(num));

    printf("\n\n\nsuthesan vj   192210542\n");
    return 0;
}
![Screenshot 2024-09-07 152037](https://github.com/user-attachments/assets/bf10e85e-a8c4-41b6-b79e-a4cd40681e27)
