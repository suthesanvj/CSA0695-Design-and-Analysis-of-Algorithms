#include <stdio.h>

void selectionSort(int arr[], int n) {
    int i, j, minIdx, temp;
    for (i = 0; i < n-1; i++) {
        minIdx = i;
        for (j = i+1; j < n; j++) {
            if (arr[j] < arr[minIdx])
                minIdx = j;
        }
        temp = arr[minIdx];
        arr[minIdx] = arr[i];
        arr[i] = temp;
    }
}

int main() {
    int n, i;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    int arr[n];
    printf("Enter elements: ");
    for (i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    selectionSort(arr, n);
    printf("Sorted array: ");![Screenshot 2024-09-07 152129](https://github.com/user-attachments/assets/9004e4a7-6f78-4bec-b40e-0e280df40dd3)

    for (i = 0; i < n; i++)
        printf("%d ", arr[i]);

    printf("\n\n\nsuthesan vj   192210542\n");
    return 0;
}
![Screenshot 2024-09-07 152129](https://github.com/user-attachments/assets/e23b461c-25fd-4761-82fd-4f2a1769d94c)
