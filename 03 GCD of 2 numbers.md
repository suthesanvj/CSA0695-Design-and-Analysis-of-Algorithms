#include <stdio.h>

int gcd(int a, int b) {
    if (b == 0)
        return a;
    return gcd(b, a % b);
}

int main() {
    int num1, num2;
    printf("Enter two integers: ");
    scanf("%d %d", &num1, &num2);
    printf("GCD of %d and %d is %d.\n", num1, num2, gcd(num1, num2));

    printf("\n\n\nsuthesan vj   192210542\n");
    return 0;
}
![Screenshot 2024-09-07 151947](https://github.com/user-attachments/assets/c3161eb7-5577-4d12-bbc5-65bcc7854585)
