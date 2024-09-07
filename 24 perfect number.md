#include <stdio.h>

int main() {
    int num, i, sum = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    for(i = 1; i <= num / 2; i++) {
        if(num % i == 0) {
            sum += i;
        }
    }

    if(sum == num) {
        printf("%d is a perfect number.\n", num);
    } else {
        printf("%d is not a perfect number.\n", num);
    }

    printf("\n\n\nsuthesan vj   192210542\n");

    return 0;
}
![Screenshot 2024-09-07 153434](https://github.com/user-attachments/assets/e86fdbbf-76a0-4425-9fde-27ff030a631c)
