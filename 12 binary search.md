#include <stdio.h>

int binarySearch(int arr[], int size, int target) {
    int low = 0, high = size - 1;
    
    while (low <= high) {
        int mid = (low + high) / 2;
        
        if (arr[mid] == target) {
            return mid;
        } else if (arr[mid] < target) {
            low = mid + 1;
        } else {
            high = mid - 1;
        }
    }
    
    return -1;
}

int main() {
    int arr[] = {2, 4, 6, 8, 10, 12, 14, 16, 18, 20};
    int size = sizeof(arr) / sizeof(arr[0]);
    int target;
    
    printf("Enter the number to search: ");
    scanf("%d", &target);
    
    int result = binarySearch(arr, size, target);
    
    if (result != -1) {
        printf("Element found at index %d\n", result);
    } else {
        printf("Element not found.\n");
    }
    printf("\n\n\nsuthesan vj   192210542\n");

    return 0;
}
![Screenshot 2024-09-07 152449](https://github.com/user-attachments/assets/acb665be-ba1e-4d33-b81a-7154d0b666fb)
