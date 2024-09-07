#include <stdio.h>

int main() {
    int n, i, min, max;
    printf("Enter the number of elements: ");
    scanf("%d", &n);
    int arr[n];
    printf("Enter %d numbers:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    min = max = arr[0];
    for(i = 1; i < n; i++) {
        if(arr[i] < min)
            min = arr[i];
        if(arr[i] > max)
            max = arr[i];
    }
    printf("Minimum value: %d\n", min);
    printf("Maximum value: %d\n", max);
    printf("Sequence from minimum to maximum:\n");
    for(i = min; i <= max; i++) {
        printf("%d ", i);
    }
    printf("\n\n\n");
    printf("suthesan vj   192210542\n");
    return 0;
}
![Screenshot 2024-09-07 153746](https://github.com/user-attachments/assets/767faf90-424b-4e30-a13d-a36d2ab87c52)
