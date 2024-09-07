#include <stdio.h>

int isPrime(int n) {
    if (n <= 1)
        return 0;
    for (int i = 2; i <= n / 2; i++) {
        if (n % i == 0)
            return 0;
    }
    return 1;
}

int main() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    if (isPrime(num))
        printf("%d is a prime number.\n", num);
    else
        printf("%d is not a prime number.\n", num);

    printf("\n\n\nsuthesan vj   192210542\n");
    return 0;
}
![Screenshot 2024-09-07 152101](https://github.com/user-attachments/assets/a5de6433-43bb-43a5-91f6-eaaf80f6d53e)
