#include <stdio.h>

int containerLoader(int weights[], int n, int capacity) {
    int total = 0;
    for (int i = 0; i < n; i++) {
        if (total + weights[i] <= capacity) {
            total += weights[i];
        } else {
            break;
        }
    }
    return total;
}

int main() {
    int weights[] = {10, 20, 30, 40, 50};
    int n = sizeof(weights) / sizeof(weights[0]);
    int capacity = 100;
    int result = containerLoader(weights, n, capacity);
    printf("Maximum weight loaded: %d\n", result);
    
    printf("\n\n\nsuthesan vj   192210542\n");
    return 0;
}
![Screenshot 2024-09-07 154637](https://github.com/user-attachments/assets/44c8eb7f-a642-43bc-adb8-62ddf7201d3f)
