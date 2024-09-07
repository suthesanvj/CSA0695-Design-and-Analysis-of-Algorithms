#include <stdio.h>

int main() {
    int n, i, pos, num;

    printf("Enter the number of elements in the list: ");
    scanf("%d", &n);

    int arr[n+1];

    printf("Enter %d elements: ", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Enter the position to insert the new number: ");
    scanf("%d", &pos);

    printf("Enter the number to insert: ");
    scanf("%d", &num);

    for(i = n; i >= pos; i--) {
        arr[i] = arr[i-1];
    }

    arr[pos-1] = num;
    n++;

    printf("List after insertion: ");
    for(i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }

    printf("\n\n\nsuthesan vj   192210542\n");

    return 0;
}
![Screenshot 2024-09-07 153827](https://github.com/user-attachments/assets/ea36a4b1-9dc9-4fc4-a684-b3b38b036b5a)
