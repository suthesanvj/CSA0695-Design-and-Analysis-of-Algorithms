#include <stdio.h>

int main() {
    int n = 4;

    for (int i = 1; i <= n; i++) {
        for (int j = 1; j <= n - i; j++) {
            printf("   ");
        }
        for (int j = 1; j <= i; j++) {
            printf("%d  ", j);
        }
        printf("\n");
    }

    printf("\n\n\nsuthesan vj   192210542\n");

    return 0;
}
![Screenshot 2024-09-07 153551](https://github.com/user-attachments/assets/86c138ab-83da-462c-967c-0ed906bed03a)
