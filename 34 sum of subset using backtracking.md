#include <stdio.h>

int n, total = 0;
int w[10], x[10];

void sum_of_subsets(int s, int k, int r) {
    x[k] = 1;
    if (s + w[k] == total) {
        for (int i = 0; i <= k; i++) {
            if (x[i] == 1)
                printf("%d ", w[i]);
        }
        printf("\n");
    } else if (s + w[k] + w[k + 1] <= total) {
        sum_of_subsets(s + w[k], k + 1, r - w[k]);
    }
    if ((s + r - w[k] >= total) && (s + w[k + 1] <= total)) {
        x[k] = 0;
        sum_of_subsets(s, k + 1, r - w[k]);
    }
}

int main() {
    int r = 0, s = 0;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    printf("Enter the elements: ");
    for (int i = 0; i < n; i++) {
        scanf("%d", &w[i]);
        r += w[i];
    }
    printf("Enter the total sum: ");
    scanf("%d", &total);

    printf("Subsets are: \n");
    sum_of_subsets(s, 0, r);

    printf("\n\n\nsuthesan vj   192210542\n");

    return 0;
}
![Screenshot 2024-09-07 153852](https://github.com/user-attachments/assets/a06d5929-9b27-4a94-bf04-51b39b001814)
