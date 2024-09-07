#include <stdio.h>

void generateFactors(int n) {
    printf("Factors of %d are: ", n);
    for (int i = 1; i <= n; i++) {
        if (n % i == 0) {
            printf("%d ", i);
        }
    }
    printf("\n");
}

int main() {
    int n = 36;
    generateFactors(n);
    
    printf("\n\n\nsuthesan vj   192210542\n");
    return 0;
}
![Screenshot 2024-09-07 154701](https://github.com/user-attachments/assets/f2bb599e-6081-45bb-82ed-a17bf57220dd)
