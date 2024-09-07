#include <stdio.h>

int fibonacci(int n) {
    if (n == 0)
        return 0;
    else if (n == 1)
        return 1;
    else
        return (fibonacci(n - 1) + fibonacci(n - 2));
}

int main() {
    int n, i;
    printf("Enter the number of terms: ");
    scanf("%d", &n);
    for (i = 0; i < n; i++)
        printf("%d ", fibonacci(i));

    printf("\n\n\nsuthesan vj   192210542\n");
    return 0;
}

![Screenshot 2024-09-07 151908](https://github.com/user-attachments/assets/b246953d-6e19-49d1-bb9f-6649a12cf211)
