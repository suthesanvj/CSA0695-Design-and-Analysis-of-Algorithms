#include <stdio.h>
#include <string.h>

void reverseString(char str[]) {
    int length = strlen(str);
    for(int i = length - 1; i >= 0; i--) {
        printf("%c", str[i]);
    }
    printf("\n");
}

int main() {
    char str[100];
    printf("Enter a string: ");
    gets(str); 
    printf("Reversed string: ");
    reverseString(str);
    printf("\n\n\nsuthesan vj   192210542\n");

    return 0;
}
![Screenshot 2024-09-07 152514](https://github.com/user-attachments/assets/313ca2e1-9bd9-4b3c-b24e-353ae98a4cd7)
