#include <stdio.h>

int main() {
    int rows, coef = 1, space, i, j;

    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    for(i = 0; i < rows; i++) {
        for(space = 1; space <= rows - i; space++)
            printf("  ");

        for(j = 0; j <= i; j++) {
            if (j == 0 || i == 0)
                coef = 1;
            else
                coef = coef * (i - j + 1) / j;

            printf("%4d", coef);
        }
        printf("\n");
    }

    printf("\n\n\nsuthesan vj   192210542\n");

    return 0;
}
![Screenshot 2024-09-07 153633](https://github.com/user-attachments/assets/0dcbba94-4525-4c83-8bf2-f0823a2eae6f)
