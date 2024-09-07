#include <stdio.h>

void findMaxMin(int arr[], int low, int high, int *max, int *min) {
    if (low == high) {
        *max = *min = arr[low];
        return;
    }

    if (high == low + 1) {
        if (arr[low] > arr[high]) {
            *max = arr[low];
            *min = arr[high];
        } else {
            *max = arr[high];
            *min = arr[low];
        }
        return;
    }

    int mid = (low + high) / 2;
    int max1, min1, max2, min2;

    findMaxMin(arr, low, mid, &max1, &min1);
    findMaxMin(arr, mid + 1, high, &max2, &min2);

    *max = (max1 > max2) ? max1 : max2;
    *min = (min1 < min2) ? min1 : min2;
}

int main() {
    int arr[] = {12, 3, 5, 7, 19, 6, 2, 15};
    int n = sizeof(arr) / sizeof(arr[0]);
    int max, min;

    findMaxMin(arr, 0, n - 1, &max, &min);

    printf("Maximum: %d\n", max);
    printf("Minimum: %d\n", min);
    
    printf("\n\n\nsuthesan vj   192210542\n");

    return 0;
}
![Screenshot 2024-09-07 152639](https://github.com/user-attachments/assets/38d7ba63-168a-4a22-8a47-7c937635f2c6)
